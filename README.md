# Running VNC on Hebbe

## On Hebbe:
- add `/priv/c3-oso/sbsw/containers/bin` to your `PATH`
  * Eg: [bashrc](hebbe/bashrc)
- Get a session on one of the NAFCI nodes by running `term`
- On this node (eg. hebbe06-x) run `vnc_container`
- Note the node:display that VNC is on. Eg. hebbe06-x:1
- Detach from the node with `Ctrl-a d`
- log out of hebbe

## On your own machine:
It's much more convenient if you have SSH keys and proxies
set up. (Proxy examples in [ssh_config](my_machine/ssh_config))

TigerVNC viewer is suggested client. Binaries [here](https://bintray.com/tigervnc/stable/tigervnc/).

- Create a SSH tunnel to the VNC session you created
  * You can use the script [vnctunnel](my_machine/vnctunnel)
  * Eg. `vnctunnel hebbe06-x:1`
- Run `vncviewer :1`
