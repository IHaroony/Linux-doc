

**Documenting Linux User and System Configuration Steps**

### 1. Created a New User

- Opened the terminal.
    
- Ran the following command to create a new user named `naruto`:
    
    ```
    sudo adduser naruto
    ```
    
- Followed the prompts to set up the user details.
    

### 2. Set a Password for the User

- Used the following command to set a password for `naruto`:
    
    ```
    sudo passwd naruto
    ```
    
- Entered the password when prompted (`An***86@`).
    

### 3. Checked and Changed the Hostname

- Viewed the current hostname by running:
    
    ```
    hostname
    ```
    
- Opened the hostname file using nano editor:
    
    ```
    sudo nano /etc/hostname
    ```
    
- Alternatively, changed the hostname directly with the following command:
    
    ```
    sudo hostnamectl set-hostname haroon
    ```
    
- Verified the hostname change:
    
    ```
    hostname
    ```
    

### 4. Navigated to the Documents Folder and Created a New Directory

- Changed the current directory to Documents:
    
    ```
    cd ~/Documents
    ```
    
- Created a new directory named `llinuxxdoc`:
    
    ```
    mkdir llinuxxdoc
    ```
    

### 5. Moved a File to the New Directory

- Used the `mv` command to move a file from another location to `llinuxxdoc`:
    
    ```
    mv /path/to/sourcefile ~/Documents/llinuxxdoc/
    ```
    

You can check the disk usage of your home directory using the following command in the terminal:


`du -sh ~`

### Explanation:

- `du` (disk usage) displays the size of files and directories.
- `-s` (summary) shows only the total size.
- `-h` (human-readable) formats the output in a readable format (e.g., KB, MB, GB).

This will give you the total disk space used by your home directory. Let me know if you need more details!



### Summary

You successfully:

- Created a user `naruto` and set a password.
    
- Viewed and changed the hostname to `haroon`.
    
- Created a new directory `llinuxxdoc` in Documents.
    
- Moved a file to the new directory.
    

This document serves as a record of the steps taken for future reference.