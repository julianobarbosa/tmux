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

```console
cd tmux
sh autogen.sh
./configure && make
sudo make install
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
