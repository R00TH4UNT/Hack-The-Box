<h1>Hack The Box We Have A Leak Challenge</h1>

This is a write-up of [We Have A Leak](https://www.hackthebox.eu/home/challenges/OSINT) challenge. Here is the problem statement:

![Problem statement](https://github.com/R00TH4UNT/Hack-The-Box/blob/master/OSINT/We%20have%20a%20leak/Screenshot_2020-06-28_10-13-49.png)

It says that Super Secure Startup's private info has been leaked and we need to find it. Also a zip file has been given with the password "hackthebox". First I download the file and uncompress it (Preferrably use 7zip to avoid errors). Here is the file structure of the zip file:
```
we_have_a_leak.zip (password: hackthebox)
|
|----> mock_ssh_login.zip
             |
             |---->username.zip (password-protected)
                      |
                      |----->password.zip (password-protected) 
                                |
                                |------> flag.txt
```
First we need to find out the password of username.zip.
I googled up "Super secure startup" and it gave me two twitter accounts:
* [@SuperSecStartup](https://twitter.com/supersecstartup?lang=en)
* [@BiankaPhelps](https://twitter.com/biankaphelps?lang=en)

Looking through the Super Secure Startup's posts I found two other employees:
* [Josh Terranwald](https://twitter.com/JTerranwald) who had joined on March 2019.

![Twitter post](https://github.com/salty-nutella/Hack-The-Box/blob/master/OSINT/We%20have%20a%20leak/Screenshot_2020-06-30_08-24-08.png)

* [Johanna Boyce](https://twitter.com/boyce_johanna) whose email address (j.boyce@supersecurestartup.com) was given in the reply to a [post](https://twitter.com/SuperSecStartup/status/1110299017127313413) by the Super Secure Startup.

![Twitter post](https://github.com/salty-nutella/Hack-The-Box/blob/master/OSINT/We%20have%20a%20leak/Screenshot_2020-06-30_08-27-31.png)

Now from the email of Johanna Boyce, we get an idea that the username of an employee in this company is of the format 
```
[First letter of name].[Last name]
```
So I try the following passwords in the username.zip file:
* b.phelps
* j.terranwald
* j.boyce

And I found that the password was j.terranwald.

Now we have to decrypt the password.zip file. There was another [post](https://twitter.com/BiankaPhelps/status/1110340484562649088/photo/1) in the twitter handle of Bianka Phelps which gives us the default ssh password of the company.

![SSH pass](https://github.com/salty-nutella/Hack-The-Box/blob/master/OSINT/We%20have%20a%20leak/Screenshot_2020-06-30_08-52-55.png)

However we need to change the season and year according to the joining date of the employee J. Terranwald ie (March 25, 2019). So the password becomes:
```
SupSecStart#Spring2019
```
Decompressing password.zip we get the flag: HTB{Sav3_The_Startup_Sav3_The_W0rld_#Hiro}
