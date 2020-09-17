# Use SSH To Connect To A Remote Server(Linux) On Windows
SSH stands for Secure Socket Shell. </br>
**On Linux:**
  1. Install openssh-server: </br>
    `sudo apt-get install openssh-server`
  2. Enable ssh server: </br>
    `sudo systemctl enable ssh`
  3. Start ssh server: </br>
    `sudo systemctl start ssh` </br>
    

**On Windows:**
`ssh username@ipaddress` </br>
The username is the remote desktop username and ip address is the remote desktop ip address </br>
**NOTE:** to look up the ip address, type `ipconfig` on windows, `ip address show` on Linux.

### Debug
---
- **Connection Reject on Port #:** </br>
  Configure Ubuntu's built-in firewall: By default the built-in firewall is disabled, to enable it: </br>
  `sudo ufw enable` </br>
  then enable the port #: </br>
  `sudo ufw allow #` </br>
  NOTE: to look up all ports: `netstat`, to look up specific port(s) contain port #: `netstat -na|grep #`
