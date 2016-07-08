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

It listed the names of all the folders and files of the directory I'm in. But sometimes, I want to know more information about the files, like their modification date.
