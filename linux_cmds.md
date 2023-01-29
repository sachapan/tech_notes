
# Linux command line-fu

## xargs dealing with spaces

Specify the delimiter as only newline.

`xargs -d "\n"`

Find all symlinks - like, for example, if you destroyed all of them on a filesystem you were trying to migrate from one hard disk to another and now you need to recover them from the backup that you did take before being an idiot:


find / -type l -exec ls -l {} \;


When copying from one volume to another:


cp -ax /<source> /<destination>


Copy MBR with and without partition table


dd if=/dev/hda of=/dev/hdb bs=512 count=1
dd if=/dev/hda of=/dev/hdb bs=446 count=1


Remove all non-current kernel packages on Ubuntu:


dpkg -l linux-* | awk '/^ii/{ print $2}' | grep -v -e `uname -r | cut -f1,2 -d"-"` | grep -e [0-9] | xargs sudo apt-get -y purge
