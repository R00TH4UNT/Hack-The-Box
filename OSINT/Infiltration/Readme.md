<h1>Hack The Box Infiltration</h1>

This is a writeup of Hack The Box [Infiltration Challenge](https://www.hackthebox.eu/home/challenges/OSINT).
Here is the problem statement.

![Challenge Screenshot](https://github.com/R00TH4UNT/Hack-The-Box/blob/master/OSINT/Infiltration/Screenshot_2020-06-26_09-59-39.png)

We are given the name of a company (Evil Corp LLC) and asked to look into social media sites for any useful information. 
First and foremost I ran a Google search on Evil Corp LLC to find out more info and here are the results I got.

![Google search](https://github.com/R00TH4UNT/Hack-The-Box/blob/master/OSINT/Infiltration/Screenshot_2020-06-26_10-07-07.png)

On the very first result I found that there was a string in the flag format, so I visted the LinkedIn page. However this was not the flag. It was a Base64 encoded string that tells you to keep going. So I looked at the employees' profiles where I found nothing except [this](https://www.linkedin.com/in/brian-delany-2ab807195/?trk=public_profile_browsemap_profile-result-card_result-card_full-click):

![Brian Delany](https://github.com/R00TH4UNT/Hack-The-Box/blob/master/OSINT/Infiltration/Screenshot_2020-06-26_10-14-58.png)

Again it was a Base64 encoded string that translates into "There are people out there that will lie, steal and cheat to hide their own imperfections and to further their progression in life. We will not sit by whilst these practices are going on. The truth will be exposed!".
Not much helpful.

So I looked into the 2nd Google search result that was the Instagram profile of [Eryn Mcmahon](https://www.instagram.com/eryn_mcmahon12/).
Looking through her posts I found this [pic](https://www.instagram.com/p/BvbnFhTj9YS/) which says "Hard at work on my first day for @EvilCorpLLC lots of factors to relationalise!".
You could confirm that it was the flag by zooming into the ID card of Evil Corp.

![ID](https://github.com/R00TH4UNT/Hack-The-Box/blob/master/OSINT/Infiltration/Screenshot_2020-06-26_10-25-49.png)

NOTE: Since this challenge was solved previouly I found out the solution pic in the Google Images Search results for Evil Corp LLC :wink:
