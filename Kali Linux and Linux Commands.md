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
     - Syntax: ls (options) (files)
     - Options:
        - **-l** : list each files with additional information
        - **-a** : list hidden files
	         - Unhidden files: no signs/symbols infront of filename
	         - Hidden files: . filename
        - **filename**: to list for a specific folders
        - **-R**: recursive, it will check every file in every folder, sub folders included
        - **-la/ -al**: to list every files even the hidden ones in detail 
2. ***tree*** : to list information about the files and folders with tree structure (current directory by default)
    - Syntax: tree (folder)
3. ***cd (change directory)***: to change currently working directory
     - Syntax: cd (directory)
     - Options: 
         - **cd**: user's home directory
         - **cd /** : the root/main directory
         - **cd ..** : 1 times back 
         - **cd ../..** : 2 times back
         - **cd "foldername"** : to change to a specific folder