Moving around in Bash
=====================

## print working directory

One of the hardest things to get a handle on with working in the terminal is to figure out where you are on your computer. It's important, because you can run commands on any file on your computer from where you are, but you gotta know where that is before you can do so. So, do this:

`$ pwd`

That should tell you where you are in your computer's file system. When I launch a new shell and type that in, I get this:

`/Users/christian`

That tells me I'm in my own user directory. I bet you are in yours, but do it and see.

## list directory

Do this:

`$ ls`

This will list everything in the directory you are in. Mine looks like this:

``` Bash
christian:~$ ls
Applications			Music
Applications (Parallels)	Pictures
Audio				Public
Box Sync			VirtualBox VMs
Desktop				dumps
Documents			gsutil
Downloads			pspp.jnl
Dropbox				trifacta
Library				waller.csv.sav
Movies
```

It listed the names of all the folders and files of the directory I'm in. But sometimes, I want to know more information about the files, like their modification date. To do this, we introduce something called **flags**, which you can think of as adding nuance or detail to a command. They start with a dash, and you can pile them on, as I'll demonstrate. First, try this:

`$ ls -l`

My output looks like this:

``` Bash
christian:~$ ls -l
total 15880
drwxr-xr-x   7 christian  staff      238 Jul 22  2015 Applications
drwxr-xr-x@  6 christian  staff      204 Feb 14  2014 Applications (Parallels)
drwxr-xr-x   5 christian  staff      170 Jun 12 14:53 Audio
drwx------  22 christian  staff      748 Jul  4 10:17 Box Sync
drwx------+ 24 christian  staff      816 Jul  7 19:01 Desktop
drwx------+ 27 christian  staff      918 Jul  5 14:53 Documents
drwx------+ 10 christian  staff      340 Jul  5 15:29 Downloads
drwx------@ 38 christian  staff     1292 Jul  5 23:17 Dropbox
drwx------@ 63 christian  staff     2142 Dec 10  2015 Library
drwx------+  9 christian  staff      306 Jul  1 15:07 Movies
drwx------+ 10 christian  staff      340 Jul  1 15:07 Music
drwx------+ 31 christian  staff     1054 Jul  1 15:07 Pictures
drwxr-xr-x+  4 christian  staff      136 Mar  4  2013 Public
drwx------   8 christian  staff      272 Jul  8 09:48 VirtualBox VMs
drwx------   4 christian  staff      136 Mar 26  2014 dumps
drwxr-xr-x  14 christian  staff      476 Oct  1  2015 gsutil
-rw-r--r--   1 christian  staff    78626 Aug 13  2015 pspp.jnl
drwxr-xr-x   5 christian  staff      170 Jul  4 20:24 trifacta
-rw-r--r--   1 christian  staff  8046293 Aug 13  2015 waller.csv.sav
```
