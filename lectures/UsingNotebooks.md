Using Jupyter Notebooks
============================

Our next lession will use [csvkit](http://csvkit.rtfd.org/), a collection of Python-based command-line tools that can help process a large amount of data really quickly. The Tutorial on the docs is pretty good, and I encourage you to go through it either before or after this lesson.

But I'm also going to introduce Jupyter Notebooks with this lesson, too. This will allow you to write notes with your code and to repeat the steps as needed. It is not necessary to use Jupyter Notebooks for some of this, but it makes it much easier to run command-line based commands both in bash and in Python.

## Move into or create a class directory

We need a safe place to work. I suggest setting up a class directory in your home/Documents folder.

```
$ cd ~/Documents
```
This puts you inside your Documents directory and prints your path to make sure you are there.

`$ mkdir rwd`

Move into it:

`$ cd rwd`


## Starting up Jupyter Notebooks

If you are not already in the *data* conda environment [we made earlier](IntroToAnaconda.md), go ahead and get in it.

`$ source activate data`

Next, we're going to install a package that will allow us to run Bash in a Jupyter Notebook. You only have to do this steop one time and then you'll always have it within the `data` environment.

> (Running Bash (or Python) in a notebook is much easier than using the command-line alone. I should probably start you without it so you know how lucly you are, but I won't.)

> (Also, I'm having trouble with the Bash kernel on Windows running in Parallels. I suggest Windows users try this, but be ready to be flexible in class if it doesn't work. You can always use a Python notebook, but start the cell with `%% bash` to emulate the bash command-line.)

OK, let's install the package. (I may choose to explain **pip** in class. Or, not.)

`$ pip install bash_kernel`

`$ python -m bash_kernel.install`

Now we are going to launch our Jupyter Notebooks server, and we'll do the rest of our work there.

`$ jupyter notebook`

This will start a Jupyter Notebooks server and throw you into a browser window. It will look something like the image below. Go under "New" and select **Bash**. (Windows users might have to use Python, then start each cell with `%% bash`.)

![notebook-start.png](../images/notebook-start.png)

This process will also take over your terminal window, which is now running the Jupyter Notebooks server. If you need to do further terminal work, you'll need to open a new window (command-n) or tab (command-t).

At the top of your new notebook, click on **Untitled** and name your notebook **APD Demographics**.

Now, in another brower window, go open my [APD Demographics data pipeline](https://github.com/utdata/cli-tools/blob/master/lectures/csvkit/APD%20Demographics%20data%20pipeline.ipynb) notebook in GitHub so you can follow along.

## Moving around Notebooks

At this point, I need to explain how to get around a Notebook.

* Markdown cell vs code cell
* Activating a cell
* Inserting a cell
* Saving the file
* Find it on your computer
* Closing it and shutting down the server
* Restarting it
