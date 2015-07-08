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
