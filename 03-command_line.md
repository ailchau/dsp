# Learn command line

Please follow and complete the free online [Command Line Crash Course
tutorial](https://web.archive.org/web/20160708171659/http://cli.learncodethehardway.org/book/) or [Codecademy's Learn the Command Line](https://www.codecademy.com/learn/learn-the-command-line). These are helpful tutorials. Each "chapter" focuses on a command. Type the commands you see in the _Do This_ section, and read the _You Learned This_ section. Move on to the next chapter. You should be able to go through these in a couple of hours.

---

### Q1.  Cheat Sheet of Commands  

Here's a list of items with which you should be familiar:  
* show current working directory path
* creating a directory
* deleting a directory
* creating a file using `touch` command
* deleting a file
* renaming a file
* listing hidden files
* copying a file from one directory to another

Make a cheat sheet for yourself: a list of at least **ten** commands and what they do.  (Use the 8 items above and add a couple of your own.)  

> > `pwd`: show current working directory path  
> > `mkdir directoryname`: creating a directory  
> > `rmdir directorname`: deleting a directory  
> > `touch filename`: creating an empty file  
> > `rm filename`: deleting a file  
> > `mv oldname newname`: renaming or moving a file  
> > `ls -a`: listing all files (including hidden files)  
> > `cp filename directory`: copy a file from one directory to another  
> > `grep string *.txt`: searches for string within inside txt files. -i ignores case distinction  
> > `pushd directoryname`: remembers current directory changes to new directory  
> > `popd`: returns to previous directory when used `pushd`  

---

### Q2.  List Files in Unix   

What do the following commands do:  
`ls`  
`ls -a`  
`ls -l`  
`ls -lh`  
`ls -lah`  
`ls -t`  
`ls -Glp`  

> > `ls`: lists the contents of the current directory  
> > `ls -a`: lists all contents (including hidden files)  
> > `ls -l`: lists the contents with additional details (including permissions)  
> > `ls -lh`: similar to -l with file size in an easier to read format (human readable format)  
> > `ls -lah`: combination of -lh and -a (including hidden files)  
> > `ls -t`: lists contents starting with the most recent  
> > `ls -Glp`: similar to -l with directories displayed in blue with /  

---

### Q3.  More List Files in Unix  

Explore these other [ls options](http://www.techonthenet.com/unix/basic/ls.php) and pick 5 of your favorites:

> > `ls -R`: lists all content and subdirectories (recursively)  
> > `ls -g`: similar to -l while omitting owner names  
> > `ls -o`: similar to -l while omitting group names  
> > `ls -1`: displays each entry on a line  
> > `ls -ltr`: lists content in long format from oldest to most recent (reverse -t order)  
> > `ls -F`: classifies contents based on the file type (/ = directory, @ = link file, * = executable file)  

---

### Q4.  Xargs   

What does `xargs` do? Give an example of how to use it.

> > `xargs` is command that executes commands or arguments. When used without arguments, it converts multi-line output into a single line. It is most powerful when used in combination with other commands (e.g., grep or find). For instance, `find /tmp -name "*.tmp" | xargs rm` searches for all the tmp files in the /tmp directory and deletes them. Similarly, `find . -name "*.txt" | xargs grep "hello"` searches for all the txt files and then returns  all the files that contain the string "hello".


 

