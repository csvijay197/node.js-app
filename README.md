CI/CD Pipeline for Node.js Application using Jenkins, Docker, Kubernetes (EKS) on AWS
1️⃣ Project Overview
Objective
To build a complete CI/CD pipeline that:
Builds a Node.js application
Creates a Docker image
Pushes the image to Docker Hub
Deploys the application to AWS EKS (Kubernetes)
Automates deployment using Jenkins
2️⃣ Tools & Technologies Used
Category
Tools
Cloud
AWS
Compute
EC2
Containers
Docker
Orchestration
Kubernetes (EKS)
CI/CD
Jenkins
SCM
GitHub
Language
Node.js
Image Registry
Docker Hub
3️⃣ Architecture Flow (High Level)
Copy code

Developer → GitHub → Jenkins → Docker Hub → EKS → LoadBalancer → User
4️⃣ EC2 Instance Creation (Jenkins Server)
4.1 EC2 Creation
AMI: Amazon Linux 2
Instance Type: t3.micro (Free Tier)
Storage: 8 GB (default)
Security Group:
SSH: 22
Jenkins: 8080
Node App (optional): 3000
Key pair created and downloaded
4.2 Connect to EC2
Copy code
Bash
ssh -i key.pem ec2-user@<public-ip>
5️⃣ Install Required Software on EC2
5.1 Update system
Copy code
Bash
sudo yum update -y
5.2 Install Java (for Jenkins)
Copy code
Bash
sudo yum install java-11-amazon-corretto -y
5.3 Install Jenkins
Copy code
Bash
sudo wget -O /etc/yum.repos.d/jenkins.repo \
https://pkg.jenkins.io/redhat-stable/jenkins.repo

sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io.key
sudo yum install jenkins -y
Start Jenkins:
Copy code
Bash
sudo systemctl start jenkins
sudo systemctl enable jenkins
Access:
Copy code

http://<public-ip>:8080
6️⃣ Jenkins Initial Setup
Unlock Jenkins using:
Copy code
Bash
sudo cat /var/lib/jenkins/secrets/initialAdminPassword
Installed plugins:
Git
Pipeline
Docker Pipeline
Credentials Binding
Kubernetes CLI
7️⃣ Docker Installation & Setup
Copy code
Bash
sudo yum install docker -y
sudo systemctl start docker
sudo systemctl enable docker
Add Jenkins to Docker group:
Copy code
Bash
sudo usermod -aG docker jenkins
sudo systemctl restart jenkins
Verify:
Copy code
Bash
docker --version
8️⃣ Docker Hub Credentials Setup
Important Learning
Docker Hub Google login does NOT provide password
Must generate Access Token
Steps:
Docker Hub → Account Settings → Security
Generate Access Token
Jenkins → Credentials → Add:
Type: Username & Password
ID: dockerhub-creds
9️⃣ GitHub Repository Setup
Repository structure:
Copy code

nodejs-app/
│
├── app.js
├── package.json
├── Dockerfile
└── k8s/
    ├── deployment.yaml
    └── service-lb.yaml
🔟 Node.js Application
Simple Express server:
Copy code
Js
app.listen(3000)
Test locally:
Copy code
Bash
node app.js
1️⃣1️⃣ Dockerfile
Copy code
Dockerfile
FROM node:16
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
EXPOSE 3000
CMD ["node", "app.js"]
1️⃣2️⃣ Kubernetes Setup (EKS)
12.1 Install AWS CLI
Copy code
Bash
sudo yum install awscli -y
aws configure
12.2 Install kubectl
Copy code
Bash
curl -LO https://dl.k8s.io/release/stable/bin/linux/amd64/kubectl
chmod +x kubectl
sudo mv kubectl /usr/local/bin/
12.3 Create EKS Cluster
(Using AWS Console or eksctl)
Cluster created with:
1 Node group
t3.micro instances
Update kubeconfig:
Copy code
Bash
aws eks update-kubeconfig --region ap-south-1 --name <cluster-name>
Verify:
Copy code
Bash
kubectl get nodes
1️⃣3️⃣ Kubernetes Manifests
Deployment
Copy code
Yaml
containers:
- name: nodejs-app
  image: messi524/node.js-app:v1
  ports:
  - containerPort: 3000
Service (LoadBalancer)
Copy code
Yaml
type: LoadBalancer
Apply manually:
Copy code
Bash
kubectl apply -f deployment.yaml
kubectl apply -f service-lb.yaml
1️⃣4️⃣ Jenkins CI/CD Pipeline
Pipeline Stages
Checkout code
Build Docker image
Push image to Docker Hub
Deploy to Kubernetes
Rollout status check
Key Jenkinsfile Logic
Copy code
Groovy
kubectl set image deployment/nodejs-app \
nodejs-app=${IMAGE_NAME}:latest -n default
Why latest?
Jenkins builds a new image every run
latest always points to newest build
Kubernetes pulls updated image automatically
1️⃣5️⃣ Common Issues Faced & Fixes
❌ Docker login failed
Reason: Google login has no password
Fix: Use Docker Hub Access Token
❌ Jenkins can’t access Kubernetes
Reason: kubeconfig missing for Jenkins user
Fix:
Copy code
Bash
sudo cp ~/.kube/config /var/lib/jenkins/.kube/config
sudo chown jenkins:jenkins /var/lib/jenkins/.kube/config
❌ unable to find container name
Reason: Container name mismatch
Fix: Match container name exactly from deployment YAML
❌ Rollout stuck / timeout
Reason:
Image pull delay
Pod restart
Resource constraints
Fix:
Check pods:
Copy code
Bash
kubectl get pods
kubectl describe pod <pod-name>
1️⃣6️⃣ Rollout Status Explanation
Copy code
Bash
kubectl rollout status deployment/nodejs-app
Why included?
Ensures deployment completed
Jenkins waits until pods are healthy
Fails pipeline if deployment is broken
1️⃣7️⃣ Verification
Copy code
Bash
kubectl get svc
kubectl get pods
Access app using:
Copy code

http://<LoadBalancer-EXTERNAL-IP>:3000
1️⃣8️⃣ CI/CD SUCCESS 🎉
Code push → Jenkins triggered
Docker image built & pushed
Kubernetes deployment updated
Application live automatically
1️⃣9️⃣ Cleanup & Cost Control (After Project)
Steps performed:
Delete LoadBalancer service
Delete Kubernetes deployment
Delete EKS node group
Delete EKS cluster
Terminate EC2 instance
Delete EBS volumes
Release Elastic IPs
Verify billing = $0
