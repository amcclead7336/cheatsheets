# Tmux Cheatsheet
## Setup
### Install package man
```bash
git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm
cat << EOF >> ~/.tmux.conf
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
### Other
Enter command mode
^b :

## Sessions (ses)
### Create Session
```bash
tmux new
tmux new -s sessionname
```

### Working with Sessions
```
## List ses
tmux ls
^b w ## Includes windows

## Attach to ses
tmux a (-t sesname)

## Detach from ses
^b d

## Move to prev and next ses
^b (
^b )

## Rename ses
^b $

## kill Session
tmux kill-ses -t sessionname
tmux kill-ses -a 

## kill all ses except sesionname
tmux kill-ses -a -t sessionname
```

## Windows
### Create window
```
^b c
```

### Working with windows
```
## Close window
^b &

## Change window
^b p
^b n

# Change by num
^b [0-9]
```

## Panes
### Create panes
```
## vert split
^b %
## horizontal split
^b "
```

### Working with Panes
```
## Close pane
^b x

## Zoom
^b z

## Convert to window
^b !

## Move right and left
^b {
^b }

## Show nums and move
^b q ([0-9])

## Toggle Layout
^b [space]
```

## Copy Mode (cm)
```
## Enter cm
^b [
^b PgUp

## Search for word (forward and backward)
/
?
## Next word occurance and Prev
n
N

## Select
Space (start)
Clear (ESC)
Copy  (Enter)
```

