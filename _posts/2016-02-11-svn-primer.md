---
layout: post
title: SVN Primer
---

st - svn status - looks up current directory and sub-directories for changed files/new files

1. svn add file_path - only for new files
2. svn st - status changes
3. svn commit file_path -m "message about the change" -  files separated by a space or directories
4. Difference of working copy (HEAD) and revision # 25719 (Revision # can be obtained from svn log | less) 
svn diff footer.comp -r 25719:HEAD 
check log changes
svn log | less 
show modified files
svn log -v | less
less - goes by line
more - goes by page
5. revert file
svn cat filepath -r28963 > filepath
6. Review code
svn diff | vim - -R 
or better add it to .bashrc: alias sd='svn diff | vim - -R
