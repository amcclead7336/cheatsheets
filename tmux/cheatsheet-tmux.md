# Tmux Cheatsheet
## Setup
### Install package man
```bash
git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm
cat < EOF >> ~/.tmux.conf
# List of plugins
set -g @plugin 'tmux-plugins/tpm'
set -g @plugin 'tmux-plugins/tmux-sensible'

# Other examples:
# set -g @plugin 'github_username/plugin_name'
# set -g @plugin 'github_username/plugin_name#branch'
# set -g @plugin 'git@github.com:user/plugin'
# set -g @plugin 'git@bitbucket.com:user/plugin'

# Initialize TMUX plugin manager (keep this line at the very bottom of tmux.conf)
run '~/.tmux/plugins/tpm/tpm'
EOF
```

## Sessions
### Summary
Sessions contain windows

### Create Session
```bash
tmux new
tmux new -s sessionname
```

### Working with Sessions
```
## List ses
tmux ls
Ctrl+b w 
## Attach to ses
tmux a (-t sesname)
## Detach from ses
Ctrl+b d
## Move to prev and next ses
Ctrl+b (
Ctrl+b )
## Rename ses
Ctrl+b $
```

### Kill Session
```bash
tmux kill-ses -t sessionname
tmux kill-ses -a 
## kill all sessions except sesion name
tmux kill-ses -a -t sessionname
```
