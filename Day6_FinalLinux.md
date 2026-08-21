## Script Installation
- Some hacking tools are developed by peoples and make it open source, that means we can get those scripts/program from GitHub.
- Can be downloaded and used using git clone
- Syntax: git clone (link of the repo)
- The tool requires some scripts and dependencies to be functional, so when git clone all those scripts and dependencies will be cloned with the tool.
- To run executable tool(bash, js, python) : ./fileName
    - If permission denied, use sudo
### Script Modules
- Script: made with scripting languages(programming). (python, ruby,bash,go,....)
- When using these programming languages to do tasks, there is modules/libraries that are needed to run the scripts as dependencies.
- There's a different way to install dependencies based on what languages were used. if its bash, there's no module
- Most tools are developed using python or go
- Example: 
    - Python: to install modules we use - pip install (moduleName)
         - For requirements file: pip install -r requirements.txt
         - Tools developed by python, there's a requirement modules defined for them.
         -  
    - GO: go install (moduleName)
    - Ruby: gen install (moduleName)
1. Python Installation
     - With no cloning needed, pip command can be run to install to tools for some tools. 
     - Command: pip install module
     - pip is a pre install tool. If it isn't run the command: pip install term,  if the command doesnt work pip install term --break-system-packages
     - If package is already installed, Command: pip install -r requirements.txt. if it doesnt work add --break-system-packages
2. GO installation
    - For GO scripts using go-lang
    - To install go: sudo apt golang-go
    - If a tools is made by a go-lang there'll be a tag at the end of the GitHub repo, @latest
    - If the tag is @latest, use the new version
    - There's 2 versions of installation method
        - Old version: go get (GitHub repo)
            - stored inside a folder /go/bin
        - New version
            - Installation: go install (GitHub repo)
            - To run it as a normal command: sudo mv fileName /usr/bin
- Help on linux commands to know about tools or commands
    1. man(manual) : give the whole manual and instruction of a tool or a command
        - only works for tool that has been installed using APT
        - Syntax: man (yourCommand)
    2. Help
        - As an option
        - List the options about the command that has been used
        - Syntax: 
            - (command) -h
            - (command) -help
            - (command) --help
## Linux Process and Services
- Process: Running instances of programs
     - User permitted tools, run in the process place
     - Manual
     - When executing program like opening a tool, running a command or starting a web all these starts as a Process
- Services: Background programs that starts automatically or manually, often for system tasks(AKA daemons)
    - A service that runs to gather any change(stop and start) on the system or to count time that the service runs on background
- To get process running: ps (options)
- More options
    - ps : for processes running on the shell
    - ps -A : view all running process
    - ps -u username : view users process
### Managing Processes
- To manage any process 
- To stop process:
    - kill (option) (PID) - PID is a process ID, helps to identify process
    - killall (program)
- Kill options
    - -19 : to stop process
    - -18: to resume the process we stopped
    - -9: stops process immediately
- PID(process ID)
- PPID(parent process ID)- A process opened by the parent process
- ps and kill aren't real time command execution, it just shows when they're done
- Top and htop is a real time process managing commands , it shows each step of the process
     - Both are preinstalled
     - top- you can only see the processes
     - htop- you can execute command and see the process simultaneously
         - To kill on htop: search for the process, choose SGNKILL(F9) and kill