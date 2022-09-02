1. TO CHANGE USER
- Create user using the useradd command:
su useradd betty
- Change the user by simply calling the username: su betty

2. TO KNOW THE PRESENT USER
- Simply invoke the whoami command: whoami

3. TO KNOW THE GROUPS
groups

4. TO CHANGE FILE OWNER
chown <username> <filename>
chown betty hello

5. TO CREATE AN EMPTY FILE
touch <filename>

6. COMMAND FOR MULTIPLE PERMISSIONS
chmod 114 hello
chmod u+x,g+x,o+r hello

7. EXECUTION PERMISSION FOR EVERYBODY
chmod 111 hello
chmod ugo+x hello

8. -rwxr-x-wx
(rwx=7; r-x=5; -wx=3)
chmod 753 hello

9. CREATE MIRROR PERMISSIONS
COMMAND: chmod --reference=<ref_file> <mirror_file>
chmod --reference=hello olleh #this works
chmod --reference olleh hello #this is what alx wants

10. PERMISSION FOR DIRECTORIES
#Create a script that adds execute permission to all subdirectories of the current directory
# for the owner, the group owner and all other users. Regular files should not be changed.
chmod -R a+X ./

11. CREATE DIRECTORY WITH PERMISSIONS
mkdir -m <permission> <dir_name>
mkdir -m 751 my_dir

12. CHANGE GROUP OWNERSHIP
#Create the group
groupadd <group_name>
groupadd school

#change group owner of the file
chgrp school hello
