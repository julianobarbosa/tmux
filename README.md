# tmux
tmux from scratch

Get source code
```console
cd /usr/src
git clone https://github.com/tmux/tmux.git
```

Check for dependency
http://libevent.org

# CentOS
```console
yum install libevent2 libevent2-devel
```

# Compile TMUX source
```console
sudo apt remove -q -y tmux
sudo apt install -q -y wget tar git libevent-dev libncurses-dev checkinstall

cd /tmp && git clone https://github.com/tmux/tmux.git
cd tmux/ && sudo sh autogen.sh
./configure && sudo make

#here in pkgversion you can point the current date for example and latest release version.
#Flag --install will auto install package to system.
sudo checkinstall --pkgname tmux --pkgversion latest-master --nodoc --install

tmux -V
```

Install Tmux Plugin Manager

```console
git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm
```

Put this at the bottom of .tmux.conf:

```console
# List of plugins
set -g @plugin 'tmux-plugins/tpm'
set -g @plugin 'tmux-plugins/tmux-sensible'

# Other examples:
# set -g @plugin 'github_username/plugin_name'
# set -g @plugin 'git@github.com/user/plugin'
# set -g @plugin 'git@bitbucket.com/user/plugin'

# Initialize TMUX plugin manager (keep this line at the very bottom of tmux.conf)
run '~/.tmux/plugins/tpm/tpm'
```

Reload TMUX environment so TPM is sourced:

```console
# type this in terminal
$ tmux source ~/.tmux.conf
```

List of Plugins
```console
# List of plugins
set -g @plugin 'tmux-plugins/tpm'
set -g @plugin 'tmux-plugins/tmux-sensible'
set -g @plugin 'tmux-plugins/tmux-resurrect'
set -g @plugin 'tmux-plugins/tmux-prefix-highlight'
set -g @plugin 'tmux-plugins/tmux-sidebar'
set -g @plugin 'tmux-plugins/tmux-open'
set -g @plugin 'tmux-plugins/tmux-battery'
set -g @plugin 'tmux-plugins/tmux-cpu'```
