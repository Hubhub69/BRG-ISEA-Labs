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
  
---
## Screenshots(s)
- Installed Ubuntu on VirtualBox
![UbuntuTerminal](https://github.com/Hubhub69/BRG-ISEA-Labs/blob/main/UbuntuTerminal.png?raw=true)
- Ran basic Linux commands (`pwd`, `ls`, `mkdir`, `touch`, `man ls`)  
![Terminal Commands](https://github.com/Hubhub69/BRG-ISEA-Labs/blob/main/CommandPage-1a.png?raw=true)
- Viewed manual page for `man ls`  
![Manual Page](https://raw.githubusercontent.com/Hubhub69/BRG-ISEA-Labs/68d06047023fd133715ecc8c983257cd46b2fd3a/ManualPage.png)
- Explored root directory structure (/etc, /home, /var)
![Root Directory](https://github.com/Hubhub69/BRG-ISEA-Labs/blob/main/root%20directory%20(1).png?raw=true)
---
## Challenges for Session 1a
- Windows Smart App Control blocked the Ubuntu ISO multiple times.
- Troubleshooting wasted around 4–5 hours.
- Solved the issue after searching on Google and watching YouTube tutorials.
- Learned patience and the importance of using community resources.
- Misconfigured VM resources (too little RAM/CPU), installation was very slow until adjusted.
- Type 'is' instead of 'ls', learned to be careful with spelling.
- Did not know how to exit 'man' pages, later learned to press 'q'.
  ---
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
 ---
### Screenshot(s)
- Listed all services
![Service List](https://github.com/Hubhub69/BRG-ISEA-Labs/blob/main/list-units.png?raw=true)
- Checked status of cron (running)
![Cron Running](https://github.com/Hubhub69/BRG-ISEA-Labs/blob/main/status%20cron%20active.png?raw=true)
- Stopped cron (inactive) 
![Cron Stopped](https://github.com/Hubhub69/BRG-ISEA-Labs/blob/main/status%20cron%20inactive.png?raw=true)
-Restarted cron (running again)  
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

## Challenges for Session 1b
- Initially confused between `chmod` and `chown`, took time to understand the difference between changing permissions vs. changing ownership.  
- Accidentally typed `ls -1` (number one) instead of `ls -l` (lowercase L), which only listed files without showing permissions. Learned to carefully check the command.  
- `grep -r` returned too many results when searching the entire `/home` directory. Solved by limiting the search to `/home/vboxuser/testfolder`.  
- Forgot that `sudo` requires the user's password. Took a few tries to realize it was the login password for `vboxuser`.  
- After reboot, the test file seemed to be missing because I was in the wrong directory. Learned to always check with `pwd` and `ls` to confirm file location.
  
---
## Session 2a - Total Cost of OwnerShip(TCO)
Compared **On-Premise** vs **AWS EC2 (Cloud)** infrastructure costs.
- Considered:
  - Hardware (servers, storage, networking)
  - Software/Licensing
  - Electricity & Cooling
  - Staff/Admin costs
- Documented monthly and yearly costs in Excel/Google Sheets.
- Projected 3-year TCO (On-Prem vs AWS).
- Calculated **ROI** and **Break-even point**.



## Screenshot(s)
TCO Cost Table
![Cost Table](https://github.com/Hubhub69/BRG-ISEA-Labs/blob/main/TCO%20table.png?raw=true)
TCO 3- Years Comparison Chart
![Comparison Chart](https://github.com/Hubhub69/BRG-ISEA-Labs/blob/main/TCO%20chart.png?raw=true)
---
### ROI
Year 1: (11,200 − 2,800) ÷ 11,200 = **75%**
- Year 2: (22,400 − 5,600) ÷ 22,400 = **75%**
- Year 3: (33,600 − 8,400) ÷ 33,600 = **75%**
- ROI is consistent across all years because both On-Prem and AWS costs grow linearly.

**Break-even Point:**
- Break-even (months) = Upfront On-Prem Hardware ÷ (On-Prem Monthly − AWS Monthly)

= 5,000 ÷ (934 − 233)

= 5,000 ÷ 701

≈ **7 months**
---
### Challenges for Session 2a
- Had difficulty deciding which cost items to include (hardware, software, staff vs hidden cloud costs like bandwidth or support).  
- Initially forgot to calculate **monthly costs** → corrected by dividing yearly values by 12. 
- First Excel formulas were wrong (totals did not update automatically) → fixed with `=SUM()` functions.  
- Chart design was confusing at first (too many details) → simplified to a clear 3-year bar chart.  
- ROI formula was easy, but understanding **Break-even logic** was tricky → solved by applying the correct formula using upfront cost ÷ monthly savings.  
---
## Session 2b – Cloud Services - AWS EC2 Lab

## 1. Create Free Tier Account
- Registered an AWS Free Tier account.  
- Accessed the AWS Management Console.
  
  -AWS Console Home (showing EC2 service)
  ![AWS Console Home](https://github.com/Hubhub69/BRG-ISEA-Labs/blob/main/AWS%20Console%20home.png?raw=true)

  ---
## 2. Launch Ubuntu Instance
- Launched an EC2 instance using **Ubuntu Server 22.04 LTS**.  
- Instance type: **t3.micro (Free Tier)**.  
- Region: **ap-southeast-2 (Sydney)**.  
- Instance ID: `i-03419803d6fc2b148`  
- Instance state: **Running**
  
  - EC2 Instance list (showing Running status)
    ![EC2 Instance](https://github.com/Hubhub69/BRG-ISEA-Labs/blob/main/EC2%20Instance.png?raw=true)

  -  Instance Summary page (showing Public IP, Instance State, Instance type)
    ![Instance Summary](https://github.com/Hubhub69/BRG-ISEA-Labs/blob/main/Instance%20summary%20page.png?raw=true)

---
## 3. Configure Security and SSH Key Pair
- Created SSH key pair and downloaded `isea-key.pem`.  
- Configured Security Group inbound rules:  
  - Allowed **SSH (Port 22, TCP)** from Anywhere (0.0.0.0/0).

    - Key pair file (`isea-key.pem`) saved on local machine
      ![Key pair file](https://github.com/Hubhub69/BRG-ISEA-Labs/blob/main/.pem%20file.png?raw=true)

      - Security Group inbound rule (showing Port 22 open)
      ![Port 22](https://github.com/Hubhub69/BRG-ISEA-Labs/blob/main/SSH%20port%2022,%20tcp.png?raw=true)
---
## 4. Connect to VM Using SSH
- Changed key permissions:
  ```bash
  chmod 400 /path/to/isea-key.pem
  
 - Connected to EC2 instance with:
     ```bash
     ssh -i /path/to/isea-key.pem ubuntu@<Public-IP>

  - Example:
     ```bash
     ssh -i /media/sf_isea-key/isea-key.pem ubuntu@54.66.169.204

- Successful SSH login (showing ubuntu@ip-... prompt)
  ![SSH](https://github.com/Hubhub69/BRG-ISEA-Labs/blob/main/connect%20to%20VM%20using%20SSH.png?raw=true)

  ---
### **Step 5 – Update OS Packages**
- Ran update and upgrade commands:
  ```bash
  sudo apt update && sudo apt upgrade -y

- Update OS Packages
  ![OS package](https://github.com/Hubhub69/BRG-ISEA-Labs/blob/main/Update%20OS%20package.png?raw=true)

- kernel upgrade notice
  ![Kernel Upgrade](https://github.com/Hubhub69/BRG-ISEA-Labs/blob/main/kernel1.png?raw=true)

  ---
## Challenges for Launch and Configure EC2 instance

 **Key Pair Access Issues**  
  - Initially had difficulty finding the `.pem` key file inside the Ubuntu VM.  
  - Solved this by locating the correct shared folder path (`/media/sf_isea-key/isea-key.pem`).

 **File Permission Error**  
  - Encountered “unprotected private key file” error.  
  - Fixed it by running `chmod 400` to restrict file permissions.

   **SSH Connection Errors**  
  - Faced repeated “No such file or directory” and “Permission denied (publickey)” errors.  
  - Learned that correct path formatting and file permissions are critical for SSH login.
    
**System Update Reboot Notice**  
  - During `sudo apt update && sudo apt upgrade`, the system requested a reboot to apply a new kernel.  
  - Restarted the instance and reconnected via SSH to verify the updated kernel.

**Time Consuming Setup**  
  - The whole process of troubleshooting SSH and permissions took several attempts, wasting extra time.  
  - Learned patience and attention to detail in handling Linux commands and AWS settings.

    ---
## Session 2b – Bash Scripting

## 1. Objectives
- Create a Bash script file (`script.sh`) with the shebang line `#!/bin/bash`.  
- Demonstrate the use of:
  - `echo`  
  - `if` statement  
  - `for` loop  
  - `while` loop  
  - cron example (as a comment/echo line)  
- Run the script using:
  - `bash script.sh`  
  - `chmod +x script.sh && ./script.sh`

 ----
 ## 2. Create the Script
- Used `nano` to create and edit `script.sh`.  
- Added the required code with `echo`, `if`, `for`, `while`, and cron example.  

- Script code inside `nano`:
![Script Code](![Uploading image.png…](https://github.com/Hubhub69/BRG-ISEA-Labs/blob/main/script%20code.png?raw=true)

--- 
## 3. Run Script with Bash
- Executed the script directly with `bash script.sh`.  
- Verified output showed:
  - Script header and timestamp  
  - `if` condition result (`The passwd file exists.`)  
  - `for` loop numbers (1–3)  
  - `while` loop counters (1–3)  
  - Example cron line

   - Terminal output (`bash script.sh`):
     ![Bash 1](https://github.com/Hubhub69/BRG-ISEA-Labs/blob/main/bash%20script.sh%201.png?raw=true)
     ![Bash 2](https://github.com/Hubhub69/BRG-ISEA-Labs/blob/main/bash%20script.sh%202.png?raw=true)
     ![Bash run](https://github.com/Hubhub69/BRG-ISEA-Labs/blob/main/run%20bash.png?raw=true)

     ---
 ## 4. Make Script Executable
- Added execute permissions with `chmod +x script.sh`.  
- Confirmed permissions via `ls -l script.sh` (showing `-rwxr-xr-x`).  
- Ran script with `./script.sh`, same output as before.  

- File permissions and executable run:
  ![Executable Run](https://github.com/Hubhub69/BRG-ISEA-Labs/blob/main/executable%20run.png?raw=true)

  ## 5. Challenges for bash scripting

- Needed to type the script line by line in `nano`, which was slow and increased the chance of typos.  
- Initially wrote `!/bin/bash` instead of `#!/bin/bash`, causing the script not to run.  
- Mistyped the `if` condition without spaces (`if[-f /etc/passwd];`), fixed it to `if [ -f /etc/passwd ]; then`.  
- Could not run `./script.sh` at first because of missing permissions, solved with `chmod +x script.sh`.  
- Unsure about the cron requirement; decided to include a cron example line inside the script instead of setting up a real cron job.  


    ---

## Session 3a - DNS and Certificates 
# Objective 
The purpose of this lab is to configure and test DNS using a free cloud DNS provider. I registered a free domain, created an A record that points to my server’s public IP, and verified DNS propagation using Linux CLI tools.
---

## 1. Register a Domain
- Registered free DNS domain using Dynu.
- Domain name: jameson06.ddnsfree.com
  ![DNS](https://github.com/Hubhub69/BRG-ISEA-Labs/blob/main/DNS.png?raw=true)

## 2. Configure A Record
- Created an A record pointing the domain to my server’s public IP address:
  ![A Record Configuration](https://github.com/Hubhub69/BRG-ISEA-Labs/blob/main/Configuration.png?raw=true)

## 3. Verify DNS Propagation
- Verified using the following commands on Ubuntu:
- nslookup jameson06.ddnsfree.com
- dig jameson06.ddnsfree.com
- ping -c 4 jameson06.ddnsfree.com
---
# Using nslookup
- The result showed that the domain successfully resolved to the correct public IP 45.195.233.213.
 ![nslookup](https://github.com/Hubhub69/BRG-ISEA-Labs/blob/main/nslookup.png?raw=true)
---
# Using dig
- dig jameson06.ddnsfree.com
- The domain resolved to the same IP 45.195.233.213, confirming that the DNS record was published globally.
![Dig](https://github.com/Hubhub69/BRG-ISEA-Labs/blob/main/Dig.png?raw=true)
---
# Using Ping 
- ping -c 4 jameson06.ddnsfree.com
- The ping command successfully resolved the domain to 45.195.233.213 and returned responses, verifying connectivity to the server.
![Ping](https://github.com/Hubhub69/BRG-ISEA-Labs/blob/main/Ping.png?raw=true)

## Digital Certificates – Use Let’s Encrypt to Secure a Server
# 1. Install Certbot
- Installed Certbot with Apache plugin:
  
-Updated package index:
- sudo apt update
  ![Apt update](https://github.com/Hubhub69/BRG-ISEA-Labs/blob/main/Apt%20update.png?raw=true)
  
- sudo apt install certbot python3-certbot-apache -y
  

