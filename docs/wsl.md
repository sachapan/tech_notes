
# WSL

## Mount an smb share:

`sudo mkdir /mnt/share`

`sudo mount -t drvfs '\\server\share' /mnt/share`

## Getting systemd working

Set the systemd flag set in your WSL distro settings
You will need to edit the wsl.conf file to ensure systemd starts up on boot.

Add these lines to the /etc/wsl.conf:

`[boot]
systemd=true`

Final steps
With the above steps done, close your WSL distro Windows and run wsl.exe --shutdown from PowerShell to restart your WSL instances. Upon launch you should have systemd running. You can check this with the command systemctl list-unit-files --type=service which should show your services’ status.
