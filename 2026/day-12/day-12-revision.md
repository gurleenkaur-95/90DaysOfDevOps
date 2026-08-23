# REVISION OF DAY 01-11 
--------------------------------------------
My goal for 2026 is to build a strong career in DevOps. I’m taking it one step at a time through consistent learning, hands-on practice, and building a solid foundation in Linux, automation, and cloud technologies. 

## Process and Services  
When my system hangs or slows down, I use the following commands to troubleshoot and check service health:

`ps aux` → Lists all running processes on the system.

`top`→ Display sorted information about processes.

`systemctl status <service>` → Displays the status of a specific service (whether it’s active, failed, or inactive).

`journalctl -u <service>`→ Displays logs for a specific service, useful for debugging issues.

## File Skills  

I have practiced creating/modifying/permission of Linux file/folder. Here is how to safely change ownership and permissions:
- Check current ownership and permissions
- ls -l /path/to/file
- Change permissions (least privilege principle)
chmod 751 /path/to/file
- Change ownership (user and group)
sudo chown user:group /path/to/file
Example:

![alt text](<../day-11/images/day11-03 task4.jpg>)


## Cheat Sheet
------------------------------------------- 

Commands to be used :-

- `whoami` — Shows the current user
- `hostname` — Shows the hostname of the current Linux machine
- `id` — Shows user ID and groups
- `who` — Shows logged-in users
- `groups` — Shows groups for the current user
- `ls -l` — Shows file permissions and ownership
- `ls -la` — Lists files, including hidden files, with permissions
- `sudo` — Runs a command with elevated privileges
- `pwd` — Shows your current directory
- `cd /path` — Moves to another directory
- `mkdir <foldername>` — Creates a directory.
- `touch <filename.txt>` — Creates an empty file
- `cp <file1.txt> <file2.txt>` — Copies a file
- `mv <file1.txt> <folder/>` — Moves the file keeping its original name <file1.txt> where <folder/> defiles the destination folder 
- `mv <file1.txt> <file2.txt>` - renames the file in the current location
- `rm <filename.txt>` — Deletes a file
- `cat <filename.txt>` — Displays file contents
- `less <filename.txt>` — Opens a large file for easy viewing
- `ps aux` - Lists all running processes with CPU/memory usage
- `mpstat` - Monitors CPU utilization across cores, highlighting bottlenecks or unusual load
- `systemctl stop <servicename>` — Stops a running service
- `systemctl start <servicename>` — Starts a service
- `systemctl list-units --type=service` — Lists currently loaded services and their status.
- `systemctl status <servicename>` - Verifies if a critical service is active, failed, or restarting.
- `systemctl restart <servicename>` - Restart a service
- `systemctl enable <servicename>` - Makes a service start automatically at boot
- `cat /var/log/nginx/error.log` - Reads raw logs for web server errors (replace with relevant service log path).
- `journalctl -u <servicename>` - Retrieves detailed logs for a given service, useful for debugging failures.
- `free -m` - Displays memory usage in MB to check for exhaustion or leaks.
- `top` — Real-time CPU, memory and process monitoring.
- `uptime` — Shows how long the system has been running and system load.
- `df -h` — Checks disk space.
- `du -sh <folder/>` — Shows how much space a folder is using.
- `history` - Shows commands you've previously run
- `pgrep <processname>` — Finds the process ID (PID) of a running process by its name
- `grep "error" app.log` - earches for error inside a file.
- `grep -i "error" /var/log/nginx/error.log` - Searches for errors without caring about uppercase/lowercase.
- `find /var/log -name "*.log"` - Finds .log files
- `kill PID` - Stops a process gracefully
- `kill -9 PID` - Force kill the process
- `chmod <permissions> <filename>` — Changes the permissions of a file or directory.
- `chown <user>:<group> <filename>` — Changes the owner and group of a file or directory
- `tail -f <logfile>` — Continuously displays new lines added to a log file in real time
- `tail -n 50 <filename>` — Displays the last 50 lines of a file
- `journalctl` — Shows all available system logs
- `journalctl -f` — Continuously shows new system log entries as they are generated
- `journalctl -u <servicename> -f` — Continuously displays new logs for a service in real time
- `journalctl -u <servicename>` — Shows logs for a specific service


