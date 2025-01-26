# Robodive

# LinuxLearning

---

## 📂 Project Structure
LinuxLearning/
├── notes/
│   └── todo.txt
├── projects/
│   └── project_list.txt
└── backup/
    └── system_log.txt
    
- **`notes/`**: Contains personal notes related to Linux learning.
  - `todo.txt`: A list of tasks to accomplish while exploring Linux commands.

- **`projects/`**: Contains files related to ongoing and future projects.
  - `project_list.txt`: A list of project ideas and descriptions.

- **`backup/`**: A directory reserved for storing backup-related information.
  - `system_log.txt`: Contains logs about system activities and backup processes.

---

## 📜 File Descriptions

### `notes/todo.txt`
This file contains a to-do list for learning Linux. Here's an example of what it includes:

    Learn basic Linux commands
    Practice creating directories and files
    Explore file permissions


### `projects/project_list.txt`
This file contains a list of projects to work on. For example:

    Build a personal website
    Develop a Python script for automation
    Create a shell script for backups

### `backup/system_log.txt`
This file contains system-related logs for the backup directory. Example:

System log initialized: 2025-01-26 12:00:00 Backup directory created successfully. Scheduled backup at midnight daily.


---

## 🛠️ How to Use

1. **Clone or Create Directory**:
   If you'd like to create the same structure, you can use the following commands:
   ```bash
   mkdir LinuxLearning
   cd LinuxLearning
   mkdir notes projects backup
   touch notes/todo.txt projects/project_list.txt backup/system_log.txt


**🛠️ Part 2: File Manipulation**

This section describes additional operations to manipulate files and directories, using key Linux commands.

**1. Copying a File**

To copy notes/todo.txt to the backup directory:
cp notes/todo.txt backup/

This creates a duplicate of todo.txt in the backup directory while keeping the original file intact in notes.

**2. Renaming a File**

To rename projects/project_list.txt to projects/active_projects.txt:

mv projects/project_list.txt projects/active_projects.txt

The mv command is used here to rename the file.

**3. Moving a File**

To move backup/system_log.txt to the home directory:
mv backup/system_log.txt ~/

The ~ represents the home directory. This moves system_log.txt to the home directory.

**4. Deleting an Empty File**

First, create an empty file (if needed):
touch empty_file.txt

Then, delete it using the rm command:
rm empty_file.txt

The file will be permanently deleted.

📁 **Final Directory Structure**

After completing the above steps, the directory structure will look like this:
LinuxLearning/
├── notes/
│   └── todo.txt
├── projects/
│   └── active_projects.txt
├── backup/
│   └── todo.txt
~/
└── system_log.txt (moved to home directory)

**🔍 Part 3: File Examination**

This section focuses on examining the contents of files and using common Linux commands.

**1. Display File Contents with cat**

To display the contents of a file, use:

cat notes/todo.txt

This command outputs the entire content of the file to the terminal.

**2. Count Words in Files with wc**

To count the number of words, lines, and characters in a file, use:

wc notes/todo.txt

Example output:

3  15  98 notes/todo.txt

3: Number of lines

15: Number of words

98: Number of characters

**3. Search for Specific Text with grep**

To search for a specific word or phrase in a file, use:

grep "Learn" notes/todo.txt

This command searches for the word "Learn" and displays the lines containing it.

Example output:

1. **Learn** basic Linux commands

**4. Sort Contents of a Text File**

To sort the lines in a file alphabetically, use:

sort notes/todo.txt

Example output (if todo.txt contains tasks):

1. Explore file permissions
2. Learn basic Linux commands
3. Practice creating directories and files

**🔑 Part 4: Permissions and Ownership**
This section focuses on managing file permissions and ownership.

**1. Check Current Permissions with ls -l**

To view the current permissions of files, use:

ls -l

Example output:

-rw-r--r-- 1 user group  98 Jan 26 12:00 todo.txt

-rw-r--r--: Indicates the file's permissions.

**2. Change File Permissions with chmod**

a) Make a File Readable Only by the Owner:

chmod 400 notes/todo.txt

The file will now be readable only by the owner.

b) Make a File Executable:

chmod +x notes/todo.txt

This makes the file executable.

**3. Change File Ownership with chown**

To change the owner of a file, use:

sudo chown new_owner notes/todo.txt

Replace new_owner with the desired username.

**🖥️ Part 5: System Information**

This section focuses on retrieving system and user information using Linux commands.

**1. Display Current User with whoami**

To display the current logged-in user:

whoami

Example output:

user

**2. Show System Information with uname**

To display system information:

uname -a

Example output:

Linux hostname 5.15.0-1051-azure #59-Ubuntu SMP Thu Mar 16 17:25:05 UTC 2023 x86_64 x86_64 x86_64 GNU/Linux

**3. Check Disk Space with df**

To view disk space usage:
df -h
The -h flag displays the output in human-readable format.

Example output:

Filesystem      Size  Used Avail Use% Mounted on
/dev/sda1        50G   20G   30G  40% /

**4. List Running Processes with ps**

To view currently running processes:

ps aux

This command lists all running processes with details such as user, process ID (PID), CPU, and memory usage.
