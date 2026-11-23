# **Linux – Complete Interview Questions & Answers**

# **Section 1 – Linux Fundamentals**

### **Q1. What is Linux? Explain its features and list some commonly used Linux distributions.**

**Answer:**

Linux is a free and open-source, Unix-like operating system.

It acts as an interface between users, applications and computer hardware.

Linux is widely used in servers, desktops and enterprise environments.

**Features of Linux:**

1. **Open Source:** Linux source code is freely available.
2. **Multi-User:** Multiple users can access the system.
3. **Multitasking:** Linux can execute multiple processes simultaneously.
4. **Security:** Linux provides user permissions and access control.
5. **Command-Line Interface:** We can perform operations using shell commands.
6. **Hardware Support:** Linux supports different types of hardware.
7. **Case Sensitive:** Linux differentiates between uppercase and lowercase filenames.

**Common Linux distributions:**

- Red Hat Enterprise Linux (RHEL).
- CentOS.
- Ubuntu.
- SUSE Linux.
- Debian.
- Fedora.
- Rocky Linux.

### **Q2. What are Single-User and Multi-User Operating Systems? Explain the difference between Windows and Linux.**

**Answer:**

There are two types of operating systems based on user access.

**1. Single-User Operating System:**

A single-user operating system allows one user to use the system at a time.

Example mentioned in my notes: Windows.

**2. Multi-User Operating System:**

A multi-user operating system allows multiple users to access the system at the same time.

Example: Linux.

**Difference between Windows and Linux:**

| Feature           | Windows                                                         | Linux                                                |
| ----------------- | --------------------------------------------------------------- | ---------------------------------------------------- |
| User access       | Traditionally described as single-user in the notes             | Multi-user                                           |
| Interface         | Mainly GUI-oriented                                             | Both CLI and GUI                                     |
| Source code       | Not open source                                                 | Open source                                          |
| Virtualization    | Requires virtualization software for many virtualization setups | Supports virtualization technologies                 |
| Security          | Less secure according to the comparison in the notes            | More secure according to the comparison in the notes |
| Case sensitivity  | Generally case-insensitive for filenames                        | Case-sensitive                                       |
| Command interface | Command Prompt / PowerShell                                     | Shell such as Bash                                   |

### **Q3. What is the difference between Desktop OS and Server OS?**

**Answer:**

**Desktop OS:**

A Desktop Operating System is designed for personal use on laptops, desktops and workstations.

Examples:

- Windows 10/11.
- macOS.
- Ubuntu Desktop.

**Server OS:**

A Server Operating System is designed to manage network services, applications, databases and multiple user connections.

Examples:

- Windows Server.
- Red Hat Enterprise Linux.
- Ubuntu Server.
- CentOS.

**Differences:**

| Desktop OS                                                    | Server OS                                             |
| ------------------------------------------------------------- | ----------------------------------------------------- |
| Designed for personal use                                     | Designed for managing servers and services            |
| Mainly used on laptops and desktops                           | Used on physical servers                              |
| Usually provides GUI                                          | Often managed using CLI                               |
| Supports user applications such as browsers and media players | Supports databases, web servers and network services  |
| Optimized for user experience                                 | Optimized for stability, speed and uptime             |
| Generally used by individuals                                 | Generally used by IT administrators and organizations |

### **Q4. What are the different root directories in Linux? Explain the purpose of important directories.**

**Answer:**

Linux follows a hierarchical filesystem structure starting from the root directory `/`.

Important directories include:

| Directory | Purpose                                          |
| --------- | ------------------------------------------------ |
| `/`       | Root directory; starting point of the filesystem |
| `/bin`    | Essential user commands                          |
| `/sbin`   | System administration commands                   |
| `/boot`   | Kernel and bootloader-related files              |
| `/dev`    | Device files                                     |
| `/etc`    | System configuration files                       |
| `/home`   | User home directories                            |
| `/root`   | Root user's home directory                       |
| `/lib`    | Essential shared libraries                       |
| `/usr`    | User applications, utilities and libraries       |
| `/var`    | Variable data such as logs                       |
| `/tmp`    | Temporary files                                  |
| `/mnt`    | Temporary mount point                            |
| `/media`  | Mount points for removable media                 |
| `/proc`   | Process and kernel information                   |
| `/sys`    | Kernel and hardware device information           |

**Example:**

When we want to check system logs, we use `/var/log`.

When we want to check system configuration files, we use `/etc`.

# **Section 2 – Linux Booting Process**

### **Q5. What are the different stages involved in the Linux booting process? Explain each stage.**

**Answer:**

According to my notes, the Linux booting process contains six major stages.

The booting process starts when we power on the server and continues until the system reaches the login prompt.

The stages are:

1. BIOS/UEFI.
2. MBR.
3. GRUB.
4. Kernel.
5. INIT.
6. Run Level Programs.

**Stage 1 – BIOS/UEFI:**

BIOS stands for Basic Input Output System.

It is firmware stored on the motherboard.

When we power on the server, BIOS performs POST (Power-On Self-Test).

POST checks whether the hardware components are functioning properly.

For example:

- RAM.
- CPU.
- CMOS.
- Storage devices.

If a hardware component fails during POST, the BIOS may report an error using beep codes or POST codes.

UEFI stands for Unified Extensible Firmware Interface. It is the modern firmware interface used to initialize hardware and manage the boot process.

**Stage 2 – MBR:**

MBR stands for Master Boot Record.

In a traditional BIOS-based boot process, BIOS identifies the boot device and executes the bootloader code stored in the MBR.

The MBR contains bootloader information and partition-table information.

**Stage 3 – GRUB:**

GRUB stands for Grand Unified Bootloader.

It is a bootloader used in Linux.

GRUB allows us to select the operating system or kernel to boot.

It can also store multiple boot entries.

**Stage 4 – Kernel:**

The Linux kernel is the core component of the operating system.

It acts as an interface between the software and hardware.

It manages:

- Process management.
- Memory management.
- Filesystem management.
- System calls.
- Device drivers.
- Hardware communication.

**Stage 5 – INIT:**

INIT is the first user-space process started by the kernel.

It is responsible for initializing the system and starting the required services.

In traditional Linux systems, INIT has PID 1.

**Stage 6 – Run Level Programs:**

Based on the configured run level, Linux starts the required services and processes.

For example, it can start networking, SSH, firewall and other services.

Finally, the system reaches the login prompt.

**Booting Flow:**

```
Power ON
    |
 BIOS / UEFI
    |
   POST
    |
 MBR / EFI Boot
    |
   GRUB
    |
  Kernel
    |
   INIT
    |
Run Level Programs
    |
 Login Prompt
```

### **Q6. What is BIOS/UEFI, and what happens during POST?**

**Answer:**

**BIOS:**

BIOS stands for Basic Input Output System.

It is firmware stored on the motherboard.

When we power on the server, BIOS initializes and checks the hardware components.

**POST:**

POST stands for Power-On Self-Test.

It is performed during the initial boot process.

POST checks whether the hardware components are functioning correctly.

Examples:

- CPU.
- RAM.
- CMOS.
- Storage devices.

If a hardware component is not working, BIOS may display an error or generate a beep code.

**UEFI:**

UEFI stands for Unified Extensible Firmware Interface.

It is an advanced firmware interface used in modern systems.

