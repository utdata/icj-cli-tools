Mixed Beverage Tax Receipts
===========================

By Christian McDonald
[christian.mcdonald@utexas.edu]

## Downloading files

Recent files are held by the State Comptroller and available on [TexasTransparency.org](http://www.texastransparency.org/Data_Center/Search_Datasets.php) portal. You can search and download files there, along with the [record layout](MIXEDBEVTAX_LYOT.txt). That said, there was a previous system for these files outlined below, and the [old record layout](OLD-MIXEDBEVTAX-LAYOUT.txt) was much more detailed and useful.

These files *seem* to be consistently named, so you could download them programatically.

`curl -L -O http://www.texastransparency.org/Data_Center/files/MIXEDBEV_03_2016.CSV`

Where those last numbers are the month and year.

(Some day I'll write a Python script to automate the download?)

## Old archive page

Before March 2016, these files were published on a different web page, and while the page is no longer available, the data files are, as least as of July 2016. Unfortunately for this data set, the file naming convention was not consistent, so you can't just `curl` the files programatically.

But you can try going to [archive.org](https://web.archive.org) and searching for this url: http://www.window.state.tx.us/taxinfo/taxfiles.html

Those result would often look something like:

* [bev02-23.csv](http://www.window.state.tx.us/filelib/bev02-23.csv) 2.3MB - (Released 02-23-15)
* [bev01-21.csv](http://www.window.state.tx.us/filelib/bev01-21.csv) 2.2MB - (Released 01-21-15)
* [bev12-23.csv](http://www.window.state.tx.us/filelib/bev12-23.csv) 2.4MB - (Released 12-23-14)

I suspect that files that were released on the same date of a previous year were overwritten.
