# Urbackup notes

## urbackup general
- [Debian Install guide](https://www.urbackup.org/debianserverinstall.html)
- [Where to find configuration files on various clients](https://forums.urbackup.org/t/location-of-server-ident-key-and-other-configuration-files/9753)
- ### Force the removal of a client
  `sudo systemctl stop urbackupsrv && sudo urbackupsrv cleanup -a 0% && sudo systemctl start urbackupsrv`  