It supports modern boot mechanisms, GPT partitioning and EFI bootloaders.

### **Q7. What is MBR and GPT? Explain their differences.**

**Answer:**

**MBR – Master Boot Record:**

MBR is a traditional partitioning scheme used to store bootloader information and partition-table information.

According to my notes, the MBR structure contains:

- 446 bytes – Bootloader code.
- 64 bytes – Partition table.
- 2 bytes – Validation/signature.

It supports a maximum of four primary partitions, or three primary partitions and one extended partition.

**GPT – GUID Partition Table:**

GPT stands for GUID Partition Table.

It is a modern partitioning scheme used with UEFI systems.

It supports more partitions and larger disk capacities than traditional MBR partitioning.

**Difference:**

| MBR                                     | GPT                                 |
| --------------------------------------- | ----------------------------------- |
| Master Boot Record                      | GUID Partition Table                |
| Traditional partition scheme            | Modern partition scheme             |
| Supports up to four primary partitions  | Supports many partitions            |
| Limited disk size support               | Supports larger disk capacities     |
| Commonly used with BIOS boot            | Commonly used with UEFI boot        |
| Stores partition information in the MBR | Maintains GPT partition information |

### **Q8. What is GRUB? What is the GRUB configuration file path, and how does GRUB select the operating system to boot?**

**Answer:**

GRUB stands for Grand Unified Bootloader.

It is a bootloader used in Linux operating systems.

Its main purpose is to load the Linux kernel and start the operating system.

**Responsibilities of GRUB:**

1. Displays available boot entries.
2. Allows users to select an operating system or kernel.
3. Loads the selected kernel.
4. Passes the required boot parameters.
5. Starts the boot process.

**Configuration file:**

My notes mention:

```
/etc/grub.conf
```

GRUB configuration locations differ between Linux distributions and GRUB versions. For example, many modern RHEL-based installations use `/etc/default/grub` and generated configuration files under `/boot/grub2/`.

**How does GRUB select the OS?**

1. BIOS or UEFI completes the hardware initialization.
2. The bootloader is loaded.
3. GRUB displays the available boot entries.
4. The user can select an entry.
5. If no entry is selected, GRUB loads the configured default entry.
6. GRUB loads the selected kernel and starts the boot process.

### **Q9. What are the different run levels in Linux? Explain each run level.**

**Answer:**

Run levels define the operating state of a Linux system and determine which services or programs should run.

According to my notes, there are seven traditional run levels:

| Run Level | Description                                               |
| --------- | --------------------------------------------------------- |
| 0         | Halt / Shutdown                                           |
| 1         | Single-user mode                                          |
| 2         | Multi-user mode without network in the traditional layout |
| 3         | Full multi-user mode with networking, without GUI         |
| 4         | Unused / User-defined                                     |
| 5         | Multi-user mode with GUI                                  |
| 6         | Reboot                                                    |

**Explanation:**

- Run Level 0: Shuts down the system.
- Run Level 1: Starts single-user or maintenance mode.
- Run Level 2: Starts multi-user mode with limited networking in traditional configurations.
- Run Level 3: Starts full multi-user mode with networking and without GUI.
- Run Level 4: Reserved or unused by default.
- Run Level 5: Starts multi-user mode with GUI.
- Run Level 6: Reboots the system.

**Note:** Traditional SysV run levels are represented differently on modern systemd-based systems, which use targets such as `multi-user.target` and `graphical.target`.

### **Q10. What is the path used to configure or change the Linux run level?**

**Answer:**

According to my notes, traditional Linux systems use:

```
/etc/inittab
```

To view the configuration:

```
cat /etc/inittab
```

To edit the file:

```
vi /etc/inittab
```

The run level is configured in the init configuration.

**Additional clarification:** Modern RHEL 9 systems use systemd rather than the traditional `/etc/inittab` run-level mechanism.

To check the default target:

```
systemctl get-default
```

To set the default multi-user target:

```
systemctl set-default multi-user.target
```

To set the graphical target:

```
systemctl set-default graphical.target
```

### **Q11. What is the first process started by the Linux kernel, and what is its Process ID?**

**Answer:**

The first user-space process started by the Linux kernel is traditionally called `init`.

Its Process ID is:

```
PID = 1
```

In modern Linux systems, `systemd` commonly performs the init role and runs with PID 1.

It is responsible for initializing the system and starting system services.

To check:

```
ps -p 1 -f
```

# **Section 3 – Linux File and Directory Management**

### **Q12. How do you get the present working directory? Explain the difference between&#x20;**`cd ~`**,&#x20;**`cd /`**&#x20;and&#x20;**`cd -`**.**

**Answer:**

To get the present working directory, we use:

```
pwd
```

It displays the current working directory.

**Difference between commands:**

```
cd ~
```

Moves to the current user's home directory.

```
cd /
```

Moves to the root directory.

```
cd -
```

Moves to the previous working directory.

### **Q13. How do you create multiple files in the same directory? How do you list normal files, hidden files and directories?**

**Answer:**

**To create a single file:**

```
touch file1
```

**To create multiple files:**

```
touch file1 file2 file3 file4 file5
```

**To list files:**

```
ls
```

**To list hidden files:**

```
ls -a
```

**To list files in long format:**

```
ls -l
```

**To list directories:**

```
ls -d */
```

### **Q14. How do you list files in long format, human-readable format and display their sizes?**

**Answer:**

We use the `ls` command.

**Long listing:**

```
ls -l
```

Displays permissions, owner, group, file size and modification time.

**Human-readable format:**

```
ls -lh
```

Displays file sizes in KB, MB or GB.

**To display sizes:**

```
ls -lh
```

**To list files sorted by size:**

```
ls -lhS
```

### **Q15. How do you display the contents of a file? Explain&#x20;**`cat`**,&#x20;**`head`**&#x20;and&#x20;**`tail`**&#x20;commands.**

**Answer:**

**1. cat:**

Used to display the complete contents of a file.

```
cat file.txt
```

To add content to a file:

```
cat > file.txt
```

To append content:

```
cat >> file.txt
```

**2. head:**

Used to display the first 10 lines of a file by default.

```
head file.txt
```

To display a specific number of lines:

```
head -n 5 file.txt
```

**3. tail:**

Used to display the last 10 lines of a file by default.

```
tail file.txt
```

To display a specific number of lines:

```
tail -n 5 file.txt
```

To monitor a file continuously:

```
tail -f file.txt
```

### **Q16. How do you overwrite, append and redirect command output into a file?**

**Answer:**

There are different operators used for redirecting output.

**1. Overwrite using&#x20;**`>`**:**

```
ls > output.txt
```

It stores the command output in the file.

If the file already contains data, the old content is overwritten.

**2. Append using&#x20;**`>>`**:**

```
date >> output.txt
```

It appends the command output to the existing file without deleting old content.

**3. Pipe using&#x20;**`|`**:**

```
ls | grep ".txt"
```

A pipe passes the output of one command as the input to another command.

**Difference:**

\| Operator | Purpose |\
\|---|---|\
\| `>` | Overwrites file content |\
\| `>>` | Appends data |\
\| `|` | Passes output to another command |

### **Q17. How do you copy, rename, move and delete files in Linux? How do you remove files forcefully?**

**Answer:**

