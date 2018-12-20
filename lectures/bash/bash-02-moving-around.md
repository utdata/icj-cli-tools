# Moving around in Bash

Of note: I use the terms "folder" and "directory" interchangeably here. The are the same thing.

## Goal

Our goal here is to become familiar with Terminal and the Bash commands to move around and access different folders on your computer.

We'll also create our class folder, which you will use for the rest of the semester.

## Home directory

I want to make sure we are all starting from the same relative location, so blindly follow me by typing the following into your terminal. (If you see a command like this that starts with `$`, don't type that in. It's just a note that it is a terminal command).

`$ cd ~`

That tilde is usually at the top left of your keyboard.

You used your first Bash command, `cd`, which is "change directory". The `~` is a shortcut that takes you to the "home" directory of the logged in user. You can always use `cd ~` to get you back to home.

## pwd

One of the hardest things to get a handle on when first working in the terminal is to figure out where you are on your computer. It's important, because you can run commands on any file on your computer from where you are, but you gotta know where that is before you can do so. So, we'll use [pwd](https://man.cx/pwd), or "print working directory" to do this:

`$ pwd`

That should tell you where you are in your computer's file system. When I launch a new shell and type that in, I get this:

`/Users/christian`

That tells me I'm in my own user directory. I bet you are in yours, but do it and see. So, remember, `~` is a shortcut to take you to this longer directory path.

## List directory

Do this:

`$ ls`

This will list everything in the directory you are in. Mine looks like this:

``` bash
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

It listed the names of all the folders and files of the directory I'm in.

### Flags

But sometimes, I want to know more information about the files, like their modification date. To do this, we introduce something called **flags**, which add nuance or detail to a command. They start with a dash, and you can pile them on, as I'll demonstrate. First, try this:

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

Well, that's a lot of info, and much of it jibberish. Let's break it down:

* `drwxr-xr-x` and similar is the permission information for a that file or folder. We aren't going to get into it here, but [you can read more](https://en.wikipedia.org/wiki/File_system_permissions#Notation_of_traditional_Unix_permissions) if you like.
* The next number is the number of files inside the folder, sort of. If this is a file, the number will be "1". If it is a folder, the number will always be at least "2". We'll come back to this.
* Next is the owner of the file or folder.
* Next is a permission level for the user when the file was created.
* Next is the file size in bytes.
* Next is the last modified date of the file or when a file was added to the folder.
* File or folder name.

### Hidden files

Let's add another flag to your command:

`$ ls -al`

My list got a TON longer:

```
christian:~$ ls -al
total 16144
drwxr-xr-x+  71 christian  staff     2414 Jul  8 17:16 .
drwxr-xr-x    5 root       admin      170 Feb 19 06:56 ..
-r--------    1 christian  staff        7 Nov  2  2014 .CFUserTextEncoding
-rw-r--r--@   1 christian  staff    30724 Jul  7 19:00 .DS_Store
drwxr-xr-x    3 christian  staff      102 Jul  9  2014 .R
drwxr-xr-x    3 christian  staff      102 Mar  5  2013 .RSA
-rw-r--r--    1 christian  staff      331 Jul 12  2014 .Rapp.history
-rw-r--r--    1 christian  staff      149 Jul 16  2015 .Rhistory
drwx------  160 christian  staff     5440 Jul  7 18:59 .Trash
drwxr-xr-x   14 christian  staff      476 Jan 17 11:46 .atom
-rw-------    1 christian  staff     7589 Jul  8 17:00 .bash_history
-rw-r--r--    1 christian  staff     1130 Oct  1  2015 .bash_profile
drwxr-xr-x   15 christian  staff      510 Jul  7 19:06 .bash_sessions
-rw-r--r--    1 christian  staff      216 Jul  7 19:15 .bashrc
-rw-------    1 christian  staff    15745 Oct  1  2015 .boto
<snip>
drwx------    4 christian  staff      136 Mar 26  2014 dumps
drwxr-xr-x   14 christian  staff      476 Oct  1  2015 gsutil
-rw-r--r--    1 christian  staff    78626 Aug 13  2015 pspp.jnl
drwxr-xr-x    3 christian  staff      102 Jul  8 17:20 test
drwxr-xr-x    5 christian  staff      170 Jul  4 20:24 trifacta
-rw-r--r--    1 christian  staff  8046293 Aug 13  2015 waller.csv.sav

```

The `-a` flag means "all" files and folders, including hidden ones. When you normally open a folder on your computer, it only shows you some of the files and folders available. Hidden folders and files start with a period, and there can be a lot of them ... I have 50 of them in my home folder, far more than regular files and folders.

Let's look at the first two listed here:

```
christian:~$ ls -al
total 16144
drwxr-xr-x+  71 christian  staff     2414 Jul  8 17:16 .
drwxr-xr-x    5 root       admin      170 Feb 19 06:56 ..
```

These are two special designations in the Unix world. A single period designates "this directory" and two periods designates the "parent directory". Every directory has these, so that's why the `ls -l` always shows two items inside a directory, even if it is "empty" of regular files or folders.

We can use these period designations (there's probably a fancy word for them I don't know) to move around into different directories, and to manage files in our current directories.

Let's see this "dot" designation in action. Do this command:

`$ open .`

Since you are in your home directory, this should open that folder in your Finder.

## cd

Both Macs and PCs have a `Documents` folder inside each user's home folder. It's typically where you save all your stuff (better than your Desktop!). It's time for us to move in our Terminal to inside this Documents folder.

The [cd](https://man.cx/cd) command is **change directory**. Let's change directory into your `Documents`:

`$ cd Documents`

Macs are particular that you capitalize a folder like `Documents`. We shouldn't rename this folder, so we'll just deal with it and type the capital D.

Let's do a review real quick. Where are you? What is your "working directory?"

`$ pwd`

What is in this current directory? It could be something like this:

`/Users/ccm346/Documents`

It should end with Documents. If it doesn't, PLEASE RAISE YOUR HAND.


## mkdir

Now, let's make a new empty folder inside this directory, using the [mkdir](https://man.cx/mkdir) command:

`$ mkdir icj`

Then list your directory again to see the new directory:

`$ ls`

You should see your new `icj` directory there along with all your other stuff inside Documents. Creating a directory like this is exactly the same as opening a desktop window on your Mac and doing Command-N to create a new folder. Folders and directories are the same thing.

Cool, let's make another directory inside of `icj`.

`$ mkdir icj/newdirectory`

Now you can do an `ls` on icj to see what is inside it.

`$ ls icj`

It should show you `newdirectory`. Something like this:

``` bash
christian:~$ ls icj
newdirectory
```

A couple of things about this:

* You have listed the contents of the `icj` directory without being inside of it. You can list the contents of any folder on your computer if you know the path to it. In fact, you can do any command on a file or folder if you know its path.
* If you try to name a directory with a **space** in it, you'll not get what you want unless you put quotes around it. Because of this, I avoid using spaces in files and folders. I try to avoid capitalization, too, because sometimes it matters.

Now, let's go inside the `icj` folder:

`$ cd icj`

Let's see what is inside:

`$ ls`

That should show you a result with the `mydirectory` that we created earlier.

Here are the commands and results of these last few commands in my terminal. I started with a `pwd` so you can see where I started from:

```
christian:~$ pwd
/Users/christian
christian:~$ cd icj
christian:testy$ ls
newdirectory
christian:testy$ pwd
/Users/christian/icj
```

So to break that down:

* I printed my working directory, which showed me I was in my Users folder.
* I did `cd` into `icj` which moved me to inside that directory.
* Now that I'm inside `icj`, I did `ls` to see the contents of my current folder, and it showed me that `newdirectory` was indeed inside.
* I did `pwd` to show that my current working directory (where I am) is inside the `icj` folder.

 Now let's get crazy:

`$ ls ../`

Remember I said that two periods means the parent directory? This should show you the list of files and folders in your Documents directory. Now, confirm where you are:

`$ pwd`

Which should still be `icj`. So you had listed the files for the folder "above" you.

## tab completion

If you are doing `ls` or `cd` or otherwise referencing a path in the terminal, you don't have to type the whole word for each directory. If you you are trying to list the contents of "newdirectory", then start with `ls newd` and then hit tab, and it will finish out the path as `ls newdirectory`. This is SUPER handy and you should use it often. Like all the time.

## On the right path

### Relative paths

You can `ls` files or `cd` into any directory relative to your current working directory using `../` to move "up" the folder structure and then use the name of the directory to move inside it. So a path like this: `ls ../../Users/Cory` is to travel up two folders, then into `Users` then into `Cory` and then list all the files there.

This is very powerful in programming, because you might be writing and testing code on your own computer, but then run the program on another computer, so if `file01.py` needs to talk to `file02.py`, you don't want to hard-code a path like `http://utdata.cmcdonald.com/scripts/file02.py`, because you might not always be on utdata.cmcdonald.com. If it's in the same folder, you could use `file02.py` or `./file02.py`.

### Root-relative paths

You can reference the "root" or the top level of whatever server or machine you are on even if you don't know the name of it, by starting your path with a slash like this: `/scripts/file01.py`. That's called a **root-relative** path. If you know the root-relative path to a file or folder, you can always find it no matter what directory you are currently in.

### Absolute paths

An absolute path includes the domain or computer name. If I reference `http://utdata.cmcdonald.com/scripts/file01.py` in my code or script, it will only work if I'm on `utdata.cmcdonald.com`. If I move that script to another computer or server, it will still try to pull from `utdata.cmcdonald.com` instead of the version on the new computer.


### Getting to your icj folder

There will be many times in the class that you will want to get into your `icj` folder, or something inside of it. Because everyone in class created this folder in the same place relative to their home folder, we can use a special command to get there, no matter where we are starting. And because of tab completion, as you are typing this, when you type Documents you only need `Docu` then hit tab and it will complete the rest of the word.

`$ cd ~/Documents/icj`

And if you knew you wanted to get inside a folder there, say called `my-project`, it would be:

`$ cd ~/Documents/icj/my-project`

---

Next: [Looking at files](bash-03-viewing-files.md)
