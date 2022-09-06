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

#10. Write a script that displays the result of BREATH to the power LOVE
echo $(($BREATH**$LOVE))

#11. Write a script that converts a number from base 2 to base 10
echo $((2#$BINARY))

#12. Create a script that prints all possible combinations of two letters, except oo.
echo {a..z}{a..z} | tr " " "\n" | grep -v "oo"

#13.Write a script that prints a number with two decimal places, followed by a new line. The number will be stored in the environment variable NUM.
printf "%.2f" $NUM | sort

#14. Write a script that converts a number from base 10 to base 16. The number in base 10 is stored in the environment variable DECIMAL. The script should display the number in base 16, followed by a new line
print '%x\n' $DECIMAL

#15. Write a script that encodes and decodes text using the rot13 encryption. Assume ASCII.
tr `echo {a..z} | tr -d ' '` `echo {n..z} $(echo {a..m}) | tr -d ' '` | tr `echo {A..Z} | tr -d ' '` `echo {N..Z} $(echo {A..M}) | tr -d ' '`

#16. Write a script that prints every other line from the input, starting with the first line.
perl -lne 'print if $. % 2 == 1'

#17. 
