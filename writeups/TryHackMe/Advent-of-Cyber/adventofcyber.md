# Advent of Cyber
*Personal writeup/notes of this room for keeping a "methodology's history", direct answer won't be post*


## Table of contents
* Task 6 - Day 1
* Task 7 - Day 2
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
