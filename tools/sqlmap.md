# SQLmap<br/>
```sqlmap``` is the most popular automated SQL injection tool.<br/><br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;```-hh``` to display the **complete options** of ```sqlmap```<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;```-u <URL>``` to specify the URL to target<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;```-g <Google dork>``` to process **[Google dork](https://en.wikipedia.org/wiki/Google_hacking) results as target URLs**<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;```-p <Parameter>``` to specify the parameter to test (ex: http://exemple.com?test=1, the parameter would be ```test```)<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;```--dbms <Value>``` to specify the **DB's target backend** (ex: if you set it to ```mysql```, then ```sqlmap``` will only test mysql injections)<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;```--level=<1-5>``` ```1``` being the default value. **The higher the value, the more accurate and more tests will be perform**.<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;```--dump``` will dump DB table entries<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;```-D <DB_name>``` combined with ```--tables``` for example, to retrieve tables of the given DB_name, *found w/ ```--dbs```*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;```-T <table_name>``` combined with previous ```-D <DB_name>``` and ```--columns``` to retrieve the colums of a given table<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;```-C <column_name>``` still combined w/ ```-D``` and ```-T``` plus ```--dump``` to retrieve value(s) stored in this column<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;```--os-shell``` to get an interactive OS shell<br/>
