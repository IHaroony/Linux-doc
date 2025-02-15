
### **1. Understanding File Permissions:**

File permissions control the actions that users can perform on files or directories. These permissions can be set for three types of users:

- **Owner** (u): The user who owns the file or directory.
- **Group** (g): Other users who are in the file's group.
- **Others** (o): Everyone else.

Each file or directory has three basic permissions:

- **Read** (r): Allows viewing the file’s contents.
- **Write** (w): Allows modifying the file.
- **Execute** (x): Allows executing the file (if it’s a script or program).

For directories:

- **Read** (r): Allows listing the contents of the directory.
- **Write** (w): Allows creating, renaming, and deleting files within the directory.
- **Execute** (x): Allows accessing the directory (i.e., to `cd` into it).

### **2. Default Permissions and How They Appear:**

When you list files with `ls -l`, you get a permission string like this:



`-rw-r--r-- 1 user group 1024 Feb 11 10:00 file.txt`

Breaking it down:

- The first character is the type of file (`-` for regular files, `d` for directories).
- The next three characters represent the owner's permissions (`rw-` = read and write).
- The next three characters represent the group’s permissions (`r--` = read-only).
- The final three characters represent others' permissions (`r--` = read-only).

### **3. Using `chmod` Command:**

The `chmod` command is used to modify file or directory permissions.

#### **Syntax:**


`chmod [options] mode file_name`

- **mode**: Specifies the permissions. This can be represented either symbolically (e.g., `rwx`) or numerically (e.g., `777`).
- **file_name**: The name of the file or directory for which you are changing permissions.

#### **4. Symbolic Mode:**

In symbolic mode, you use characters to represent permissions:

- **r** = read
- **w** = write
- **x** = execute
- **u** = user (owner)
- **g** = group
- **o** = others
- **a** = all users (user, group, others)

To modify permissions:

- **+**: Adds the specified permission.
- **-**: Removes the specified permission.
- **=**: Sets the exact permission, removing others.

Examples:

bash

CopyEdit

`chmod u+x file.txt   # Add execute permission to the owner chmod g-w file.txt   # Remove write permission from the group chmod o=r file.txt   # Give read permission only to others chmod a+x file.txt   # Add execute permission to everyone`

#### **5. Numeric (Octal) Mode:**

In numeric mode, each permission is represented by a number:

- **r = 4**
- **w = 2**
- **x = 1**

You sum these values to set permissions:

- **7** = read (4) + write (2) + execute (1)
- **6** = read (4) + write (2)
- **5** = read (4) + execute (1)
- **4** = read (4)
- **3** = write (2) + execute (1)
- **2** = write (2)
- **1** = execute (1)
- **0** = no permissions

Each user class (owner, group, others) has its own value, so a typical `chmod` value like `755` means:

- Owner: `7` (read, write, execute)
- Group: `5` (read, execute)
- Others: `5` (read, execute)

Examples:

bash

CopyEdit

`chmod 755 file.txt   # Owner has full access, group and others have read/execute chmod 644 file.txt   # Owner can read/write, group and others can only read chmod 777 file.txt   # Full access to everyone (read, write, execute) chmod 700 file.txt   # Only the owner has full access, others have no access`

#### **6. Special Permissions:**

There are also special file permissions:

- **Setuid** (`s` on owner’s execute position): When set on an executable file, the program runs with the privileges of the owner. Example:
    
    
    
    `chmod u+s /usr/bin/some_program`
    
- **Setgid** (`s` on group’s execute position): When set on a directory, new files created in the directory will inherit the group of the directory. Example:
    
    
    
    `chmod g+s /my_directory`
    
- **Sticky Bit** (`t` on others’ execute position): Only the file owner can delete files in a directory, even if others have write permissions. Example:
    

    
    `chmod +t /some_directory`
    

### **7. Using `ls` with `-l` to View Permissions:**

You can check the current permissions of files or directories with the `ls -l` command:



`ls -l file.txt`

This will display permissions in the format shown earlier, like:



`-rw-r--r-- 1 user group 1024 Feb 11 10:00 file.txt`

### **8. Recursively Changing Permissions:**

If you want to apply permissions to directories and their contents (including subdirectories), you can use the `-R` (recursive) option:



`chmod -R 755 /my_directory`

This will set the permissions for all files and directories inside `/my_directory` to `755`.

### **Further Reading:**

- The `chmod` manual page:  
    You can access the manual page for `chmod` by running the following command in the terminal:
    
    
    `man chmod`
    

This will provide detailed information on the command and its options.