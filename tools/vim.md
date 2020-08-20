# Vim
[Cheatsheet](http://vimsheet.com/)
### Moving around<br/>
* ```h``` to go **left** ```j``` **down** ```k``` **up** ```l``` **right**
* ```:q``` or ```helpclose```
* ```:u``` to undo & ```Ctrl+R``` to redo
* ```w``` to move forward word per word & ```b``` for the opposite
* ```e``` to move to the next end of a word & ```ge``` for the opposite
* ```^``` move the cursor to the first non-blank character of the line (```0``` to the very first char of the line) & ```$``` to the end
<br/>

### Insert<br/>
* ```<count>a``` to **append** *count* time the text typed (need to ```esc``` for the changes to be applied)
* ```<count>i``` similar to ```a``` but **before the cursor**
* ```<count>A``` same as ```a``` but at the end of the line
* ```<count>I``` same as ```i``` but at the beginning of the line
* ```<count>o``` to jump to a new line and type the text *count* time(s)<br/>
&nbsp;&nbsp;&nbsp;*If you don't type any text and press ```esc``` it'll insert X new blank lines*
<br/>

### Edit<br/>
* ```:tabedit <filename>``` to open a **new tab** with the desired file
* ```gt``` to go to the next tab & ```gT``` to go to the previous one
* ```<count>yy``` to copy X line(s)
* ```y$``` to copy from the cursor, to the end of the line
* ```<count>dd``` to cut X line(s)
* ```D``` to cut from the cursor, to the end of the line
* ```x``` to cut a character
* ```p``` to paste the clipboard **after the cursor**
* ```P``` to paste the clipboard **before the cursor**
<br/>

### Search<br/>
* ```/<pattern>``` to search, **forward**; for a *pattern*
* ```?<pattern>``` to search, **backward**, for a *pattern*
* ```n``` to repeat the search in the **same direction**
* ```N``` to repeat the searh in the **opposite direction**
* ```:%s/<old>/new/g``` to replace *old* by *new*
* ```:vimgrep <pattern> <file>``` to search for *pattern* in the different(s) *file(s)*
### Exit<br/>
* ```:w !sudo tee %``` to save the changes but don't exit, **as root**
* ```:wqa``` to save and quit **all active tabs**