We use the following commands:

**1. Copy a file:**

```
cp file1.txt /home/user/
```

**2. Rename a file:**

```
mv file1.txt myfile.txt
```

**3. Move a file:**

```
mv file1.txt /home/user/
```

**4. Delete a file:**

```
rm file1.txt
```

**5. Forcefully delete a file:**

```
rm -f file1.txt
```

**6. Delete multiple files:**

```
rm file1.txt file2.txt file3.txt
```

### **Q18. How do you create, delete and rename directories in Linux?**

**Answer:**

**1. Create a directory:**

```
mkdir mydir
```

**2. Create nested directories:**

```
mkdir -p /home/user/test/dir1
```

**3. Remove an empty directory:**

```
rmdir mydir
```

**4. Remove a directory containing files:**

```
rm -r mydir
```

**5. Forcefully remove a directory:**

```
rm -rf mydir
```

**6. Rename a directory:**

```
mv old_dir new_dir
```

### **Q19. How do you search for files and directories using the&#x20;**`find`**&#x20;command? How do you find a file named&#x20;**`test.py`**&#x20;under&#x20;**`/etc`**&#x20;and obtain its full path?**

**Answer:**

The `find` command is used to search for files and directories in Linux.

**Syntax:**

```
find <path> -name <file_name>
```

**To find&#x20;**`test.py`**&#x20;under&#x20;**`/etc`**:**

```
find /etc -name "test.py"
```

**To search for a directory:**

```
find /home -type d -name "mydir"
```

**To search for files:**

```
find /home -type f
```

**To search for empty files:**

```
find /home -type f -empty
```

The `find` command displays the path of the matching file.

### **Q20. How do you list files starting with a particular name and ending with&#x20;**`.py`**? How do you copy matching Python files to another directory?**

**Answer:**

We use wildcard characters for pattern matching.

**To list files starting with&#x20;**`python`**&#x20;and ending with&#x20;**`.py`**:**

```
ls python*.py
```

**To list all Python files:**

```
ls *.py
```

**To copy Python files to another directory:**

```
cp *.py /etc/var/log/
```

The wildcard `*` matches any sequence of characters.

### **Q21. What is the&#x20;**`grep`**&#x20;command? How do you search for a pattern recursively and count the number of occurrences?**

**Answer:**

`grep` is used to search for a specific keyword or pattern in files and command output.

**Syntax:**

```
grep "keyword" file.txt
```

**To ignore case:**

```
grep -i "python" file.txt
```

**To display matching line numbers:**

```
grep -n "python" file.txt
```

**To search recursively inside directories:**

```
grep -r "python" /home/user/
```

**To count matching lines:**

```
grep -c "python" file.txt
```

**To perform an exact fixed-string search:**

```
grep -F "storage" file.txt
```

### **Q22. How do you replace a particular string in a file using the Linux command line?**

**Answer:**

We can use the `sed` command to search and replace strings in a file.

**Syntax:**

```
sed 's/old_string/new_string/g' file.txt
```

This displays the modified content without changing the original file.

To replace the content directly in the file:

```
sed -i 's/old_string/new_string/g' file.txt
```

**Example:**

```
sed -i 's/Linux/UNIX/g' file.txt
```

This replaces all occurrences of `Linux` with `UNIX` in the file.

### **Q23. How do you create and extract ZIP and TAR archive files?**

**Answer:**

We use `zip`, `unzip` and `tar` commands.

**ZIP:**

To create a ZIP file:

```
zip files.zip file1 file2 file3
```

To extract a ZIP file:

```
unzip files.zip
```

**TAR:**

To create a TAR archive:

```
tar -cvf files.tar file1 file2 file3
```

To extract a TAR archive:

```
tar -xvf files.tar
```

**Options:**

- `c` – Create archive.
- `x` – Extract archive.
- `v` – Verbose output.
- `f` – Specify archive filename.

### **Q24. How do you find and delete empty files in Linux?**

**Answer:**

We use the `find` command.

**To find empty files:**

```
find /path -type f -empty
```

**To delete empty files:**

```
find /path -type f -empty -delete
```

Here:

- `-type f` searches for regular files.
- `-empty` identifies empty files.
- `-delete` deletes the matching files.

### **Q25. How do you save the output of a Linux command into a file?**

**Answer:**

We use output redirection.

**To overwrite a file:**

```
ls > output.txt
```

**To append output:**

```
date >> output.txt
```

**To save standard output and standard error together:**

```
command > output.txt 2>&1
```

The `>` operator overwrites the file, while `>>` appends the output.

### **Q26. How do you count the number of characters in a file?**

**Answer:**

We use the `wc` command.

**To count characters:**

```
wc -m file.txt
```

**To count bytes:**

```
wc -c file.txt
```

**To count lines:**

```
wc -l file.txt
```

**To count words:**

```
wc -w file.txt
```

`wc` stands for Word Count.

# **Section 4 – Linux File Permissions, Inodes and Links**

### **Q27. What are file permissions in Linux? Explain Read, Write and Execute permissions.**

**Answer:**

Linux provides three basic types of file permissions:

1. Read (r).
2. Write (w).
3. Execute (x).

These permissions control what users can do with files and directories.

**1. Read (r):**

Allows users to read the contents of a file.

**2. Write (w):**

Allows users to modify or update a file.

**3. Execute (x):**

Allows users to execute a file or script.

Linux has three categories of users:

- Owner (User).
- Group.
- Others.

**Example:**

```
ls -l file.txt
```

Output:

```
-rwxr-xr-- 1 user group 1024 Nov 23 file.txt
```

Here:

- `rwx` – Owner has read, write and execute permissions.
- `r-x` – Group has read and execute permissions.
- `r--` – Others have read permission only.

### **Q28. What are the different permission modes in Linux? How do you change permissions using&#x20;**`chmod`**?**

**Answer:**

Linux supports two common ways of specifying file permissions:

1. Symbolic mode.
2. Numeric or octal mode.

**Symbolic Mode:**

We use:

- `r` – Read.
- `w` – Write.
- `x` – Execute.
- `u` – Owner.
- `g` – Group.
- `o` – Others.

**Numeric Mode:**

| Permission  | Numeric Value |
| ----------- | ------------- |
| Read (r)    | 4             |
| Write (w)   | 2             |
| Execute (x) | 1             |

To calculate permissions, we add the corresponding values.

For example:

- `7 = 4 + 2 + 1 = rwx`
- `6 = 4 + 2 = rw-`
- `5 = 4 + 1 = r-x`
- `4 = r--`

**chmod:**

`chmod` is used to change file permissions.

**To give full permissions to everyone:**

```
chmod 777 file.txt
```

**To give owner full permissions, group read/execute and others read/execute:**

```
chmod 755 file.txt
```

**To provide read and write permissions to the owner:**

```
chmod 600 file.txt
```

**To provide full permission only to the owner:**

```
chmod 700 file.txt
```

### **Q29. What is an inode in Linux, and what information does it contain? How do you find the inode number of a file?**

**Answer:**

An inode is a data structure used by the Linux filesystem to store metadata about a file.

It contains information such as:

- File permissions.
- File owner.
- Group information.
- File size.
- Timestamps.
- File type.
- Data block locations.

The inode does not normally store the filename. The directory maintains the mapping between a filename and its inode number.

