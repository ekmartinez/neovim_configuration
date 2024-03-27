# Neovim Setup Guide

1. Install Neovim
2. Install Vim-Plug
3. Install-Update-Remove Plugins
4. Setup Python & C Code Completions

## Install Neovim

Installation:
```bash
sudo pacman -S neovim
```
Create configuration folder:
```bash
mkdir ~/.config/nvim
```
Create a vim.init file (or download from here) inside ~/.config/nvim

## Install Vim-Plug
Go to https://github.com/junegunn/vim-plug and download vim-plug for neovim as follows:
```bash
sh -c 'curl -fLo "${XDG_DATA_HOME:-$HOME/.local/share}"/nvim/site/autoload/plug.vim --create-dirs \
       https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim'
```
## Install-Update-Remove Plugins
To install a plugin you should first include in your vim.init config file.  For example:
```bash

call plug#begin()

Plug 'preservim/nerdtree'

call plug#end()

```
Afterwards, open the neovim editor and type:
```bash
:PlugInstall
```
Similarly, to update installed plugins you do so by typing:
```bash
:PlugUpdate
```
To update vim-plug, you do so by typing:
```bash
:PlugUpgrade
```
To remove a plugin, you will first need to remove the entry on the config file and the type the following on your editor:
```bash
:PlugClean
```
