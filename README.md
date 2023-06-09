0. Where am I?.
1. What’s in there?
2.There is no place like home
3. The long format
4. Hidden files
5. I love numbers
6. Welcome
7. Betty in my first directory
8. Bye bye Betty
9. Bye bye My first directory
10. Back to the future
11. Lists
0x00. Shell, basics
DevOps
Shell
Bash
 By: Julien Barbier
 Weight: 1
 Project will start Jun 7, 2023 6:00 AM, must end by Jun 8, 2023 6:00 AM
 Checker was released at Jun 7, 2023 6:00 AM
 An auto review will be launched at the deadline
About Bash projects
Unless stated, all your projects will be auto-corrected with Ubuntu 20.04 LTS.



Resources
Read or watch:

What Is “The Shell”?
Navigation
Looking Around
A Guided Tour
Manipulating Files
Working With Commands
Reading Man pages
Keyboard shortcuts for Bash
LTS
Shebang
man or help:

cd
ls
pwd
less
file
ln
cp
mv
rm
mkdir
type
which
help
man
Learning Objectives
At the end of this project, you are expected to be able to explain to anyone, without the help of Google:

General
What does RTFM mean?
What is a Shebang
What is the Shell
What is the shell
What is the difference between a terminal and a shell
What is the shell prompt
How to use the history (the basics)
Navigation
What do the commands or built-ins cd, pwd, ls do
How to navigate the filesystem
What are the . and .. directories
What is the working directory, how to print it and how to change it
What is the root directory
What is the home directory, and how to go there
What is the difference between the root directory and the home directory of the user root
What are the characteristics of hidden files and how to list them
What does the command cd - do
Looking Around
What do the commands ls, less, file do
How do you use options and arguments with commands
Understand the ls long format and how to display it
A Guided Tour
What does the ln command do
What do you find in the most common/important directories
What is a symbolic link
What is a hard link
What is the difference between a hard link and a symbolic link
Manipulating Files
What do the commands cp, mv, rm, mkdir do
What are wildcards and how do they work
How to use wildcards
Working with Commands
What do type, which, help, man commands do
What are the different kinds of commands
What is an alias
When do you use the command help instead of man
Reading Man Pages
How to read a man page
What are man page sections
What are the section numbers for User commands, System calls and Library functions
Keyboard Shortcuts for Bash
Common shortcuts for Bash
LTS
What does LTS mean?
Copyright - Plagiarism
You are tasked to come up with solutions for the tasks below yourself to meet with the above learning objectives.
You will not be able to meet the objectives of this or any following project by copying and pasting someone else’s work.
You are not allowed to publish any content of this project.
Any form of plagiarism is strictly forbidden and will result in removal from the program.
Requirements
General
Allowed editors: vi, vim, emacs
All your scripts will be tested on Ubuntu 20.04 LTS
All your scripts should be exactly two lines long ($ wc -l file should print 2)
All your files should end with a new line (why?)
The first line of all your files should be exactly #!/bin/bash
A README.md file at the root of the repo, containing a description of the repository
A README.md file, at the root of the folder of this project, describing what each script is doing
You are not allowed to use backticks, &&, || or ;
All your scripts must be executable. To make your file executable, use the chmod command: chmod u+x file. Later, we’ll learn more about how to utilize this command.
More Info
Example of line count and first line

julien@ubuntu:/tmp$ wc -l 12-file_type 
2 12-file_type
julien@ubuntu:/tmp$ head -n 1 12-file_type 
#!/bin/bash
julien@ubuntu:/tmp$ 
In order to test your scripts, you will need to use this command: chmod u+x file. We will see later what does chmod mean and do, but you can have a look at man chmod if you are curious.

Example

julien@ubuntu:/tmp$ ls
12-file_type
lll
julien@ubuntu:/tmp$ ls -la lll
-rw-rw-r-- 1 julien julien 15 Sep 19 21:05 lll
julien@ubuntu:/tmp$ cat lll
#!/bin/bash
ls
julien@ubuntu:/tmp$ ls -l lll
-rw-rw-r-- 1 julien julien 15 Sep 19 21:05 lll
julien@ubuntu:/tmp$ chmod u+x lll # you do not have to understand this yet
julien@ubuntu:/tmp$ ls -l lll
-rwxrw-r-- 1 julien julien 15 Sep 19 21:05 lll
julien@ubuntu:/tmp$ ./lll
12-file_type
lll
julien@ubuntu:/tmp$ 
Quiz questions
Great! You've completed the quiz successfully! Keep going! (Show quiz)
Tasks
0. Where am I?
mandatory
Write a script that prints the absolute path name of the current working directory.

Example:

$ ./0-current_working_directory
/root/alx-system_engineering-devops/0x00-shell_basics
$
Repo:

GitHub repository: alx-system_engineering-devops
Directory: 0x00-shell_basics
File: 0-current_working_directory
   
1. What’s in there?
mandatory
Display the contents list of your current directory.

Example:

$ ./1-listit
Applications    Documents   Dropbox Movies Pictures
Desktop Downloads   Library Music Public
$
Repo:

GitHub repository: alx-system_engineering-devops
Directory: 0x00-shell_basics
File: 1-listit
   
2. There is no place like home
mandatory
Write a script that changes the working directory to the user’s home directory.

You are not allowed to use any shell variables
julien@ubuntu:/tmp$ pwd
/tmp
julien@ubuntu:/tmp$ echo $HOME
/home/julien
julien@ubuntu:/tmp$ source ./2-bring_me_home
julien@ubuntu:~$ pwd
/home/julien
julien@ubuntu:~$ 
Repo:

GitHub repository: alx-system_engineering-devops
Directory: 0x00-shell_basics
File: 2-bring_me_home
   
3. The long format
mandatory
Display current directory contents in a long format

Example:

$ ./3-listfiles
total 32
-rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:19 0-current_working_directory
-rwxr-xr-x@ 1 sylvain staff 19 Jan 25 00:23 1-listit
-rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:29 2-bring_me_home
-rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:39 3-listfiles
$
Repo:

GitHub repository: alx-system_engineering-devops
Directory: 0x00-shell_basics
File: 3-listfiles
   
4. Hidden files
mandatory
Display current directory contents, including hidden files (starting with .). Use the long format.

Example:

$ ./4-listmorefiles
total 32
drwxr-xr-x@ 6 sylvain staff 204 Jan 25 00:29 .
drwxr-xr-x@ 43 sylvain staff 1462 Jan 25 00:19 ..
-rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:19 0-current_working_directory
-rwxr-xr-x@ 1 sylvain staff 19 Jan 25 00:23 1-listit
-rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:29 2-bring_me_home
-rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:39 3-listfiles
-rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:41 4-listmorefiles
$
Repo:

GitHub repository: alx-system_engineering-devops
Directory: 0x00-shell_basics
File: 4-listmorefiles
   
5. I love numbers