# Introduction to Linux
## Linux
- Not an operating system alone, its a **kernel**.
- What' s a ***kernel***?
    - Its a code/program that used to meet your Software and Hardware together
    - It also allocate some resources.
## History of Linux
- It was created  in 1969, original name was **Unix** 
- It was made by *Ken Thompson* and *Dennis Ritchie*.
- Comparing to the current Linux, Unix had a lot of setbacks.
     1. **Expensive**: To install the OS and use the software that exists people used to pay
     2. **Not open source**: No one can access the source code besides the developers.
- After some few years, **Linus Torvalds** created Linux kernel using C programming language and made it open source.
- But still, Linux alone couldn't be an OS because:
     - one system to be an operating system it must have *kernel* and *software* but Linux only accompany the kernel.
- Richard Stallman announced GNU project in 1983.
    - GNU is a free software replacement to the UNIX OS
- GNU + Linux= GNU Linux OS
## Shell
### What is shell?
- Using shell a user can communicate with a kernel
- It's a CLI that translate commands entered by the user and convert them into a language that's understood by the kernel.
- Types of shell:
    - More than 512 shells based on features
    - Basic 4:
        + SH
        + BASH
        + ZH
        + FISH
    - The above 4 differ in coloring, piping(spaces of tabs where to start typing), command compilation(autofill commands that has been previously written)
## Operating System
- Main software part of computer that helps users to work.
- One system to be an operating system it must have:
    1. **Kernel**
    2. **Software**
    3. **Desktop Environment**: A GUI that provide user to interact with the 
       - For Linux systems there are 4 desktop environments: **Mate, XFCE , KDE plasma, gnome**
       - Desktop Environment picks differ in PC performance
    4. .**File extensions**
    5. **Windows Manager**: manages every action 
       - For Linux: i3 windows manager
    
## Why Linux?
- 4 major benefits of using Linux 
   1. **Fast OS**: compatible for every computer, has no lag
   2. Most used: Almost every system is powered with Linux
   3. Most hacking tools are Linux based
   4. Most secured: unlike windows the  your log stays within your OS
      - No Linux based malware haven't been developed yet, mostly malwares are Microsoft based
## Linux Distributions/ Distro
- **Distro**: modified Linux kernel type of OS with different *Linux kernel, packages(GNU), package manager(OS based SW installer) and Desktop UI*
- Known Linux distros
   1. **Debian**(package manager: apt)
    - kali Linux
    - ubuntu
    - parrot OS
   2. **Arch**(package manager: packman)
     - Black arch
     - Garuda
   3. **Fedora**
   4. **Red Hat**
   5. **Gentoo**
   6. **Android**
- Recommended:
     - *Kali Linux(has every option possible), ubuntu(customizable) , parrot OS, Garuda and Black arch*
1. **Kali Linux**
    - Debian derived Linux distro
    - Mainly designed for digital forensics and penetrating testing
    - **Desktop Environment**: ***XFCE***
    - **Package Manager**: ***apt***
    - **Shell**: ***ZSH***
2. **Parrot OS**
    - Debian based Linux
    - Focus: security, privacy and development
    - Different versions for developers and hackers
    - **Desktop Environment**: ***Mate***
    - **Package Manager**: ***apt***
    - **Shell**: ***bash***
3. **Garuda**
    - Arch based Linux distro
    - .**Desktop Environment**: ***KD plasma***
    - **Package Manager**: ***packman***
    - **Shell**: ***FISH***
4. **Ubuntu**
    - ***Desktop Environment**: ***gnome***
    - **Package Manager**: ***apt***
    - **Shell**: ***bash***

*Windows doesn't have any distros since it isn't open source code, They update it and add features themselves*
## How to use Linux
1. **Main OS/ Main boot**
    - Linux as the main sole OS
    - *Advantage*
         - High performance/ speed
         - Simplicity
         - Secure
    - *Disadvantage*
         - No other access to other OS
         - Data loss on previous OS
2.  **Dual Boot/ 2 in 1**
     - Linux installed alongside with other OS(windows or any other distros)
     - *Advantage*
         - Access to multiple OS
         - Data Preservation
    - *Disadvantage*
         - Complexity
         - Resource Sharing
3. **Live Boot**
    - Accessing the Linux OS via USB/DVD
    - *Advantage*
        - Privacy
        - No risk of data loss
    - *Disadvantage*
         - Resource Sharing
4. **Cloud Terminal**
    - Using website based terminal to use Linux
    - [Webminal](https://www.webminal.org/)
5. **Virtual Machine**
    - Using both the physical and virtual computer together
    - Done by: ***Virtualization***
         - 2 types
         1.***Type 1(Bare metal hypervisor)***
             - The VM directly runs on the physical HW
             - It doesn't require a host OS
             - Hypervisors: VMware esx, proxmox, xen
             - Hypervisors allow computer to have a VM
             - **Advantage**:
                - High performance and efficiency
                - Better resource management and isolation
                - Used in Enterprise Environment for server virtualization
        2. ***Type 2(Hosted Hypervisor)***
            - VM runs directly runs on Host OS
            - It relies on the host OS to manage hardware resources
            - Hypervisors: VMware workstation, oracle VirtualBox
            - **Advantage**
               - Easier setup and use
               - Suitable for Personal or Development environment
6. **WSL V2/ Windows subsystem for Linux**
    - Installing Linux terminal in windows OS(cwd)
7. **Termux/For Android**
    - Used on Phone to install Linux
    - To run codes and for simple things
    - Package manager: pkg
    