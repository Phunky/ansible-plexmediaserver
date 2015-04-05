# Plex Media Server

This is my Ansible playbook for setting up Plex Media Server on a Ubuntu 14.04 install.

Currently I run PMS on an Intel NUC with all my media stored on a TranquilPC BBS2 NAS, which is
shard via SAMBA. The NAS is managed by its own Playbook which is also included in this repo.

This is used soley for transencoding media for each of my Plex clients (iOS, Andriod and Chromecasts) as the NAS wasn't quite powerful to handle this task (It's only Intel ATOM based!).

## Switch from Centos 6.5 to Ubuntu

I'm no sysadmin or linux user and found I was constantly hitting a brick wall with Centos, although I got it working it was just too much effort for what i'm doing. Also going forward its likely that i'd have to do so much more, so made switch to Ubuntu that usually has better support from the likes of Plex, Sickbeard and other media centre projects.

## Installing Plex Media Server

1. Install Ansible on a client machine.
2. Install Ubuntu 14.04 on the PMS machine.
3. Clone this repo on the client machine.
4. Edit group_vars/pms to your liking.
  - Make sure to update host value!
5. run "ansible-playbook -i hosts plexmediaserver.yml -u root -k -v".
6. Enter password when prompted.
7. Go make a cuppa, your not needed anymore.

You may also notice the nas.yml file in the repo, this is the other playbook I used for managing
my NAS storage machine.

## plexmediaserver.yml automates the following

- [x] Updating all base install packages.
- [x] Sets machine hostname.
- [x] Create user groups.
- [x] Create user accounts.
- [x] Adds users to sudoers list.
- [x] Installs Plex Media Server.
- [x] Handles installed software configuration.
- [x] Manages iptables requirements.

## nas.yml automates the following
- [x] Updating all base install packages.
- [x] Sets machine hostname.
- [x] Create user groups.
- [x] Create user accounts.
- [x] Adds users to sudoers list.
- Installation and configuration of
  - [x] Sabnzbd
  - [x] Sickbeard
  - [ ] Couchpatato
  - [ ] Headphones
  - [x] Ngnix
  - [ ] PHP-FPM
  - [ ] Hack
  - [ ] MariaDB
  - [ ] Dnsmasq
  - [ ] Steam Lancache

