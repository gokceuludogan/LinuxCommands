#  `screen` Command Tutorial: Terminal Multitasking

##  What is `screen`?
`screen` is a terminal multiplexer that allows you to:
- Run multiple terminal sessions in one terminal window
- Detach from a session and leave it running in the background
- Reattach later, even after disconnecting (great for SSH)

---

##  Install `screen`

```bash
sudo apt install screen
```

##  Create a New Named Session
```bash
screen -S mysession
```

Creates and enters a session named mysession.

##  Detach From the Session

Press:
```
Ctrl + A, then D
```

This detaches the session but keeps it running.


##  Reattach to the Session

List active sessions:
```bash
screen -ls
```

Reattach:
```bash
screen -r mysession
```
Or use session ID:
```bash
screen -r 12345
```


##  Kill a Session

Inside the session:
```bash
exit
```

Outside the session:
```bash
screen -X -S mysession quit
```

Kill all detached sessions:
```bash
screen -ls | grep Detached | cut -d. -f1 | awk '{print $1}' | xargs -n 1 screen -X -S quit
```


##  Useful Keybindings (Inside `screen`)

| Action                        | Keybinding             |
|------------------------------|------------------------|
| Detach session               | `Ctrl + A`, then `D`   |
| Create new window            | `Ctrl + A`, then `C`   |
| Next window                  | `Ctrl + A`, then `N`   |
| Previous window              | `Ctrl + A`, then `P`   |
| List windows                 | `Ctrl + A`, then `"`   |
| Split screen horizontally    | `Ctrl + A`, then `S`   |
| Switch between panes         | `Ctrl + A`, then `Tab` |
| Close window/pane            | `exit`                 |

---

## Run a Script in a Named Session

```bash
screen -S backup ./backup.sh
```

Runs `./backup.sh` in a screen named `backup`.


## Tip

Use `screen` when running long processes or working on a remote server to avoid losing progress due to terminal disconnection.

