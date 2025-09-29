# BRG-ISEA-Labs
My lab activities and documentation for the ISEA module
 ## Session 1a - Linux Setup
- Created a GitHub account and repository ('BRG-ISEA-Labs') to document lab progress.
- Added 'README,md' to start recording activities, screenshots, and challenges.
- Installed Ubuntu on VirtualBox.
- Created an Ubuntu VM using Ubuntu 22.04 ISO.
  - configured VM settings:
  - Memory: 4096 MB
    - CPU: 4
    - Disk: 20 GB
- Installed Ubuntu successfully and accessed the desktop.
- Practiced basic Linux commands:
  - `pwd` → print working directory
  - `ls` → list files
  - `cd` → change directory
  - `mkdir testfolder` → create folder
  - `touch testfile.txt` → create empty file
- Explored directory structure:
  - `/etc` → system configuration files
  - `/var` → variable data/log files
  - `/home` → user home directories
- Used `man` to explore Linux manual pages (e.g., `man ls`).
  

##Screenshots(s)
![UbuntuTerminal](https://github.com/Hubhub69/BRG-ISEA-Labs/blob/main/UbuntuTerminal.png?raw=true)
![Terminal Commands](https://github.com/Hubhub69/BRG-ISEA-Labs/blob/main/CommandPage-1a.png?raw=true)
![Manual Page](https://raw.githubusercontent.com/Hubhub69/BRG-ISEA-Labs/68d06047023fd133715ecc8c983257cd46b2fd3a/ManualPage.png)
![Root Directory](https://github.com/Hubhub69/BRG-ISEA-Labs/blob/main/root%20directory%20(1).png?raw=true)

## Challenges for Session 1a
- Windows Smart App Control blocked the Ubuntu ISO multiple times.
- Troubleshooting wasted around 4–5 hours.
- Solved the issue after searching on Google and watching YouTube tutorials.
- Learned patience and the importance of using community resources.
- Misconfigured VM resources (too little RAM/CPU), installation was very slow until adjusted.
- Type 'is' instead of 'ls', learned to be careful with spelling.
- Did not know how to exit 'man' pages, later learned to press 'q'.
  
## Session 1b - Exploring Linux

## Activities 
- Explored Linux service:
- Listed all services
- ```bash
    systemctl list-units --type=service
    ```
  - Checked status of `cron` service:
    ```bash
    sudo systemctl status cron
    ```
  - Started and stopped services:
    ```bash
    sudo systemctl stop cron
    sudo systemctl start cron
    ```

- Worked with file and directory permissions:
   - Viewed permission:
     ```bash
     ls -1
    
 - Changed file permissions:
     ```bash
    chmod 755 testfile.txt
    ```
     
  - Changed file ownership:
    ```bash
    sudo chown vboxuser:vboxuser testfile.txt
    ```
    - Searched for text inside files:
    ```bash
    grep -r "hello" /home/vboxuser
    ``
    
