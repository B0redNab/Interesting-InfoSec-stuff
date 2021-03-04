# Nmap
Find a specific NSE script:
* [NSE doc](https://nmap.org/nsedoc/)
* ```/usr/share/nmap/scripts/script.db```

## Firewall evasion
Some options to evade firewalls/IDS, full list [here](https://nmap.org/book/man-bypass-firewalls-ids.html)<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;```-f``` (fragment packets into 8 bits or less **after the IP header**)<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;```-f -f``` (fragment packets into 16 bits)<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;``` --mtu <size>``` (<size> musst be a multiple of 8)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *Fragmentation don't work with TCP Connect Scan (-sT)*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;```-D <decoy1>[,<decoy2>][,ME]``` can be use in pair with ```RND:<number>``` to generate X random addr.<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;```--source-port <port_num>``` can work if net admin allow incoming common port request, like DNS or FTP<br/>
