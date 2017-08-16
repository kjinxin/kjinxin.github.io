---
layout: post
title: Git
comments: true
categories: Tools
---
## git config: set user name and email address...

git config --global user.name "Xin Jin"
git config --global user.email "xinjin@gmail.com"

git config --list ::: list all the settings.

## git frequently used operations

git rebase --whitespace=fix HEAD~1
git rebase -i HEAD~4
git reset --soft HEAD~1
git checkout -b master4
git branch --set-upstream master4 remotes/origin/master
