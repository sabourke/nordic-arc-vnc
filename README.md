# Running VNC on Hebbe

## On Hebbe:
- add `/priv/c3-oso/sbsw/containers/bin` to your `PATH`
- Get a session on one of the NAFCI nodes by running `term`
- On this node (eg. hebbe06-x) run `vnc_container`
- Note the node:display that VNC is on. Eg. hebbe06-x:1
- Detatch from the node with `Ctrl-a d`
- log out of hebbe

## On your own machine
It's much more convienent if you have SSH keys and proxys
set up. (Proxy examples in `my_machine/ssh_config`)

- Create a SSH tunnel to the VNC session you created
  * Eg. `vnctunnel hebbe06-x:1`
- Run `vncviewer :1`
