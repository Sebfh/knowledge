# Howto setup a Raspberry Pi

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

1. Check if SSH is running:

	$ sudo service ssh status
	# [ ok ] sshd is running.

2. Update aptitude and apt-get to get the latest versions

	$ sudo aptitude update
	$ sudo apt-get update

3. Install the Chromium browser
	
	$ sudo apt-get install chromium-browser

4. Add Chromium-browser to the startup

	$ sudo nano /etc/xdg/lxsession/LXDE/autostart

Add '@chromium-browser --kiosk --incognito http://example.com' to the autostart file. To test if this works reboot your Raspberry Pi:

	$ sudo shutdown -r now
	# -r means reboot, now means now!
