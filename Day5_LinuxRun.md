## Advanced Linux User
### Advanced User Commands
1. **To change password of the user**
    - *Syntax* : **sudo passwd username**
    - This syntax 
        - To add new password for users created by useradd
        - To change password for users created by adduser
2. **To change existing ID or user and group**
    - *For user ID*: **sudo usermod -u newID username**
    - *For group ID*: **sudo groupmod -g newID**
    - Same or different ID can be created for users and groups
 3. **To delete user**
     - *Command*: **sudo userdel -r username**   
     - userdel: user delete
     -  -r : Force delete, because sometimes without -r, the username might not be deleted normally because it might contains folder and files
4. **To login to other user on terminal**
    - Command: **su - username**
    - To go to the normal user: exit
    - Why is user adding important?
        - To do multiple tasks 
        - Reduce work load
5. **To create a folder for a user**
    - Users created by useradd doesn't have their own folder
    - When a user is creates without an existing home directory
    - *Command*: **sudo mkhomedir_helper (username)** 
6. **To change shell**
    - To change the default home shell of a user to their specified shell
    - Note that: In order to change your shell your device must have all the required shell on it
    - *Command*: **sudo usermod (username) -s/bin/(specifiedShell)**
## Advanced Commands
1. **To create a new group** (if not created for a user) - *rare occurrence*
    - *Command*: **sudo groupadd (groupName)**
2. **To add users in a group**
    - *Command*: **sudo usermod -aG (groupName) (userName)**
    - -aG: add group
3. **Verifying the users group membership**
    - *Command*: **groups userName**
4. **Remove a user from a group**
    - *Command*: **sudo gpasswd -d userName groupName**
## Sudoers File
- A file in linux and unix admins that use to *allocate system right to system users*
- User that are created after the normal user, doesnt have the power to use sudo as the normal user. This happens because the new user *are not added in the sudoers file*
- To access this file 
    -  *Command* : **sudo visudo**
    - Only works for the normal user
    - Go to normal user -> run sudo visudo command
