- `Ctrl+Z` = pause
    
- `bg` = resume in background
    
- `disown` = detach from terminal 
- `-h` means "**disown without sending SIGHUP**" (hangup signal).
`disown -h
`
OR 

Create tmux terminal :

`tmux new -s moveplex`

Re attach to tmux terminal :

`tmux attach -t moveplex