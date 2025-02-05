---
title: 'git Configuration'
date: 2025-02-04T10:00:00+07:00
draft: false
description: 'Setup git for development & testing'
menus:
  toolchain:
---
Setup git for development & testing

Set the default branch to main instead of master:  

    git config --global init.defaultBranch main

<!--more-->
Set global name and email:  

    git config \--global user.name "Your Name"  
    git config \--global user.email "you@your-domain.com"

Improved git log:  

    git config --global alias.lg "log --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an\>%Creset' --abbrev-commit"

Now use:  

    git lg

