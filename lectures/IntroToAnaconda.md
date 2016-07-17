Introduction to Anaconda
===================

We want to use some Python tools to do data processing and data analysis. When using Python, it is a good idea to cordon off your work area in something called a **virtual environment**, which creates a walled garden of Python wonderfulness, keeping the parts we need together and away from other projects or parts of your computer. This is especially important for Macs, as they use Python as part of the operating system, and we don't wanna mess that up.

There is a software package called **conda** makes creating these environments and loading packages pretty easy. If you are new to programming, I probably lost you, and that's OK. Let's just do it.

## Anaconda or Miniconda?

While **conda** is the package manager software, the folks who make it bundle conda with Python in a couple of ways:

The full **[Anaconda](https://www.continuum.io/downloads)** includes a Python distribution, the conda package manager, Jupyter notebooks and a suite of the most popular data science packages. It's pretty big, like 1.8G, so it needs space and takes a couple of minutes to download and install.

If you are worried about disc space, you can use **[Miniconda](http://conda.pydata.org/miniconda.html)**, which is a smaller version with just Python and conda, and you can install just the packages you need.

You can start with either. I use Anaconda on my Mac, and Miniconda on my Windows partition.

## Which version of Python?

We'll be using Python 3.5 in our class, so you might as well download that version of the installer so it will use 3.5 by default. If it ends up mattering to you later, you can build environments in either version of the language.

## Download and install

* [Anaconda](https://www.continuum.io/downloads). For my Macbook Air, I used the Python 3.5 64-bit graphical installer. You don't have to sign up for Anaconda Cloud at this time.
* [Miniconda](http://conda.pydata.org/miniconda.html). I used the Miniconda version because I already have full Anaconda on the Mac side of my machine. Use the default to set your PATH variable.

## Update conda

Once you have installed everything, go to your Terminal and close all the windows and then launch a new one. Shells don't understand that new updates happened if they are already open.

Let's make sure it is installed properly. Do:

`$ conda list`

And you should see a string of names fly by. If not, let me know. Let's update conda, as new stuff is released all the time.

`$ conda update conda`

If it asks you if you want to proceed to install, answer yes with `y`.

## Create an environment

We're going to create a new conda environment. Do this:

`$ conda create --name data python=3 csvkit pandas jupyter`

Let's break this command down word by word:

* `conda` is the program we are using
* `create` is the command we are giving `conda`. The command creates a new environment.
* `--name` is saying we want to give our environment a name, so we can refer to it later.
* `data` is the name we are giving our environment.
* `python=3` we are specifying Python 3. If you installed Anaconda3, it would give you 3 by default, but we are being careful and specifying it.
* `csvkit` is a Python package we want included in our environment. We list it and all those we wish to install here (`pandas` and `jupyter`) because these packages sometimes have dependencies (as you'll see).

When you ran the command, you get something like this. (It will differ if you are running Miniconda.):

```
The following packages will be downloaded:

    package                    |            build
    ---------------------------|-----------------
    csvkit-0.9.1               |           py35_1          63 KB

The following NEW packages will be INSTALLED:

appnope:           0.1.0-py35_0
backports:         1.0-py35_0
csvkit:            0.9.1-py35_1
decorator:         4.0.10-py35_0
entrypoints:       0.2.2-py35_0
et_xmlfile:        1.0.1-py35_0
freetype:          2.5.5-1
... <snip> ...
tornado:           4.3-py35_1
traitlets:         4.2.1-py35_0
wheel:             0.29.0-py35_0
xlrd:              1.0.0-py35_0
xz:                5.2.2-0
zlib:              1.2.8-3

Proceed ([y]/n)?
```

This says conda has to download `csvkit-0.9.1` from the Internet, and it needs the rest of the packages meet our demands for `csvkit`, `pandas` and `jupyter`.

Type `y` to proceed.

## Enter our environment

Now that we created our environment (our special walled garden), it's time to enter it.

`$ source activate data`

(You might see reference to Windows using only `activate`. Git Bash makes it work like Unix, so we use `source activate`.)

On my machine, my prompt line has changed to indicate I'm in the 'data' environment:

```
christian:~$ source activate data
(data) christian:~$
```

I noticed on my Git Bash on Windows that it had the **(data)** part on the line above my prompt.

---

Next: [Using Notebooks](UsingNotebooks.md)
