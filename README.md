# General
This a simple configuration for vim + tmux + zsh

# Prerequisites
```
sudo apt-get install git vim tmux zsh
```

# Installation
First, clone the repo to your home directory:
```bash
git clone https://github.com/nickbatsaras/dotfiles.git ~/.dotfiles
```
Then, we need to install vundle (a plugin manager for vim):
```bash
git clone https://github.com/VundleVim/Vundle.vim.git ~/.dotfiles/bundle/Vundle.vim
```
Link to the cloned configs:
```bash
ln -s ~/.dotfiles/.vimrc ~/.vimrc
ln -s ~/.dotfiles/.tmux.conf ~/.tmux.conf
```
Then, install vim plugins:
```
vim +PluginInstall +qall
```
Now that we're done with vim and tmux, let's install the oh-my-zsh repo:
```
sh -c "$(wget https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)"
```
Use the cloned zsh config instead of default one:
```
mv ~/.zshrc ~/.zshrc_old
ln -s ~/.dotfiles/.zshrc ~/.zshrc
```
Finally, make zsh default shell:
```
chsh -s $(which zsh)
```
