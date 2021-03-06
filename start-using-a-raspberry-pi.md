# Howto setup a Raspberry Pi to boot into Chromium

This document describes how to setup a stock Raspberry Pi running Debian. The Raspberry Pi is beeing setup to automaticaly boot into Chromium kioskmode.

To check your Raspberry pi's ipaddress type:

	$ sudo ifconfig
	# This will be used later on in this document

## Raspi-config

First walk through the raspi-config

	$ sudo raspi-config

1. Update raspi-config
2. Enable SSH
3. Start desktop on boot
4. Change timezone

## Installation

Check if SSH is running:

	$ sudo service ssh status
	#[ok] sshd is running

Update aptitude and apt-get to get the latest versions

	$ sudo aptitude update
	$ sudo apt-get update

Install the Chromium browser
	
	$ sudo apt-get install chromium-browser

Add Chromium-browser to the startup

	$ sudo nano /etc/xdg/lxsession/LXDE/autostart

Add '@chromium-browser --kiosk --incognito http://example.com' to the autostart file. 

Test if this all works, reboot your Raspberry Pi:

	$ sudo shutdown -r now
	# -r means reboot, now means now!

To prevent Raspberry from sleeping

In the file /etc/lightdm/lightdm.conf edit this "xserver-command". This worked for me at least.

[SeatDefaults]
xserver-command=X -s 0 -dpms
