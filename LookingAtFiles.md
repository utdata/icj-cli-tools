Looking at files
=================

Some more command-line juju working with files. These commands will help you deal with other stuff we work on later.

## Let's get something to work with. We'll go to our home directory, make a directory to work in, then move into it. (This is review from [Moving Around](MovingAround.md)).

```
$ cd ~
$ mkdir myproject
$ cd myproject
```

We need some text to work with, so we're going to pull down some text from Github. I might as well explain what we are doing.

## curl

[curl](http://man.cx/curl) is a command to transfer files. I think of it as "Capture URL". We need to give `curl` a couple of arguments for this job:

* **-L** stands for "Location". It allows `curl` to follow a URL if it is redirected.
* **-o** for "output". So we can write this to a file instead of our terminal window. We need to follow it with the file name we want. (We could use **-O** to just use the current file name.)

`$ curl -L -o data.csv https://github.com/utdata/cli-tools/blob/master/csvkit/hotels/data-done/austin-hotels.csv?raw=true`

OK, now we should be able to `ls` and see our file is there.

```
christian:mydata$ ls
data.csv
```
