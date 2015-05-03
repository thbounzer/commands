#Shell things
---
* Stdout and stderr to file: `yourcommand &> /dev/file`

#Shell expansion designators
 * !! Spoken as bang-bang, this command refers to the most recent command. The exclamation point is often called bang on Linux and Unix systems.
 * !n Refer to command n from the history. Use the history command to display these numbers. 
 * !-n Refer to the current command minus n from the history.
 * !string Refer to the most recent command starting with string.
 * !?string Refer to the most recent command containing string.
 * ^string1^string2 Quick substitution. Repeat the last command, replacing the first occurrence of string1 with string2.

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
##


#Libraries
---
* Display shared libs required by *program*: `ldd program`
* ld.so does not find a shared library, then boom. To update the cache index of shared libraries, use `ldconfig`

#Password generation
---
* Generation of pretty secure random password: `openssl rand -base64 32`





