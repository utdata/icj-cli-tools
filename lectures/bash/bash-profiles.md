# Editing the Bash profile

There is a hidden file on your computer that is the profile for your bash terminal. If you have VS Code installed and configured as your text editor, you can open it with this:

`$ code ~/.bashrc`

We'll be adding lines to that file and then saving it. So see the changes reflected in your terminal, you have to exit and open a new one.

## Shorten your terminal name

My prompt line in my terminal is really long. It looks like this:

`CHRISTIANs-MacBook-Air-2:~ christian$`

You can shorten it to just your login name by adding this line to your `.bashrc` file.

`PS1='\u:\W\$ '`

## List all long including hidden

When I want to see everything in a directory, including all the hidden files and the other details like size, date, etc., then the command is `ls -al`. But I put in a alias so all I have to type is `ll` to get that long list. Add this to your `.baschrc`:

`alias ll="ls -al"`
