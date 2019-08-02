---
layout: post
title:  "git general"
date:   2016-04-11
categories: git
url: /category/git/general
---

Add all files in current folder & subfolder

~~~shell
git add -A `is equivalent to git add --all`
git add -u `is equivalent to git add --update`
~~~

Revert all changes in working copy
**Make sure execute the command under the root of the git repo**

~~~shell
git checkout .
git checkout -- .
~~~

Revert all changes in stage

~~~shell
git reset # put the staged changes back to working copy
git reset --hard HEAD # completely revert all changes, the change will not stay in your working copy either. 
~~~

Rename of a file(s)

~~~shell
git mv originalname newname
~~~

Fully clean your working copy & index 

~~~shell
git fetch origin && git reset --hard <branchname> && git clean -df
~~~

Revert one commit on both local & remote

~~~shell
git revert [sha] && git push origin
~~~