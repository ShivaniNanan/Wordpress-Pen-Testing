# Project 7 - WordPress Pen Testing

Time spent: **15** hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pen Testing Report

### 1. User Enumeration

- [ ] Summary: When a user comments and their comment is accepted by an admin, it allows them to bypass further approvals and allows them to comment without further needing additional approvals on any page/post
  - Vulnerability types: User Enumeration
  - Tested in version: WordPress 6.0.2
  - Fixed in version: 
- [ ] GIF Walkthrough: <img src="https://github.com/ShivaniNanan/Wordpress-Pen-Testing/blob/main/userenumeration.gif" alt="My Project GIF">
- [ ] Steps to recreate: 
    1. Comment on a post using a non admin profile
    2. Admin approve the comment
    3. User without admin profile comments again and does not need further approvals from admin
- [ ] Affected source code:
  - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
  
### 2. Stored XSS

- [ ] Summary: When an admin or another approved user creates a post, and javascript is inserted, it is executed.
  - Vulnerability types: Stored XSS
  - Tested in version: WordPress 6.0.2
  - Fixed in version:
- [ ] GIF Walkthrough: <img src= "https://github.com/ShivaniNanan/Wordpress-Pen-Testing/blob/main/xss1.gif" alt="SecondTest GIF">
- [ ] Steps to recreate: 
    1. As an admin, create a new post
    2. Create a custom html in the block
    3. Write the appropriate script
    4. Select Preview and payload will execute
- [ ] Affected source code:
  - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)

### 3. Stored Cross Site Scripting (XSS)

- [ ] Summary: When an admin creates a post and a alertscript is entered it is executed.
  - Vulnerability types:
  - Tested in version: WordPress 6.0.2
  - Fixed in version: 
- [ ] GIF Walkthrough: <img src= "https://github.com/ShivaniNanan/Wordpress-Pen-Testing/blob/main/xsscrosssite.gif" alt="ThirdTest GIF">
- [ ] Steps to recreate: 
    1. As an admin, create a post
    2. Add an alert script to a URL using "onload" 
    3. Preview the post
- [ ] Affected source code:
  - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)



## Assets

List any additional assets, such as scripts or files

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with  ...
[ScreenToGif](https://www.screentogif.com/) for Windows


## Notes

Describe any challenges encountered while doing the work

## License

    Copyright [yyyy] [name of copyright owner]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
