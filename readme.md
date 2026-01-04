ravi@ip-172-31-7-96:~/git/node.js-app/k8s$ history
    1  docker ps
    2  docker run hello-world
    3  docker ps
    4  docker run hello-world
    5  curl -fsSL https://pkg.jenkins.io/debian/jenkins.io.key | sudo tee /usr/share/keyrings/jenkins-keyring.asc > /dev/null
    6  echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] https://pkg.jenkins.io/debian binary/ | sudo tee /etc/apt/sources.list.d/jenkins.list > /dev/null
    7  sudo apt update 
    8  sudo rm -f /etc/apt/sources.list.d/jenkins.list
    9  sudo rm -f /usr/share/keyrings/jenkins-keyring.asc
   10  curl -fsSL https://pkg.jenkins.io/debian/jenkins.io.key | sudo tee /usr/share/keyrings/jenkins-keyring.asc > /dev/null
   11  echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] https://pkg.jenkins.io/debian binary/ | sudo tee /etc/apt/sources.list.d/jenkins.list > /dev/null
   12  sudo apt update 
   13  sudo rm -f /etc/apt/sources.list.d/jenkins.list
   14  sudo rm -f /usr/share/keyrings/jenkins-keyring.asc
   15  curl -fsSL https://pkg.jenkins.io/debian/jenkins.io.key | sudo gpg --dearmor -o /usr/share/keyrings/jenkins-keyring.asc
   16  ls -l /usr/share/keyrings/jenkins-keyring.asc
   17  echo "deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] https://pkg.jenkins.io/debian binary/" | sudo tee /etc/apt/sources.list.d/jenkins.list
   18  cat /etc/apt/sources.list.d/jenkins.list
   19  sudo apt update 
   20  sudo rm -f /etc/apt/sources.list.d/jenkins.list
   21  curl -fsSL https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key | sudo tee   /usr/share/keyrings/jenkins-keyring.asc > /dev/null
   22  echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] https://pkg.jenkins.io/debian-stable binary/ | sudo tee /etc/apt/sources.list.d/jenkins.list > /dev/null
   23  sudo apt update 
   24  ~sudo apt install jenkins -y
   25  sudo apt install jenkins -y
   26  sudo systemctl start jenkins 
   27  sudo systemctl enable jenkins 
   28  sudo systemctl status jenkins 
   29  pwd
   30  hostname -I
   31  hostname -i
   32  sudo systemctl status jenkins 
   33  sudo netstat -tulnp | grep 8080
   34  sudo nano /etc/default/jenkins
   35  sudo systemctl restart jenkins 
   36  sudo netstat -tulnp | grep 8080
   37  sudo systemctl restart jenkins 
   38  sudo netstat -tulnp | grep 8080
   39  sudo nano /etc/default/jenkins
   40  sudo netstat -tulnp | grep 8080
   41  sudo systemctl deamon-reexec
   42  sudo systemctl d
   43  sudo systemctl restart jenkins 
   44  sudo ss -tulnp | grep 8080
   45  sudo systemctl status jenkins 
   46  sudo ss -tulnp | grep 8080
   47  sudo systemctl status jenkins 
   48  sudo systemctl restart jenkins 
   49  curl http://43.204.110.124:8080
   50  sudo ufw status
   51  sudo ufw allow 8080
   52  sudo ufw reload
   53  sudo systemctl restart jenkins 
   54  curl http://43.204.110.124:8080
   55  sudo cat /var/lib/jenkins/secrets/initialAdminPassword
   56  sudo systemctl stop jenkins 
   57  sudo nano /var/lib/jenkins/config.xml 
   58  sudo systemctl start jenkins 
   59  sudo systemctl status jenkins 
   60  exit
   61  logout
   62  sudo ufw allow openssh
   63  sudo ufw enable
   64  sudo ufw status
   65  sudo apt install -y curl wget unzip git net-tools 
   66  pwd
   67  cd ..
   68  ls
   69  cd ravi
   70  pwd
   71  cd ..
   72  ls
   73  cd ubuntu/
   74  sudo cd ubuntu/
   75  sudo -s cd ubuntu
   76  ls
   77  cd ravi/
   78  ls
   79  pwd
   80  git --version 
   81  sudo apt install openjdk-17-jdk -y
   82  java --version 
   83  git --version 
   84  sudo apt install docker.io -y
   85  docker -V
   86  docker - V
   87  docker --version 
   88  docker -V
   89  docker --V
   90  sudo systemctl start docker 
   91  docker -v
   92  sudo systemctl enab
   93  sudo systemctl status docker 
   94  docker ps
   95  sudo usermod -aG docker ravi 
   96  docker ps
   97  newgrp docker 
   98  sudo systemctl restart docker 
   99  sudo systemctl enable docker 
  100  sudo systemctl enable jenkins
  101  sudo systemctl status jenkins 
  102  sudo apt install gh -y
  103  gh auth login 
  104  wget -O- https://apt.releases.hashicorp.com/gpg | gpg --dearmor | sudo tee /usr/share/keyrings/hashicorp.gpg
  105  sudo apt update && sudo apt upgrade -y
  106  java --version
  107  git --version
  108  docker --version
  109  jenkins --version
  110  sudo usermoad -aG docker ravi
  111  sudo usermod -aG docker ravi
  112  sudo usermod -aG docker jenkins
  113  newgrp docker 
  114  wget -O- https://apt.releases.hashicorp.com/gpg | gpg --dearmor | sudo tee /usr/share/keyrings/hashicorp.gpg
  115  terraform version
  116  wget -O- https://apt.releases.hashicorp.com/gpg | gpg --dearmor | sudo tee /usr/share/keyrings/hashicorp.gpg
  117  echo "deb [signed-by=/usr/share/keyrings/hashicorp.gpg] \
  118  https://apt.releases.hashicorp.com \
  119  $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/hashicorp.list
  120  sudo apt update
  121  sudo apt install terraform
  122  terraform version
  123  sudo apt update
  124  sudo apt update
  125  curl -Lo kubectl https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl
  126  chmod +x kubectl
  127  sudo mv kubectl /usr/local/bin/
  128  kubectl version --client
  129  sudo apt update
  130  curl https://raw.githubusercontent.com/helm/helm/main/scripts/get-helm-3 | bash
  131  helm version
  132  sudo apt update
  133  curl -fsSL https://deb.nodesource.com/setup_lts.x | sudo -E bash - && sudo apt install -y nodejs
  134  node -v
  135  npm -v
  136  sudo apt update
  137  sudo usermod -aG docker jenkins
  138  sudo systemctl restart docker
  139  sudo systemctl restart jenkins
  140  dockewr run hello-world
  141  docker run hello-world
  142  docker --version
  143  docker ps
  144  sudo systemctl status docker
  145  sudo apt update
  146  docker pull sonarqube:lts
  147  docker ps 
  148  docker run -d   --name sonarqube   -p 9000:9000   -e SONAR_ES_BOOTSTRAP_CHECKS_DISABLE=true   sonarqube:lts
  149  DOCKER PS 
  150  sudo apt update 
  151  docker ps 
  152  docker run -d   --name sonarqube   -p 9000:9000   -e SONAR_ES_BOOTSTRAP_CHECKS_DISABLE=true   sonarqube:lts
  153  docker ps -a
  154  docker start sonarqube 
  155  docker ps 
  156  sudo apt update
  157  docker ps
  158  docker start sonarqube 
  159  docker ps
  160  docker ps - a
  161  docker ps -a
  162  docker logs sonarqube
  163  free -h
  164  sudo apt update 
  165  git clone https://github.com/csvijay197/node.js-app.git
  166  ls
  167  mkdir git 
  168  ls
  169  cd git/
  170  git clone https://github.com/csvijay197/node.js-app.git
  171  ls
  172  cd ..
  173  ls
  174  rm -rf node.js-app/
  175  ls
  176  cd git/
  177  vi app.js
  178  ls
  179  cd node.js-app/
  180  vi app.js
  181  ls
  182  cat app.js 
  183  vi package.JSON
  184  cat package.JSON 
  185  npm install
  186  ls
  187  cat package-lock.json
  188  cat package.JSON 
  189  ls 
  190  rm -rf package-lock.json package.JSON 
  191  ls
  192  vi package.json
  193  cat package.json 
  194  ls
  195  npm install
  196  npm app.js 
  197  curl http://43.204.109.234:3000/
  198  sudo ufw status 
  199  sudo ufw allow 3000
  200  sudo ufw status 
  201  sudo ufw reload
  202  curl http://43.204.109.234:3000/
  203  node app.js 
  204  sudo lsof -i :3000
  205  curl http://localhost:3000
  206  vi app.js 
  207  sudo lsof -i :3000
  208  kill -9 2487
  209  kill -9 3144
  210  sudo lsof -i :3000
  211  kill -9 3114
  212  sudo lsof -i :3000
  213  ls
  214  node app.js 
  215  cat app.js 
  216  vi app.js 
  217  sudo lsof -i :3000
  218  sudo lsof -i :3000
  219  sudo lsof -i :3000
  220  node app.js 
  221  curl http://43.204.109.234:3000/
  222  sudo lsof -i :3000
  223  kil -9 3346 3386 
  224  kill -9 3346 3386
  225  node app.js 
  226  sudo apt update 
  227  docker ps 
  228  docker ps -a
  229  cd git/
  230  cd node.js-app/
  231  ls
  232  vi Dockerfile
  233  cat Dockerfile 
  234  docker build - t nodejs-app:v1
  235  docker build -t nodejs-app:v1
  236  docker build -t node.js-app:v1
  237  pwd
  238  docker build -t node.js-app:v1
  239  docker build -t node.js-app:v1 .
  240  docker ps 
  241  docker images 
  242  docker run -d -p 3000:3000 --name node.js-container node.js-app:v1 
  243  docker ps 
  244  docker ps -a
  245  docker run -d -p 3000:3000 --name nodejs node.js-app:v1 
  246  docker ps 
  247  sudo lsof -i :3000
  248  kill -9 4894
  249  sudo lsof -i :3000
  250  docker ps 
  251  docker run -d -p 3000:3000 --name nodejs node.js-app:v1 
  252  docker run -d -p 3000:3000 --name nodejs1 node.js-app:v1 
  253  docker ps 
  254  docker login
  255  docker images 
  256  docker tag node.js-app:v1 messi524/node.js-app:v1
  257  docker images 
  258  docker push messi524/node.js-app:v1
  259  ls
  260  git status 
  261  vi .gitignore
  262  git commit -m "Initial node.js with docker and k8s"
  263  git config --global user.email "vijayendrarahul.97@gmail.com"
  264  git config --global user.email "csvijay197"
  265  git config --global --list
  266  history
  267  git commit -m "Initial node.js with docker and k8s"
  268  git config --global --list
  269  history
  270  git config --global user.name "csvijay197"
  271  git commit -m "Initial node.js with docker and k8s"
  272  git push origin main 
  273  ls
  274  cd
  275  pwd
  276  ls
  277  cd git
  278  pwd
  279  ls
  280  cd node.js-app/
  281  ls
  282  mkdir k8s
  283  ls
  284  pwd
  285  cd k8s/
  286  pwd
  287  ls
  288  docker images 
  289  docker ps
  290  ls
  291  vi deployment.yaml
  292  cat deployment.yaml 
  293  vi service.yaml
  294  cat service.yaml 
  295  ls -la
  296  cd ~/git/node.js-app/
  297  git add k8s/
  298  git commit -m "Add k8s deployment"
  299  git push origin main
  300  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
  301  git push origin main
  302  kubectl version --client 
  303  minikube version 
  304  kubectl get nodes 
  305  curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
  306  sudo install minikube-linux-amd64 /usr/local/bin/minikube
  307  minikube version
  308  minikube start --driver=docker
  309  pwd
  310  cd
  311  ls
  312  logout
  313  sudo apt update 
  314  sudo lsof -i :3000
  315  docker ps 
  316  docker ps -a
  317  docker run -d -p 3000:3000 --name nodejs2 node.js-app:v1 
  318  docker ps 
  319  docker ps -a
  320  cd git/node.js-app/
  321  ls
  322  cd k8s/
  323  ls
  324  cat deployment.yaml 
  325  docker ps -a
  326  aws --version 
  327  curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
  328  unzip awscliv2.zip
  329  aws --version 
  330  sudo ./aws/install
  331  aws --version 
  332  aws configure
  333  aws sts get-caller-identity
  334  kubectl version --client
  335  aws --version 
  336  eksctl version
  337  curl -sL https://github.com/weaveworks/eksctl/releases/latest/download/eksctl_$(uname -s)_amd64.tar.gz | tar xz
  338  sudo mv eksctl /usr/local/bin
  339  eksctl version
  340  export HISTTIMEFORMAT="%F %T  "
  341  history
  342  eksctl create cluster --name nodejs-eks-cluster --region ap-south-1 --nodegroup-name linux-nodes --node-type t3.small --nodes 2 --nodes-min 1 --nodes-max 2 --managed
  343  kubectl get nodes 
  344  aws eks update-kubeconfig --region ap-south-1 --name nodejs-eks-cluster
  345  kubectl get ns
  346  ls
  347  cd ..
  348  ls
  349  aws --version
  350  cd k8s/
  351  ls
  352  kubectl apply -f deployment.yaml 
  353  cat deployment.yaml 
  354  kubectl apply -f deployment.yaml 
  355  docker ps
  356  cat deployment.yaml 
  357  kubectl apply -f deployment.yaml 
  358  vi deployment.yaml 
  359  kubectl apply -f deployment.yaml 
  360  cat deployment.yaml 
  361  vi deployment.yaml 
  362  kubectl apply -f deployment.yaml 
  363  kubectl get pods
  364  cat deployment.yaml 
  365  docker ps 
  366  docker images
  367  cat deployment.yaml 
  368  vi deployment.yaml 
  369  kubectl apply -f deployment.yaml 
  370  kubectl get pods
  371  kubectl describe pod nodejs-app-767b7455b9-cp6j4
  372  cat deployment.yaml 
  373  kubectl get pods
  374  cat deployment.yaml 
  375  vi deployment.yaml 
  376  kubectl apply -f deployment.yaml 
  377  kubectl get pods
  378  cat service.yaml 
  379  kubectl apply -f service.yaml 
  380  kubectl get svc
  381  sudo ufw status 
  382  sudo ufw allow 30007
  383  sudo ufw reload
  384  kubectl get svc
  385  curl http://65.0.99.154:30007/
  386  curl http://localhost:30007/
  387  kubectl get pods -o wide
  388  cd git/node.js-app/k8s/
  389  kubectl get pods
  390  kubectl get svc
  391  kubectl get pods --show-labels
  392  ip addr | grep inet 
  393  kubectl port-forward svc/nodejs-service 3000:3000 --address 0.0.0.0
  394  sudo lsof -i :3000
  395  kubectl port-forward svc/nodejs-service 8080:3000 --address 0.0.0.0
  396  sudo ufw status 
  397  sudo ufw allow 9090
  398  sudo ufw reload
  399  kubectl get pods
  400  kubectl port-forward svc/nodejs-service 9090:3000 --address 0.0.0.0
  401  cd git/node.js-app/k8s/
  402  ls
  403  kubectl get pods
  404  kubectl get svc
  405  sudo ss -lntp | grep java
  406  ls
  407  git status 
  408  git push origin main 
  409  cd git/node.js-app/k8s/
  410  ls
  411  git add service-lb.yaml 
  412  git status 
  413  git reset --soft HEAD -1
  414  git reset --soft HEAD~1
  415  git status
  416  git reset --hard HEAD~1
  417  git log --oneline 
  418  ls
  419  cd ..
  420  ls
  421  cd k8s/
  422  ls
  423  ll
  424  ls
  425  git reflog 
  426  git reset --hard HEAD@{3}
  427  ls
  428  git reset --hard HEAD@{0}
  429  ls
  430  git reset --hard HEAD@{1}
  431  ls
  432  git reset --hard HEAD@{2}
  433  ls
  434  docker images
  435  ls
  436  cd ..
  437  ls
  438  cd k8s/
  439  ls
  440  git log --oneline 
  441  ls
  442  aws --version 
  443  ls
  444  git status 
  445  kubectl get pods
  446  kubectl get svc
  447  vi service-lb.yaml 
  448  ls
  449  git add service-lb.yaml 
  450  git commit -m "adding lb file"
  451  git push origin main
  452  ls
  453  kubectl apply -f service-lb.yaml 
  454  kubectl get svc
  455  kubectl get nodes
  456  du - sh *
  457  df - sh *
  458  du -h
  459  free -h
  460  df -h
  461  sudo du -h --max-depth=1 / | sort -hr
  462  docker system df
  463  docker ps 
  464  docker ps -a
  465  docker images
  466  ls
  467  history
  468  ls
  469  cd git/
  470  cd node.js-app/k8s/
  471  ls
  472  cd git/node.js-app/k8s/
  473  ls
  474  cd
  475  sudo su - jenkins 
  476  docker ps
  477  docker ps -a
  478  docker ps
  479  docker images
  480  cd git/node.js-app/k8s/
  481  ls
  482  kubectl get deployment nodejs-app -o yaml | grep -A 5 containers:
  483  cd
  484  su - jenkins 
  485  sudo su - jenkins
  486  cd git/
  487  cd node.js-app/k8s/
  488  ls
  489  sudo apt update
  490  ls
  491  systemctl status jenkins
  492  systemctl restart jenkins
  493  systemctl status jenkins
  494  history
  495  ls
  496  docker images
  497  kubectl get ns
  498  ls
  499  ps aux | grep jenkins
  500  sudo su - jenkins 
  501  cd git/node.js-app/k8s/
  502  ls
  503  cd ..
  504  ls
  505  cd node_modules/
  506  ls
  507  cd ..
  508  ls
  509  cd ..
  510  ls
  511  cd git/node.js-app/k8s/
  512  ls
  513  history
