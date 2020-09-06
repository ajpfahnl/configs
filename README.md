# configs
Config options for various programs
## .vimrc
```
syntax on

set wrap
set autoindent
  
set tabstop=4
set shiftwidth=4
set softtabstop=4
"" set expandtab
```
## .gitignore
```
.DS_Store
```
## .ssh/config
```
Host pi
    HostName 192.168.1.96
    User pi

Host beagle
    HostName 192.168.7.2
    User root

Host rhel8
    HostName 127.0.0.1
    User ajp
    Port 2200
```
## git and oh-my-zsh
Disable tracking with oh-my-zsh to speed things up. Add `--global` option to apply to all repos.
```
git config --add oh-my-zsh.hide-status 1
git config --add oh-my-zsh.hide-dirty 1
```
