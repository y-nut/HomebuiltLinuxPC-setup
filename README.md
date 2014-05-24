HomebuiltLinuxPC-setup
======================

This file is created in order to gather all the set up steps I have taken for eventually having my Linux Mint 17 up running.

Installation:
I installed the Linux Mint 17 from a sanDisk 4GB USB stick. I 'burned' the ISO-image downloaded from the
Linux Mint website with the preinstalled GUI 'USB Image Writer' in Linux Mint. After that I booted from USB.
Sometimes I experience that I get a blue screen error saying:

        Failed to start xserver
        ...
        
This error is apparantly caused because there is no graphics driver

I solved that by typing (from fresh install):
1. Ctrl+Alt+F1 (shell)
2. sudo su
3. sudo Xorg -configure
4. cd (directs to root. Ensure there is a file called "xorg.conf.new" here by typing the command 'ls')
5. cp xorg.conf.new /etc/X11/xorg.conf
6. Finish by typing the command 'startx'

The machine should now reboot to the desktop where Linux Mint can be installed from by clicking the logo.

Src: http://forums.linuxmint.com/viewtopic.php?f=46&t=103142

After installation
I ran a glmark2 test after installation to test if my graphics card (AMD/ATI Bonaire R7 260x?) was installed correctly.
I scored 190, which is low. I was supposed to get a score of 4000 sth. Therefore I had to install the drivers.


Update system (Graphics drivers)
http://community.linuxmint.com/tutorial/view/1316