**To find the inode number of a file:**

```
ls -i file.txt
```

**To display detailed information:**

```
ls -li
```

**Example:**

```
56009907 file.txt
```

Here, `56009907` is the inode number.

### **Q30. What is the difference between Hard Link and Soft Link? Explain how to create them.**

**Answer:**

There are two types of links in Linux:

1. Hard Link.
2. Soft Link.

**1. Hard Link:**

A hard link is another directory entry that points to the same inode as the original file.

It acts as another name for the same underlying file data.

**To create a Hard Link:**

```
ln original.txt hardlink.txt
```

**2. Soft Link:**

A soft link, also called a symbolic link, is a shortcut that points to the original file through its path.

It has a different inode from the original file.

**To create a Soft Link:**

```
ln -s original.txt softlink.txt
```

**Difference between Hard Link and Soft Link:**

| Hard Link                                                        | Soft Link                                         |
| ---------------------------------------------------------------- | ------------------------------------------------- |
| Points to the same inode                                         | Points to the original file path                  |
| Has the same inode number as the original file                   | Has a different inode number                      |
| File data remains accessible if the original filename is deleted | May become broken if the original file is deleted |
| Generally restricted to the same filesystem                      | Can point across filesystems                      |
| Cannot normally be created for directories                       | Can point to directories                          |

**Example:**

Suppose we create a hard link and soft link for `file1.txt`.

```
ln file1.txt hardlink.txt
ln -s file1.txt softlink.txt
```

If we delete `file1.txt`, the hard link can still access the data, whereas the soft link becomes broken.

### **Q31. How do file permissions differ for Owner, Group and Others?**

**Answer:**

Linux divides users into three categories for permission management.

**1. Owner:**

The owner is the user who owns the file.

The owner can have read, write and execute permissions.

**2. Group:**

The group contains users who share the same group permissions.

All members of the group receive the permissions assigned to that group.

**3. Others:**

Others are users who are neither the owner nor members of the file's group.

They receive the permissions assigned to others.

**Example:**

```
chmod 754 file.txt
```

Here:

- Owner: `7` = Read + Write + Execute.
- Group: `5` = Read + Execute.
- Others: `4` = Read only.

# **Section 5 – Linux Users, System Administration and Process Management**

### **Q32. How do you create and delete users, change passwords and switch between root and normal users?**

**Answer:**

Linux provides user-management commands to create, delete and manage users.

**1. To list users:**

```
users
```

**2. To create a user:**

```
useradd username
```

**3. To delete a user:**

```
userdel username
```

To delete the user's home directory as well:

```
userdel -r username
```

**4. To change a password:**

```
passwd username
```

**5. To check the current user:**

```
whoami
```

**6. To switch to another user:**

```
su - username
```

**7. To switch to root:**

```
su -
```

**8. To return to the previous user:**

```
exit
```

**Difference between Root User and Normal User:**

| Root User                                         | Normal User                                              |
| ------------------------------------------------- | -------------------------------------------------------- |
| Has administrative privileges                     | Has limited permissions                                  |
| Can create and delete users                       | Cannot manage other users without privileges             |
| Can modify system configurations                  | Cannot modify protected system configurations by default |
| Can install and remove packages                   | Requires elevated privileges                             |
| Incorrect commands can affect the complete system | Safer for daily operations                               |

### **Q33. How do you check and permanently change the hostname of a Linux machine?**

**Answer:**

A hostname is the name assigned to a Linux machine in a network.

**To check the current hostname:**

```
hostname
```

**To display system hostname information:**

```
hostnamectl
```

**To change the hostname permanently:**

```
hostnamectl set-hostname server1
```

**To verify:**

```
hostnamectl
```

The hostname helps identify the machine in the network.

### **Q34. How do you display and change the current date and time in Linux?**

**Answer:**

We use the `date` command.

**To display the current date and time:**

```
date
```

**To display the date in a particular format:**

```
date +"%Y-%m-%d"
```

**To set the date and time:**

```
date -s "2026-11-23 10:30:00"
```

Changing system time generally requires administrative privileges.

### **Q35. What are the commands used to retrieve system information, CPU information, RAM information and complete hardware information?**

**Answer:**

Linux provides different commands to collect system and hardware information.

**1. Complete system information:**

```
uname -a
```

Displays kernel and system information.

**2. CPU information:**

```
lscpu
```

Displays CPU architecture, model, cores and other CPU details.

We can also use:

```
cat /proc/cpuinfo
```

**3. RAM information:**

```
free -h
```

Displays total, used and available memory.

We can also use:

```
cat /proc/meminfo
```

**4. Hardware information:**

```
sudo dmidecode
```

Provides BIOS, motherboard, processor and memory-related hardware information.

**5. Block device information:**

```
lsblk
```

Lists storage block devices.

**6. PCI device information:**

```
lspci
```

Lists PCI devices connected to the system.

**7. USB device information:**

```
lsusb
```

Lists USB devices.

**8. SCSI device information:**

```
lsscsi
```

Lists SCSI devices.

### **Q36. What is&#x20;**`/proc`**&#x20;in Linux? What type of information does it contain?**

**Answer:**

`/proc` is a virtual filesystem in Linux that provides information about running processes and kernel-related system information.

It does not store ordinary files on disk in the same way as a normal filesystem.

It provides information dynamically through the Linux kernel.

Important files include:

| File               | Information             |
| ------------------ | ----------------------- |
| `/proc/cpuinfo`    | CPU information         |
| `/proc/meminfo`    | Memory information      |
| `/proc/version`    | Kernel version          |
| `/proc/uptime`     | System uptime           |
| `/proc/loadavg`    | System load information |
| `/proc/mounts`     | Mounted filesystems     |
| `/proc/modules`    | Loaded kernel modules   |
| `/proc/partitions` | Partition information   |

**Example:**

To check CPU information:

```
cat /proc/cpuinfo
```

To check memory information:

```
cat /proc/meminfo
```

### **Q37. How do you list all running processes in Linux? Explain&#x20;**`ps`**&#x20;command and its commonly used options.**

**Answer:**

A process is an instance of a running application or program.

Whenever we start an application, a process is created.

We use the `ps` command to display process information.

**To display processes:**

```
ps
```

**To list all running processes:**

```
ps -e
```

**To display all processes with detailed information:**

```
ps -ef
```

**To display processes in full format:**

```
ps -eaf
```

**To search for a particular process:**

```
ps -ef | grep python
```

Important process fields include:

- UID – User ID.
- PID – Process ID.
- PPID – Parent Process ID.
- CMD – Command used to start the process.

### **Q38. How do you monitor real-time system performance, CPU utilization, memory usage and system uptime?**

**Answer:**

We use different Linux commands to monitor system performance.

**1. Real-time system performance:**

```
top
```

The `top` command displays real-time information such as CPU utilization, memory usage and running processes.

**2. System uptime:**

```
uptime
```

Displays how long the system has been running since the last boot.

**3. Memory utilization:**

```
free -h
```

Displays total, used and available memory.

**4. Disk space utilization:**

```
df -h
```

Displays filesystem disk usage.

**5. Storage I/O statistics:**

```
iostat -x
```

Displays detailed storage device I/O statistics when the relevant utility is installed.

**6. System information:**

```
uname -a
```

Displays system and kernel details.

