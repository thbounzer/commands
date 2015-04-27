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
