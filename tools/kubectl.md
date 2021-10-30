# Install Kubectl

## Install using native package management
```bash
sudo apt-get update && sudo apt-get install -y apt-transport-https gnupg2 curl
```
```bash
curl -s https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo 
apt-key add -
```
```bash
echo "deb https://apt.kubernetes.io/ kubernetes-xenial main" | sudo tee -a /etc/apt/sources.list.d/kubernetes.list
```
```bash
sudo apt-get update
```
```bash
sudo apt-get install -y kubectl
```

## Install kubectl binary with curl on Linux

1. Download the latest release

```
curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"
```

2. Download the kubectl checksum file:
```
curl -LO "https://dl.k8s.io/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl.sha256"
```

- Validate the kubectl binary

```
echo "$(<kubectl.sha256) kubectl" | sha256sum --check
```

3. Install kubectl
```
sudo install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl
```

Documentation:

`https://kubernetes.io/docs/tasks/tools/install-kubectl-linux/`