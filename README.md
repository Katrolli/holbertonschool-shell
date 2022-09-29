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

## I/O Redirections and filters

- Input/Output redirection basics

The simplest example we can make to explain what input/output are is by thinking on how we give commands to the terminal and how the terminal replies to us. Basically we *input* our code using the keyboard and the terminal responds by *outputting* messages in our computers display.

The terminal supports this powerful feature which is *I/O* redirection, allowing us to input information from other sources and outputting the result into another direction.

- Standart Output 

Most command line programs that display their results do so by sending their results to a facility called standard output. By default, standard output directs its contents to the display. To redirect standard output to a file, the ">" character is used like this:

```ls > file_list.txt```

In this example, the ls command is executed and the results are written in a file named file_list.txt. Since the output of ls was redirected to the file, no results appear on the display.

Each time the command above is repeated, file_list.txt is overwritten from the beginning with the output of the command ls. To have the new results *appended* to the file instead, we use ">>" like this:

```ls >> file_list.txt```

When the results are appended, the new results are added to the end of the file, thus making the file longer each time the command is repeated. If the file does not exist when we attempt to append the redirected output, the file will be created.

- Standart Input

Many commands can accept input from a facility called standard input. By default, standard input gets its contents from the keyboard, but like standard output, it can be redirected. To redirect standard input from a file instead of the keyboard, the "<" character is used like this:

```sort < file_list.txt```

In the example above, we used the ***sort*** command to process the contents of file_list.txt. The results are output on the display since the standard output was not redirected. We could redirect standard output to another file like this:

```sort < file_list.txt > sorted_file_list.txt```

As we can see, a command can have both its input and output redirected. Be aware that the order of the redirection does not matter. The only requirement is that the redirection operators (the "<" and ">") must appear after the other options and arguments in the command.

## Pipelines

The most useful and powerful thing we can do with I/O redirection is to connect multiple commands together to form what are called *pipelines*. With pipelines, the standard output of one command is fed into the standard input of another. Here is a very useful example:

```ls -l | less```

In this example, the output of the ls command is fed into less. By using this "| less" trick, we can make any command have scrolling output.


### Filters

One kind of program frequently used in pipelines is called a *filter*. Filters take standard input and perform an operation upon it and send the results to standard output. In this way, they can be combined to process information in powerful ways. Here are some of the common programs that can act as filters:

[sort](http://linuxcommand.org/lc3_man_pages/sort1.html) -	Sorts standard input then outputs the sorted result on standard output.

[uniq](http://linuxcommand.org/lc3_man_pages/uniq1.html) -	Given a sorted stream of data from standard input, it removes duplicate lines of data (i.e., it makes sure that every line is unique).

[grep](http://linuxcommand.org/lc3_man_pages/grep1.html) - Examines each line of data it receives from standard input and outputs every line that contains a specified pattern of characters.

[fmt](http://linuxcommand.org/lc3_man_pages/fmt1.html) - Reads text from standard input, then outputs formatted text on standard output.

[pr](http://linuxcommand.org/lc3_man_pages/pr1.html) - Takes text input from standard input and splits the data into pages with page breaks, headers and footers in preparation for printing.

[head](http://linuxcommand.org/lc3_man_pages/head1.html) - Outputs the first few lines of its input. Useful for getting the header of a file.

[tail](http://linuxcommand.org/lc3_man_pages/tail1.html) - Outputs the last few lines of its input. Useful for things like getting the most recent entries from a log file.

[tr](http://linuxcommand.org/lc3_man_pages/tr1.html) - Translates characters. Can be used to perform tasks such as upper/lowercase conversions or changing line termination characters from one type to another (for example, converting DOS text files into Unix style text files).

[sed](http://linuxcommand.org/lc3_man_pages/sed1.html) - Stream editor. Can perform more sophisticated text translations than tr.

[awk](http://linuxcommand.org/lc3_man_pages/awk1.html) - An entire programming language designed for constructing filters. 
 
## This repo will serve as a basic introduction to shell , terminal and scripting ideas for Holberton School Albania.

- Please check inside for the other README files for further info.
