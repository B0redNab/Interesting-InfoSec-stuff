# Hydra
Usefull options:<br/>
* ```-l <user> / -L <path_to_user_list>```
* ```-p <pass> / -P <path_to_pwd_list>```
* ```-vV``` show login+pwd for each attempt
<br/><br/>
Hydra supported several "services" (ex: gtp, ssh, rdp, smb, http-post-form, etc). Full cmd example:<br>
 ```hydra <ip> -l admin -P <path_to_pwd_list> <service> "/path/to/login/page.php:<randomstringusername=^USER^randomstringpassword=^PASS^stringlogin=login:login failed>```
<br/>
**Tips**: as the authent request may differ because of the techno behind the web server or just the authent process, use burp suite to intercept the login request then paste the request into your hydra cmd and "mark" the username, password and login result
within the request w/ ^USER^ ^PASS^ and Login failed
