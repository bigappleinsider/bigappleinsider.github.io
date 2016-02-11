---
layout: post
title: git log - show commit history
---
SHA hash and commit message
`git log --pretty=oneline`


912a2d1 Sun Sep 29 20:53:09 2013 -0400 - initial commit, var and media
folders excluded [Vlad V]
`git log --pretty=format:"%h %ad - %s [%an]"`

Show lines that were changed
`git log --oneline -p`

Add to .bashrc
`alias gitlog='git log --pretty=format:"%h %ad - %s [%an]"'
alias gitlogp='git log --pretty=format:"%h %ad - %s [%an]" -p'`
