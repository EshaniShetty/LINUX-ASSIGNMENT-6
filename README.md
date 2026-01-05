# LINUX-ASSIGNMENT-6
Linux Programming Assignment 6: Advanced directory management, hidden file handling, permission troubleshooting, and complex command pipelining using find and tee.

Overview
This repository focuses on practical directory operations, file attribute analysis, and the construction of advanced command pipelines for system administration.

Topics & Commands Covered
1. Directory Operations
ls (List): Comprehensive use of the list command to view directory contents.

ls -l: Long format showing permissions, owner, size, and timestamps.


ls -a: Revealing hidden files (those starting with a .) .


mkdir (Make Directory): Creating new directory structures like 123test_dir.

2. File Metadata & Identification
file Command: Determining the actual file type (e.g., ASCII text, directory, or executable) regardless of its extension.


stat Command: Retrieving detailed status information including Inode numbers, links, and exact access/modify/change times .

3. Permission Troubleshooting
A step-by-step workflow for resolving "Permission Denied" errors when executing scripts:

Check: Use ls -l to identify current permission strings (e.g., -rw-r--r--).

Identify: Use whoami to see if you are the owner, group member, or other.

Grant: Use chmod u+x (owner), chmod g+x (group), or chmod +x (all) to add execute permissions.

Verify: Re-run ls -l to confirm the x attribute is present.

4. Advanced Command Pipelining
Designing complex pipelines to automate system tasks. A key example included is searching for modified logs:

Scenario: Find all .log files in /var/log modified within the last 2 days and save the list while viewing it.

Command: find /var/log -name "*.log" -mtime -2 | tee recent_logs.txt
