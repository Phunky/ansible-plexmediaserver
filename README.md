# Plex Media Server

This is my Ansible playbook for setting up Plex Media Server on a CentOS 6.x minimal install.

Currently I run PMS on an Intel NUC with all my media stored on a TranquilPC BBS2 NAS, which is
shard via SAMBA. The NAS is managed by its own Playbook which i'll be sharing shortly.

This is used soley for transencoding media for each of my Plex clients (iOS, Andriod and Chromecasts) as the NAS wasn't quite powerful to handle this task (It's only Intel ATOM based!).

# Currently automates the following

- [x] Updating all base install packages.
- [x] Sets machine hostname.
- [x] Create user groups.
- [x] Create user accounts.
- [x] Adds users to sudoers list.
- [x] Installs Plex Media Server.
- [ ] Installs Sabnzbd.
- [ ] Installs Sickbeard.
- [ ] Installs Couchpatato.
- [ ] Installs Headphones.
- [ ] Installs Ngnix.
- [x] Handles installed software configuration.
- [x] Manages iptables requirements.


