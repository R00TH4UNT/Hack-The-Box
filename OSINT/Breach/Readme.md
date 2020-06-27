<h1>Hack The Box Breach Challenge</h1>

This is a write-up of [The Breach Challenge](https://www.hackthebox.eu/home/challenges/OSINT#). Here is the problem statement.

![Statement](https://github.com/R00TH4UNT/Hack-The-Box/blob/master/OSINT/Breach/Screenshot_2020-06-27_20-43-09.png)

It says that we have got access to some files off the ftp server of the Super Secure Server website and also a public breach dump of the employees. Also it says that we need to open the "keys" file. Pretty straight-forward.

First I unzipped the Breach.zip file using 7zip command and using hackthebox as the password as it has been given in the statement.
```
7x x Breach.zip -p hackthebox
```
Here are the files that you get:

![Files](https://github.com/R00TH4UNT/Hack-The-Box/blob/master/OSINT/Breach/Screenshot_2020-06-27_20-59-20.png)

Under the ftp-files section we get 2 docx files:
* keys.docx
* web-developer-needed.docx

Needless to say the keys.docx file is password protected. So we look into the web-developer-needed.docx file.

![Hiring notice](https://github.com/R00TH4UNT/Hack-The-Box/blob/master/OSINT/Breach/Screenshot_2020-06-27_22-14-49.png)

It is a recruitment notice that says that the company is looking for a web developer and also an email of the HR department of the company. Now doing a google search on "Super Secure Startup" I found out the following twitter handles regarding the companyand its employees:
* [@SuperSecStartup](https://twitter.com/supersecstartup?lang=en)- A twitter handle of the company
* [@BiankaPhelps](https://twitter.com/biankaphelps?lang=en)- A twitter handle of a HR proffessional of the company.
