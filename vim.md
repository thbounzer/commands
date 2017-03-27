#Vim tips and others

* set the tabspace: set tabstop=x set tabstop=n - set shiftwidth=n
* delete until the file end `dG`
* Remove comments: First char, press CtrlV, and go down until the last commented line and press x, that will delete all the comment characters vertically.
* Comment a block of text: go to the first line you want to comment, press CtrlV, and select until the last line. Second, press ShiftI(commentchar)Esc (then give it a second), and it will insert a (commentchar) character on all selected lines.
* Search and replace(each occurrence all lines) : `:%s/this/that/g` 
