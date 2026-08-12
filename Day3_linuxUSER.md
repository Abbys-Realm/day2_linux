## Kali Linux
- Uses the desktop environment: *GNOME*
- Previously knows as : ****Backtrack Linux****
### Kali Linux Tool Categories
- It provides us with various tools for system testing and multiple other purposes.
- Basic 15 categories:
1. **Information Gathering**
    - Tools that exists for information gathering in systems, network and hosts.
    - **Example**: **maltego**, **recon-ng**, netdiscover, ***nmap***, legion
2. **Vulnerability Analysis**
    - Tools to find vulnerability in systems and networks.
    - **Example**: Legion, Lynis, ***Nikto***, **Nmap**
3. **Web Applications Analysis** 
     - Tools to find vulnerability and exploitation on web apps.
     - **Example**: **sqlmap**, webscarap, commix, Paros, skipfish
4. **Database Assessments**
     - Tools to find vulnerabilities and exploitation on Databases.
     - **Example**: JSQL injection, ***sqlmap***, mdb-sql, os-scanner
5. **Password Attacks**
    - For exploiting password for login, websites, applications, windows
    - The tools will help to crack the password, They'll check all possible password for the user , if they found they'll return the password.
    - **Example**: **Hashcat**, ***wordlists**, ophcrack, medusa
6. **Wireless Attack**
     - For exploiting wireless systems like WIFI and Bluetooth
     - **Example**:
7. **Reverse Engineering**
     - To exploit any software, mobile application and any binary files
     - They'll trace an already made system to it's original code and they check for any vulenrabilities.
     - **Example**: ***Apktool***, **ghidra**, NASM shell, clang
8. **Exploitation Tools**
     - Exploit software, mobiles, computers, websites and any systems.
     - **Example**: Metasploit, SQLmap, termineter
9. **Sniffing and Spoofing**
     -  Tools for listening and hijacking networks
     - **Example**: ***Wireshark***, hamster, driftnet, macchanger
10. **Post Exploitation**
     - For maintaining our access
     - Used after exploiting a system
	- **Example**: backdoor, exe2hex, powerspoilt
11. **Forensics/Digital Forensics**
     - For doing researches and investigating a cyber attacks
     - **Example**: **hashdeep**, foremost
12. **Reporting Tools **
     - Tools for report preparation after some forensic research and assessment of attacks, it has to be reported back
     - **Example**: cutycapt, maltego,**recordmydesktop**
13. **Social Engineering tools**
     - These tools target a specific person or organization
     - Aka fooling
     - **Example**: maltego, backdoor, socialengineering
14. **System Service**
     - A tool that run automatically/manually on the background
     - You wont be able to see the program running because they run on the background
     - There are some buttons to start the service
     - **Example**: Beef start, beef stop, dradis start, dradis stop
15. **Usually used application**
     - Software for basic purposes
     - There're multiple categories
         - Graphics, Internet, Office, Programming, Sound & Video ...etc


Kali Linux also provide us with:
  - *Workspace Manager*: which allows you to work on multiple tabs, it can hold up to 4 workspaces
  - *Desktop Properties*: differ from desktop environment to environment. (same as windows)
  - *Folder Manager*: Major 3 kinds: Dolphin(gnome, KDEplasma) , Thunar(ubuntu), Nautilus
      - Windows also have different file explorers but they arent free.
  - *Shell*: it communicate with kernel and used to write codes.
      - Terminal/shell have 5 parts
         - *Username*: your username
         - *Hostname*
         - *Current Directory*: the file path you're in
         - *Privilege*: 
            - **$(user)**: limited privilege, access and power
            - **#(root)**: This user can do anything. all privilege, access and power
         - Command Place: **__**   to write a command
      - Directories:
         -  Home directory: **~**
         - Local directory: **.**
         - All directory: *****
## Linux Commands
- Over 1000 commands
- Commands have their own *options* and *arguments*.
   -  **Options**: additional settings that the commands take.
         - usually written **--** or **-**
  - **Arguments**: inputs to pass for the commands
### Commands
1. ***ls(List directory)***: to list folder and information about the files in the folder(current directory by default)
     - Syntax:**ls (options) (files)**
     - Options:
        - **-l** : list each files with additional information
        - **-a** : list hidden files
	         - Unhidden files: no signs/symbols infront of filename
	         - Hidden files: . filename
        - **filename**: to list for a specific folders
        - **-R**: recursive, it will check every file in every folder, sub folders included
        - **-la/ -al**: to list every files even the hidden ones in detail 
2. ***tree*** : to list information about the files and folders with tree structure (current directory by default)
    - Syntax:**tree (folder)**
