---
title: Mounting Stuff (accessing drives)
weight: -20
---

### /etc/fstab
- UUID=$(sudo blkid...) /mnt/... ext4  rw  0 0

### /etc/fstab ntfs
- UUID=$(sudo blkid...) /mnt/storage ntfs-3g defaults,auto,uid=1000,gid=1000,umask=002 0 0

### Boot without non-OS drive connected
- UUID=$(sudo blkid...) /mnt/storage ntfs-3g defaults,nofail,auto,uid=1000,gid=1000,umask=002 0 0

### USB@console w/user permissions
- Check ftype with: fsck -N /dev/xxx
- Volume was not properply unmounted..
    - fsck /dev/xxx (yes fix dirty bit)
- sudo mkdir /run/media/usb (/run/media/weyoun/usb;/media/weyoun/usb..)
- sudo chown -R user /run/media/usb (...)
- sudo chmod 0777 /run/media/usb
- EXT2
    - sudo mount /dev/xxx /run/media/usb -o user,umask=000
- EXT3/4
    - sudo mount /dev/xxx /run/media/usb -o user

### External Storage Multiple Users
- sudo groupadd storage
- sudo chgrp storage /mnt/external...
- sudo chmod g+w /mnt/external..