### **Q39. How do you terminate a process forcefully using its PID or process name?**

**Answer:**

We use the `kill` command to terminate a process.

**To terminate a process using PID:**

```
kill 1234
```

**To forcefully terminate a process:**

```
kill -9 1234
```

**To terminate a process using application name:**

```
pkill application_name
```

**Example:**

```
pkill python
```

Here, the command terminates matching Python processes for which the user has sufficient permissions.

### **Q40. What is the purpose of&#x20;**`nice`**&#x20;and&#x20;**`renice`**&#x20;commands in Linux?**

**Answer:**

`nice` and `renice` are used to manage the scheduling priority of processes.

**Nice:**

The `nice` command is used to start a process with a specific nice value.

Example:

```
nice -n 10 python script.py
```

**Renice:**

The `renice` command is used to change the nice value of an already running process.

Example:

```
renice 10 -p 1234
```

**Nice Value:**

Nice values generally range from `-20` to `19`.

- `-20` represents the highest scheduling priority.
- `19` represents the lowest scheduling priority.

### **Q41. How do you find the users currently logged in to a Linux system?**

**Answer:**

We can use the following commands:

**1. To display currently logged-in users:**

```
who
```

**2. To display users and their current activity:**

```
w
```

**3. To display usernames currently logged in:**

```
users
```

These commands help us identify which users are currently accessing the Linux machine.

### **Q42. What are the different package management tools in Linux? Explain RPM, YUM, APT and their commands for installing, updating and removing packages.**

**Answer:**

Package management tools are used to install, update, remove and manage software packages in Linux.

According to my notes, the important package management tools are:

1. RPM.
2. YUM.
3. APT.

**1. RPM – Red Hat Package Manager**

RPM is used for package management in Red Hat-based distributions.

It can be used for offline package installation.

**To install an RPM package:**

```
rpm -ivh package.rpm
```

**To list installed RPM packages:**

```
rpm -qa
```

**To uninstall a package:**

```
rpm -e package_name
```

**To upgrade a package:**

```
rpm -Uvh package.rpm
```

**2. YUM – Yellowdog Updater Modified**

YUM is an advanced package management tool used in Red Hat-based Linux distributions.

It supports online package installation and dependency management.

**To install a package:**

```
yum install package_name
```

**To update a package:**

```
yum update package_name
```

**To remove a package:**

```
yum remove package_name
```

**To list installed packages:**

```
yum list installed
```

**3. APT – Advanced Package Tool**

APT is mainly used in Debian-based distributions such as Ubuntu.

**To install a package:**

```
apt-get install package_name
```

**To update package information:**

```
apt-get update
```

**To upgrade installed packages:**

```
apt-get upgrade
```

**To remove a package:**

```
apt-get remove package_name
```

**Difference:**

| RPM                           | YUM                                        | APT                                        |
| ----------------------------- | ------------------------------------------ | ------------------------------------------ |
| Package manager               | Higher-level package manager               | Higher-level package manager               |
| Red Hat-based systems         | Red Hat-based systems                      | Debian-based systems                       |
| Can install RPM packages      | Resolves dependencies through repositories | Resolves dependencies through repositories |
| Supports offline installation | Supports online installation               | Supports online installation               |

### **Q43. How do you start, stop and restart services in Linux? How do you list all services?**

**Answer:**

A service is a background program that provides system-level functionality.

Examples:

- SSH.
- Network.
- Firewall.
- Storage-related services.

We use `systemctl` or `service` commands to manage services.

**Using systemctl:**

To check service status:

```
systemctl status sshd
```

To start a service:

```
systemctl start sshd
```

To stop a service:

```
systemctl stop sshd
```

To restart a service:

```
systemctl restart sshd
```

To list active services:

```
systemctl list-units --type=service --state=running
```

**Using service command:**

```
service sshd status
service sshd start
service sshd stop
service sshd restart
```

### **Q44. What are kernel modules? How do you list, install and remove kernel modules? Explain&#x20;**`lsmod`**,&#x20;**`modprobe`**,&#x20;**`insmod`**&#x20;and&#x20;**`rmmod`**.**

**Answer:**

Kernel modules are components that can be loaded into or removed from the Linux kernel.

They provide additional functionality such as hardware and device driver support.

**1. lsmod:**

Used to list currently loaded kernel modules.

```
lsmod
```

**2. modprobe:**

Used to load a kernel module and automatically handle its dependencies.

```
modprobe module_name
```

To remove a module:

```
modprobe -r module_name
```

**3. insmod:**

Used to manually insert a kernel module.

```
insmod module_name.ko
```

It does not automatically resolve module dependencies.

**4. rmmod:**

Used to remove a loaded kernel module.

```
rmmod module_name
```

**Difference between modprobe and insmod:**

| modprobe                                   | insmod                                     |
| ------------------------------------------ | ------------------------------------------ |
| Can handle module dependencies             | Does not automatically handle dependencies |
| Uses module names and module configuration | Usually requires module file path          |
| Used for normal module management          | Used for manual insertion                  |

# **Section 6 – Linux Storage and File System Management**

### **Q45. What is partitioning in Linux? How do you create and delete partitions using&#x20;**`fdisk`**?**

**Answer:**

Partitioning is the process of dividing a physical storage device into multiple logical sections called partitions.

Each partition can be used for a different purpose.

For example, we can create separate partitions for:

- Operating system.
- User data.
- Boot files.
- Swap space.

We use the `fdisk` command to manage disk partitions.

**To identify available disks:**

```
lsblk
```

**To open a disk using fdisk:**

```
fdisk /dev/sdb
```

**Steps to create a partition:**

1. Open the required disk using `fdisk`.
2. Enter `n` to create a new partition.
3. Select the partition type: Primary or Extended, where supported by the partition table.
4. Select the partition number.
5. Enter the first sector or accept the default.
6. Enter the last sector or partition size.
7. Enter `w` to save the changes.

**Important fdisk commands:**

| Command | Purpose                             |
| ------- | ----------------------------------- |
| `n`     | Create new partition                |
| `d`     | Delete partition                    |
| `p`     | Display partition table             |
| `w`     | Save changes                        |
| `q`     | Exit without saving pending changes |

**To delete a partition:**

1. Open the disk using `fdisk`.
2. Enter `d`.
3. Select the partition number.
4. Enter `w` to save the changes.

Example:

```
fdisk /dev/sdb
```

**Note:** Partition changes can destroy data if performed incorrectly. Always verify the selected disk and its contents before making changes.

### **Q46. What is the difference between MBR and GPT partitioning?**

**Answer:**

This is the same concept covered in Q7.

- **MBR:** Traditional Master Boot Record partitioning scheme. It supports up to four primary partitions and has limitations on disk capacity.
- **GPT:** Modern GUID Partition Table scheme. It supports larger disks and more partitions and is commonly used with UEFI systems.

| MBR                             | GPT                             |
| ------------------------------- | ------------------------------- |
| Traditional partitioning        | Modern partitioning             |
| Maximum four primary partitions | Supports many partitions        |
| Limited disk capacity           | Supports larger disk capacities |
| Commonly associated with BIOS   | Commonly associated with UEFI   |

### **Q47. What is a filesystem? Explain different Linux and Windows filesystems. How do you create and check a filesystem in Linux?**

