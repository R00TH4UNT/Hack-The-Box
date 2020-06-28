<h1>Hack The Box We Have A Leak Challenge</h1>

This is a write-up of [We Have A Leak](https://www.hackthebox.eu/home/challenges/OSINT) challenge. Here is the problem statement:

![Problem statement](https://github.com/R00TH4UNT/Hack-The-Box/blob/master/OSINT/We%20have%20a%20leak/Screenshot_2020-06-28_10-13-49.png)

It says that Super Secure Startup's private info has been leaked and we need to find it. Also a zip file has been given with the password "hackthebox". Forst I download the file and uncompress it. Here is the file structure of the zip file:
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

