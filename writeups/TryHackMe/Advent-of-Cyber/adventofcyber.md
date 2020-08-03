# Advent of Cyber
*Personal writeup/notes of this room for keeping a "methodology's history", direct answer won't be post*<br/>
Link to the room: [Advent of Cyber](https://tryhackme.com/room/25daysofchristmas)

## Table of contents
* Task 6 - Day 1
* Task 7 - Day 2
* Task 8 - Day 3
* Task 9 - Day 4
<br/>
<br/>

### [Day 1] Inventory Management

#### Description
*Elves needed a way to submit their inventory - have a web page where they submit their requests and the elf mcinventory can look at what others have submitted to approve their requests. It’s a busy time for mcinventory as elves are starting to put in their orders. mcinventory rushes into McElferson’s office.*



*I don’t know what to do. We need to get inventory going. Elves can log on but I can’t actually authorise people’s requests! How will the rest start manufacturing what they want.*  

*McElferson calls you to take a look at the website to see if there’s anything you can do to help. Deploy the machine and access the website at **http://<your_machines_ip>:3000** - it can take up to 3 minutes for your machine to boot!*

*Supporting material for the challenge is [here](https://docs.google.com/document/d/1PHs7uRS1whLY9tgxH1lj-bnEVWtXPXpo45zWUlbknpU/edit?usp=sharing)!*

<br/>

#### Solve
Register a new user (i went with **qwer**) and login with it. Once done open the web console, you should notice a cookie ```authid```, *its value is **base64 encoded***<br/>
Once ```cXdlcnY0ZXI5bGwxIXNz```decoded (i used ```base64 -d``` cmd) i got ```qwer<11 other char>```<br/><br/>
Registered a new user (**qwer2**) and repeat the process. Once decoded i got ```qwer2<11 other char>``` **with the 11 chars being the same for the 2 users**.<br/><br/>
We musst retrieve some data hold by the user ```mcinventory```, so encode ```mcinventory<11 other char>``` to get its base64 encoded version we'll use to access the desired data. Just replace the ```authid``` value with the new base64's one and refresh the page to get access to the desired information.

<br/>

### [Day 2] Arctic Forum

#### Solve
* Checked the code with the web's console, looking for comments that may include sensitive infos => didn't find anything usefull
* Used ```dirb http://<your-machine_ip>:3000```<br/>
Found an interesting page containing a **usefull comment** that will help you solve the chall

<br/>

### [Day 3] Evil Elf
*You'll need to download a pcap file for this chall*<br/>

#### Solve
The first question ask you to find an information into a specific packet. The destination port used in this packet number should be familiar.<br/>
Applying this protocol as a filter in Wireshark will return 3 packets. The first one will give you the answer to the 2nd question. And the 2nd & 3rd one will help us for the last question.<br/>
It's about **password cracking**, you've been ask to retrieve the password of ```buddy``` contained in ```/etc/shadow```<br/>


<br/>

**1.** Username.<br/>
**2.** Password : encrypted password. Usually, password format is ```$id$salt$hashed```, the ```$id``` being the algorithm used. Here are some of the most commons, *cf. [Hashcat](https://hashcat.net/wiki/doku.php?id=example_hashes) for a quite complete list*:<br/>
&nbsp;&nbsp;&nbsp;```$1$``` is MD5<br/>
&nbsp;&nbsp;&nbsp;```$2a$``` is Blowfish<br/>
&nbsp;&nbsp;&nbsp;```$2y$``` is Blowfish<br/>
&nbsp;&nbsp;&nbsp;```$5$``` is SHA-256<br/>
&nbsp;&nbsp;&nbsp;```$6$``` is SHA-512<br/>
  
*add a img of /etc/shadow field*
  
**3.** Last password change (lastchanged) : Days since Jan 1, 1970 that password was last changed<br/>
**4.** Minimum : Number of days left before the user is allowed to change his/her password<br/>
**5.** Maximum : Number of days after that user is forced to change his/her password<br/>
**6.** Warn : Number of days before password is to expire that user is warned that his/her password must be changed<br/>
**7.** Inactive : Number of days after password expires that account is disabled<br/>
**8.** Expire : days since Jan 1, 1970 that account is disabled i.e. an absolute date specifying when the login may no longer be used.<br/>

Now i learned how to identify the hash algorithm used, let's check how to crack it:<br/>
Another method to identify the hash algorithm is ```hashid```:<br/>
```hashid '<your_hash>' -m```<br/>
&nbsp;&nbsp;&nbsp;```-m``` will return the corresponding ```hashcat``` value, it will be needed.<br/><br/>
*i used ```hashcat``` and the ```rockyou.txt``` wordlist available by default on Kali, located in ```/usr/share/wordlists``` (need to decompress it first).*<br/>
```hashcat -m <hash_id> '<your_hash>' /usr/share/wordlists/rockyou.txt --force```<br/>
:warning: Having ```<your_hash>``` **enclosed in single quotes is required if your hash contains** ```$```:warning: <br/>

<br/>

### [Day 4] Training