**Answer:**

A filesystem is a set of structures and rules followed by an operating system to organize and manage data on a storage device.

We use filesystems to store, organize and access data.

**Different filesystems:**

**Linux filesystems:**

- EXT2.
- EXT3.
- EXT4.
- XFS.
- ZFS.
- NFS.

**Windows filesystems:**

- NTFS.
- FAT.
- FAT32.

**VMware filesystem mentioned in my notes:**

\- VMFS.

**Storage arrays:**

Different storage array vendors may also implement their own storage management and filesystem technologies.

Examples mentioned in my notes:

- HPE.
- Dell EMC.
- Pure Storage.
- DDN.
- Hitachi.

**To create a filesystem:**

We use the `mkfs` command.

Example:

```
mkfs.ext4 /dev/sdb1
```

To create an XFS filesystem:

```
mkfs.xfs /dev/sdb1
```

**To check a filesystem:**

```
fsck /dev/sdb1
```

This command checks and, where appropriate, repairs filesystem inconsistencies.

**Important:** Filesystem creation normally overwrites existing filesystem metadata. Verify the device carefully before executing `mkfs`.

### **Q48. What is mounting in Linux? Explain local and remote mounting with commands. How do you unmount a filesystem?**

**Answer:**

Mounting is the process of attaching a storage device or filesystem to a directory in Linux so that users can access its contents.

We have two types of mounting:

1. Local Mount.
2. Remote Mount.

**1. Local Mount:**

Local mounting is used to mount a storage device connected directly to the system.

**Step 1 – Create a mount directory:**

```
mkdir -p /mnt/d1
```

**Step 2 – Mount the device:**

```
mount /dev/sdb1 /mnt/d1
```

**Step 3 – Verify the mount:**

```
df -h
```

**2. Remote Mount:**

Remote mounting is used to access storage exported from another server.

For example, using NFS:

```
mount -t nfs 192.168.1.100:/storage /mnt/d1
```

Here:

- `-t nfs` specifies the filesystem type.
- `192.168.1.100:/storage` is the remote exported directory.
- `/mnt/d1` is the local mount point.

**3. To unmount a filesystem:**

```
umount /mnt/d1
```

We can also use:

```
umount /dev/sdb1
```

After unmounting, the storage is no longer accessible through that mount point.

### **Q49. What is Swap Memory? Why is it used, and where is it located in Linux?**

**Answer:**

Swap memory is a storage area used by Linux when the available physical RAM is insufficient for memory requirements.

When the system experiences memory pressure, Linux can move selected memory pages from RAM to swap space.

It helps the system manage memory pressure.

Swap can be configured as:

1. Swap Partition.
2. Swap File.

**To check swap memory:**

```
free -h
```

**To check swap details:**

```
swapon --show
```

**Location:**

A swap partition is a dedicated disk partition, while a swap file can be created at a filesystem path such as:

```
/swapfile
```

The exact location depends on the system configuration.

### **Q50. How do you identify block devices, SCSI devices and PCI devices using Linux commands?**

**Answer:**

Linux provides different commands to identify storage devices and hardware components.

**1. Block Devices:**

We use:

```
lsblk
```

It lists block devices such as HDDs, SSDs, NVMe drives and partitions.

**2. SCSI Devices:**

We use:

```
lsscsi
```

It lists SCSI devices connected to the system.

**3. PCI Devices:**

We use:

```
lspci
```

It lists PCI devices such as:

- Storage controllers.
- Network adapters.
- Graphics devices.
- NVMe controllers.

**4. Detailed Drive Information:**

We use:

```
hdparm -I /dev/sda
```

This provides detailed drive information for supported ATA devices.

**5. Device Information:**

```
lsblk -f
```

Displays block devices along with filesystem information.

### **Q51. What is the difference between&#x20;**`df`**&#x20;and&#x20;**`du`**&#x20;commands? How do you check disk space utilization?**

**Answer:**

**df – Disk Free:**

The `df` command is used to check filesystem-level disk space utilization.

Example:

```
df -h
```

It displays:

- Total filesystem size.
- Used space.
- Available space.
- Usage percentage.
- Mount point.

**du – Disk Usage:**

The `du` command is used to identify how much disk space is occupied by files and directories.

Example:

```
du -sh /home/user
```

**Difference:**

| df                               | du                                                  |
| -------------------------------- | --------------------------------------------------- |
| Displays filesystem disk usage   | Displays file and directory disk usage              |
| Checks total and available space | Checks space consumed by selected files/directories |
| Works at filesystem level        | Works at file/directory level                       |
| Example: `df -h`                 | Example: `du -sh /home`                             |

### **Q52. How do you collect I/O statistics in Linux? Which commands are used to monitor storage performance?**

**Answer:**

Linux provides different commands to monitor storage performance and I/O activities.

**1. iostat:**

Used to collect CPU and device I/O statistics.

```
iostat
```

For extended device statistics:

```
iostat -x
```

**2. vmstat:**

Used to display system performance information, including memory, processes and I/O activity.

```
vmstat
```

**3. sar:**

Used to collect and report system activity information.

```
sar
```

**4. top:**

Used to monitor real-time system performance and process activity.

```
top
```

For storage validation, I would particularly use `iostat -x` to observe device-level I/O behaviour.

# **Section 7 – Linux Networking and Remote Management**

### **Q53. What is an IP Address and MAC Address? What is the difference between them?**

**Answer:**

**IP Address:**

An IP address is a logical address assigned to a device in a network.

It is used to identify and communicate with devices across networks.

Example:

```
192.168.0.173
```

**MAC Address:**

A MAC address is a hardware address associated with a network interface.

It is generally assigned by the hardware manufacturer.

Example:

```
00:1A:2B:3C:4D:5E
```

**Difference:**

| IP Address                                 | MAC Address                                       |
| ------------------------------------------ | ------------------------------------------------- |
| Logical address                            | Hardware address                                  |
| Can change based on network configuration  | Generally fixed to the network interface          |
| Used for network communication and routing | Used for communication within a local network     |
| IPv4 and IPv6 formats                      | Usually represented as 48-bit hexadecimal address |

### **Q54. What is the difference between Static IP and Dynamic IP?**

**Answer:**

**Static IP:**

A Static IP address is manually configured on a device.

It generally does not change unless an administrator modifies the configuration.

It is commonly used for servers and network devices.

**Dynamic IP:**

A Dynamic IP address is automatically assigned by a DHCP server.

It may change when the device reconnects or when its DHCP lease changes.

It is commonly used for client machines.

| Static IP                            | Dynamic IP                       |
| ------------------------------------ | -------------------------------- |
| Manually configured                  | Automatically assigned           |
| Generally remains unchanged          | Can change                       |
| Used for servers and network devices | Commonly used for client devices |
| Requires manual configuration        | Uses DHCP                        |

### **Q55. How do you check and configure/change the IP address of a Linux machine? Which configuration file is used for network configuration?**

**Answer:**

We use different Linux commands to view and configure IP addresses.

**1. To check the IP address:**

```
ip addr
```

We can also use:

```
ifconfig
```

**2. To check the network interfaces:**

```
ip link
```

**3. To configure a static IP address:**

According to my notes, the network interface configuration file in traditional RHEL-based systems is:

```
/etc/sysconfig/network-scripts/ifcfg-<interface>
```

