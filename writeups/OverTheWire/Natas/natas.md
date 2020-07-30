# Natas
*Personal writeup of this wargame*

Link to the wargame: [Natas](https://overthewire.org/wargames/natas/)

## Table of contents
* Level 0 -> Level 1
* Level 1 -> Level 2
* Level 2 -> Level 3
* Level 3 -> Level 4
* Level 4 -> Level 5
* Level 5 -> Level 6
* Level 6 -> Level 7
* Level 7 -> Level 8
* Level 8 -> Level 9
* Level 9 -> Level 10
* Level 10 -> Level 11
* Level 11 -> Level 12
* Level 12 -> Level 13
* Level 13 -> Level 14
* Level 14 -> Level 15
* Level 15 -> Level 16
* Level 16 -> Level 17
* Level 17 -> Level 18
* Level 18 -> Level 19
* Level 19 -> Level 20
* Level 20 -> Level 21
* Level 21 -> Level 22
* Level 22 -> Level 23
* Level 23 -> Level 24
* Level 24 -> Level 25
* Level 25 -> Level 26
* Level 26 → Level 27
* Level 27 → Level 28
* Level 28 → Level 29
* Level 29 → Level 30
* Level 30 → Level 31
* Level 31 → Level 32
* Level 32 → Level 33
* Level 33 → Level 34
<br/>
<br/>


### Level 0
![](https://github.com/B0redNab/Interesting-InfoSec-stuff/blob/master/writeups/OverTheWire/Natas/screens/Level0.PNG?raw=true)
* Open ```http://natas0.natas.labs.overthewire.org/``` <br/>
***Username:** natas0 **Password:** natas0*
* Open the web console of your browser, you'll find the password ```gtVrDuiDfck831PqWsLEZy5gyDz1clto``` in the code (comment)<br/>
### Level 0 -> Level 1
* Use the previsouly found password to connect
* Open the web console of your browser, the password is in the code again ```ZluruAthQk7Q2MqmDeTiUij2ZvWy2mBi```<br/>
### Level 1 -> Level 2
* Once connected you'll have a message indicating "*There is nothing on this page*"<br/>
But if you open your web console you should see a ```img``` tag with  ```src="files/pixel.png"```
* I added ```/files/pixel.png``` to the url and was expecting to find the password but there isn't anything usefull here<br/>
As the image is contained in the ```files``` directory i checked it out. There's another file ```users.txt```containing the password ```sJIJNW6ucpu6HPZ1ZAchaDtwd7oGrD14```<br/>
### Level 2 -> Level 3
* Once connected you'll have another message indicating "*There is nothing on this page*"<br/>
Opened the web console again and notice a comment saying "*No more information leaks!! Not even Google will find it this time...*"<br/>
Made me think about the ```robots.txt``` file, *cf. [https://developer.mozilla.org/en-US/docs/Glossary/Robots.txt](https://developer.mozilla.org/en-US/docs/Glossary/Robots.txt)*
