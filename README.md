# Test Networking Protocols Between Client and Server

## Project Overview
Project icmp, ssh and rdp signals from sender to receiver.

## Objectives
- [ ] **Objective 1**: Send and Receive ICMP
- [ ] **Objective 2**: Send and Receive SSH
- [ ] **Objective 3**: Send and Receive RDP

## Setup Instructions
1. **Prerequisites**
   If you have not spin up your Linux Mint (client) and Ubuntu Server (server) please follow instructions below.
   https://github.com/aizhuxue007/vbox-client-server-vms
   - Go to Network settings to ensure Bridge Adapter is applied for both VMs.
   - Find ip address for both VMs by typing into Terminal `ip a`
   - RDP: you need xrdp and xfreerdp packages for Linux Mint and Ubuntu Server respectively
         - In the terminals enter: `sudo apt update` then `sudo apt install <package name>`
             - download xrdp for linux mint
             - download freerdp2-x11 for ubuntu linux

3. **Send and Receive ICMP**  
   - In the Linux Mint Terminal type  `ping <ubuntu-server-ipaddress>`
   - Should get this response to indicate successful ICMP transmission
  ![Alt text for the image](path/to/image.jpg)

4. **Send and Receive SSH**  
   - In the Linux Mint Terminal type  `ssh username:<ubuntu-server-ipaddress>`
   - Include expected outputs and troubleshooting tips.
  ![Alt text for the image](path/to/image.jpg)

5. **Send and Receive RDP**
   - Linux Mint Setup
       - sudo systemctl start xrdp
       - sudo systemctl enable xrdp
       - sudo systemctl status xrdp
         - if all is working there should be an `active (running)` indicator
   - Ubuntu server
       - type `telnet <mint ip> 3389`
       - Output should be like this
     ![Alt text for the image](path/to/image.jpg)


