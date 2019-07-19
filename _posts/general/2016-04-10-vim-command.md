---
layout: post
author: "Joe"
title:  "vim"
date:   2016-04-10
categories: vim
permalink: /category/vim
url: /category/vim
tags: 
  - vim
---

A few vim commands

~~~shell
$ :number # go to specified line

$ w # move one word forward
$ b # move one word backward
$ $ # move the cursor to the end of current line
$ 0 # move the cursor to the first of current line
$ gg # move the cursor to the beginning of the file
$ G # move the cursor to the end of the file

$ u # undo 
$ U # undo all changes to the current line

$ x # delete one character
$ dw # delete one `word`
$ d$ # delete all content after the cursor till the end of the line
$ dd # delete the whole line

$ yy # copy the whole line
$ yw # copy the content start from the cursor till the end of the current **word**
$ y$ # copy the content start from the cursor till the end of the current **line**

$ p # paste

$ :e! # discard the change and reload the file to edit
$ :wq # save and exit 
$ ZZ # save and exit
$ :q! # discard and exit


$ ctrl+f scroll one screen down
$ ctrl+b scroll one screen back

$ :%s/oldkeyword/newkeyword/g replace all old keywords to new keywords
$ :s/oldkeyword/newkeyword/g replace all old keywords to new keywords in current line

~~~