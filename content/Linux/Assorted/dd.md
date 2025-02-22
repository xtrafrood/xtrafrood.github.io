---
title: 💻 Disk Destroyer (DD)
author: Chris Schammert (csmertx -- Christopher Schammert )
published: 2023-01-30
weight: -20
---

<!-- The content of this website was written by Christopher Schammert aka Chris Schammert -->

<br />

> An earned reputation for destroying all the things

## Find blocksize

- ```sudo blkid```

## Write .img file to drive

- ```sudo dd if=/mnt/Storage/qemu/winxppro.img of=/dev/sXX```

- ```sudo gunzip -c /backup/backup.image.gz | dd of=/dev/sXX```

## Backup drive to compressed .img

- ```sudo dd if=/dev/sXX conv=sync,noerror bs=4K | gzip -c > /backup/backup.image.gz```

## Blank a drive (NOT FOR SSDs!)

- ```sudo dd if=/dev/zero of=/dev/xXx bs=1M```

## Securely Blank a drive (NOT FOR SSDs!)

- ```sudo dd if=/dev/urandom of=/dev/xXx bs=1M```

## Blank MBR (!)

- ```sudo dd if=/dev/zero of=/dev/xXx bs=446 count=1```

## Copy DVD

> MakeMKV for copying media is highly recommended

- Open video with VLC first..

    > Because reasons..

- ```blocks=$(isosize -d 2048 /dev/sr0)```

- ```sudo dd if=/dev/sr0 of=/tmp/output.iso bs=2048 count=$blocks status=progress```

## Copy CD

- ```mount```

- ```sudo umount /dev/cdrom```

- ```sudo dd if=/dev/cdrom of=/dir/cdimg1.iso```

## Resources

- [Arch Wiki: dd](https://wiki.archlinux.org/title/Dd)

<br />

<div style="text-align: center; font-size:12px; color:dimgray">
    Created: 01/07/2023 • Edited: 02/09/2025 • Author: Chris Schammert (csmertx) • 
    <a href="https://github.com/csmertx/csmertx.github.io/commits/main/content/Linux/Assorted/dd.md" 
       title="Github.com | csmertx \ csmertx.github.io \ commits \ main \ content \ Linux \ Assorted \ Disk Destroyer (DD)">
       History 🕵️
    </a>
</div>