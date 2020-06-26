<h1>Hack The Box Easy Phish Challenge</h1>

This is a writeup for Hack The Box OSINT challenge [Easy Phish](https://www.hackthebox.eu/home/challenges/OSINT). This is the problem statement.

![Challenge Screenshot](https://github.com/R00TH4UNT/Hack-The-Box/blob/master/OSINT/Easy%20Phish/Screenshot_2020-06-26_08-36-59.png)

It says that Customers of secure-startup.com have been receiving lots of phishing emails. So we can take a guess that this problem is about email spoofing method.
Now if you Google about how domains prevent their emails from getting spoofed you would find three ways:
* SPF (Sender Policy Framework)
* DKIM (DomainKeys Identified Mail)
* DMARC (Domain-based Message Authentication, Reporting and Conformance)

You can visit [here](https://www.smartertools.com/blog/2019/04/09-understanding-spf-dkim-dmarc) to know more about how each of them work.
We are now going to take a look at these records and see if we get anything interesting. 
I am using these tools to view the [SPF](https://mxtoolbox.com/spf.aspx) and [DMARC](https://mxtoolbox.com/dmarc.aspx) records.
Here are the results:

![SPF](https://github.com/R00TH4UNT/Hack-The-Box/blob/master/OSINT/Easy%20Phish/Screenshot_2020-06-26_08-56-32.png)



![DMARC](https://github.com/R00TH4UNT/Hack-The-Box/blob/master/OSINT/Easy%20Phish/Screenshot_2020-06-26_08-56-46.png)

So as you can see we have got our flag ie, HTB{RIP_SPF_Always_2nd_F1ddl3_2_DMARC}

