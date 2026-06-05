#### **File and Directory Management:**

- `ls` – List directory contents.
	- `-l` – List in long format (detailed view).
	- `-a` – Show hidden files (those starting with a dot `.`).
	- `-h` – Human-readable file sizes (works with `-l`).
	- `-R` – List directories and subdirectories recursively.
	- `-t` – Sort by modification time.
	- `-S` – Sort by file size.
- `cd` – Change directory.
- `pwd` – Print working directory.
- `mkdir` – Create a new directory.
- `rmdir` – Remove an empty directory.
- `rm` – Remove files or directories.
- `cp` – Copy files or directories.
- `mv` – Move or rename files or directories.
- `cat` – Concatenate and display file content.
- `more` – View file contents one page at a time.
- `head` – Display the first few lines of a file.
- `tail` – Display the last few lines of a file.
- `chmod` – Change file permissions.
- `chown` – Change file owner and group.
- `chgrp` – Change the group ownership of a file or directory.
- `touch` – Create a new empty file or update the timestamp of an existing file.
- `find` – Search for files in a directory hierarchy.
- `ln` – Create hard and symbolic links.
    - Example: `ln -s /path/to/file link_name`


#### **Text Processing and Editing:**

- `echo` – Display a message or variable value.
- `man` – Display the manual (help) for a command.
- `nano` – Text editor in the terminal.
- `vim` – Another text editor in the terminal.
- `grep` – Search for patterns in a file.
- `sort` – Sort lines of text in a file.
- `uniq` – Report or omit repeated lines in a file.
- `cut` – Remove sections from each line of a file.
- `tr` – Translate or delete characters from a stream of text.
- `wc` – Count the number of lines, words, and characters in a file.
- `tee` – Read from standard input and write to standard output and files.

#### **System Management:**

- `ps` – Display current running processes.
- `top` – Display real-time system processes.
- `kill` – Terminate processes.
- `uptime` – Show how long the system has been running.
- `whoami` – Display the current logged-in user.
- `last` – Show the last logins to the system.
- `id` – Display user and group ID information.
- `hostname` – Show or set the system’s hostname.
- `shutdown -h now` – Shut down the system immediately.
- `shutdown -r now` – Reboot the system immediately.
- `reboot` – Reboot the system.
- `poweroff` – Power off the system.
- `halt` – Halt the system immediately.
- `exit` – Exit the shell.
- `alias` – Define or display aliases for commands.
- `history` – Show command history.

#### **Networking and Remote Access:**

- `ping` – Send ICMP echo requests to a network host.
- `netstat` – Display network connections, routing tables, and interface statistics.
- `ssh` – Securely connect to a remote server via SSH.
- `scp` – Securely copy files between hosts over SSH.
- `rsync` – Efficiently sync files and directories between locations.
- `ip` – Show or manipulate routing, devices, and tunnels.
- `ifconfig` – Display network interface configuration.
- `hostname` – Show or set the system’s hostname.
- `iostat` – Report CPU and I/O statistics.
- `lsof` – List open files.
    - Example: `lsof -i :8080`

#### **Disk and File System Management:**
- `df` – Show disk space usage.
    - Example: `df -h`  
- `du` – Show disk usage of files and directories.
    - Example: `du -sh folder_name`
- `lsblk` – List information about block devices.
- `mount` – Mount a filesystem.
    - Example: `sudo mount /dev/sdb1 /mnt/usb`
- `umount` – Unmount a filesystem.
    - Example: `sudo umount /mnt/usb`
- `fdisk` – Partition a disk.
- `blkid` – Find the block device attributes.

#### **Package Management (Distro-Specific):**

- `apt-get` – Package management for Debian-based distributions (like Ubuntu).
    - Example: `sudo apt-get install package_name`
- `yum` – Package management for Red Hat-based distributions (like CentOS).
    - Example: `sudo yum install package_name`
- `dpkg` – Low-level package manager for Debian-based systems.
    - Example: `sudo dpkg -i package.deb`
- `chkconfig` – Check or configure system services on Red Hat-based systems.

#### **System and Service Control:**

- `systemctl` – Control the `systemd` system and service manager.
    - Example: `systemctl restart apache2`
- `journalctl` – View system logs (on systems using `systemd`).
    - Example: `journalctl -xe`

#### **Archiving and Compression:**

- `tar` – Archive files or directories.
    - Example: `tar -czvf archive.tar.gz folder_name`
- `gzip` – Compress files using the gzip compression.
    - Example: `gzip file.txt`
- `bzip2` – Compress files using the bzip2 compression.
    - Example: `bzip2 file.txt`
- `xz` – Compress files using the xz compression.
    - Example: `xz file.txt`
- `unzip` – Extract files from a ZIP archive.
    - Example: `unzip file.zip`

#### **File and Directory Permissions:**

- `chmod` – Change file permissions.
    - Example: `chmod 755 file.sh`
- `chown` – Change file owner and group.
    - Example: `chown user:group file.txt`
- `chgrp` – Change the group ownership of a file or directory.


#### **Time and Date:**

- `date` – Display or set the system date and time.
    - Example: `date`
- `time` – Measure the time taken for a command to execute.
    - Example: `time ls`

#### **Command Execution and Monitoring:**

- `watch` – Execute a command repeatedly and show output.
    - Example: `watch -n 5 df -h` (refresh `df -h` every 5 seconds)
- `sudo` – Execute a command as a superuser.
    - Example: `sudo apt update`
- `alias` – Define or display aliases for commands.
    - Example: `alias ll='ls -la'`

#### **Miscellaneous:**

- `who` – Show who is logged in and what they are doing.
- `uptime` – Show how long the system has been running.
- `last` – Show the last logins to the system.
- `iostat` – Report CPU and I/O statistics.