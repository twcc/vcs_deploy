# Deploy [Minikube](https://minikube.sigs.k8s.io/docs/start/)

## Single Node Configuration
1. install docker

`ansible-playbook -vvv install_docker.yml`

2. add user and group to user

`sudo usermod -aG docker $USER && newgrp docker`

3. install minikube

`ansible-playbook -vvv install_minikube.yml`

