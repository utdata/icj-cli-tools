# Using a Terminal

## Terminal vs shell

Terminal (Mac) and Git Bash (Windows) are programs that can run a **shell**, which is a text-based user interface where you type commands that your computer understands.

> People (including myself) will use the term **shell** and **terminal** interchangeably. This means when I say "type into your shell" or "in your terminal", I mean type at the prompt in your Terminal or Git Bash program. (Just to add confusion, I use a different Mac terminal program called iTerm, but Terminal is fine.)

Developers use a shell to issue commands to their computer to do things, like install programs, change what folder their are in, etc. Using a terminal program to use your computer can be confusing at first, but it will become second-nature as you progress through this class.

The shell programming language we will use for these text-based interactions is called **Bash**.

**Windows** doesn't understand Bash at all without the help of another program. This is why we installed **Git Bash** so we can all speak the same language. (If you are a Windows user and haven't yet installed Git, [do it now](https://github.com/utdata/icj-setting-up/blob/master/windows-01.md#install-git).)

For what its worth, Bash is a Unix-based program. Most of the Internet runs on Unix (or Linux) computers.

**Macs** understand Bash natively, but some day they will change to a similar language called zsh. When you launch a shell on newer Macs you might get a message _The default interactive shell is now zsh. To update your account to use zsh, please run `chsh -s /bin/zsh`._ **DON'T DO THIS! JUST IGNORE IT.** We will continue to use **Bash**. Later we will add a command to disable this message. If somehow your terminal gets set to use zsh, you can [check and/or change it to Bash](bash-change-mac.md).

## Launch your terminal

1. For **Macs** you can use your Launchpad and type in _Terminal_ and launch it. Or you can use the Spotlight search to find it.

It will look like this:

![Mac Terminal](../../images/terminal-startup.png)

1. For **Windows** you can go to your Start menu and type in _Git Bash_ and launch it.

It will look like this:

![Windows Git Bash](../../images/gitbash-startup.png)

## The terminal prompt

When I launch my terminal, the commands inside it look like this:

```bash
COMMA21617:~ ccm346$
```

The first part before the `~` is my computer name, and the part after is my username.

> I actually shorten my prompt name to `crit:~$` so you'll see that in my examples. We'll shorten yours later, too.

Lastly we have the `$`. This is the "prompt" where you type commands. You type your commands AFTER the $ and then hit **Return** to execute them.

When I give command instructions for you to type, I sometimes (but not always) include the `$` at the beginning to indicate this should go at the prompt in your terminal. DON'T TYPE IN THE $. For instance:

`$ pwd`

Means you type in just "pwd" and then hit return.

## Typing vs copy/paste

I encourage you to type commands into your terminal instead of copy and pasting them from the lessons. Build muscle _and_ mind memory. Typing a command wrong and then having to figure out why it broke will help you learn it and remember it. If you just copy and paste blindly, then you won't learn anything other than command-c and command-v.

---

**Next**: [Moving around in the Terminal](bash-02-moving-around.md)
