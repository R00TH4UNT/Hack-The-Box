<h1>Hack The Box Breach Challenge</h1>

This is a write-up of [The Breach Challenge](https://www.hackthebox.eu/home/challenges/OSINT#). Here is the problem statement.

![Statement](https://github.com/R00TH4UNT/Hack-The-Box/blob/master/OSINT/Breach/Screenshot_2020-06-27_20-43-09.png)

It says that we have got access to some files off the ftp server of the Super Secure Server website and also a public breach dump of the employees. Also it says that we need to open the "keys" file. Pretty straight-forward.

First I unzipped the Breach.zip file using 7zip command and using hackthebox as the password as it has been given in the statement.
```
7x x Breach.zip -p hackthebox
```
