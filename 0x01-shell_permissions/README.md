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


