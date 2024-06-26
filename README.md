# Mastering DevOps
[![Outlook](https://img.shields.io/badge/Outlook-0078D4?style=for-the-badge&logo=microsoft-outlook&logoColor=white)](mailto:engzaman2020@outlook.com) [![LinkedIn](https://img.shields.io/badge/linkedin-%230077B5.svg?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/ahmad-awsaf-uz-zaman/)


## Table of Contents
- [DevOps Roadmap](#devops-roadmap)
- [Bash Cheatsheet](#bash-cheatsheet)
- [Linux Cheatsheet](#linux-cheatsheet)
- [OpenSSH Cheatsheet](#openssh-cheatsheet)


## ℹ️ DevOps Roadmap

![DevOps Roadmap](https://github.com/awsaf-utm/public-resources/blob/main/DevOps-Roadmap.png?raw=true)

## ℹ️ Bash Cheatsheet

The shell prompt can change to indicate whether the current user has administrative (root) privileges or not.

### Standard User Prompt ($)
When you are logged in as a regular user, the shell prompt typically ends with a dollar sign ($). This signifies that you do not have administrative privileges and your commands are executed with normal user permissions.

``` bash
user@hostname:~$
```

### Root User Prompt (#)
When you are logged in as the root user or have elevated your privileges using a command like sudo -i or su, the shell prompt changes to a hash or pound sign (#). This indicates that you have administrative privileges and can execute commands with full system access.

``` bash
root@hostname:~#
```

### File and Directory Management
1. **ls - List directory contents.**
```bash
ls  # Lists files and directories in the current directory
ls -l  # Lists files and directories with detailed information
ls -a  # Lists all files, including hidden files
```
2. **cd - Change directory.**
```bash
cd /home/user/Documents  # Change to the specified directory
cd ..  # Move up one directory level
cd ~  # Move to the home directory
```
3. **pwd - Print working directory. Shows the current directory path.**
```bash
pwd  # Shows the current directory path
```
4. **mkdir - Make directories.**
```bash
mkdir new_folder  # Create a new directory
mkdir -p parent_folder/child_folder  # Create nested directories
```
5. **rmdir - Remove empty directories.**
```bash
rmdir empty_folder  # Remove an empty directory
```
6. **rm - Remove files or directories.**
 - rm file_name - Remove a file.
```bash
rm unwanted_file.txt  # Remove a file
rm -r old_directory  # Remove a directory and its contents recursively
rm -f file_to_force_delete.txt  # Force remove a file without confirmation
```
7. **cp - Copy files or directories.**
```bash
cp source_file.txt destination_file.txt  # Copy a file
cp -r source_directory destination_directory  # Copy a directory and its contents
```
8. **mv - Move or rename files or directories.**
```bash
mv old_name.txt new_name.txt  # Rename a file
mv file.txt /new/location/  # Move a file to a new location
```
9. **touch - Create an empty file or update the timestamp of an existing file.**
```bash
touch newfile.txt  # Create a new empty file
```
### File Viewing and Editing
10.	**cat - Concatenate and display file content.**
```bash
cat example.txt  # Display the content of a file
```
11. **more / less - View file content page by page.**
```bash
more large_file.txt  # View file content with pagination
less large_file.txt  # Similar to more, but with more capabilities
```
12.	**head - Output the first part of files.**
```bash
head example.txt  # Display the first 10 lines of a file
head -n 5 example.txt  # Display the first 5 lines of a file
```
13.	**tail - Output the last part of files.**
```bash
tail example.txt  # Display the last 10 lines of a file
tail -n 5 example.txt  # Display the last 5 lines of a file
tail -f log.txt  # Follow the content of a log file in real-time
```
14.	**nano / vim / emacs - Text editors.**
```bash
nano file.txt  # Edit a file with Nano
vim file.txt  # Edit a file with Vim
emacs file.txt  # Edit a file with Emacs
```
### File Permissions
15.	**chmod - Change file mode (permissions).**
```bash
chmod 755 script.sh  # Change permissions of a file to rwxr-xr-x
```
16.	**chown - Change file owner and group.**
```bash
chown user:group file.txt  # Change the owner and group of a file
```
### System Information
17.	**uname - Print system information.**
```bash
chown user:group file.txt  # Change the owner and group of a file
```
18.	**df - Report file system disk space usage.**
```bash
df -h  # Human-readable disk space usage
```
19.	**du - Estimate file space usage.**
```bash
du -sh /home/user/Documents  # Display the size of a directory
```
20.	**top / htop - Display Linux tasks.**
```bash
top  # Display tasks with CPU usage
htop  # Enhanced version of top (if installed)
```
21.	**ps - Report a snapshot of current processes.**
```bash
ps aux  # Detailed view of all running processes
```
22.	**free - Display memory usage.**
```bash
free -h  # Human-readable memory usage
```
### Networking
23.	**ping - Send ICMP ECHO_REQUEST to network hosts.**
```bash
ping google.com  # Ping a host
```
24.	**ifconfig / ip - Configure network interfaces.**
```bash
ifconfig  # Display network interface configuration (older systems)
ip addr  # Display IP addresses and interfaces (newer systems)
```
25.	**netstat - Print network connections, routing tables, interface statistics, masquerade connections, and multicast memberships.**
```bash
netstat -tuln  # Display listening ports
```
26.	**ssh - OpenSSH SSH client (remote login program).**
```bash
ssh user@host  # Connect to a remote host via SSH
```
### Searching and Sorting
27.	**grep - Print lines that match patterns.**
```bash
grep 'pattern' file.txt  # Search for a pattern in a file
grep -r 'pattern' /path/to/search  # Recursively search for a pattern in a directory
```
28.	**find - Search for files in a directory hierarchy.**
```bash
find /path -name file.txt  # Find a file by name
find /path -type d -name 'dir_name'  # Find a directory by name
```
29.	**sort - Sort lines of text files.**
```bash
sort file.txt  # Sort the contents of a file
```
30.	**wc - Print newline, word, and byte counts for each file.**
```bash
wc file.txt  # Count lines, words, and bytes in a file
wc -l file.txt  # Count lines in a file
```
### Archiving and Compression
31.	**tar - Store, list, or extract files in an archive.**
```bash
tar -cvf archive.tar directory_name  # Create a tar archive
tar -xvf archive.tar  # Extract a tar archive
tar -czvf archive.tar.gz directory_name  # Create a gzip-compressed tar archive
tar -xzvf archive.tar.gz  # Extract a gzip-compressed tar archive
```
32.	**gzip / gunzip - Compress or expand files.**
```bash
gzip file.txt  # Compress a file
gunzip file.txt.gz  # Decompress a file
```
33.	**zip / unzip - Package and compress (archive) files.**
```bash
zip archive.zip file.txt  # Create a zip archive
unzip archive.zip  # Extract a zip archive
```
### Miscellaneous
34.	**echo - Display a line of text.**
```bash
echo "Hello, World!"  # Print text to the terminal
```
35.	**date - Display or set the system date and time.**
```bash
date  # Show the current date and time
date "+%Y-%m-%d %H:%M:%S"  # Show date and time in a specific format
```
36.	**whoami - Print the current user ID.**
```bash
whoami  # Display the current user
```
37.	**sudo - Execute a command as another user.**
```bash
sudo apt-get update  # Run a command with superuser privileges
```
38.	**history - Show the command history.**
```bash
history  # Display the command history list
```
39.	**alias - Create an alias for a command.**
```bash
alias ll='ls -l'  # Create a shortcut for a command
alias grep='grep --color=auto'  # Enhance grep with color output
```
40.	**man - An interface to the system reference manuals.**
```bash
man ls  # Display the manual for the ls command
```

## ℹ️ Linux Cheatsheet

### System Management
1.	**systemctl - Manage systemd services**
bash
```bash
systemctl start service_name  # Start a service
systemctl stop service_name  # Stop a service
systemctl restart service_name  # Restart a service
systemctl status service_name  # Check the status of a service
systemctl enable service_name  # Enable a service to start on boot
systemctl disable service_name  # Disable a service from starting on boot
```
2.	**journalctl - View logs from systemd**
bash
```bash
journalctl -u service_name  # View logs for a specific service
journalctl -xe  # View the end of the log file with detailed information
```
3.	**kill - Terminate a process by ID**
bash
```bash
kill process_id  # Send a termination signal to a process
kill -9 process_id  # Forcefully terminate a process
```
4.	**pkill - Terminate processes by name**
bash
```bash
pkill process_name  # Terminate processes by name
pkill -9 process_name  # Forcefully terminate processes by name
```
5.	**crontab - Schedule periodic tasks**
bash
```bash
crontab -e  # Edit the current user's crontab
crontab -l  # List the current user's crontab entries
crontab -r  # Remove the current user's crontab
```
### User Management
6.	**useradd - Create a new user**
bash
```bash
sudo useradd username  # Create a new user
sudo useradd -m username  # Create a new user with a home directory
sudo userdel username  # Delete a user
```
7.	**passwd - Change user passwords**
bash
```bash
passwd  # Change the password for the current user
sudo passwd username  # Change the password for a specific user
```
8.	**usermod - Modify a user account**
bash
```bash
sudo usermod -aG groupname username  # Add a user to a group
sudo usermod -L username  # Lock a user account
sudo usermod -U username  # Unlock a user account
```
9.	**groupadd - Create a new group**
bash
```bash
sudo groupadd groupname  # Create a new group
sudo groupdel groupname  # Delete a group
```
### Disk Management
10.	**fdisk - Partition a disk**
bash
```bash
sudo fdisk /dev/sdX  # Partition a disk (replace X with the appropriate letter)
```
11.	**mkfs - Build a Linux file system**
bash
```bash
sudo mkfs.ext4 /dev/sdX1  # Create an ext4 file system on the specified partition
```
12.	**mount - Mount a file system**
bash
```bash
sudo mount /dev/sdX1 /mnt  # Mount a partition to a directory
sudo umount /mnt  # Unmount the file system from the directory
```
13.	**fsck - File system consistency check and repair**
bash
```bash
sudo fsck /dev/sdX1  # Check and repair a file system
```
### Package Management
14.	**apt - Package handling utility for Debian-based distributions (like Ubuntu)**
bash
```bash
sudo apt update  # Update package index
sudo apt upgrade  # Upgrade all installed packages
sudo apt install package_name  # Install a new package
sudo apt remove package_name  # Remove an installed package
sudo apt autoremove  # Remove unnecessary packages
```
15.	**yum - Package manager for RPM-based distributions (like CentOS)**
bash
```bash
sudo yum update  # Update all packages
sudo yum install package_name  # Install a new package
sudo yum remove package_name  # Remove an installed package
```
16.	**dnf - Next-generation package manager for RPM-based distributions (like Fedora) **
bash
```bash
sudo dnf update  # Update all packages
sudo dnf install package_name  # Install a new package
sudo dnf remove package_name  # Remove an installed package
```
### System Monitoring
17.	**iostat - Report CPU and I/O statistics**
bash
```bash
iostat  # Display CPU and I/O statistics
```
18.	**vmstat - Report virtual memory statistics**
bash
```bash
vmstat  # Display virtual memory statistics
```
19.	**iotop - Display I/O usage by processes**
bash
```bash
sudo iotop  # Display I/O usage by processes
```
20.	**lsof - List open files**
bash
```bash
lsof  # List all open files
lsof -i :8080  # List open files on a specific port
```
### Miscellaneous
21.	**wget - Non-interactive network downloader**
bash
```bash
wget http://example.com/file.txt  # Download a file from the web
```
22.	**curl - Transfer data from or to a server**
bash
```bash
curl http://example.com  # Fetch the content of a URL
curl -O http://example.com/file.txt  # Download a file from the web
```
23.	**scp - Secure copy (remote file copy program)**
bash
```bash
scp file.txt user@remote_host:/path/to/destination  # Copy a file to a remote host
scp user@remote_host:/path/to/file.txt /local/path  # Copy a file from a remote host
```
24.	**rsync - Remote file and directory synchronization**
bash
```bash
rsync -avz /local/dir/ user@remote_host:/remote/dir/  # Synchronize directories
```
25.	**htop - Interactive process viewer**
bash
```bash
htop  # Display interactive process viewer
```


## ℹ️ OpenSSH Cheatsheet

![OpenSSH Cheatsheet](https://github.com/awsaf-utm/public-resources/blob/main/OpenSSH-Cheatsheet.png?raw=true)

### *Checking if OpenSSH Client is Installed*
### On Windows
1. **Using Command Prompt or PowerShell**
 - Open Command Prompt or PowerShell.
 - Type the following command and press Enter:
```powershell
ssh –V
```
- If OpenSSH client is installed, you will see the version information. If not, you will receive an error indicating that the command is not recognized.
2. **Installing OpenSSH Client on Windows 10/11**
 - Open Settings.
 - Go to Apps > Optional features.
 - Scroll down and look for OpenSSH Client. If it is not installed, click on Add a feature.
 - Find OpenSSH Client in the list, check it, and click Install.
3. **Verifying Installation**
 - Open Command Prompt or PowerShell again and run:
```powershell
ssh –V
```
 - The OpenSSH client version information should now be seen.

### On Linux
1. **Using the Terminal**
 - Open a terminal window.
 - Type the following command and press Enter:
```bash
ssh –V
```
 - If OpenSSH client is installed, you will see the version information. If not, you will need to install it using the package manager for your Linux distribution.
2.	**Installing OpenSSH Client on Different Distributions**
 - Ubuntu/Debian:
```bash
sudo apt update
sudo apt install openssh-client
```
 - CentOS/RHEL:
```bash
sudo yum install openssh-clients
```
 - Fedora:
```bash
sudo dnf install openssh-clients
```
3.	**Verifying Installation**
- Open a terminal window and run:
```bash
ssh –V
```
 - The OpenSSH client version information should now be seen.

### *Check if OpenSSH Server is Installed and Running*

### On Linux Server
1. **Check if OpenSSH Server is Installed**
- Run the following command to check if the sshd service (OpenSSH daemon) is installed:
```bash
sshd –V # OpenSSH daemon
```
- If sshd is not found, it means the OpenSSH server is not installed. You can install it using the package manager for your distribution.
### On Ubuntu/Debian:
```bash
sudo apt update
sudo apt install openssh-server
```
### On CentOS/RHEL
```bash
sudo yum install openssh-server
```
2.	**Check if OpenSSH Server is Running**
- To verify that the OpenSSH server is running, you can check the status of the sshd service:
```bash
sudo systemctl status sshd
```
- If the service is running, you should see output indicating that sshd is active (running). If it is not running, you can start it with:
```bash
sudo systemctl start sshd
```
3.	**Enable OpenSSH Server to Start on Boot**
- To ensure the SSH server starts automatically when the server boots, enable it with:
```bash
sudo systemctl enable sshd
```

### *Steps to Connect to a Remote Server*
1.	**Open Your Terminal**
 - On Linux or macOS, open the terminal application.
 - On Windows, you can use Command Prompt, PowerShell, or a terminal application like Git Bash.
2.	**Use the ssh Command**
 - The basic syntax for connecting to a remote server is:
```bash
ssh username@hostname # example.com
```
Or,
```bash
ssh username@serverhost # subdomain.maindomain.com
```
Or,
```bash
ssh username@ip-address # 192.168.20.5
```
  - Passwordless login syntax:
```bash
ssh -i /path/to/private_key ubuntu@ip_address
```
  
 - Replace username with the username you have on the remote server.
 - Replace hostname or serverhost or ip address with the domain name or IP address of the remote server.
For example:
```bash
ssh ubuntu@192.168.1.10
```
3.	**Accept the Remote Server’s SSH Key**
 - The first time you connect to a new remote server, you’ll see a message like:
```vbnet
The authenticity of host 'hostname (ip)' can't be established.
ECDSA key fingerprint is SHA256:xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx.
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no)?
```
 - Type yes and press Enter. This adds the remote server’s SSH key to your known hosts file.
4.	**Enter Your Password**
 - After accepting the key, you’ll be prompted to enter the password for the user on the remote server.
 - Type the password and press Enter. Note that you won’t see any characters appear as you type the password.
5.	**Successful Connection**
 - If the username and password are correct, you’ll be logged into the remote server, and you’ll see the remote server’s command prompt.
Additional Options
 - Specify a Port: If the SSH server is running on a non-standard port (other than 22), you can specify the port number using the -p option:
```bash
ssh -p 2222 user@hostname_or_ip
```
 - Use an SSH Key for Authentication: If you’re using SSH key-based authentication, you can specify the private key file with the -i option:
bash
ssh -i /path/to/private_key user@hostname_or_ip
 - Verbose Output: For troubleshooting connection issues, you can enable verbose output by adding the -v option:
```bash
ssh -v user@hostname_or_ip
```
Example Commands
 - Basic Connection:
```bash
ssh user@example.com
```
 - Connection with a Non-Standard Port:
```bash
ssh -p 2222 user@example.com
```
 - Connection Using an SSH Key:
```bash
ssh -i ~/.ssh/id_rsa user@example.com
```
 - Following these steps will allow you to connect to a remote server using OpenSSH.

