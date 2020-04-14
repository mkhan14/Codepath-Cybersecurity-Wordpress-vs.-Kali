# Project 7 - WordPress Pentesting

Time spent: **20** hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

1. (Required) User Enumeration
  - [ ] Summary: By using wpscan to enumerate all usernames, we can see if a user account exists on WordPress.
    - Vulnerability types: User Enumeration
    - Tested in version: 4.2
    - Fixed in version: 
  - [ ] GIF Walkthrough: <img src="enumerate" width="800">
  - [ ] Steps to recreate: Run ```wpscan --url http://wpdistillery.vm --enumerate u``` in the Kali Linux terminal.
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
2. (Required) Vulnerability Name or ID
  - [ ] Summary: We can brute force passwords and get username and password combinations by using a wordlist of common passwords.
    - Vulnerability types: Bruteforce
    - Tested in version: 4.2
    - Fixed in version: 
  - [ ] GIF Walkthrough: <img src="wordlist2" width="800">
  - [ ] Steps to recreate: Run ```wpscan --url http://wpdistillery.vm --passwords /home/kali/Desktop/rockyou.txt --usernames admin``` in the Kali Linux terminal.
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
3. (Required) Authenticated Stored Cross-Site Scripting (XSS)
  - [ ] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 
  - [ ] GIF Walkthrough: <img src="post" width="800">
  - [ ] Steps to recreate: On the WordPress site, add a new post and put ```<a href="[caption code="]</a><a title=" onmouseover=alert('hi') ">link</a>``` into the body of the post. Then click preview to see the result. An alert pops up after hovering the mouse over "link".
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)

## Assets

List any additional assets, such as scripts or files

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

The main challenges that I encountered was setting up Vagrant, finding commands in Powershell that are equivalent to commands in Linux, and running the Kali Linux terminal as the administrator.

## License

    Copyright [2020] [Mahin Khan]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