We edit the required interface configuration file:

```
vi /etc/sysconfig/network-scripts/ifcfg-eth0
```

We configure the required static IP, subnet mask, gateway and other network settings.

**4. Restart the network service:**

```
systemctl restart network
```

**5. Verify the IP address:**

```
ip addr
```

**Important additional clarification:** Modern RHEL versions generally use NetworkManager. The older `network-scripts` path and `systemctl restart network` procedure may not apply to modern installations. NetworkManager tools such as `nmcli` are commonly used instead.

### **Q56. What is DHCP? Explain how a device receives an IP address through DHCP.**

**Answer:**

DHCP stands for Dynamic Host Configuration Protocol.

It is a network protocol used to automatically assign IP addresses and other network configuration details to devices.

Using DHCP, administrators do not need to configure every client IP address manually.

**DHCP Working Process – DORA:**

There are four main steps.

**1. Discover:**

The client sends a DHCP Discover message to find available DHCP servers.

**2. Offer:**

The DHCP server sends an offer containing an available IP address.

**3. Request:**

The client sends a DHCP Request message to request the offered IP address.

**4. Acknowledge:**

The DHCP server sends a DHCP ACK message confirming the IP allocation.

**Flow:**

```
Client
  |
Discover
  |
DHCP Server
  |
Offer
  |
Client
  |
Request
  |
DHCP Server
  |
ACK
  |
IP Address Assigned
```

### **Q57. What are Subnet Mask, Default Gateway and DNS? Explain their purposes.**

**Answer:**

**1. Subnet Mask:**

A subnet mask is used to divide an IP address into network and host portions.

Example:

```
IP Address: 192.168.1.10
Subnet Mask: 255.255.255.0
```

Here, the network portion is `192.168.1`, and the host portion is `10`.

**2. Default Gateway:**

A default gateway is the IP address of the router used by a device to communicate with other networks.

Example:

```
192.168.1.1
```

When a device needs to communicate outside its local network, it sends traffic through the default gateway.

**3. DNS:**

DNS stands for Domain Name System.

It converts domain names into IP addresses.

Example:

```
www.google.com
```

DNS resolves the domain name into an IP address so the system can communicate with the destination.

### **Q58. How do you find the IP address of a hostname? Explain DNS resolution.**

**Answer:**

We use the `nslookup` command to identify the IP address associated with a hostname.

**Command:**

```
nslookup hostname
```

Example:

```
nslookup google.com
```

It displays the IP address associated with the domain name.

**DNS Resolution Process:**

1. A user enters a domain name.
2. The system checks the DNS resolver.
3. The DNS resolver queries the required DNS server.
4. The DNS server resolves the domain name into an IP address.
5. The IP address is returned to the client.
6. The client communicates with the destination using that IP address.

### **Q59. What are the port numbers of SSH, FTP, HTTP and iSCSI?**

**Answer:**

The commonly used default port numbers are:

| Protocol | Port Number | Purpose                                   |
| -------- | ----------- | ----------------------------------------- |
| SSH      | 22          | Secure remote login                       |
| FTP      | 21          | File Transfer Protocol control connection |
| HTTP     | 80          | Web communication                         |
| iSCSI    | 3260        | iSCSI storage communication               |

### **Q60. What is the use of&#x20;**`netstat`**? How do you check network connections and listening ports?**

**Answer:**

`netstat` stands for Network Statistics.

It is used to display network connections, listening ports, routing information and network statistics.

**1. To display network connections:**

```
netstat -an
```

**2. To display listening TCP and UDP ports:**

```
netstat -tuln
```

**3. To display processes associated with listening ports:**

```
netstat -tulnp
```

Root privileges may be required to display process information.

**Note:** On modern Linux distributions, `ss` is commonly used as a replacement for `netstat`.

### **Q61. What are SSH, WinSCP and RDP? How do you connect to a remote Linux machine?**

**Answer:**

**1. SSH – Secure Shell:**

SSH is used to establish a secure remote connection to another Linux machine.

Default port:

```
22
```

Syntax:

```
ssh username@IP_address
```

Example:

```
ssh root@192.168.0.100
```

**2. WinSCP:**

WinSCP is a tool used to transfer files between Windows and remote systems.

It commonly uses the SFTP protocol over SSH.

**3. RDP – Remote Desktop Protocol:**

RDP is used to access and control a remote desktop, commonly a Windows machine.

Default port:

```
3389
```

**Difference:**

| SSH                        | WinSCP                          | RDP                       |
| -------------------------- | ------------------------------- | ------------------------- |
| Remote command-line access | File transfer                   | Remote graphical desktop  |
| Commonly used for Linux    | Used for file transfers         | Commonly used for Windows |
| Port 22                    | Commonly uses SFTP over port 22 | Port 3389                 |

### **Q62. How do you copy files and directories between two Linux machines using&#x20;**`scp`**?**

**Answer:**

`scp` stands for Secure Copy.

It is used to transfer files and directories between remote systems using SSH.

**Syntax to copy a file from local machine to remote machine:**

```
scp file.txt username@192.168.0.100:/home/user/
```

**To copy a file from remote machine to local machine:**

```
scp username@192.168.0.100:/home/user/file.txt .
```

**To copy a directory:**

```
scp -r mydir username@192.168.0.100:/home/user/
```

The `-r` option is used to copy directories recursively.

### **Q63. What is the use of the&#x20;**`curl`**&#x20;command?**

**Answer:**

`curl` is a command-line tool used to transfer data to or from servers using supported network protocols.

It is commonly used to communicate with HTTP and HTTPS endpoints.

**To check a website:**

```
curl https://example.com
```

**To display HTTP response headers:**

```
curl -I https://example.com
```

**To download a file:**

```
curl -O https://example.com/file.txt
```

It is useful for checking network connectivity and testing web endpoints.

### **Q64. What is the use of the&#x20;**`ping`**&#x20;command? How do you check whether a remote machine is reachable?**

**Answer:**

The `ping` command is used to check whether a remote device is reachable through the network.

It sends ICMP Echo Request packets to the destination and waits for Echo Reply packets.

**Syntax:**

```
ping <IP_address>
```

Example:

```
ping 192.168.0.173
```

**To send five packets:**

```
ping -c 5 192.168.0.173
```

If the destination responds, we receive replies.

If there is no response, possible reasons include:

- Network connectivity problem.
- Incorrect IP address.
- Firewall blocking ICMP.
- Destination device unavailable.

### **Q65. What are Hub, Switch and Router? What is VLAN, and why is it used?**

**Answer:**

**1. Hub:**

A Hub operates at the Physical Layer (Layer 1) of the OSI model.

It sends received data to all connected devices.

It does not maintain a MAC address table.

**2. Switch:**

A Switch operates mainly at the Data Link Layer (Layer 2).

It uses MAC addresses to forward frames to the destination device.

It maintains a MAC address table.

**3. Router:**

A Router operates at the Network Layer (Layer 3).

It uses IP addresses to connect different networks and forward packets between them.

**Difference:**

| Hub                               | Switch                               | Router                      |
| --------------------------------- | ------------------------------------ | --------------------------- |
| Layer 1                           | Layer 2                              | Layer 3                     |
| Does not use MAC address table    | Uses MAC address table               | Uses IP routing table       |
| Sends data to all ports           | Forwards frames to appropriate ports | Connects different networks |
| No intelligent traffic forwarding | MAC-based forwarding                 | IP-based routing            |

