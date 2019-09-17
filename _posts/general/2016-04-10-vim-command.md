---
layout: post
author: "Joe"
title:  "vim"
date:   2016-04-10
url: /category/vim
tags: 
  - vim
---

A few vim commands

```shell

ys : add surround for selections. like ysiw' will add single quot to one word. yss" will add double quot to one whole line. 
cs : change surronds for selections. like cs"' will change double quots to single quot for one word
ds : remove surronds for selections. like ds' will remove single quot 

gU/u : change case for selections. gUU upper case the whole line

$ ctrl+f scroll one screen down
$ ctrl+b scroll one screen back

$ :%s/oldkeyword/newkeyword/g replace all old keywords to new keywords
$ :s/oldkeyword/newkeyword/g replace all old keywords to new keywords in current line

```