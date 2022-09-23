# holbertonschool-shell
# The "Shell"

Simply put, the shell is a program that takes commands from the keyboard and gives them to the operating system to perform. In the old days, it was the only user interface available on a Unix-like system such as Linux. Nowadays, we have graphical user interfaces (GUIs) in addition to command line interfaces (CLIs) such as the shell.

On most Linux systems a program called bash (which stands for Bourne Again SHell, an enhanced version of the original Unix shell program, **sh**, written by Steve Bourne) acts as the shell program. Besides bash, there are other shell programs available for Linux systems. These include: **ksh**, **tcsh** and **zsh**.

- The Terminal

It is a program that opens a window and allows you to interact with the shell getting input from the keyboard and executing command lines. The first thing we should see is a shell prompt that contains our user name and the name of the machine followed by a % sign. Something like this: ```user@users-MacBook-Pro ~ % ```

Interacting with the terminal is as simple as typing something inside of it, you can try some random message and see how it reacts...

```user@users-MacBook-Pro ~ % Hello kind shell, please respond```

```zsh: command not found: Hello```

Turns out that the shell responds to specific input that we can call *command lines*, think of command lines as a unique designed language that the shell understands and executes.
Now hit the "up" arrow on your keyboard, as you can probably guess... yes the terminal has a *command history* which is a handy feature.

- Navigation

The first thing that you might want to get an idea is navigation in the shell.
Unlike most modern computers the terminal does not have a Graphical user interface (GUI) which is a visual representation of what you are doing with your mouse, what files can you click, move etc... So it might get pretty confusing at the beginning if you are unaware of some basic commands to orient yourself.

The 3 basic commands you might wanna learn asap are :

[pwd](http://linuxcommand.org/lc3_man_pages/pwdh.html) (print working directory), [cd](http://linuxcommand.org/lc3_man_pages/cdh.html) (change directory), [ls](http://linuxcommand.org/lc3_man_pages/ls1.html) (list files and directories)

***pwd*** is like asking the question "where am i ?" to which the shell responds
```/Users/user```

***cd*** is like requesting to the shell to navigate to a specified location
for example ```user@users-MacBook-Pro ~ % cd Desktop/``` is the same as saying to the shell "Go to my desktop" which normally you would just use your mouse to go to.

**ls** is the same as requesting to the shell to list all the files and directories of the place where we are currently standing, in the above example, the desktop.

```user@users-MacBook-Pro Desktop % ls```

```Test Project``` would me the file.

You could try navigating the shell and poking around the system to get these commands under your fingertips.

- Manipulating files and directories

Now that you feel competent enough to navigate through the system, there are a handful of commands to manipulate files, so to say, copy them, move them around, rename or delete them.

[cp](http://linuxcommand.org/lc3_man_pages/cp1.html) - copy files and directories

[mv](http://linuxcommand.org/lc3_man_pages/mv1.html) - move or rename files and directories

[rm](http://linuxcommand.org/lc3_man_pages/rm1.html) - remove files and directories

[mkdir](http://linuxcommand.org/lc3_man_pages/mkdir1.html) - create directories

## This repo will serve as a basic introduction to shell , terminal and scripting ideas for Holberton School Albania.

- Please check inside for the other README files for further info.
