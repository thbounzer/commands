#Shell things
---
* Stdout and stderr to file: `yourcommand &> /dev/file`

#Shell shortcuts
 * C-p Previous line (also up arrow)
 * C-n Next line (also down arrow)
 * C-b Back one character (also left arrow)
 * C-f Forward one character (also right arrow)
 * C-a Beginning of line
 * C-e End of line
 * C-l Clear the screen, leaving the current line at the top of the screen 
 * M-< Top of history
 * M-> Bottom of history
 * C-d Delete character from right
 * C-k Delete (kill) text from cursor to end of line
 * C-y Paste (yank) text previously cut (killed)
 * M-d Delete (kill) word
 * C-rtext Reverse search for text
 * C-stext Forward search for text

#Libraries
---
* Display shared libs required by *program*: `ldd program`
* ld.so does not find a shared library, then boom. To update the cache index of shared libraries, use `ldconfig`

