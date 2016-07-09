Introduction to Anaconda
===================

We want to use some Python programming to do data processing and data analysis. When using Python, it is a good idea to cordon off your work area in something called a **virtual environment**, which keeps all your pieces together, and keeps them from affecting other projects or parts of your computers (especially important for Macs, as they use Python as part of the operating system, and we don't wanna mess that up.)

There is a software package called **conda** makes creating these environments and loading packages pretty easy. If you are new to programming, I probably lost you, and that's OK. Let's just do it.

## Anaconda or Miniconda?

While **conda** is the package manager software, the folks who make it also bundle together conda with Python in a couple of ways:

The full **[Anaconda](https://www.continuum.io/downloads)** includes a Python distribution, the conda package manager, Jupyter notebooks and a suite of the popular data science packages already loaded. It's pretty big, like 1.8G, so it needs space and takes a couple of minutes to download and install.

If you are worried about disc space, you can use **[Miniconda](http://conda.pydata.org/miniconda.html)**, which is a smaller version with just Python and conda, and you can install just the packages you need.

You can start with either. I use Anaconda on my Mac, and Miniconda on my Windows partition.

## Which version of Python?

We'll be using Python 3.5 in our class, so you might as well download that version of the installer so it will use 3.5 by default. If it ends up mattering to you later, you can build environments in either version of the language.

## Download and install

* [Anaconda](https://www.continuum.io/downloads). For my Macbook Air, I used the Python 3.5 64-bit graphical installer. You don't have to sign up for Anaconda Cloud at this time.
* [Miniconda](http://conda.pydata.org/miniconda.html). I used the Miniconda version because I already have full Anaconda on the Mac side of my machine. Use the default to set your PATH variable.
