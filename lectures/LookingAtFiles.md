Looking at files
=================

Some more command-line juju working with files. These commands will help you deal with other stuff we work on later.

Let's get something to work with. We'll go to our home directory, make a directory to work in, then move into it. (This is review from [Moving Around](MovingAround.md)).

```
$ cd ~
$ mkdir myproject
$ cd myproject
```

We need some text to work with, so we're going to pull down some text from Github. I might as well explain what we are doing.

## curl

[curl](http://man.cx/curl) is a command to transfer files. I think of it as "Capture URL". We need to give `curl` a couple of flags (or options) for this job:

* **-L** stands for "Location". It allows `curl` to follow a URL if it is redirected.
* **-o** for "output". So we can write this to a file instead of our terminal window. We need to follow it with the file name we want. (We could use **-O** to just use the current file name.)

`$ curl -L -o data.csv https://raw.githubusercontent.com/utdata/cli-tools/master/data/example.csv`

OK, now we should be able to `ls` and see our file is there. My output looks like this:

```
christian:mydata$ ls
data.csv
```

## head

[head](http://man.cx/head) allows you to print the top of a file to your screen so you can see what it is. It will default to show you the first 10 lines of a file. When you type this in, hit tab after you type "head da" to let tab completion help you.

`$ head data.csv`

will give you this:

```
christian:mydata$ head data.csv
Month,Taxpayer Number,Taxpayer Name,Taxpayer Address,Taxpayer City,Taxpayer State,Taxpayer Zip Code,Taxpayer County,Outlet Number,Location Name,Location Address,Location City,Location State,Location Zip Code,Location County,Location Room Capacity,Location Tot Room Receipts,Location Taxable Receipts
January,32016602719,BHAKTA DAYARAM,2627 MANOR RD,AUSTIN,TX,78722,227,00001,ACE MOTEL,2627 MANOR RD,AUSTIN,TX,78722,227,27,9165.0,8580.0
January,32016658448,SIDNEY CORINNE LOCK,4300 AVENUE G,AUSTIN,TX,78751,227,00005,ADAMS HOUSE BED & BREAKFAST,4300 AVENUE G,AUSTIN,TX,78751,227,3,14903.0,13544.0
January,32043492993,AMANDA K CRIBBS,4202 FLAGSTAFF DR,AUSTIN,TX,78759,227,00007,ALLANDALE RENTALS,1107A BRENTWOOD ST,AUSTIN,TX,78757,227,2,250.0,250.0
January,32043492993,AMANDA K CRIBBS,4202 FLAGSTAFF DR,AUSTIN,TX,78759,227,00009,ALLANDALE RENTALS,11900 ALOE VERA TRL,AUSTIN,TX,78750,246,8,2728.0,2728.0
January,32043492993,AMANDA K CRIBBS,4202 FLAGSTAFF DR,AUSTIN,TX,78759,227,00010,ALLANDALE RENTALS DUPLEX,2200 LANIER DR # B,AUSTIN,TX,78757,227,1,0.0,0.0
January,32043492993,AMANDA K CRIBBS,4202 FLAGSTAFF DR,AUSTIN,TX,78759,227,00008,ALLANDALE RENTALS/DUPLEX,2200 LANIER DR # A,AUSTIN,TX,78757,227,4,773.0,773.0
January,32043492993,AMANDA K CRIBBS,4202 FLAGSTAFF DR,AUSTIN,TX,78759,227,00004,ALLENDALE RENTALS,2105 LANIER DR,AUSTIN,TX,78757,227,1,2369.0,2369.0
January,32043492993,AMANDA K CRIBBS,4202 FLAGSTAFF DR,AUSTIN,TX,78759,227,00006,ALLENDALE RENTALS,5010 PLACID PL,AUSTIN,TX,78731,227,1,4038.0,0.0
January,32024286760,"ALTEMATE REAL ESTATE, LLC",2307B RIVERSIDE FARMS RD,AUSTIN,TX,78741,227,00008,ALTEMATE REAL ESTATE LLC,76 SAN MARCOS ST,AUSTIN,TX,78702,227,1,1125.0,1125.0
```

It might look like more than 10 lines on your screen because they wrap.

If you want to say how many lines, use the flag **-n** for number of lines:

`$ head -n 2 data.csv`

That will give you two lines, the first which is the header of that file.

## tail

[tail](http://man.cx/tail) shows you the bottom of the file. It takes the same **-n** flags

## cat

[cat](http://man.cx/cat) means to concatenate and print a file to your window. If you feed it two file names, it will give you the first, then the other. Do this:

`$ cat data.csv`

This will print the contents of `data.csv` to your screen. There so much of it you can even see it all.

But what you can do is redirect that output into a file by using `>`.

If I wanted to take two files, `file01.txt` and `file02.txt`, and then combine them into a single file on your computer, it would look like this. (Don't do this as we don't have the files, but ...):

`$ cat file01.txt file02.txt > combined.txt`

Now, `combined.txt` would be the combination of both files.

## wc

[wc](http://man.cx/wc) I think of as "word count", but it can also count lines and bytes.

`$ wc data.csv`

gives you this output:

```
christian:mydata$ wc data.csv
    6692   88224 1162130 data.csv
```

The first column is lines, then words, then bytes.

If you want just the number of lines, us **-l**.

`$ wc -l data.csv`

## grep

[grep](http://man.cx/grep) is for using regular expressions to find parts of a file. It takes a regular expression input and the file name and give in return the lines of the file that match that regular expression.

`$ grep 'JW MARRIOT' data.csv`

... will print out just the lines in `data.csv` that have 'JW MARRIOT' somewhere in them.

If you want to just know how many lines there are with 'JW MARRIOT', use the **-c** flag for count:

`$ grep -c  'JW MARRIOT' data.csv`

The answer should be 11.

## piping commands

You can "pipe" command together with the `|` character, which you'll find as the shift of your backslash key. You can string commands together with that, so if I just wanted to see the first two lines of those that have 'JW MARRIOT' in them, I can do this:

`$ grep 'JW MARRIOT' data.csv | head`

----

Next: [Intro to Anaconda](IntroToAnaconda.md)