**VLAN – Virtual Local Area Network:**

VLAN is a logical network that separates devices into different broadcast domains.

We use VLANs to:

1. Separate devices into logical networks.
2. Improve network security.
3. Reduce unnecessary broadcast traffic.
4. Manage network segmentation.

For example, we can create different VLANs for storage traffic, management traffic and application traffic in an enterprise server environment.

# **Section 8 – Linux Installation and Configuration**

### **Q66. What are the different ways of installing Linux on a physical server? Explain installation using USB/Pen Drive, BMC Virtual Media, PXE/Network Boot and SAN Boot.**

**Answer:**

According to my notes, there are four different ways to install Linux on a physical server:

1. USB/Pen Drive.
2. BMC Virtual Media.
3. PXE/Network Boot.
4. SAN Boot.

**1. Installation using USB/Pen Drive:**

This method uses a bootable USB drive containing the Linux installation ISO.

**Steps:**

1. Download the required Linux ISO image.
2. Create a bootable USB using a tool such as Rufus.
3. Power off the server.
4. Insert the bootable USB into the server.
5. Power on the server.
6. Enter the boot menu using the appropriate key, such as F11 or F12, depending on the server.
7. Select the USB device as the boot device.
8. The Linux installation screen appears.
9. Select the installation disk.
10. Configure partitions and filesystem.
11. Configure hostname and root password.
12. Start the installation.
13. Wait until installation is completed.
14. Remove the USB and reboot the server.
15. Verify that Linux boots successfully.

**2. Installation using BMC Virtual Media:**

BMC Virtual Media allows us to mount an ISO image remotely through the server's management interface.

**Steps:**

1. Connect your laptop to the same network as the BMC.
2. Find the BMC IP address.
3. Open the BMC web interface using its IP address.
4. Enter the BMC username and password.
5. Open the Virtual Media option.
6. Select the required ISO image from the laptop.
7. Map the ISO to the server as virtual media.
8. Configure the server to boot from Virtual CD/DVD.
9. Reboot the server.
10. The server boots from the mounted ISO.
11. Complete the Linux installation.
12. Unmount the ISO after installation.
13. Reboot the server and verify successful installation.

**3. Installation using PXE/Network Boot:**

PXE stands for Preboot Execution Environment.

It allows us to boot and install an operating system over the network without using a physical USB drive.

**Steps:**

1. Power on the server.
2. Enter the boot menu.
3. Select Network Boot/PXE Boot.
4. The server sends a DHCP request to obtain an IP address.
5. The DHCP server assigns an IP address and provides boot information.
6. The server downloads the boot files from the PXE server.
7. The Linux installation environment starts.
8. Select the language, keyboard layout and other settings.
9. Select the installation disk.
10. Configure partitions, hostname and root password.
11. Start the installation.
12. After installation, reboot the server.
13. Verify that Linux boots successfully from the installed disk.

**4. Installation using SAN Boot:**

SAN Boot is a method of booting a server from a boot LUN provided by an external storage system.

**Steps:**

1. Create a boot LUN on the storage array.
2. Create a host group and add the server's HBA WWPN.
3. Configure SAN zoning between the server HBA and storage port.
4. Map the boot LUN to the host.
5. Verify that the server can detect the boot LUN.
6. Configure the BIOS boot settings to boot from SAN.
7. Mount the Linux installation ISO using USB, BMC Virtual Media or PXE.
8. Start the Linux installation.
9. Select the mapped boot LUN as the installation disk.
10. Complete the OS installation.
11. Reboot the server.
12. Verify the boot path:

```
Server HBA
    |
SAN Switch
    |
Storage Array
    |
Boot LUN
    |
Linux Operating System
```

### **Q67. What are the minimum partition requirements for Linux installation? What are the commonly created partitions and directories during installation?**

**Answer:**

A Linux installation requires a filesystem structure that provides space for the operating system and its required files.

**Commonly used partitions:**

1. `/` – Root partition. It contains the Linux operating system and its main directory structure.
2. `/boot` – Stores boot-related files such as the kernel and bootloader files.
3. `swap` – Used as additional virtual memory when physical RAM is under pressure.
4. `/home` – Can be created separately to store user data.

For UEFI-based installations, an EFI System Partition is also required.

**Minimum partition requirement:**

A basic Linux installation can use a single root filesystem partition, with additional boot and swap arrangements depending on the installation mode and requirements.

**Example partition layout:**

| Partition   | Purpose                             |
| ----------- | ----------------------------------- |
| `/boot/efi` | UEFI boot files                     |
| `/boot`     | Kernel and bootloader-related files |
| `/`         | Main operating system filesystem    |
| `swap`      | Swap memory                         |
| `/home`     | User data                           |

**Important:** These are mount points and partitions, not all separate root directories. Linux creates its normal directory hierarchy under `/`.

### **Q68. What is the maximum supported filename length in Linux?**

**Answer:**

In most commonly used Linux filesystems, the maximum filename length for a single filename component is typically **255 bytes**.

For example:

```
/home/user/test.txt
```

Here, `test.txt` is one filename component.

The maximum filename length depends on the filesystem.

Also, the complete path can have a different length limit from an individual filename.

# **Linux – Final Completion Summary**

68/68 Questions Answered

## **Important Linux commands for interview revision**

| Operation                 | Command                           |
| ------------------------- | --------------------------------- |
| Present working directory | `pwd`                             |
| List files                | `ls -l`                           |
| List hidden files         | `ls -a`                           |
| Create file               | `touch file.txt`                  |
| Create directory          | `mkdir dir`                       |
| Copy file                 | `cp file1 file2`                  |
| Rename file               | `mv file1 file2`                  |
| Delete file               | `rm file.txt`                     |
| Display file contents     | `cat file.txt`                    |
| First 10 lines            | `head file.txt`                   |
| Last 10 lines             | `tail file.txt`                   |
| Search text               | `grep "word" file.txt`            |
| Find file                 | `find / -name "file.txt"`         |
| Change permissions        | `chmod 755 file.txt`              |
| Find inode                | `ls -i file.txt`                  |
| Create hard link          | `ln file1 hardlink`               |
| Create soft link          | `ln -s file1 softlink`            |
| CPU information           | `lscpu`                           |
| Memory information        | `free -h`                         |
| Hardware information      | `dmidecode`                       |
| Block devices             | `lsblk`                           |
| SCSI devices              | `lsscsi`                          |
| PCI devices               | `lspci`                           |
| Disk utilization          | `df -h`                           |
| Directory usage           | `du -sh`                          |
| Real-time performance     | `top`                             |
| Storage I/O statistics    | `iostat -x`                       |
| IP address                | `ip addr`                         |
| Hostname                  | `hostname`                        |
| DNS lookup                | `nslookup`                        |
| Network reachability      | `ping`                            |
| Remote connection         | `ssh`                             |
| Remote file copy          | `scp`                             |
| Kernel modules            | `lsmod`                           |
| Service status            | `systemctl status`                |
| Package installation      | `yum install` / `apt-get install` |
| Linux version             | `cat /etc/os-release`             |

**Linux preparation is complete.**
