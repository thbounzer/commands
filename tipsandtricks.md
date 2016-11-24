#tips and tricks
---
##remap caps lock with esc (useful with vim)
* paste this to a file: 
		! Swap caps lock and escape
		remove Lock = Caps_Lock
		keysym Escape = Caps_Lock
		keysym Caps_Lock = Escape
		add Lock = Caps_Lock
* then invoke the file with: `xmodmap file`

##Exim cheatsheet
* [http://bradthemad.org/tech/notes/exim_cheatsheet.php](exim cheatesheet)

##generate a standard password (works with debian, needs testing with other distro) 
* use this command: `perl -e 'print crypt("password","\$6\$saltsalt\$") . "\n"'` 

##Propagate a system change to the kernel
* `for i in `grep line /sys/devices/system/memory/*/state |grep offline|cut -f6 -d/` ; do echo online > /sys/devices/system/memory/$i/state $i;done`

##See with wireshark a remote tcpdump using ssh:
* Create a named pipe on your machine 
* Start the remote tcpdump, write to local pipe: `ssh user@machine "tcpdump -s 0 -U -n -w - -i yourinterface not port 22" > /tmp/yourlocalnamedpipe`
* Run wireshark: `wireshark -k -i /tmp/yourlocalnamedpipe`

## Delete found files with find:
* execute: `find . -name something -exec rm -rf {} \;`

## See every cron job for every user:
* `for user in $(cut -f1 -d: /etc/passwd); do echo $user; crontab -u $user -l; done`

## No more ssh timeouts:
* Add this to your .ssh/config:
```
Host *
  ServerAliveInterval 240
```

## Kill a expired not responding session:
Host *
* Enter ~ .

## Netcatting
`netcat -l 12345 > file.pdf` 
or 
`netcat -l -p 12345 > file.pdf`
then, on the source pc 
`netcat $MY_IP_ADDRESS 12345 < file.pdf`

## Sound generation with sox
Generate a 4000 Hz square soundwave with a time length of 0.1 seconds and a gain of -18
`play "|sox -n -p synth 0.1 squ 4000 gain -18"`


## Multiple numbered-named file download with curl

`curl -o 'file_#1.pdf' 'http://url.address.web/filesdir/filename_[00-28].pdf'`

## Kvm use liveusb image to boot

`kvm -usbdevice disk:/path/to/liveusb.img -boot menu=on`

## Multiple pdf concatenation with ghostscript

`gs -dBATCH -dNOPAUSE -q -sDEVICE=pdfwrite -sOutputFile=merged.pdf file1.pdf file2.pdf ..`

## Top ten biggest dirs/files
`du -hsx * | sort -rh | head -10`

## SCSI scanning for new disks
`grep mpt /sys/class/scsi_host/host?/proc_name`
and then, assuming that the grepped host is host0:
`echo "- - -" > /sys/class/scsi_host/host0/scan`

## Force swap to ram (WARNING: if there is not enough memory available, kernel will kill processes. use with caution)
* Launch this command:`swapoff -a` then keep an eye on memory occupation (with htop for example) 
* When swapoff has completed the transfer of swap to phy ram, enable swap again: `swapon -a`

## Change swappiness
* Swappiness controls how aggressive the kernel should use swap mem. 0=avoid swapping as much as possible, 100=use swapping as much as possible
* Value stored in /proc/sys/vm/swappiness
* Temp change: `sudo sysctl vm.swappiness=10`
* Perm change(WARNING): `echo vm.swappiness=10 >> /etc/sysctl.conf`

 

