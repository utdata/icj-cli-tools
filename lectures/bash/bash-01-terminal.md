# Using a Terminal

## Terminal vs shell

Terminal (Mac) and Git Bash (Windows) are programs that can run a **shell**, which is a word-based user interface where you type commands that your computer understands. The default language for these interactions is called **Bash**, and we used them when we set up your computer in [icj-setting-up](https://github.com/utdata/icj-setting-up).

People (including myself) will use the term **shell** and **terminal** interchangeably. This means when I say "type into your shell", I mean type at the prompt in your terminal window. Just to add confusion, Mac named their program "Terminal". (I actually use a different Mac program called iTerm, but Terminal is fine.)

Macs understand Bash natively, but some day they will change to a similar language called zsh. When you launch a shell on newer Macs you might get a message **The default interactive shell is now zsh. To update your account to use zsh, please run `chsh -s /bin/zsh`.** DON'T DO THIS! JUST IGNORE IT. We will continue to use **Bash**. If somehow you are set to use zsh, you can [check and/or change it to Bash](bash-change-mac.md).

**PCs** don't understand Bash at all without the help of another program. This is why we installed **Git Bash** so we can all speak the same language.

For what its worth, Bash is a Unix-based program. Most of the Internet runs on Unix (or Linux) computers.

## Code examples in lessons

When I give example commands for you to type, you may see a `$` at the beginning to indicate this should go at the prompt in your terminal. DON'T TYPE IN THE $.

`$ pwd`

That means you type in "pwd" and then hit return.

## Typing vs copy/paste

I encourage you to type commands into your terminal instead of copy and pasting them from the lessons. Build muscle _and_ mind memory. Typing a command wrong and then having to figure out why it broke will help you learn it and remember it. If you just copy and paste blindly, then you won't learn anything other than command-c and command-p.

---

**Next**: [Moving around in the Terminal](bash-02-moving-around.md)
