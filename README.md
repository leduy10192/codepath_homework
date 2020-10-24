# Project 7 - WordPress Pentesting

Time spent: **10** hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

### 1. (Required) Vulnerability Name or ID: Authenticated Stored Cross-Site Scripting(XSS1)
  - [x] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2.3

  - [x] GIF Walkthrough: ![Alt Text](http://g.recordit.co/azZ7tIajjz.gif)
  - [x] Steps to recreate: 
    - ++ If the attacker types /* <a href="[caption code=]"></a><a title=" onmouseover=alert('test')  ">link</a>. */
    - ++ Then WP will become "test" hyperlink
  - [x] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
  
  
  
### 2. (Required) Vulnerability Name or ID: User Enumeration 
  - [x] Summary: 
    - Vulnerability types: User Enumeration
    - Tested in version: 4.2
    - Fixed in version: 4.7.3
  - [x] GIF Walkthrough: ![Alt Text](http://g.recordit.co/LWkkhQYgSf.gif)
  
  - [x] Steps to recreate: 
   - ++ Create a new user account
   - ++ Enter admin as a username and an invalid password to log in 
   - ++ An error message is shown to tell attacker where the error comes from.
   - ++ When you randomly input username and password, it shows the error which is invalid username
   
  - [x] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)

### 3. (Required) Vulnerability Name or ID: Unauthenticated Stored Cross-Site Scripting (XSS2)
  - [x] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2.4
  - [x] GIF Walkthrough: ![Alt Text](http://g.recordit.co/Wkr8JDDzSy.gif)
  
  - [x] Steps to recreate: 
       - ++ Create a new post, and insert the code [caption width="1" caption='<a href="' ">]</a><a href=" onmouseover='alert("WARNING")' ">CAPTION!</a> into the post content . 
       - ++ Then it shows 1 when you view the comment of this post in future.
  - [x] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
### 4. (Optional) Vulnerability Name or ID : Oversized File Upload Error CSS
  - [x] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2.12
  - [x] GIF Walkthrough: ![Alt Text](http://g.recordit.co/bnn6gFSMAL.gif)
  
  - [x] Steps to recreate: 
  - ++ Create a new video format post
  - ++ Type in [embed src='https://youtube.com/embed/123\x3csvg onload=alert(9234234)\x3e'][/embed]
  - ++ It will show 123456 each time 
  - [x] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)

## Assets

List any additional assets, such as scripts or files

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

Describe any challenges encountered while doing the work
Pretty much a straight forward assignment. Nothing to discuss more

## License

    Copyright [2020] [Duy Le]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.

