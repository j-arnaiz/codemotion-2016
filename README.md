# Tmux

## Instalation:

### For ubuntu/debian:

```
sudo apt-get install tmux tmuxinator
```

### For other SO check:
- [Tmux](https://tmux.github.io/)
- [Tmuxinator](https://github.com/tmuxinator/tmuxinator)



### Configuration:

```
cp config_files/.tmux.conf ~/
```

To work with tmuxinator you should set EDITOR env variable:

```
export EDITOR=vim
```

Thats all you need to run tmux and tmuxinator.


## For pair programing

Activate ssh server for your machine and then allow others
to connect to your tmux session adding this line to your ~/.ssh/authorized_keys


```
command="/path/to/your/tmux attach -t pair" <public_key>
```

Now a remote user could do ssh your_user@your_host and attached to tmux session if it exists

# Vim

## Instalation

Silversearcher and YouCompleteMe is used by vim plugins and is optional but recommended to install,
to prevent errors with the vim config of this project.

Rubocop is used by Syntastic but do not install it if you are not going to use ruby.


### Vim For Ubuntu/debian

```
sudo apt-get install vim-gtk
```

It is also recommended to use powerline fonts see
[PowerLine Fonts](https://github.com/powerline/fonts) for installation.

### Vim For other OS

Check this pages for instructions:
- [Vim](http://www.vim.org/)
- [PowerLine Fonts](https://github.com/powerline/fonts) for installation.

### Setting vim config

Installing Vundle plugin manager
```
git clone https://github.com/gmarik/vundle.git ~/.vim/bundle/vundle
```

Using vim config from this repo
```
cp config_files/.vimrc* ~/
```

Finally downloading plugins
```
vim +BundleInstall +qall
```

Vim ready just lets complete installation enabling two more plugins


### SilverSearcher

On ubuntu/debian:

```
sudo apt-get install silversearcher-ag
```

On other OS check:
- [SilverSearcher Ag](https://github.com/ggreer/the_silver_searcher)


### YouCompleteMe (YCM)

On Ubuntu/Debian:

#### Dependencies
```
sudo apt-get install build-essential cmake python-dev python3-dev
```

On other OS check:
- [YouCompleteMe](https://github.com/Valloric/YouCompleteMe)


#### Compiling

After setting vim config and installing YCM dependencies
```
cd ~/.vim/bundle/YouCompleteMe && ./install.py
```

This compiles YCM server part

### Rubocop

To use syntastic with ruby as seen on the slide shows
just make sure you have ruby ~2.3.0 and rubocop in your path
I recommend to use rbenv to install ruby:

- [rbenv](https://github.com/rbenv/rbenv#installation)

when you have installed ruby just
```
gem install rubocop
```
