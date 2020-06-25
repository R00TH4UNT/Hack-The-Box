<h1>Hack The Box Invite Challenge</h1>

This is a write-up of [Hack-The-Box invite challenge](https://www.hackthebox.eu/invite) as on 25/6/2020.

![Screenshot of initial page](https://github.com/R00TH4UNT/Hack-The-Box/blob/master/Invite%20Challenge/Screenshot_2020-06-25_20-59-34.png)

When we visit the url we have this invite code form for login.
Opening up Inspector in Firefox (by pressing the F12 key) we can find an interesting image in the console tab.

![Screenshot of console](https://github.com/R00TH4UNT/Hack-The-Box/blob/master/Invite%20Challenge/Screenshot_2020-06-25_21-14-59.png)

The image tells us to take a look at the javascript files that the site loads.
So by clicking on the Debugger tab we can easily view all the js files. We find that there are two of them:
* htb-frontend.min.js
* inviteapi.min.js

![Screenshot of Debugger tab](https://github.com/R00TH4UNT/Hack-The-Box/blob/master/Invite%20Challenge/Screenshot_2020-06-25_21-20-45.png)

Now for obvious reasons we are going to take a look at the inviteapi file. If you have problems understanding the javascript code you can use [this site](www.jsnice.org) for deobfuscation.

![Screenshot of JS file](https://github.com/R00TH4UNT/Hack-The-Box/blob/master/Invite%20Challenge/Screenshot_2020-06-25_21-26-51.png)

By reading the code we can see that a POST request is being sent to the link /api/invite/how/to/generate. 
So we try sending a POST request to the link using cURL (You can use any tool of your choice). Here is the syntax for cURL.

```
curl -X POST https://www.hackthebox.eu/api/invite/how/to/generate
```
We get a response. Here is a screenshot of it.

![Screenshot of response](https://github.com/R00TH4UNT/Hack-The-Box/blob/master/Invite%20Challenge/Screenshot_2020-06-25_21-37-19.png)

So I have a [ROT13](https://en.wikipedia.org/wiki/ROT13) encoded data. Please note that you may recieve data with different encryptions. Use suitable tools to decrypt the data. 
when I decrypt the data I get the following

![Screenshot of decrypted data](https://github.com/R00TH4UNT/Hack-The-Box/blob/master/Invite%20Challenge/Screenshot_2020-06-25_21-43-00.png)
