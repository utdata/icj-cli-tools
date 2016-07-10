Hotel Occupancy Tax Receipts
============================

By Christian McDonald
[christian.mcdonald@utexas.edu]

Hotel Occupancy Tax data is available on the Texas Comptroller's [TexasTransparency.org](http://www.texastransparency.org/Data_Center/Search_Datasets.php) portal. You can search for and download the data and [record layout](HOTELTAX_LYOT.TXT) there. (That record layout is less detailed than an [older record](old-hoteltax-layout.txt) layout on the previous portal described below.)

The file names on TexasTransparency are not consistent, at least not in the beginning. They generally follow this format:

http://www.texastransparency.org/Data_Center/files/HOTEL_01_2016.csv

But sometimes the `.csv` is `.CSV`. Some files are just missing or blank.

(This repo has a full record of 2015 data, culled from TexasTransparency and old file locations noted below.)

According to the portal:

> The information contained in this file is hotel occupancy tax data reported by taxpayers under Chapter 156 of the Texas Tax Code. The files include master and outlet addresses and receipts by reporting period. The monthly file includes only taxpayers that are monthly filers.

The data is released monthly, but the Statesman has learned that monthly data does not always include all records, and that Quarterly data files are more reliable. However, the Comptroller has yet to upload Quarterly data to TexasTransparency as of July 2016, but it can be requested.

E-mail: open.records@cpa.state.tx.us
Phone: 1-800-531-5441, ext. 6-6013 (936-6013 in Austin)

## Old archive page

Before March 2016, these files were published on a different web page, and while the page is no longer available, the data files are, as least as of July 2016. The naming convention is consistent and files can be downloaded programatically.

If you want to find the old page, you can try going to [archive.org](http://web.archive.org) and searching for this page: http://comptroller.texas.gov/taxinfo/taxfiles.html

Quarterly data is formatted like this:

`http://comptroller.texas.gov/filelib/hotl14q3.csv`

Where the file name is `hotl` follwed by the year `YY`, then `q` and the number of the quarter, 1-4.

Monthly data is formatted like this:

`http://comptroller.texas.gov/filelib/hotl1501.csv`

Where the file name is `hotl` followed by `YYMM`.

Because these URLs are well formatted, you can download a series of these files using [curl](http://man.cx/curl):

`curl -L -O http://comptroller.texas.gov/filelib/hotl15[01-12].csv`

This will get you all the files for the year 2015.

Monthly data looks to be updated to February 2016, but I'm unsure if files will continue to be uploaded there now that the Comptroller has moved to TexasTransparency.


http://comptroller.texas.gov/filelib/hotl15q1.csv
