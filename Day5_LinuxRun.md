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
## Linux File Permission
- Every file on linux have their own owner and permission
- To *know the owner and permission*: **ls -l**
    -  There'll be 5 main parts on the listing: *Permission, Owners, Date, Size and Filename*
### Ownership
- Owner of the file
- 2 kinds: *User, Group*
- To *change the owner* of file: **sudo chown user: group** filename. (*chown: change ownership*)
### Permission
-  3 types of permission. 
    - **Read(r)** : to read the content of files and files of folders
    - **Write(w)** : to add and remove contents from file/folder
    - **Execute(x)** : permission to run files. example: java file, JavaScript file
- The permission syntax has *3 parts(user-group-other)*
- Total syntax is 9 chars: *the first 3- user, the second- group, the third- other*
- Folders and files differ with **'d'(Folders)** and **'-'(Files)** on the beginning of the permission
#### To whom is the permission is given? 
- **User(u)** : power of user defined on the ownership
- **Group(g)**: power of user defined on the ownership
- **Other(o)** : power of other users
- **All(a)**: power of all(user, group and others)
- Command to *change permission*: **chmod (option) fileName**
- CHMOD command
    - helps to change files permission
    - each permission have a number representations
        - **Read: 4-r**
        - **Write: 2-w**
        - **Execute: 1-x**
     - Syntax: **chmod (parameter) filename**
     - The parameter can be represented in *numbers* and *symbols*
        1. **Symbol**:
            - *chmod a+x filename*, adding execute permission for all
            - *chmod a+x filename*, adding execute permission for users
            - *chmod -x filename*, removing execute permission for all
            - *chmod a+rwx,u-rw,g-x,o-xw filename*, gives rwx for all and removes some permission from all
        2. **Number**:
	        - To give permission *we add the numerical value of the permission*
	        - *chmod 621 filename*, 6 for user, 2 for group, 1 for other 
#### Special file permission
- 3 special file permission
1. **SUID bits(s)**: *set user id bits*
    - This permission is only given by one user
    - Wklna in another word
    - Add 4 Infront of our numeric value (eg:4000)
2. **SGID bits()**: *set group id bits*
    - Focuses on group ownership
    - Add 2 Infront of our numeric value(eg: 2777)
3. **Sticky bits(t)**- *set other id bits*
     - Add 1 Infront of our numeric values (eg: 1602)
     - Execute and read only, less power than SGID and SUID
 - These permissions are like execute(x), but they will *set the execute permission under the user who settled them*, without any sudo command
## Package installation on Linux
- To install software : **package manager (apt, pacman,pkg)**
- On Debian distro package manager: *APT and another one called dpkg.*
- **Package Managers**: free software UI that work with an online server to handle the installation and removal of software on Debian and other Debian based distro.
- When one package is installed, solely the package wont be installed associated package dependencies and package metadata will be installed as well.
- **Package Dependencies(Modules)**: additional files that helps the main software to be functional.
- **Package Metadata**: more data about the package installed
- **Repository**: site/server kali use to upload the packages
    - to access the repository, use internet
### Advanced package tool /apt
- free software user interface that work with an online server to handle installation and removal of software on Debian
    - Work *online(for installation)* and *offline(for removal) *purpose
    - previously used as 'apt-get'
    - Syntax: 
        - **sudo apt update** : inform if there's any update regrading software that's been installed using apt to update
        - **sudo apt search (software)** : check the software in the repo and inform if it exists or not
        - **sudo apt install (software)** : check the software in the repo then install it
        - **sudo apt remove (software)** : remove the software package only
        - **sudo apt upgrade**: similar with update, but instead of just informing it will update it automatically
        - **sudo apt purge (software)**: similar as remove, this removes the package and its dependencies and metadata
- *Package dependencies*: software can be build base on another program (modules)
    - A program to be functional, dependencies have to be installed successfully
#### Common Linux Repository Errors
1. **Could not get lock - /var/lib/apt/lists/lock**
    - Occurs when *2 different apt's run* or if there is *another apt process running on the background*.
    - **Solutions**: *restarting PC, closing the another apt process*
2. **Could not open lock - /var/lib/dpkg/lock- frontend**
    - Occurs when you *forget to run apt with sudo*
3. **Unable to locate package**
    - Occurs when *misspelling the program name*
4. **The repository "kali repo" doesn't have a release file**
    - Occur when there's a *problem on repository configuration*. Sometimes *link might be broken or updated*
    - Check **/etc/apt/sources.list**
- No closing apt while installation
- Repository errors if it happens fix it using: ***sudo apt edit-sources***
### dpkg/ Debian package manager
- Offline package managing program. For installation (online)
- The package should contain .deb to be installed
- Packages on Debian have an extension ".deb"
- Syntax
   - **sudo dpkg -i (packageName)** : *Installing*
   - **sudo dpkg -r (packageName)** : *Removing (only package)*
   - **sudo dpkg -p (packageName)** : *Purge (package + dependency + metadata)*
### Flatpak
- For all linux distro
- *Universal software packaging and distribution system* for linux desktop applications
- Simplify process of developing, *distributing an installing applications across various linux distros*
- ***How to use flatpak***
    -  *Install flatpak* : **sudo apt install flatpak**
    - *Install an application* : **flatpak install flathub applicationName**
    - *Run an application*: **flatpak run applicationName**
    - *Search for applications*: **flatpak search applicationName**
    - *Uninstall an application* : **flatpak uninstall applicationName**
    - *Update all flatpak applications*: **flatpak update**
    - *List installed flatpak apps*: **flatpak list**
    - *Check if flatpak is working*: **flatpak --version**