# Proxmox

### Post install scripts

From <https://tteck.github.io/Proxmox/>:

`bash -c "$(wget -qLO - https://github.com/tteck/Proxmox/raw/main/misc/post-pve-install.sh)"`

### Removing the subscription nag

[My ansible script](https://github.com/sachapan/ansible/blob/main/playbooks/proxmox-nag.yml)

https://github.com/foundObjects/pve-nag-buster

### Other hints and reminders

[Import qcow2 images](https://ostechnix.com/import-qcow2-into-proxmox/)

Slow boot times on containers?  Change IPv6 to SLAAC.

[Resolve error: You have not turned on protection against thin pools running out of space.](https://www.thegeekdiary.com/how-to-enable-the-automatic-extension-for-a-thin-lvm-volume/)

[Adding new thinpool](https://www.diytechguru.com/2020/12/12/create-lvm-thin-pool-in-proxmox/)

I found [this article](https://static.xtremeownage.com/blog/2024/proxmox---debian-cloud-init-templates/#clone) very helpful in further automating vm creation with cloudinit.
