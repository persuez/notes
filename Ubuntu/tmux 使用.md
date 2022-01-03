# 保存和恢复

## Tmux Plugin Manager

### 下载安装

```
$ git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm
```

新建 ~/.tmux.conf 文件：

```
# List of plugins
set -g @plugin 'tmux-plugins/tpm'
set -g @plugin 'tmux-plugins/tmux-sensible'
set -g @plugin 'tmux-plugins/tmux-resurrect'

# Other examples:
# set -g @plugin 'github_username/plugin_name'
# set -g @plugin 'git@github.com/user/plugin'
# set -g @plugin 'git@bitbucket.com/user/plugin'

# Initialize TMUX plugin manager (keep this line at the very bottom of tmux.conf)
run '~/.tmux/plugins/tpm/tpm'
```

tmux source ~/.tmux.conf

tmux

C-b Shift-i 安装