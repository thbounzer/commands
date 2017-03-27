# MACOSX useful commands
---

#### Mounting a dmg 

* Mount a dmg Volume: `hdiutil attach file.dmg`

* Unmount a dmg Volume: `hdiutil detach /path/to/volume`

#### Ramdisk creation

* Mount a ramdisk of 10 Mb: `hdiutil attach -nomount ram://20480` For calculating size(gb): (size * 1023^3) / 512 (mb): 1023^2

#### FS things
* Erase and format HFS+ : `diskutil erasevolume HFS+ 'givitaname' /dev/device`

---
### User and groups 

* Adding a user to a group (kg to weightunits): ´sudo dseditgroup -o edit -a kg -t user weightunits´
