Kube Playground
===================

Steps to install minikube in local and experiment,

1. Install docker by following instructions at https://docs.docker.com/engine/install/debian/

2. Install docker-compose

```bash
sudo curl -L "https://github.com/docker/compose/releases/download/1.27.3/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose

sudo chmod +x /usr/local/bin/docker-compose

docker-compose --version
```

3. Install minikube

```bash
curl -Lo minikube https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64 \
  && chmod +x minikube
sudo mkdir -p /usr/local/bin/
sudo install minikube /usr/local/bin/
```

4. Install hypervisor driver
- set docker as default driver
  ```bash
  minikube config set driver docker
  ```

- start minikube with docker driver
  ```bash
  minikube start --driver=docker
  ````

- check minikube status
  ```bash
  minikube status
  ```

5. Install kubectl

```bash
curl -LO "https://storage.googleapis.com/kubernetes-release/release/$(curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt)/bin/linux/amd64/kubectl"
chmod +x ./kubectl
sudo mv ./kubectl /usr/local/bin/kubectl
kubectl version --client
```
