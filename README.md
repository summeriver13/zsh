# zsh

summeriver13's zsh-setting

## quick-start

### install zsh

Install zsh with apt.

```bash
sudo apt install zsh
```

Set zsh as the default shell.

```bash
chsh -s /bin/zsh
```

### install oh-my-zsh

Download and install oh-my-zsh with srcipt.

```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

### install zsh theme:Powerlevel10k 

```bash
git clone https://github.com/romkatv/powerlevel10k.git $ZSH_CUSTOM/themes/powerlevel10k
```

### install zsh plugins

- zsh-syntax-highlighting
- zsh-autosuggestions

```bash
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
git clone git://github.com/zsh-users/zsh-autosuggestions $ZSH_CUSTOM/plugins/zsh-autosuggestions

```

### write .zshrc

edit .zshrc

```bash
nvim ~/.zshrc
```

copy code into .zshrc

```bash
# Enable Powerlevel10k instant prompt. Should stay close to the top of ~/.zshrc.
# Initialization code that may require console input (password prompts, [y/n]
# confirmations, etc.) must go above this block; everything else may go below.
if [[ -r "${XDG_CACHE_HOME:-$HOME/.cache}/p10k-instant-prompt-${(%):-%n}.zsh" ]]; then
  source "${XDG_CACHE_HOME:-$HOME/.cache}/p10k-instant-prompt-${(%):-%n}.zsh"
fi

# nvim
export PATH="$PATH:/opt/nvim-linux64/bin"

# rbenv
export PATH="$HOME/.rbenv/bin:$PATH"
eval "$(rbenv init -)"
export RUBY_BUILD_MIRROR_URL=https://cache.ruby-china.com

# nvm
export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"  # This loads nvm
[ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"  # This loads nvm bash_completion

# zsh-setting
export ZSH="$HOME/.oh-my-zsh"           # zsh path
ZSH_THEME="powerlevel10k/powerlevel10k" # zsh theme
# zsh plugins
plugins=(
  git
  zsh-syntax-highlighting
  zsh-autosuggestions
)   
# shell-setting
HIST_STAMPS="yyyy-mm-dd" # history

# oh-my-zsh
source $ZSH/oh-my-zsh.sh

# To customize prompt, run `p10k configure` or edit ~/.p10k.zsh.
[[ ! -f ~/.p10k.zsh ]] || source ~/.p10k.zsh
```

reload .zshrc

```bash
source ~/.zshrc
```

## theme

- [powerlevel10k](https://github.com/romkatv/powerlevel10k)

## plugin

- git
- [zsh-syntax-highlighting](https://github.com/zsh-users/zsh-syntax-highlighting)
- [zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions)
 
