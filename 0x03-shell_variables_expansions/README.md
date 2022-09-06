PROJECT TITLE: 0x03. Shell, Init Files, Variables and Expansions

This README.md file houses all the scripts for the tasks in this project.

#0. Create a script that creates an alias.
#Name: ls
#Value: rm *
alias ls="rm *"

#1. Create a script that prints hello user, where user is the current Linux user.
echo "hello $USER"

#2. Add /action to the PATH. /action should be the last directory the shell looks into when looking for a program.
export PATH=$PATH:/action

#3. Create a script that counts the number of directories in the PATH.
#Got two solutions for this that does the same thing:
echo $(printf $PATH | tr ":" "\n" | wc -w)
echo $((`echo $PATH | grep -o ":/" | wc -l`+ 1))

#4. Create a script that lists environment variables.
printenv

#5. Create a script that lists all local variables and environment variables, and functions.
set

#6.   
