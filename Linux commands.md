
Linux commands



### **Basic Commands**

- `pwd` – Print the current working directory
- `ls` – List files and directories
- `cd [directory]` – Change directory
- `mkdir [directory]` – Create a new directory
- `rm [file]` – Remove a file
- `rm -r [directory]` – Remove a directory and its contents
- `cp [source] [destination]` – Copy files or directories
- `mv [source] [destination]` – Move or rename files or directories

### **File Operations**

- `touch [file]` – Create an empty file
- `cat [file]` – View the contents of a file
- `nano [file]` – Open a file in the Nano text editor
- `vim [file]` – Open a file in Vim editor
- `head -n [number] [file]` – Show the first _n_ lines of a file
- `tail -n [number] [file]` – Show the last _n_ lines of a file

### **Permissions and Ownership**

- `chmod [mode] [file]` – Change file permissions (e.g., `chmod 755 script.sh`)
- `chown [user]:[group] [file]` – Change file ownership

### **Process Management**

- `ps aux` – Show running processes
- `top` – Show system resource usage
- `kill [PID]` – Terminate a process by its PID
- `pkill [name]` – Kill processes by name
- `htop` – Interactive process viewer (requires installation)

### **Networking**

- `ping [host]` – Check network connectivity
- `curl [URL]` – Fetch data from a URL
- `wget [URL]` – Download a file from a URL
- `netstat -tulnp` – Show active network connections
- `ip a` – Show IP addresses

### **Disk and System Information**

- `df -h` – Show disk space usage
- `du -sh [directory]` – Show size of a directory
- `free -h` – Show memory usage
- `uname -a` – Show system information
- `uptime` – Show system uptime

### **User Management**

- `whoami` – Show current user
- `who` – Show logged-in users
- `adduser [username]` – Create a new user
- `passwd [username]` – Change a user’s password
- `su [user]` – Switch to another user
- `sudo [command]` – Execute a command as root

### **Package Management**

#### **Debian/Ubuntu**

- `apt update` – Update package lists
- `apt upgrade` – Upgrade installed packages
- `apt install [package]` – Install a package
- `apt remove [package]` – Remove a package

#### **RHEL/CentOS**

- `yum update` – Update packages
- `yum install [package]` – Install a package
- `yum remove [package]` – Remove a package

#### **Arch Linux**

- `pacman -Syu` – Update the system
- `pacman -S [package]` – Install a package

## **Sudo Commands**

Sudo (Superuser Do) allows a permitted user to execute commands as the root user or another user, ensuring system security and control.

- `sudo apt update` – Update package lists (Debian/Ubuntu)
    
- `sudo apt upgrade` – Upgrade installed packages
    
- `sudo apt install [package]` – Install a package (Debian/Ubuntu)
    
- `sudo apt remove [package]` – Remove a package (Debian/Ubuntu)
    
- `sudo yum update` – Update packages (RHEL/CentOS)
    
- `sudo yum install [package]` – Install a package (RHEL/CentOS)
    
- `sudo yum remove [package]` – Remove a package (RHEL/CentOS)
    
- `sudo pacman -Syu` – Update the system (Arch Linux)
    
- `sudo pacman -S [package]` – Install a package (Arch Linux)
    
- `sudo systemctl restart [service]` – Restart a system service
    
- `sudo systemctl status [service]` – Check the status of a system service
    
- `sudo systemctl enable [service]` – Enable a service to start on boot
    
- `sudo systemctl disable [service]` – Disable a service from starting on boot
    
- `sudo reboot` – Reboot the system
    
- `sudo shutdown -h now` – Shut down the system immediately
    
- `sudo visudo` – Edit the sudoers file











### **Archiving and Compression**

- `tar -cvf archive.tar [files]` – Create a tar archive
- `tar -xvf archive.tar` – Extract a tar archive
- `gzip [file]` – Compress a file with gzip
- `gunzip [file.gz]` – Decompress a gzip file
- `zip -r archive.zip [directory]` – Create a zip archive
- `unzip archive.zip` – Extract a zip archive