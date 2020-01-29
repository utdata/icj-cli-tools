# What is a Terminal

Terminal (Mac) and Git Bash (Windows) are programs that can run a **shell**, which is the user interface your computer understands. The default language for these interactions is called **Bash**. All these crazy [commands](bash-04-commands.md) I'm going to teach you are BASH commands.

> Newer Macs are using **zsh** instead of **Bash**. Mac users take a minute to [check and/or change it to Bash](bash-change-mac.md).

People (including myself) will use the term **shell** to mean "the terminal window you have open". This means when I say "type into your shell", I mean type at the prompt in your terminal window.

## Macintosh

Oh, you are so lucky. Since Macs are Unix-based, you have everything you need already on your computer to get started with some command-line fun.

Look for a program called **Terminal** on your computer. I do this by clicking on the rocket ship icon and searching for **Terminal**.

It'll look something like this:

![Terminal](../../images/iterm2-start.png)

I use an alternative shell program called [iTerm2](https://iterm2.com/) which has some additional functionality, but Apple's Terminal program is just fine.

## PCs

For the PCs, when you installed git for Windows, it also installed  **Git Bash**, which is the terminal program we'll use. Windows is NOT a Unix-based machine like a Mac, so it doesn't naturally understand Unix commands. Git Bash is a program that does.

You should be able to use the Windows "Search" bar to find **Git Bash** to launch it.

> When using the Terminal within Visual Studio code on Windows, we might need to change the default shell to Git Bash. I think there is a drop-down menu for that.

## Code examples in lessons

When I give example commands for you to type, you may see a `$` at the beginning to indicate this should go at the prompt in your terminal. DON'T TYPE IN THE $.

`$ pwd`

That means you type in "pwd" and then hit return.

## Typing vs copy/paste

I encourage you to type commands into your terminal instead of copy and pasting them from the lessons. Build muscle _and_ mind memory. Typing a command wrong and then having to figure out why it broke will help you learn it and remember it. If you just copy and paste blindly, then you won't learn anything other than command-c and command-p.

---

**Next**: [Moving around in the Terminal](bash-02-moving-around.md)
