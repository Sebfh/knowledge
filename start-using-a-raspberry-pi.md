# Default Credentials

raspberrypi login: pi
Password: raspberry

# Raspi-config

Firts walk through the config

1. update raspi-config
2. Enable SSH
3. Start desktop on boot
4. Change timezone

# Installation

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