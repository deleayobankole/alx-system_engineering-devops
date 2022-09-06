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

#6. Create a script that creates a new local variable. Name: BEST Value: School
BEST="School"

#7. Create a script that creates a new global variable.
export BEST="School"

#8. Write a script that prints the result of the addition of 128 with the value stored in the environment variable TRUEKNOWLEDGE, followed by a new line.
echo $(($TRUEKNOWLEDGE + 128))

#9. Write a script that prints the result of POWER divided by DIVIDE, followed by a new line. POWER and DIVIDE are environment variables
echo $(($POWER/$DIVIDE))
