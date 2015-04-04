#Shell things
---
* Stdout and stderr to file: `yourcommand &> /dev/file`

#Libraries
---
* Display shared libs required by *program*: `ldd program`
* ld.so does not find a shared library, then boom. To update the cache index of shared libraries, use `ldconfig`

