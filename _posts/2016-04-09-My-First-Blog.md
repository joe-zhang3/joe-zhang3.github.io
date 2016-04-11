---
layout: post
title:  "Branch"
date:   2016-04-09
categories: git
permalink: /archivers/git
---

# Branch

Create and switch to a new branch

~~~shell 
git checkout -b newbranch
~~~

Push local branch to remote, if remote branch does not exist, create it.

~~~shell
git push origin local_branch:remote_branch
~~~

List all branches/remote branches
~~~shell
git branch -a
git branch -r
~~~

