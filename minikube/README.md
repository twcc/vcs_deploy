# Deploy [Minikube](https://minikube.sigs.k8s.io/docs/start/)

## Single Node Configuration

0. register your TWCC API Key

`twccli config init`

1. install docker

`ansible-playbook -vvv install_docker.yml`

2. add user and group to user

`sudo usermod -aG docker $USER && newgrp docker`

3. install minikube

`ansible-playbook -vvv install_minikube.yml`

4. check for service up and running

`kubectl get svc hello-kubernetes-twcc-say-hello -n twcc-svc`

5. expose service

`ansible-playbook -vvv update_nginx.yml`

6. open link according to mesg
