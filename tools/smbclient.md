# Smbclient
Similar to ```smbmap``` but there is an interactive prompt<br/><br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;```-w <workgroup>``` to specify the domain/workgroup to use when connecting to the host<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;```-I <host_ip>```<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;```-c <cmd>``` *just like ```smbmap```, surround your command with **double quotes***<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;```-U <username>```<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;```-P <password>```<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;```-N``` to specify to **not use a password**<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;```get <filename>```, *once you get a interactive prompt*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;```put <local_filename> <remote_filename>```, *once you get a interactive prompt*<br/>
List of cmd available once you've got an interactive prompt: [here](https://www.samba.org/samba/docs/current/man-html/smbclient.1.html)
