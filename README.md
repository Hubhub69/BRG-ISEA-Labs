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
  

## Screenshots(s)
- Installed Ubuntu on VirtualBox
![UbuntuTerminal](https://github.com/Hubhub69/BRG-ISEA-Labs/blob/main/UbuntuTerminal.png?raw=true)
- Ran basic Linux commands (`pwd`, `ls`, `mkdir`, `touch`, `man ls`)  
![Terminal Commands](https://github.com/Hubhub69/BRG-ISEA-Labs/blob/main/CommandPage-1a.png?raw=true)
- Viewed manual page for `man ls`  
![Manual Page](https://raw.githubusercontent.com/Hubhub69/BRG-ISEA-Labs/68d06047023fd133715ecc8c983257cd46b2fd3a/ManualPage.png)
- Explored root directory structure (/etc, /home, /var)
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

*Explored Linux services**
  - Listed all services:
    ```bash
    systemctl list-units --type=service
    ```
  - Checked status of `cron` service:
    ```bash
    sudo systemctl status cron
    ```
  - Started and stopped `cron`:
    ```bash
    sudo systemctl stop cron
    sudo systemctl start cron
    ```

- **Worked with file and directory permissions**
  - Viewed permissions:
    ```bash
    ls -l
    ```
  - Changed file permissions:
    ```bash
    chmod 755 testfile.txt
    ```
  - Viewed updated permissions:
    ```bash
    ls -l testfile.txt
    ```
  - Changed file ownership:
    ```bash
    sudo chown vboxuser:vboxuser testfile.txt
    ```

- **Searching the filesystem**
  - Found file by name:
    ```bash
    find /home/vboxuser -name "testfile.txt"
    ```
  - Searched text inside files (limit to your folder to avoid tons of matches):
    ```bash
    grep -r "hello" /home/vboxuser/testfolder
    ```
### Screenshot(s)
- Listed all services
![Service List](https://github.com/Hubhub69/BRG-ISEA-Labs/blob/main/list-units.png?raw=true)
- Checked status of cron (running)
![Cron Running](https://github.com/Hubhub69/BRG-ISEA-Labs/blob/main/status%20cron%20active.png?raw=true)
- Stopped cron (inactive) 
![Cron Stopped](https://github.com/Hubhub69/BRG-ISEA-Labs/blob/main/status%20cron%20inactive.png?raw=true)
- Restarted cron (running again)  
![Cron Restarted](https://github.com/Hubhub69/BRG-ISEA-Labs/blob/main/status%20cron%20Restarted.png?raw=true)
---
### 2. Linux Permissions
- Permissions before 
![Permissions Before](https://github.com/Hubhub69/BRG-ISEA-Labs/blob/main/chomd%20before.png?raw=true)
- Permissions After
![Permissions After](https://github.com/Hubhub69/BRG-ISEA-Labs/blob/main/chomd%20after.png?raw=true)
-  Changed file ownership 
![Changed Ownership](https://github.com/Hubhub69/BRG-ISEA-Labs/blob/main/sudo%20chown.png?raw=true)
---
### 3. Searching Filesystem
- Verified file contents with `cat` 
![File Content](https://github.com/Hubhub69/BRG-ISEA-Labs/blob/main/cat.png?raw=true)
- Found file with `find` 
![File Search - Find](https://github.com/Hubhub69/BRG-ISEA-Labs/blob/main/find.png?raw=true)
- Searched text with `grep` 
![File Search - grep](https://github.com/Hubhub69/BRG-ISEA-Labs/blob/main/grep.png?raw=true)
