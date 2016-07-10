Using csvkit to process data
============================

[Csvkit](http://csvkit.rtfd.org/) is a collection of Python-based command-line tools that can help process a large amount of data really quickly. The Tutorial on the docs is pretty good, and I encourage you to go through it either before or after this lesson.

I'm going to introduce Jupyter Notebooks with this lesson, too. This will allow you to write notes with your code and to repeat the steps as needed.

## Create our project directory

We need a place to work on all this stuff. So create a working directory for this project. Perhaps you can start with `cd ~` to get in your home directory, and then create a new working directory called `hotels`.

`$ mkdir hotels`

And then make another directory inside of that:

`$ mkdir hotels/data`

Then move inside the `hotels` directory:

`$ cd hotels`

## Starting up Jupyter Notebooks

If you are not already in the *data* conda environment [we made earlier](IntroToAnaconda.md), go ahead and get in it.

`$ source activate data`

Next, we're going to install a package that will allow us to run Bash in notebook.

`$ pip install bash_kernel`

`$ python -m bash_kernel.install`

Now we are going to launch our Jupyter Notebooks server, and we'll do the rest of our work there.

`$ jupyter notebook`

This will start a Jupyter Notebooks server and throw you into a browser window. It will look something like this:

![notebook-start.png](notebook-start.png)
