# Install Kubectl

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