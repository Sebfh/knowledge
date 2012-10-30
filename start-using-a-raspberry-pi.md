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

$ sudo bash
$ ssh-keygen

$ ls /root/.ssh/

$ service ssh start

$ service ssh status


$ sudo aptitude update
$ sudo apt-get update

$ sudo apt-get install chromium-browser

$ sudo shutdown -r now

$ startx