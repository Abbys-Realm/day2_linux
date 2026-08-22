## Script Installation
- Some *hacking tools are developed by peoples and make it open source*, that means we can get those scripts/program from GitHub.
- Can be downloaded and used using git clone
- *Syntax*: **git clone (link of the repo)**
- The **tool requires some scripts and dependencies to be functional,** so when git clone all those scripts and dependencies will be cloned together with the tool.
- To *run executable tool*(bash, JavaScript, python) : ***./fileName***
    - If permission denied, use *sudo*
### Script Modules
- **Script**: *made with scripting languages*(programming). (python, ruby,bash,go,....)
- When using these programming languages to do tasks, there is modules/libraries that are needed to run the scripts as dependencies.
- There's a *different way to install dependencies based on what languages were used*. if its *bash*, there's **no module**
- Most tools are developed using python or go
- Example: 
    - **Python**: to install modules we use - **pip install (moduleName)**
         - For *requirements* file: **pip install -r requirements.txt**
         - Tools developed by python, there's a requirement modules defined for them.
    - **GO**: **go install (moduleName)**
    - **Ruby**: **gem install (moduleName)**
1. ***Python Installation***
     - With no cloning needed, pip command can be run to install to tools for some tools. 
     - Command: **pip install module**
     - pip is a pre install tool. If it isn't run the command: pip install term,  if the command doesnt work *pip install term **--break-system-packages***
     - If package is already installed, Command: pip install -r requirements.txt. if it doesnt work add --break-system-packages
2. ***GO installation***
    - For GO scripts using go-lang
    - To install go: **sudo apt golang-go**
    - If a tools is made by a go-lang there'll be a tag at the end of the GitHub repo, @latest
    - If the tag is @latest, use the new version
    - There's 2 versions of installation method
        - **Old version**: *go get (GitHub repo)*
            - stored inside a folder */go/bin*
        - **New version**
            - Installation: *go install (GitHub repo)*
            - To run it as a normal command: *sudo mv fileName /usr/bin*
- Help on linux commands to know about tools or commands
    1. ***man(manual)*** : give the *whole manual and instruction of a tool or a command*
        - only *works for tool that has been installed using APT*
        - Syntax: **man (yourCommand)**
    2. ***Help***
        - As an option
        - *List the options about the command that has been used*
        - Syntax: 
            - **(command) -h**
            - **(command) -help**
            - **(command) --help**
## Linux Process and Services
- **Process**: *Running instances of programs*
     - User permitted tools, run in the process place
     - *Manual*
     - When executing program like opening a tool, running a command or starting a web all these starts as a Process
- **Services**: *Background programs that starts automatically or manually*, often for system tasks(AKA daemons)
    - A service that runs to gather any change(stop and start) on the system or to count time that the service runs on background
- To get process running: **ps (options)**
- More options
    - **ps** : for *processes running on the shell*
    - **ps -A** : view *all running process*
    - **ps -u username** : view *users process*
### Managing Processes
- To *manage any process*
- To stop process:
    - **kill (option) (PID)** - PID is a process ID, helps to identify process
    - **killall (program)**
- Kill options
    - **-19** : to stop process
    - **-18**: to resume the process we stopped
    - **-9**: stops process immediately
- PID(process ID)
- **PPID**(parent process ID)- A *process opened by the parent process*
- ps and kill *aren't real time command execution*, it just shows when they're done
- Top and htop is a *real time process managing commands* , it shows each step of the process
     - Both are preinstalled
     - **top**- you can *only see the processes*
     - **htop**- you can *execute command and see the process simultaneously*
         - To kill on htop: search for the process, choose *SGNKILL(F9) and kill*
### Foreground and Background
- **Foreground**: a commands that *run the prompts and complete them right there on the terminal*
    - We'll see it happening in the terminal
- **Background** : commands that will *run at the background,* we can't see them running
- *Foreground -> background*
    - **&** : append at the end of the command
    - **ctrl + z**
- *Background -> foreground*
    - **fg** on the terminal
- To *stop ongoing process* inside terminal - **ctrl +c**
- To know *processes running* on the background : **ps**
### Managing Services
- **Services can be stopped and started**.
- Programs that's running under services can't be visible, but for manually started services statuses can be changed.
- 2 commands to manage services
    - ***systemctl*** - **Commonly used**
        - **sudo systemctl start (serviceName)** : *temporarily starts the service* but it will terminate when the PC restarts / boots.
        - **sudo systemctl stop (serviceName)** : *temporarily stops the service* but it will terminate when the PC restarts / boots.
        - **sudo systemctl status (serviceName)** : *checking the status(stop/start) of a service.*
        - **sudo systemctl enable (serviceName)** : *permanent start*, even when PC boots up it'll stay enabled.
        - **sudo systemctl disable (serviceName)** : *permanent stop*, even when PC boots up it'll stay disabled.
    - **service** 
        - **sudo service start (serviceName)** 
        - **sudo service start (serviceName)**
- A program that runs in the process run in the foreground
- Services run in the background
## Null Device
- **Path : /dev/null**
- *Redirects output nowhere*
- If output has to be ignored, user doesn't want to see error, user doesnt want to a file redirect them to /dev/null.
- Throws away whatever it's being fed
- On shell output there's two things
    - **STDERR** =2
        - To redirect error from command
        - **command 2> filename**
    - **STDOUT** =1
        - To redirect error free output
        - **command 1> filename**
- *cat /dev/null* : prints nothing
## Symbolic Linking
- Work the *same as a shortcut*
- Process of *creating a linked shortcut form of file to some pre-existed file/folder*
- If file path is too long, create a symbolic linking for it
- *Permission part* starts with ***l*** when running ls l command
- Syntax : **ln -s source_filePath fileName**
- Works for *folders and files only*
## Alias
- *Nickname for commands*
- Works **temporarily when the PC is on**, doesn't work after closing a terminal
- For **permanent** : *add to shell config file*
    - Bash: **~/.bashrc**
    - ZSH: **~/.zshrc**
    - Fish: **/.config/fish/config-fish**
- Syntax : **alias nickname= "command"** / **alias nickname= 'command'**
## TMUX - terminal multiplexer
- Helps to ***classify terminal work***
- Already *pre-installed*, but it it's not install sudo apt install tmux
- To Split terminal
    1. Create a config file: *nano .tmux.conf*
    2. Write configuration code
        - unbind
- Without the  configuration file splitting doesn't work
- *Horizontal Split* : **^A then O**
- *Vertical* Split: **^A then E**
- *Exit*: **^A then X / exit**
- *Tab*: **^A then C**
- * Rename tab*: **^A then ,**
- *Switch tab*: **^A then tabNumber**
- *To skip through splitted screen* : **^A then arrow**
- Super key is ^A 
## WGET
- *Tool to download files from websites/ servers*
- Syntax: **wget (link) / wget (options) (link)**
- Offesticate: encrypting codebase of a website
- Deoffesticate: decrypt codebase of a website
## Find
- A terminal *to search for files/folders/music/videos*
- Essential tool
- **Drawback**: *mix the errors with correct output*
- Syntax: **find (searchPath) (Options) (Word)**
- Options
    - find / **-name** "linux" : to search name 
    - find / **-perm** 777 : to search for permission
    - find **-type f** : to search for files
    - find **-type d** : to search for directories
    - find / **-type f -perm 4000** : special file permission