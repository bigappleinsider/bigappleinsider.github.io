---
layout: post
title: Vim Tip Of the Day
---

    Undo Change, Redo Change
    u, Control + r

    Page Down, Page Up
    Control + f, Control + b

    Jump to End of File
    nG

    Split screen/open another file
    :vs  - split screen      :e  - open another file      
    
    Ctrl + ww  - move from one screen to another
    :sp - horizontal split

    :tabe - open in a new tab     gt - move from one tab to another

    Run shell command in vi
    :sh - show command line   Control + D - go back to vi
    control-z - will suspend the process and get back to your     shell
    fg - will resume suspended vim
    ps - list foreground processes

    Tab selected text, Repeat last command
    Shift + >, .

    Jump to End of a curly brace
    Shift + %

    Visual select, Copy selection, Copy current line
    v, gyy, yy

    Paste text
    p

    Move to the begining of the line and insert mode
    I

    Move to the end of the line and insert mode
    A

    Search and Replace
    Find word under cursor
    forward: Shift + 8 (*), back: Shift + 3 (#)

    First occurrence on current line, Globally (all) on current line
    :s/OLD/NEW, :s/OLD/NEW/g

    Forwad, Back
    n, N

    Between two lines #,#:                 
    :#,#s/OLD/NEW/g

    Every occurrence in file:
    :%s/OLD/NEW/g
    :%s/foo/bar/gc Change each 'foo' to 'bar', but ask for confirmation first.

    :%s/foo/bar/gci Change each 'foo' (case insensitive) to 'bar'; ask for confirmation.

    The g flag means global – each occurrence in the line is changed

    Turn off escape chars
    %sno/regex/new_text/g or \V

    Cut text
    cw - word
    ci" - delete inside quote
    ci}
    cit - inside tag

    marks

    m and any of the caps letters
    mQ
    mW
    mE

    jump to mark
    'Q
    'W
    'E
