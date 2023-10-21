## Disable Bitlocker encryption 

Launch an elevated command prompt and run the command manage-bde off C:, changing C: as necessary.

# WSL

Mount an smb share:

`sudo mkdir /mnt/share`

`sudo mount -t drvfs '\\server\share' /mnt/share`
