---
layout: post
title:  "git branch"
date:   2016-04-09
categories: git
permalink: /category/git/branch
url: /category/git/branch
---

CCreate and switch to a new branch

~~~shell 
ggit checkout -b newbranch
~~~

equals to

~~~shell
git branch <newbranch>
git checkout <newbranch>
~~~

Push local branch to remote, if remote branch does not exist, create it.

~~~shell
git push origin <localbranch>:<remotebranch>
~~~

List all branches/remote branches

~~~shell
git branch -a
git branch -r
~~~

Show remote branches and also trach information. 

~~~shell
git remote show origin
~~~

Remove a local branch which does not exist in remote

~~~shell
git fetch -p
~~~

How to rename a remote branch  
1. Delete a remote branch  
2. Rename local branch  
3. Push local branch to remote  

~~~shell
git push --delete origin <branchname>
git branch -m <original branch name> <new branch name>
git push origin origin <new branch name>
~~~

build up the track information between local branch and remote

~~~shell
git branch --set-upstream-to <localbranch> <origin/remotebranch>
~~~

