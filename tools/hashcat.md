# Hashcat
```hashcat``` is a password recovery tool / hash cracking tool<br/>
Full list of hashcat modes [here](https://hashcat.net/wiki/doku.php?id=example_hashes)<br/><br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;```-m <hash_id>``` or ```--hash-type <hash_id>``` to **specify the hash's type**, ```<hash_id>``` can be retrieve with ```hashid <hash> -m```<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;```-a <attack_mode>``` to specify which attack method to use:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;```0 = Straight``` e.q **Dictionnary / worldlist attack**<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;```1 = Combination``` Usage of **multiple wordlists**<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;```3 = Brute-force``` Usage of ```mask``` actually, instead of ```brute-force``` because it's **more efficient** with the use of **built-in charsets and pattern**<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;```?l = abcdefghijklmnopqrstuvwxyz```<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;```?u = ABCDEFGHIJKLMNOPQRSTUVWXYZ```<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;```?d = 0123456789```<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;```?h = 0123456789abcdef```<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;```?H = 0123456789ABCDEF```<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;```?s = «space»!"#$%&'()*+,-./:;<=>?@[\]^_`{|}~```<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;```?a = ?l?u?d?s```<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;```?b = 0x00 - 0xff```<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;```--increment``` permit to automatically **test possibilities until it reach the mask length** sets by the user<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;ex: ```hashcat -m <hash_type> -a 3 ?l?l?l?l?l --increment``` will test 1 length possibilities, then 2, up to provided mask length<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;```6 = Hybrid (Worldlist + Mask)```<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;```7 = Hybrid (Mask + Wordlist)```<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Thoses 2 are the same, in a case you'll use a wordlist and append a mask to the wordlist content. And in the other case you'll prepend a mask to it<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;ex: ```... -a 6 example.dict ?d?d?d?d``` => ```passwordXXXX```<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;```... -a 7 ?d?d?d?d example.dict``` => ```XXXXpassword```<br/>
