# Git version control

Make sure you've [installed VS Code, Git and configured Github](https://github.com/utdata/setting-up) before you get going here.

## Defining verison control

[Search on google](https://www.google.com/search?q=understanding+git+version+control&oq=understanding+git+version+control) and you'll find a ton of [posts](https://www.atlassian.com/git/tutorials/what-is-version-control), [tutorials](https://www.codecademy.com/learn/learn-git) and [videos](https://www.youtube.com/watch?v=Y9XZQO1n_7c) about git and version control systems. I encourage you to explore some that fit you learning style. We'll just cover enough here to get you going and we'll learn by doing.

At its most basic, git allows you to save your work at intervals and it keeps a history of every save point on your computer. Once you have something that works, you save it and leave a comment about what you've done. You can then go back to that exact point in time if you need to. This frees the coder to experiment and make changes that may NOT work, because you know you can always go back. It works for any kind of file you want to put under verison control.

Git allows for a "distributed" version control system, meaning that other people can share the entire code base. When they "check out" a repository (or repo), they get the entire code base. Contributors can then make changes and "check in" those changes for others to use.

Github is the central server where we will save our code. It's also a project management tool and a social network of sorts. It's probalby the most popular code sharing app, but there are others, like Atlassian's [Bitbucket](https://bitbucket.org/).

## Our goals

A "repo" is a folder on your computer that is tracked by git. Our goals here are the following:

* Create a folder in your Documents folder called `code`. This is where we will store all our projects for the rest of the class
* Create a folder inside of `code` called `myproject-firstname` but with your name. This will be your project and code.
* Create a text file in `myproject-firstname` called `README.md`. Every coding project should have this file that describes the project, any dependencies the code base needs, etc. It is written in a language called [Markdown](https://guides.github.com/pdfs/markdown-cheatsheet-online.pdf), which is a text-based syntax that Github turns into pretty HTML when it is published, but is completely readable as text. Here is [tutorial on Markdown](https://guides.github.com/features/mastering-markdown/) you may find useful.
* We'll `init` (initialize) the folder to be tracked by git.
* We'll `add` (or stage) our changes
* We'll `commit` our changes, and include a comment about it.
* We'll go to Github and create a master repo to save our work to
* We'll `push` our repo to the master on github.
* We'll make more changes, rinse and repeat.

### Create our folder structure

There are many ways to create folders on your computer. We're going to use the Terminal and the Code app so we can get used to using them.

* Open your Terminal and type in `$ cd ~/Documents/`
* Create your two directories, but use your name. Always user lowercase letters and no spaces in file and folder names. You'll thank me later:

``` bash
mkdir code
mkdire code/myproject-firstname
```

* Move into your folder: `$ cd code/myproject-firstname`.

### Creating files

We're going to start using our code editor now to manage both our files and our Terminal. If you've configured your text editor right, we'll be able to create our file and launch the editor in the right folder all at the same time.

`$ code README.md`

Hollar if that doesn't work. [This may help if it doesn't](https://code.visualstudio.com/docs/setup/mac).

Let's talk about that command. `code` is the command to invoke the VS Code editor. We followed that with the name of the file. It would open it if it existed, but it has intead created it since it wasn't there already.

You may have noticed we broke our rule about lowercase names for `README.md`. Uppercasing README is a convention that breaks the rule. Just the way it is.

### Adding some content

Our README file is a Markdown file where we'll add some content that describes our project.

``` markdown
# My first github project

I'm learning git and github and this repo will help me. Don't judge.
```

You can save the file, but keep it open.

### Initialize the repo

A cool thing about VS Code is you can open a Terminal window inside the editor and do shell commands there. You can find this under View > Integrated Terminal, or use Control-` on a Mac. This should open a terminal at the root of the project you have open. It will look something like this:

![terminal](../../images/integrated-terminal.png)

Inside this terminal, type in the command to initialize git. Here is my command and response:

``` bash
16:00 $ git init
Initialized empty Git repository in /Users/christian/Documents/code/github-crit/.git/
```

Now git knows we are tracking, but we haven't given it any files yet.

### The git cycle

There typically three steps to committing code in git:

* `add` files that have changed.
* `commit` the files. We'll add a comment at the same time.
* `push` the changes to Github

There is a fourth git command I use a lot, and that is `status`, which tells you what state each file is in the cycle.

You'll repeat these steps a lot.

Let's check the status of our repo. The command is `git status`. Here is my command and response:

``` bash
16:14 $ git status
On branch master

Initial commit

Untracked files:
  (use "git add <file>..." to include in what will be committed)

        README.md

nothing added to commit but untracked files present (use "git add" to track)
(base) ✔ ~/Documents/code/github-crit [master L|…1]
```

We have one untracked file, `README.md`. Let's add it with `git add README.md`. Here is the command and response:

``` bash
16:22 $ git add README.md
(base) ✔ ~/Documents/code/github-crit [master L|●1]
```

There wasn't really a response, but because I have the git-bash-prompt extension installed (in [setting-up](https://github.com/utdata/setting-up)), I have some feedback. We haven't talked about that before, but that part `[master L|●1]` tells me we are on the `master` branch (more on that later) and that I have one staged file. Just watch how those signals change as we go through the cycle.

Now let's commit the file. We will also add a "message" to the commit using the flag `-m`, which you should ALWAYS do. It's good coding practice. Here is the call and response:

``` bash
16:28 $ git commit -m "my first commit"
[master (root-commit) 28bdf3b] my first commit
 1 file changed, 3 insertions(+)
 create mode 100644 README.md
(base) ✔ ~/Documents/code/github-crit [master L|✔]
```

Congrats! You have made your first commit. It might not seem like much now, but we're about to add Github to see the power of distributed code.

### Adding Github to the mix

* Go to a brower and log into github.com.
* Click on the **repositories** link across the top.
* Click on the big green **New** button.
* Name your repository that same name as your folder, so `myproject-name`. (For reals, this doesn't HAVE to be the same name, but I find it very helpful to keep things straight.)
* Add a Description. Something like: My first repo.
* Leave it Public (which is free).
* Leave the "Initialize with README.md" unchecked, because we already have one.
* Click the "Create repository" button.

What you get in response are the commands to create a new repo on your computer to hook up to this repo, but we've done the first several steps already. The part you need is the the `remote add` line. Copy that whole line.

* Go back to VS Code
* Go to the Integrated Terminal and paste the line in and hit return to execute it.
* You won't get much of a response for that (or you shouldn't, anyway.)
* Now we'll `push` our code to github. Here is the call and response:

``` bash
16:38 $ git push origin master
Counting objects: 3, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 302 bytes | 0 bytes/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To github.com:critmcdonald/myproject-crit.git
 * [new branch]      master -> master
```

Now go back to your browser and hit refresh on your repo, and you'll see the result there. Woo hoo!

## Change, commit, push

Now let's make a change to your README.

* Go into VS Code and add a new sentence to your README file.
* Use the terminal to check the status of your repo using `$ git status`.
* Add the change. This time we'll use a fancy command to add all the changed files so we don't have to name it. That period means "all changed files".

`$ git add .`

* Commit the change using `$ git commit -m "new change"`.
* Push the changes to Github using `$ git push origin master`.
* Go to Github in your browser and refresh to see your changes.

And there you have it. You've learned the most common git and Github commands.

----

Next: [Working with others](git-clone.md)
