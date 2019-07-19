---
layout: post
title:  "git delete"
date:   2016-04-09
categories: git
permalink: /category/git/delete
url: /category/git/delete
---

Add all files in current folder & subfolder

~~~shell
git rm <filename>
~~~

Delete a local branch 

~~~shell
git branch -d <branchname>
~~~

Delete a remote branch

~~~shell
git push origin :<branchname>
git push origin --delete <branchName>
~~~

Delete a remote tag

~~~shell
git push originl --delete tag <tagname>
~~~