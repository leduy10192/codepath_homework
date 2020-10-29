x# Project 8 - Pentesting Live Targets

Time spent: **3** hours spent in total

> Objective: Identify vulnerabilities in three different versions of the Globitek website: blue, green, and red.

The six possible exploits are:

* Username Enumeration
* Insecure Direct Object Reference (IDOR)
* SQL Injection (SQLi)
* Cross-Site Scripting (XSS)
* Cross-Site Request Forgery (CSRF)
* Session Hijacking/Fixation

Each color is vulnerable to only 2 of the 6 possible exploits. First discover which color has the specific vulnerability, then write a short description of how to exploit it, and finally demonstrate it using screenshots compiled into a GIF.

## Blue

Vulnerability #1: SQL Injection

Description: The Blue target is vulnerable for SQL Injection Attack. As replacing the salesperson's id with a SQL command: 'OR SLEEP(3)=0--' causes the page to delay for 3 seconds before displaying the result.

<img src="http://g.recordit.co/cZjbTwM49Q.gif">

Vulnerability #2: Session Hijacking/Fixation

Description: Using the tool provided by CodePath (public/hacktools/change_session_id.php), we can obtain the session ID from a browser and use it to login to another page in another browser with clear cookies.

<img src="http://g.recordit.co/VmE1eHk27J.gif">

## Green

Vulnerability #1: Username Enumeration

Description: Logging in with correct username applies "failure" css class (a bold alert message) while logging in with incorrect usename applies "failed" css class. We can use the "inspect element" feature in firefox to find this vulnerability.

<img src="http://g.recordit.co/uCteXlTk8p.gif">

Vulnerability #2: Cross-Site Scripting

Description: In the Contact Us page, add a script (<script>alert(‘XSS Attack Found by LeDuy!’)</script>) in both name and feedback and submi. Then login and go to the Feedback button, an alert will pop up from running script.

<img src="http://g.recordit.co/wtK2QMQuCE.gif">


## Red

Vulnerability #1:  Insecure Direct Object Reference

Description:From the URL: https://35.184.88.145/green/public/salesperson.php?id= , if we put id = 11 in the red target, it will show a fired salesperson while doing the same in the green target just refreshes the page.

<img src="http://g.recordit.co/36msh9P1PJ.gif">

Vulnerability #2:  Cross-Site Request Forgery

Description: Changing the value of csrd_token and then edit the users is only doable in the red target not the other blue and green target

<img src="http://g.recordit.co/LXgKYNZuiD.gif">


## Notes

Describe any challenges encountered while doing the work
