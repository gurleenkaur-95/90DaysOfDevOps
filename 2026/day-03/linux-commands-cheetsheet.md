----------------------PROCESS MANAGEMENT COMMANDS  ---------------------

used to view, monitor, control, and terminate running programs (processes). Process management means:



| Command                        | Use                                              |
| ------------------------------ | ----------------------------------------------------- |
| `ps`                          | Show running processes on current terminal            |
| `ps -ef`                   | Show all processes with full details like snapshop       |
| `ps aux`                       |  show processes using CPU and RAM                     |
| `top`                          | Live monitoring of processes                          |
| `htop`                         | like top , but detailed and interactive monitoring    |
| `pidof <process name>`         | Get the Process ID (PID).                             |
| `pgrep <process name>`         | show PID (sort of search, filter etc)                 |
| `pstree`                       | Show processes in a tree hierarchy.                   |
| `jobs`                         | List background jobs in the current shell.            |
| `bg`                           | Resume a stopped job in the background.               |
| `fg`                           | Bring a background job to the foreground.             |
| `&`                            | Run a command in the background.                      |
| `nohup <command> &`            | Keep a process running after logout.                  |
| `kill <PID>`                   | Gracefully terminate a process.                       |
| `kill -9 <PID>`                | Forcefully kill a process.                            |
| `killall <process>`            | Kill all processes with the same name.                |
| `pkill <process>`              | Kill processes by name or pattern.                    |
| `nice -n <priority> <command>` | Start a process with a specific priority.             |
| `renice <priority> -p <PID>`   | Change priority of a running process.                 |
| `free -h`                      | View memory usage.                                    |
| `vmstat`                       | Display CPU, memory, and process statistics.          |
| `uptime`                       | Show system uptime and load average.                  |
| `lsof -p <PID>`                | List files opened by a process.                       |
| `lsof -i :<port>`              | Find which process is using a port.                   |
| `netstat -tulnp` | network ports are open on your system & what applications are listening to them
| `ss -tulnp`                    | Modern replacement for `netstat` which is faster      |
| `watch <command>`              | Run a command repeatedly and show live updates.       |
| `strace -p <PID>`              | Trace system calls of a running process.              |
| `time <command>`               | Measure execution time of a command.                  |
| `xargs`                        | Pass output from one command as arguments to another. |





-------------------------- FILE SYSTEM COMMANDS -------------------------

used to create, view, organize, copy, move, rename, and delete files and directories (folders).

 

| Command          | Use                             |
| ---------------- | ---------------------------------- |
| `pwd`            | Show current directory.            |
| `ls`             | List files and folders.            |
| `cd`             | Change directory.                  |
| `mkdir`          | Create a directory.                |
| `touch`          | Create a file.                     |
| `cp`             | Copy files/directories.            |
| `mv`             | Move or rename files.              |
| `rm`             | Delete files/directories.          |
| `cat`            | View file contents.                |
| `head`           | View first lines of a file.        |
| `tail`           | View last lines of a file/log.     |
| `tail -f`        | Monitor logs in real time.         |
| `find`           | Search for files.                  |
| `grep`           | Search text inside files.          |
| `chmod`          | Change file permissions.           |
| `chown`          | Change file ownership.             |
| `ps`             | View running processes.            |
| `top`            | Monitor processes live.            |
| `kill`           | Stop a process.                    |
| `df -h`          | Check disk space.                  |
| `du -sh`         | Check folder size.                 |
| `free -h`        | Check RAM usage.                   |
| `ping`           | Test network connectivity.         |
| `curl`           | Test APIs or websites.             |
| `ss -tulnp`      | Check listening ports.             |
| `history`        | View previously executed commands. |
| `clear`          | Clear the terminal screen.         |
| `man`            | Open a command's manual.           |
| `command --help` | Show help for a command.           |





---------------------------  NETWORKING COMMANDS  ---------------------------

used to check, configure, and troubleshoot network connections between your computer and other devices or servers.



| Command          | Use                                                |
| ---------------- | ----------------------------------------------------- |
| `ping`           | Check if a server or website is reachable.            |
| `curl`           | Test APIs and websites; fetch web content.            |
| `wget`           | Download files from the internet.                     |
| `ip a`           | Show IP addresses of your machine.                    |
| `ip route`       | Show the routing table (network routes).              |
| `ss -tulnp`      | Show listening ports and the processes using them.    |
| `netstat -tulnp` | Show network connections (older alternative to `ss`). |
| `nslookup`       | Find the IP address of a domain.                      |
| `dig`            | Query detailed DNS information.                       |
| `hostname`       | Display the system's hostname.                        |
| `hostname -I`    | Display the machine's IP address.                     |
| `traceroute`     | Show the path packets take to reach a destination.    |



------------------------------------- SERVICE COMMANDS -----------------------------------

Service commands (systemctl) are used to manage background services (daemons) running on Linux.
example of services:-
nginx → web server
docker → container service
ssh → remote access service
mysql → database service

| Command                               | Use                                      |
| ------------------------------------- | ---------------------------------------- |
| `systemctl status <service>`          | Check if service is running              |
| `systemctl start <service>`           | Start service now                        |
| `systemctl stop <service>`            | Stop service now                         |
| `systemctl restart <service>`         | Restart service                          |
| `systemctl reload <service>`          | Reload config without stopping           |
| `systemctl enable <service>`          | Start service automatically after reboot |
| `systemctl disable <service>`         | Remove auto-start after reboot           |
| `systemctl list-units --type=service` | see all running services                 |



----------------------------- LOGS COMMANDS -------------------------------

Log commands are used to view, monitor, and troubleshoot system/application events. Logs help find errors, failures, warnings, and service activity. 
Simple rule:
Status tells you "what happened"; logs tell you "why it happened".
When used in DevOps:
Service not starting → check logs
Application crashed → find error message
Server issue → check system logs
Debug deployment failures (Docker, Kubernetes, CI/CD)

| Command                   | Use                             |
| ------------------------- | --------------------------------- |
| `journalctl`              | View systemd logs                 |
| `journalctl -u <service>` | View logs of a specific service   |
| `journalctl -f`           | Follow logs live (like `tail -f`) |
| `journalctl -n 50`        | Show last 50 log entries          |
| `dmesg`                   | View kernel/hardware logs         |
| `tail -f <file>`          | Monitor a log file live           |
| `cat <logfile>`           | Read a log file                   |
| `grep <word> <logfile>`   | Search inside logs                |
