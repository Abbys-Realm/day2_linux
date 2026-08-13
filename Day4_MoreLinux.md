## Linux File Hierarchy
- A special file system than windows.
- **File system** : directory structure that the OS uses.
- **System files** : files used by the system software/ OS
- *For windows*: local disk c:
- *For Linux*: root directory (/)
1. **/ (root)**
    - A directory that *stores files for the Linux OS* to operate
    - Every files and directory starts from the root directory
    - Difference between /root and /
        - /root: root of users home directory
        - / : the main directory
    - Only the root user has the right to write under this directory
2. **/bin - Binary Executables**
     - *Essential command binaries* that need to be available to the user
     - Store the command files 
     - If the command doesn't exist in the bin file, it wont let the user/access use it 
     - can be accessed by the normal or root user
     - *Example*:  cd, ls, pwd
3. **/boot - Boot loader files**
    - Files and folders that *helps the Linux OS boot*
    - *Example*: initrd.img-2.6.32-24-generic, vmlinuz-2.6.32-24-gneneric
4. **/dev - Essential device files**
    - *Include terminal devices, USB or any device attached to the system*
    - The  OS is downloaded in the hardware part of the device and the /dev will hold files and folders essential for the parts of the hardware
    - *Example*: /dev/tty1 , /dev/usbmon0
5. **/etc - et cetera**
    - *Contains configuration files* required by all programs
    - It might be programs, software, these have associated configuration file that helps them to work. 
    - *Example*: /etc/resolv.conf , /etc/hosts , /etc/passwd , /etc/shadow
    - Also contains startup and shutdown shell scripts used to start/stop individual programs. 
6. **/home - Home Directory**
     - For *all users to store personal files*
     - *Example*: /home/user1 , /home/user2
     - user1 and user2 cant access each other files, unless they know the login of the users. (security)
     - ~ = /home/user1 : where user1 is the user you logged in with
7. **/lib - Libraries essential for the binaries in  /bin and /sbin (system binary)**
    - Hold the libraries *file/folders of an installed command/ existing command* 
    - Library filenames : ld* or lib*.so.*
    - *Example*: ld-2.11.1.so , libncurses.so.5.7
8. **/media - Mount points for removable media such as CD-ROMs**
    - *Files from the removable devices* will be stored inside /media 
    - *Example* : /media/cdrom - CD-ROM , /media/floppy - Floppy disk
9. **/mnt - Temporary mounted files**
    - To *store a temporary file/folder*, create it inside /mnt
    - They only exist when the device is on, when it restart they will be erased
    - Only *accessible by the root user* /system admins
10. **/opt - Optional Application Software Packages**
    - For personal use
    - *Contains add-ons applications from the user*
    - Application should be installed under either /opt/ or /opt/sub-dir
11. **/sbin - System Binary**
    - *Contain binary executable* 
    - Linux commands store under this directory are *used by the root user only* , for system maintenance purpose
12. **/tmp - Temporary Files**
     - Same as /mnt
     - *Accessible both for the normal or root user*
     - Files under this directory are *deleted when system is rebooted*
13. **/usr - User Utilities**
    - *Contains binaries, libraries, documents and source-code for second level programs.*
    - A secondary device can access files/folders that is stored inside your device
    - */usr/bin* : binary files for user programs
    - */usr/sbin* : binary files for system admins
    - */usr/lib* : contains libraries for /usr/bin and /usr/sbin
    - */usr/src* : Linux kernel sources, header-files and documentations
## Text Editors
- Programs used for text processing
- Linux Command line text editors : VIM, nano, emacs, neovim
- Linux Graphical text editors : *Sublime, VSCODE, gedit, pluma*
1. ***VIM***
    - primarily *VI* used on UNIX - It was a line editor, user was able to see/edit only one line of text at a time
    - Improved and developed for Linux : VIM  (VI iMproved)
    - VIM editor 
        - Very powerful editor
        - Complex/cryptic
        - Hard to learn (for window users)
	    - **4 modes**: *Command, Visual, Input, Normal*
    - To open : **vim filename** (if file exist, it will open it without eliminating its content. it the file doesn't exist, it create a new one)
    - By default : open in Normal mode
    - **Normal mode**: only seeing is allowed
    - **Insert mode**: ***press i***
         - To edit texts(add / delete)
    - **Command mode**: ***press esc***
        - Allowed: *save (:w)* , *quit (:q)* ,  *save & quit (:wq!)* , *force quit & save(! - force)* , *undo(:u)* , *execute bash commands( :%1bashcommand action)*
    - **Visual mode**: select and manipulate block of text
        - *Character wise*: select text character by character, drag your cursor along the line you want and select
            - **command mode + press v**
        - *Line wise*: select entire lines of text regardless of block / space
            - **command mode + press shift+v**
        - *Block wise*: select rectangular block of text , consider a rectangle like shape 
            - **command mode + press ctrl+v or  ctrl+q**
        - Commands in visual mode:
           - **press d**: to delete a selected text
           - **press y**: copy the selected text
           - **press p**: paste the selected text after the cursor
2. ***NANO***
    - User- friendly, free and open source text editor
    - Pre-installed when installing Linux
    - Starting nano : nano filename (if file doesn't exist, it'll create a new one. if it does, it will open it)
    - No modes
    - Asterix on the above, shows that there's new thing that's added which hasn't been saved
    - Shortcuts
        - **save**: ctrl +s
        - **undo** : alt+u
        - **redo**: alter
        - **exit**: ctrl+t
        - **command execute**: ctrl+t then add your command
        - **select**: use your cursor/ shift+arrow
    - Paste and copy all over Linux is
        - **copy**: alt+6 
        - **cut**: cltr+k  
        - **paste**:ctrl+u 
    - Append feature only exist in nano, to append:
        - **ctrl + r ** ->** insert the filename or its path
## Linux user management
- Person who uses the computer : **user**
- Every users have a group of their own (visible on linux )
- Groups are useful because you can add many users to the group, when a user is created an associated group will be created for it as well
- If username is User1, the group will be named after the user which is User1. For file sharing , you can add other users to the User1.
- Users have their own file and applications
- To know our user name(linux) : "**whoami**"
- Users have power/priviledge
- Any user on linux have their *own identifier number*(ID)
- Two kinds of user
    - **root**: by default installed when you install linux
        - Have *all the power to do everything*, *can access everything*
        - Only one root admin in the OS
        - **ID: 0**(always), doesnt increment or change
    - **normal**: the *first created user* on linux
        - *less power than root*, only access their own personal file
        - **ID: 1-999**
        - For the first ever created normal users:  ID= 100, continue until 1999. The normal user and the thousandth (2000) or 1999th user doesnt have the same power
- ***Sudo*** *(super user do)*: if normal users want to have a root access.
    - The normal user can have all the power as the root
    - **sudo yourCommand**
    - Pass the permission denying
#### Creating Users
- Two ways
    - **useradd** - simple to create user, wont ask for password
        - Syntax : *sudo useradd username*
        - Shell: *sh*
    - **adduser** - detailed information required
        - Syntax: *sudo adduser username*
        - Shell: *bash*
    - *Both commands exist in sbin* 
    - User files are stores inside **/etc/passwd**, the folder will store the created username, id, path, shell and when it created except its password
    - **/etc/skel** : have all *the essential files to be a user* when creating a new user
    - **/etc/shadow** : *store user's password encrypted*, and other sensitive files. Accessible by the root user
    - To check id for the logged in username : id command
#### To access root user
- *Command* : **sudo su**
- To change a shell that your in: */bin/theShellYouWant*
- To go put of the root user, command : **exit**