3. ***cd (change directory)***: to change currently working directory
     - Syntax:**cd (directory)**
     - Options: 
         - **cd**: user's home directory
         - **cd /** : the root/main directory
         - **cd ..** : 1 times back 
         - **cd ../..** : 2 times back
         - **cd "foldername"** : to change to a specific folder
4. ***pwd / print working directory*** : prints the path of our working directory, it starts from the root.
     - Syntax: **pwd (options)**
     - *Description*:
        - -L / --logical : 
5. ***echo***: used to display line of text/string that are passed as an argument
    - Syntax: **echo (string)** /use double or single quote
    - Useful for **Output redirecting**: writing output of any commands into files(if file doesn't exist it'll create one by itself) . Most of commands in Linux has an output except cd and some commands.
        - **echo "string" > file.txt** or **command output > file.txt**
            - Create a new file, add the string text and save
            - If file exits, it'll erase the current content of the file and save the new command output.
        - **echo "string" >> file.txt** or **command output >> file.txt**
             - File has to exit in order to append the string
             - If file doesn't exist, it will create the file and append
 6. ***cat/head/tail/less***
     - **cat** : display *all the contents* that exist inside a file
         - display *on the command line*/ terminal
         - *syntax*: **cat (file)**
         - option: **cat (file) -n**:- show how many line that exist on the file
    - **less**:  display *all the contents* of the tile like cat but
         - Doesn't display it on the command line
         - used *its own command line based text editor*
         - to get out of the command line : press Q
         - *syntax*: **less (file)**
    - **head**: display the *top 10 lines* of the file
        - display on the command line/ terminal
        - *syntax*: **head (file)**
    - **tail**:  display the *bottom 10 lines* of the file
        - display on the command line/ terminal
        - *syntax*: **tail (file)**
7. **touch**: create a file without no content inside it
    - **touch (file1) (file2) (file3)**
    - Can create one or multiple files
    - **touch "file 1" or touch 'file 2'** : To create a file that contains a space
8. ***mkdir / make directory*** : to create a new folder
    - A folder with a name separated with a blank space: use double/ single quotation
    - **mkdir (folder1) (folder2) (folder3)** : for multiple individual folders
    - For a main folder and sub folders: mkdir -p folder1(main)/folder2(sub)/folder3(sub-sub)
9. ***Clear***: to clear any logs from the terminal
    - Alternative options: ctrl+ l (but it wouldn't delete/erase it , it would push it to above)
10. ***rm /remove*** : to remove file
     -  **rm (file) / rm (file1) (file2) (file3)**
     - options
        - **-r** (recursive) : delete recursively. if a folder exist with subfolder and some file it will delete all of them recursively
        - **-i** (for prompt) : it'll prompt u to make sure if you want to delete the file/folder or not (yes or no question)
        - **-f** (force delete): happens with in a folder.
        -  **-rf** : recursive force delete
11. ***cp | mv copy/move***:  to copy and move files
     - syntax: 
        -  **cp (oldFilePlace)(newFilePlace)**
        -  **mv (oldFilePlace)(newFilePlace)**
        - If files are in different path
           - **cp/mv (oldFilePath) (newFilePath)**
        - To copy folders: -r (recursive)
            - **cp/mv -r (folder1) (folder2)**
            - **cp/mv -r (oldFolderPath) (newFolderPath)**
12. ***grep (global search  for regular expression and print out)***
     - Search a file for a specific pattern or chars, and display the lines that contains that pattern
     - Pattern that is searched in the file: regular expression
     - Syntax:**grep (options) "pattern" (file)**
     - options
        - **-i** : case sensitive, filter out the capitial and small words
        - **-c** : count number of lines that the pattern exists
        - **-ic** : count number of lines which are case sensitive
        - **-l "pattern"** * : find that pattern with in the home dir 
        - **-r "pattern" foldername** : recurse the folder to find the specified pattern
        -  **-v** : remove the line that the pattern was found
        - **-n** : return the line where the pattern was found
        - **-o** : display the specific pattern only not the associated line
        - **-a** : search through any binary, json and config files for the pattern
13. ***wc / word count***
     - To find out number of lines, word count, byte and char count in the file specified in the file arguments.
     - Syntax: **wc (options) (File)**
     - options
         - **-l**(line) - how many lines in the file
         - **-w**(word) -  how many word in the file
         - **-c**(byte) -  how many byte in the file
## Multiple Command Execution
- To run/ execute multiple commands in in 1 line
- 3 methods
     - **AND (&&)** : all commands will be executed if all the commands are valid
     - **OR ( || )**:  commands will be executed, if either of the commands are valid or not. If either one of the commands are valid, they will be executed.
         - If the first command works it'll be executed but the second wont be executed regardless of validity (vise versa)
     - **PIPEING ( | )** : Run commands by using the output of the first command as the input for the second command
1. ***sed / Stream editor***
    - Powerful command line too for parsing and transforming text
    - Process files line by line
    - Efficient for large test processing task
    - Main uses: 
        - Text substitution/Replacement
        - Deleting/Selecting specific text
        - Text manipulation for tasks like network information gathering and pentesting
    - Syntax : sed (options) 'command' file
    - Substitution (can use / or | )
        -  **sed 'S/oldWord/newWord'** - for one word
        -  **sed 'S/oldWord/newWord/g'**- for more than  one word or all word that is specified 
    - Delete :  **sed '/pattern/d' file**- delete the line with specified pattern
2. ***awk***
    - Versatile command line text processing tool
    - For pattern scanning and data extraction
    - Named after creators : **A**ho, **W**einberger, **K**ernighan
    - Features
        - Process text line by line
        - Complex pattern matching
        - Field based text manipulation (great for column based data like CSV files)
    - Syntax
        - **awk 'pattern {action}' file.txt**
        - **awk '{print $1, $2}' file.txt** - print column 1 and 2
        - **awk '/pattern/ {print $0}' file.txt** - print lines that matches the pattern
    - By default awk determines columns if they are separated. the space knows as delimiter.
        - Changing delimiter: **' -F "sign" '**
    - Built in variables: 
        - **$0**: Entire line of the text
        - ** $1,$2**: each column in a line
        - **$NR** : record number, display a random row from each  column 
        - **NF** :Number of fields in the last record/column

   

   
    