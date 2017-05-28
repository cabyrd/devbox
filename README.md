# **Devbox**
A quick and easy development environment based upon fedora:latest.
Containers are expected to contain a few common development tools as follows:

### Shell 
* [bash](https://www.gnu.org/software/bash/)
* [bash-it](https://github.com/Bash-it/bash-it)

### C C++
* autotools
* make
* gcc / gcc
* cppcheck

### Golang
* Go 1.7.5
* vim-go

### Python 3
* python3
* pip3
* pylint

### Ruby 
* [RVM](https://rvm.io/)
* [Ruby 2.4.1](https://www.ruby-lang.org/en/downloads/)

### Source Control
* Git 
* Subversion

###  Editor
* vim 8.0
* [vundle](https://github.com/VundleVim/Vundle.vim)

### Utilities 
* [tmux](https://tmux.github.io/)
* [tmuxinator](https://github.com/tmuxinator/tmuxinator)
  
## **Getting Started**
```
docker pull cabyrd/devbox:latest
docker run -ti docker.io/cabyrd/devbox
```

## Mapping $GOPATH
$GOPATH inside the container is defined as $GOPATH="/home/dev/godev",
if you have a need to mount a volume to your host GOPATH, you can do so 
as follows:

```
docker run -ti -v $GOPATH:/home/dev/godev docker.io/cabyrd/devbox
```


Starting containers as shown above will give you access to a 
development environment.  Keep in mind that all source code
will reside inside the container file system, so be sure to 
push important commits before tearing down any important 
container.
