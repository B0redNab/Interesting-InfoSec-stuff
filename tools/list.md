# List of tools / cmd<br/>
*A list to keep "track" of tool(s) i discovered / i'm discovering thanks to challenge's website / wargame / CTFs*<br/>
## Already "known"
* ```nmap```
* ```nc```
* ```ZAP```

## Discovering<br/>
### Web <br/>
#### Web crawler <br/>
* ```gobuster```
* ```dirb```
* ```dirbuster```
* ```Burp```
#### Web vulnerability scanner<br/>
* ```Nikto```
#### SQL Injection<br/>
* [```sqlmap```](https://github.com/B0redNab/Interesting-InfoSec-stuff/blob/master/tools/sqlmap.md)<br/>
*Sometimes it's not possible to use tools to automate SQL injection, so you'll need to know how to test manually if a webapp if vulnerable, cf [OWASP WebSec testing guide](https://owasp.org/www-project-web-security-testing-guide/stable/)*
<br/>

#### Hash cracking<br/>
* ```hashid```&nbsp;&nbsp;&nbsp;&nbsp;Identify hash used to encrypt data, with ```-m``` it'll return the hastcat mode
* [```hashcat```](https://github.com/B0redNab/Interesting-InfoSec-stuff/blob/master/tools/hashcat.md)&nbsp;&nbsp;&nbsp;&nbsp;Password recovery tool
* [```John The Reaper```](https://github.com/B0redNab/Interesting-InfoSec-stuff/blob/master/tools/JohnTheReaper.md)
#### Pentest framework<br/>
* [```metasploit```](https://github.com/B0redNab/Interesting-InfoSec-stuff/blob/master/tools/metasploit.md)

<br/>

### OS <br/>
* [```impacket```](https://github.com/SecureAuthCorp/impacket)&nbsp;&nbsp;&nbsp;&nbsp;Collection of usefull windows scripts
* ```gpp-decrypt```&nbsp;&nbsp;&nbsp;&nbsp;Retrieve password stored in GPO (```cpassword``` field value)

#### Linux<br/>
* [```tmux```](https://github.com/B0redNab/Interesting-InfoSec-stuff/blob/master/tools/txmux.md)
* [```find```](https://github.com/B0redNab/Interesting-InfoSec-stuff/blob/master/tools/find.md)
* [```vim```](https://github.com/B0redNab/Interesting-InfoSec-stuff/blob/master/tools/vim.md)
#### Samba<br/>
* [```smbmap```](https://github.com/B0redNab/Interesting-InfoSec-stuff/blob/master/tools/smbmap.md)&nbsp;&nbsp;&nbsp;&nbsp;Enumerate [samba](https://www.samba.org/samba/docs/SambaIntro.html) share drives across an entire domain
* [```smbclient```](https://github.com/B0redNab/Interesting-InfoSec-stuff/blob/master/tools/smbclient.md)&nbsp;&nbsp;&nbsp;&nbsp;Similar to ```smbmap``` but allows you to have a **interactive prompt**
