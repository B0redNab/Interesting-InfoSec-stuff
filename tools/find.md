# Find
Usefull flags:<br/>
* ```2> /dev/null``` to suppress results you're not allowed to access<br/>
* ```-name <pattern>``` and ```-iname <pattern>``` (= case insensitive)<br/>
&nbsp;&nbsp;&nbsp;**If you use wildcards you'll need to enclose your pattern in quotes**<br/>
* ```-perm <perm>``` accept octal format (ex: ```644```) and symbolic form (ex: ```u=rw```)<br/>
&nbsp;&nbsp;&nbsp;```-perm 644``` will return files with this **exact permissions**<br/>
&nbsp;&nbsp;&nbsp;```-perm -644``` will return files with, **at least**, permissions you've specified<br/>
&nbsp;&nbsp;&nbsp;```-perm /644``` will return files that match **any** of the permissions you've set.<br/>
&nbsp;&nbsp;&nbsp;```-perm /4000``` will return files with SUID set<br/>
&nbsp;&nbsp;&nbsp;```-perm /2000``` will return files with GUID set<br/>
&nbsp;&nbsp;&nbsp;```-perm /6000``` will return files with both GUID and SUID set<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;In our case it'll return file readable and writable by **at least** the owner, group or others<br/>
* ```-size <XXX>```can be:<br/>
&nbsp;&nbsp;&nbsp;```200<suffix>``` will matches **equal** to 200<br/>
&nbsp;&nbsp;&nbsp;```-200<suffix>```will matches **lesser than** 200<br/>
&nbsp;&nbsp;&nbsp;```+200<suffix>```will matches **greater than** 200<br/>
&nbsp;&nbsp;&nbsp;Possible to specify a size in suffix ```c``` is for bytes, ```k``` for KB & ```M``` for MB (ex: ```-size 200c```)<br/>
* ```-time <time>``` accept:<br/>
&nbsp;&nbsp;&nbsp;```<prefix>min <value>``` for minutes<br/>
&nbsp;&nbsp;&nbsp;```<prefix>time <value>``` for days<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;```<prefix>``` can be either:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;```a``` to specify when a file was last **accessed**<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;```m``` to specify when a file was last **modified**<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;```c``` to specify when a file was last **changed**<br/>
&nbsp;&nbsp;&nbsp;**Just like** ```size``` **you can use** ```-``` and ```+``` **to search for file modified more/less than X days ago**
* ```-type <type>``` most commons (```f``` and ```d```)<br/>
* ```-user <username>``` will search file owned by the specified user
