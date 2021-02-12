# Tools
 
## ZSH
1. Install zsh
```bash
sudo apt update
sudo apt install zsh
```
2. https://gist.github.com/dogrocker/1efb8fd9427779c827058f873b94df95

Install with curl
```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```
3.  Enabling Plugins (zsh-autosuggestions & zsh-syntax-highlighting)

 - Download zsh-autosuggestions by
 
 ```bash
 git clone https://github.com/zsh-users/zsh-autosuggestions.git $ZSH_CUSTOM/plugins/zsh-autosuggestions
 ```
 
 - Download zsh-syntax-highlighting by
 
 ```bash
 git clone https://github.com/zsh-users/zsh-syntax-highlighting.git $ZSH_CUSTOM/plugins/zsh-syntax-highlighting
 ```
  - `nano ~/.zshrc` find `plugins=(git)`
 
 - Append 
 ```bash
plugins=(
  git
  zsh-autosuggestions
  zsh-syntax-highlighting
  ansible
  helm
  kubectl
  docker
  docker-compose
  oc
  zsh-kubectl-prompt
)
 ```
  
 - Reopen terminal