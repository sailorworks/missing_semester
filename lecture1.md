# The shell

## Why shell?
The shell is a very basic textual interface that allows you to change programmes that won't change unless you use a command from the root user, and the root user can only be accessed through the shell. This also helps to understand how things work internally at the [kernel level](https://en.wikipedia.org/wiki/Kernel_(operating_system)).

## Understanding shell:

We can understand shell as a programming environment and just like that it has conditionals, loops and functions. If you are using linux or mac os the terminal is the main textual interface to the shell. For windows you have to use [windows subsystem for linux](https://learn.microsoft.com/en-us/windows/wsl/) or a linux virtual machine just to use unix-style command line tools.

## Getting started with shell:

#### - With the help of few commands we will understand how to get around shell

Let's type a simple command : date
```sh
Last login: 12345 on ttys000
sahilprasad@randomrandom ~ % date
Mon Dec 12 14:52:29 IST 1999
```
 *ls command:*
```sh
ls
```
gives the list of the folder or files in that directory
```sh
sahilprasad@randomrandom ~ % ls
Applications	Documents	Library		Music		Public
Desktop		Downloads	Movies		Pictures	pico.save
```



*cd command:*
```sh
cd
```
cd is change directory, and let's say we want to navigate from the current directory to the desktop and then list it's contents we get
```sh
sahilprasad@randomrandom ~ % cd desktop
sahilprasad@randomrandom desktop % ls
game1
game2
game3
game4
```
*ls -l command:*
```sh
ls -l
```
ls -l gives you the permission of that file and folders in that directory
```sh
sahilprasad@randomrandom desktop % cd nand2tetris
sahilprasad@randomrandom nand2tetris % cd tools
sahilprasad@randomrandom tools % ls -l
total 96

-rw-rw-r--   1 sahilprasad  staff  1107 Mar 12  2016 HardwareSimulator.bat
-rwx------   1 sahilprasad  staff  1432 Mar 12  2016 HardwareSimulator.sh
-rw-rw-r--   1 sahilprasad  staff   730 Mar 12  2016 JackCompiler.bat
-rw-rw-r--   1 sahilprasad  staff  1050 Mar 12  2016 JackCompiler.sh
drwxrwxr-x  10 sahilprasad  staff   320 Jan 27  2017 OS
drwxrwxr-x   8 sahilprasad  staff   256 Dec 11 17:45 bin
```

Here, the first three letters represent that the file is owned by the user, in this case, sahilprasad; the next three letters represent that the file is owned by a group of people; and the final three letters represent permission for everyone (including those who do not own the file). 

Let us define what does each and every letter in front of files/folders does.
 
- d represent that it is a folder/directory
- r represent that you can only read that file
- w represent that you can write, save and add more to it
- x means that it is executable



*rmdir command:*
```sh
sahilprasad@randomrandom desktop % rmdir fold
```
As the name suggest it's remove directory, what I did is delete a folder named "fold" from the desktop - note, that you can only delete folder or directory when it is empty.

| *command (pipe):*
```sh
|
```
It just wires two programs
```sh
sahilprasad@Sahils-MacBook-Air desktop % ls | tail -n1 
game4
```
Pipe command  took two different programmes which are not correlated and printed the output.

exercise

![lul](https://user-images.githubusercontent.com/97829644/207043312-04848661-cea8-400b-9572-1b8991a8ff7f.png)
