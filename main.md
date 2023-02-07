# Introduction

My name is Kevin McCall.

I am here to give a thorough overview of Vim.

-   What is everyone's experience with Vim?

# Intro to Vim

Vim, or vi improved, is a modal text editor from the 1990s. Vim is a rewrite of vi to improve the codebase and extends vi's features. It is different from many text editors because what you type is not what appears on your document. Despite that Vim has a steep learning curve, once you master Vim, you will never reach for your mouse again.

# How to install Vim

By default, vi comes installed on most linux distributions. However, you must download Vim manually.

## Using a Package Manager

-   Ubuntu, Debian (Aptitude): `sudo apt install vim`
-   CentOS, Red Hat Enterprise Linux (yum): `yum install vim`
-   Arch Linux (Pacman): `pacman -S vim`

## Using your web browser

Download the version of Vim specific to your operating system.

-   [Download Vim](https://www.vim.org/download.php#pc)

# Basic Editing

-   [Cheat sheet one](https://devhints.io/vim)
-   [Cheat sheet two](https://vim.rtorr.com/)

Use **h** **j** **k** and **l** to move around the document.
Use **x** to delete a single character under the cursor.

```
helllo my name is kevin maccl.

My favortite animl is a dog.
```

# Insert mode

This is the mode that you use whenever you are typing text.
This mode is most commonly entered with the kebinds i, a, or o.

```

```

# Normal Mode

This is the mode you want to be in most of the time, this is where you chain commands to maneuver and edit the document.

You can always get back to this mode by pressing escape (pressing escape three times in a row guarantees you get back in normal mode).

# Command Mode

This is used for specific commands that do not have keyboard shortcuts.
This mode is entered with a colon **:**.

# Visual Mode

This is a mode where you can refine a selection of text to work with.
Enter visual mode by pressing v.
Visual mode helps you create a selection where you can apply an edit to.

```
I want to delete from this point ** all the way to this point **
```

# Leaving Vim

You can't. jk.

After you are finished editing a file, you probably want to leave the text editor to do something else
You can chain these commands to exit files.

-   **:q** is for quitting
-   **:w** is for writing
-   **:a** is for “all files”
-   **!** mark forces the command to occur

**For example:** To leave Vim regularly without saving your changes, type **:q!**
If you want to exit Vim with multiple files open, type **:qa!**
If you want to save the current and exit Vim you would type **:wq**

# Operators

Vim is composed of operators

They are either in the form of:

-   {operator}{count}{motion}

or

-   {count}{operator}{motion}

Most commands on the keyboard have a similar version mapped to **shift+{key}**

**For example:** To append text press **a**. To append text to the end of a line, press **shift+a**

# Motions

Motions are how you move around the document

HJKL are movement keys, but there are many more options

-   **B** and **W** will send you one word forward
-   **gg** to go to the start of a file
-   **G** to go to the end of a file
-   **{** and **}** to go forward / backward paragraphs

## Repeating motions

Motions in Vim can be given a number to repeat for that many times

**For example:** **5w** will move 5 words forward

This is useful because you can make multiple edits without having to repeat the command yourself manually

# Copy/Pasting Text

There are two ways to copy text in Vim:

1. Whenever you do a deletion command, this will count as “cutting the text” and it will copy it
2. You can regularly copy text by using the y operator with a motion

You can paste text after your cursor with p and before your cursor with P

# Common Commands / Shortcuts

-   O - adding a new line
-   dd - delete the current line
-   / - search the document
-   Ctrl - l - refresh the screen and get rid of highlighting
-   CTRL - N in insert mode - autocomplete
-   . - Repeat the last command
-   Splitting windows with ctrl-w + v / ctrl-w + s
-   Switching between windows with ctrl + movement keys
-   Ctrl-f / ctrl-b to page forward / backward
-   Ctrl-d in command mode -> autocomplete

```

```

# Find and Replace

Vim has support to find text in a document and to replace it

# More Complex File Editing

See example

# Help Features

Vim has the command :h that will let you search for help topics
You can figure out things inside of Vim without having to google it

## Keyboard Representations

Caret **^** corresponds to ctrl

## :helpgrep

Use this to research topics you have a general idea of what you want to see
**For example:** :helpgrep windows
Use **CTRL-]** to go to the next result and **CTRL-i** to go back

## Help formatting

-   **:h :command** " help for ex-command 'command'
-   **:h 'option'** " help for option 'option'
-   **:h function()** " help for function 'function'
-   **:h modifier-key** " help for 'modifier'-'key' in normal mode
-   **:h mode_modifier-key** " help for 'modifier'-'key' in 'mode'
-   **:h mode_modifier-key_modifier-key** " help for 'modifier'-'key' 'modifier'-'key' in 'mode'

## vimtutor

vimtutor is a tool to teach you Vim interactively through short exercises. In total, it takes about 30 minutes to complete. Access vimtutor by typing `vimtutor` in the terminal.

# RTFM

## **Read The Friendly Manual**

Bram Moolenaar wrote a series of manuals written for Vim that teach you how to improve your workflow.

Access these manuals by typing :help, scrolling down to the user\_##.txt files, and pressing **shift+k** on them

# Setting options in Vim

Vim is a very customizable editor that allows you to change features
Using the set command you can set settings to change how Vim works

**For example:** You can set line numbers using :set number
Each option has its own way of being set - use the help to figure out what it needs

# Useful commands

-   **:set syntax** -> set syntax highlighting for the current file
-   **:set number** -> set line numbers on the current file
-   **set tabstop=4**
-   **set shiftwidth=4**
-   **set expandtab**

# .vimrc

This file is a way to set all of your settings persistently between Vim sessions

This file is located at either **~/.vimrc** or **~/.config/.vimrc** on linux

Vim will autoload this file each time it is opened

This config file is written in vimscript, which is _more or less_ command mode

# Extending Vim (Plugins)

They allow you to download extra functionality for the software created by people online

# Finding plugins

You can search online for plugins on websites like https://vimawesome.com/

This website will tell you installation instructions for all major plugin managers

**For example:** Lets look at vim-airline:

-   [vim-airline-superman](https://vimawesome.com/plugin/vim-airline-superman)

# Installing Plugins

There are many plugin managers available for Vim
You can install plugins natively through Vim, but it is unclean and hard to mange

I use and recommend vim-plug to manage plugins:

-   [vim-plug](https://github.com/junegunn/vim-plug)

# Other stuff

## Tmux / GNU Screen

Tmux is a “terminal multiplexer” and so is GNU Screen.
Install either of them through your package manager.

Both of them allow your terminal to have multiple instances and to be split so that you can jump between Vim and the terminal when coding.

## Sensible Defaults

Vim is based on vi which is old. The standards for interacting with programs have changed since 1976.
Therefore, you should consider finding config files online that make the default settings a little more user friendly

-   [vim-sensible](https://github.com/tpope/vim-sensible)

## Visual Studio Code Vim Bindings

If you really love Vim, you can install a plugin for visual studio code to replicate the modal editing of Vim
[Vim Bindings for VS Code](https://marketplace.visualstudio.com/items?itemName=vscodevim.vim)

# Questions?
