
# Linux Fundamentals Lab: File Management, Permissions, Networking, and System Monitoring

## Overview
This folder contains basic Linux command-line exercises practiced during cybersecurity training.

# OBJECTIVE
Practice essential Linux command-line operations including:
- File creation and management
- Directory navigation
- File permissions
- Network configuration and connectivity testing
- System monitoring

# ENVIRONMENT
- OS: Kali Linux (VMware Virtual Machine)
- Shell: Bash

# 1. FILE CREATION

Created two files for lab exercises using the commands:
touch newfile
touch myfile

# 2. FILE COPYING

Copied contents of 'newfile' into 'myfile' using the command:
cp newfile myfile

# 3. DIRECTORY CREATION

Created a personal working directory for lab files using the command:
mkdir mydirectory

# 4. FILE RENAMING / MOVING

Renamed 'myfile' back to 'newfile' using the command:
mv myfile newfile

# 5. LIST FILES

Verified file existence in current directory using the command:
ls

# 6. FILE DELETION

Removed 'newfile' to practice safe deletion using the commands:
rm newfile
ls

# 7. DIRECTORY NAVIGATION

Navigated into the lab directory using the command:
cd mydirectory

# 8. FILE PERMISSIONS – ADD READ ACCESS

Created a file, granted read permission to others and viewd the permissions using the commands:
touch myfile
chmod o+r myfile
ls -al myfile

# 9. FILE PERMISSIONS – FULL PERMISSION SET
I change the permissions for the owner, group and others to;
- Owner: read, write, execute
- Group: read, write
- Others: no access
	Using the command 'chmod 760 myfile' and viewed permissions using 'ls -al myfile'

# 10. NETWORK CONFIGURATION CHECK

Checked local network interface configuration using the command:
ifconfig

# 11. NETWORK CONNECTIVITY TEST

Tested connectivity to an external domain using the command:
ping ocsaly.com

# 12. SYSTEM MONITORING

Monitored CPU, memory, and running processes using the command:
top

# RESULT

- Successfully managed files and directories
- Configured file permissions using chmod
- Verified network configuration and connectivity
- Observed system performance and running processes
- Demonstrated core Linux skills relevant to cybersecurity roles

# SECURITY NOTE

Sensitive information such as usernames, MAC addresses, and IP details were blurred/omitted in screenshots before uploading to GitHub.

# TOOLS USED

- Kali Linux
- Bash Shell
- Linux Core Utilities

## Learning Outcome
Built confidence navigating Linux systems and performing basic administrative and networking tasks.

