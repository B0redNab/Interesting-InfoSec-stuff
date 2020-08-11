# Smbmap<br/>
```smbmap``` is use to enumerate samba shares across a domain<br/><br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;```-u <username>``` if ommited, null session assumed<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;```-p <password || NTLM hash>```<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;```-H <host_IP>```<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;```-x <cmd>```, assume you have the permissions to do it w/ the credentials provided, combined w/ ```--mode <cmd_mode>``` that can be either
```wmi```(**default**) or ```psexec```<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;```-s <share>``` to specify a share (default is ```C$```)<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;```-d <domain>``` to specify the doamin name<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;```--download <file_path>``` download a file from the remote system (ex: "C$\temp\pass.txt")<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;```--upload <src> <dest>``` upload a file a the remote system (ex: "/tmp/payload.exe C$\temp\payload.exe")<br/>
