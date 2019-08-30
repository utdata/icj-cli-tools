<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [What is a Terminal](#what-is-a-terminal)
  - [Macintosh](#macintosh)
  - [PCs](#pcs)
  - [Code examples in lessons](#code-examples-in-lessons)
  - [Typing vs copy/paste](#typing-vs-copypaste)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

# What is a Terminal

Terminal (Mac) and Git Bash (Windows) are programs that can run a **shell**, which is the user interface your computer understands. The default language for these interactions is called **Bash**. All these crazy [commands](lectures/Commands.md) I'm going to teach you are BASH commands.

People (including myself) will use the term **shell** to mean "the terminal window you have open". This means when I say "type into your shell", I mean type at the prompt in your terminal window.

## Macintosh

Oh, you are so lucky. Since Macs are Unix-based, you have everything you need already on your computer to get started with some command-line fun.

Look for a program called **Terminal** on your computer.

It'll look something like this:

![Terminal](../../images/iterm2-start.png)

I use an alternative shell program called [iTerm2](https://iterm2.com/) which has some additional functionality, but Apple's Terminal program is just fine.

## PCs

For the PCs, when you install git for Windows, it also installs  **Git Bash**, which is the terminal program we'll use. Windows is NOT a Unix-based machine like a Mac, so it doesn't naturally understand Unix commands. Git Bash is a program that does.

## Code examples in lessons

When I give example commands for you to type, you may see a `$` at the beginning to indicate this should go at the prompt in your terminal. DON'T TYPE IN THE $.

`$ pwd`

That means you type in "pwd" and then hit return.

## Typing vs copy/paste

I encourage you to type commands into your terminal instead of copy and pasting them from the lessons. Build muscle _and_ mind memory. Typing a command wrong and then having to figure out why it broke will help you learn it and remember it. If you just copy and paste blindly, then you won't learn anything other than command-c and command-p.

---

**Next**: [Moving around in the Terminal](bash-02-moving-around.md)
