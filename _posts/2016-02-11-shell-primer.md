---
layout: post
title: Shell Primer
---
    Ctrl + C - keyboard interrupt
    Ctrl + D - disconnect, close shell

    jobs - list of process


    Tougle between vi and shell
    Ctrl + Z - suspends 
    bg - continue process
    fg - get back into the

    :sh
    Ctrl +D

      sudo apt-get install gt5
      disk usage
     find / -size +10M -ls

    free - free memory
    uptime

    du -h media/ - size of a folder

    find . -name ".htaccess" -print

    grep -sr 'text' .


    Grep a file, show several surrounding lines:
    -B num to set how many lines before the match
    -A num for the number of lines after the match
    grep -B 3 -A 2 foo README.txt

    Grep by file type
    grep -r -i --include \*.h

    scp helloworld.zip user@vivawebsolutions.com:/home/content/07/5607462/html/

    strip 3 leading directories
    tar -xvf ../dev-store.tar --strip-components=3


    ls -l    list files
    h - compresses kilobytes

    touch filename      creates empty file if not exists, updates last modified date

    ls -lh
    total 16K
    -rw-rw-r-- 1 vlad vlad  762 Sep 17 16:40 hour0.txt

    chmod 777 filename      changing permissions
    each digit corresponds to user, group, other
    r-w-x each has a bit, summup to get a permission #
    1-1-1 => 7 (permission to read, write, and execute)
    1-1-0 => 6 (permission to read and write)
    1-0-0 => 4 (permission to read)

    chmod u=rw,g=r,o=r filename
    chmod 644 filename

    id      list groups that user is part of

    history | grep ssh      view shell history

    !757    run command from history #757

    !757:p  view command from history #757

    !!      run last command
