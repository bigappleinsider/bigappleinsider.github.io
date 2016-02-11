---
layout: post
title: Renaming a Branch in Git
---
First, you want to change your local branch. This couldn't be easier:

`git branch -m my-hot-feature feature-15`

Delete the remote branch with the old name:
`git push origin :my-hot-feature`

Re-create the remote branch with the new name:
`git push origin feature-15`
