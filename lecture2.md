# Shell tools and scripting
## Shell script VS other scripting languages
Shell script is basically used to perform operation such as printing (echo), program excution (./<fileName>) and manupilation(touch).

On the other hand, many different scripting languages have been developed that can handle tasks that shell script cannot. Here you need a processor to perform certain functions.

## Bash scripting
Now we will understand some command from ground level up - basically we will try to run different programs wired with other programs.
### Scripting time:

Let us understand how '' and "" works in shell:
```sh
sahilprasad@randomrandom ~ % print "$foo"
bar
sahilprasad@randomrandom ~ % print '$foo'
$foo 
```
As we can see, single inverted commas literally takes the string, on the other hand double inverted commas can further render that string.

*Shell script parameters* :

When different arguments are given to a file, parameters are assigned to these arguments.

Some shell parameters are as follows:

| Syntax      | Used for: |
| ----------- | ----------- |
| $0      | Name of the script.    |
| $1 to $9  |  Arguments to the script. $1 is the first argument and so on.   |
|$@|All the arguments|
|$#|Number of arguments|
|$?|Return code of the previous command|
|$$|PID of the script|
|||

``` $?``` command:

Let's understand $? command with true and false program:
```sh
sahilprasad@randomrandom ~ % false
sahilprasad@randomrandom ~ % $?
zsh: command not found: 1
sahilprasad@randomrandom ~ % true
sahilprasad@randomrandom ~ % $?
zsh: command not found: 0
```
//self explanatory

Let's combine ``` $?```  with ```'||'``` and ```'&&'``` :
```sh
sahilprasad@randomrandom ~ % false || echo "Oops, fail"
Oops, fail
sahilprasad@randomrandom ~ % true || echo "Will not be printed"
sahilprasad@randomrandom ~ % true && echo "Things went well"
Things went well
sahilprasad@randomrandom ~ % false && echo "Will not be printed"
sahilprasad@randomrandom ~ % 
```
Here, when OR operator is used with false and echo, see above that false is ignored as it gave a return code of 1 for ```$?``` command. True gives 0 when ```$?``` is used and therefore OR operator does not have to go  check for the other condition.
Now things change a little bit when it comes to AND operator because it gives output as false or 0 even if one input is zero. Now, after knowing this we can interpret last 2 command easily.

*Command substitution:*
Here, the shell takes the output of the command and then use it as a command further. It can be used with different prgrammes. Let's take one simple example though you can try it with many others:
```sh
sahilprasad@randomrandom ~ % echo "Starting program at $(date)"
Starting program at Fri Dec 16 18:43:33 IST 2022
sahilprasad@randomrandom ~ % 
```
easter egg: try running manual page for test

*Populate a directory* using ```{}``` :
```sh
sahilprasad@randomrandom dir1 % mkdir f1 f2
sahilprasad@randomrandom dir1 % touch f1/file{1..10}.txt
sahilprasad@randomrandom dir1 % touch f2/file{1..11}.txt
sahilprasad@randomrandom dir1 % ls f*
file{1...10}.txt

f1:
file1.txt	file2.txt	file4.txt	file6.txt	file8.txt
file10.txt	file3.txt	file5.txt	file7.txt	file9.txt

f2:
file1.txt	file2.txt	file5.txt	file8.txt
file10.txt	file3.txt	file6.txt	file9.txt
file11.txt	file4.txt	file7.txt
sahilprasad@randomrandom dir1 % 
```
Let's understand it line by line, here what we did is make 2 folders f1 and f2 used ```touch``` command to go in that particular folder and make multiple file at once. ```*``` matches one or any amount of characters.

### Different shell tools:
Finding and locating files:

```sh
sahilprasad@randomrandom ~ % find . -name src -type d
./Desktop/Visual Studio Code.app/Contents/Resources/app/extensions/ms-vscode.js-debug/src
```

The syntax here used, is simple we can understand it as the name of the file being 'src' and for d it is a directory. There are many other ways to find files in the system, manual page has it all.

```locate``` command:

For ```locate``` command, shell goes through an updated database i.e done via cron. Let's check a simple command here.
```sh
sahilprasad@randomrandom ~ % locate mysql
/Applications/LibreOffice.app/Contents/Frameworks/libmysql_jdbclo.dylib
```
P.S- Obviously, there would be many files; I've just shortened it. I'll cover grep in a further blog.

*```History``` command:*
You can always use up and down arrows to navigate through your previously used command but to list each and every one of the command as an output, we can use ```History``` command.

```sh
sahilprasad@Sahils-MacBook-Air ~ % history
 11  java - version
 19  cd desktop
```
There are commands to curate your ```History``` output. We can used control+r(mac) to enable backward search through the history.

