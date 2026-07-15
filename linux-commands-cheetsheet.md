----------------------PROCESS MANAGEMENT COMMANDS  ---------------------
used to view, monitor, control, and terminate running programs (processes). Process management means:



| Command                        | Usage                                                 |
| ------------------------------ | ----------------------------------------------------- |
| `ps`                           | Show running processes on current terminal            |
| `ps -ef`                       | Show all processes with full details.                 |
| `ps aux`                       | Display all running processes (common format).        |
| `top`                          | Monitor running processes in real time.               |
| `htop`                         | Interactive process viewer (better than `top`).       |
| `pidof <process name>`         | Get the Process ID (PID).                             |
| `pgrep <process name>`         | Find PID by process name.                             |
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
| `netstat -tulnp`               | network ports are open on your system & what applications are listening to them
| `ss -tulnp`                    | Modern replacement for `netstat` which is faster      |
| `watch <command>`              | Run a command repeatedly and show live updates.       |
| `strace -p <PID>`              | Trace system calls of a running process.              |
| `time <command>`               | Measure execution time of a command.                  |
| `xargs`                        | Pass output from one command as arguments to another. |





-------------------------- FILE SYSTEM COMMANDS -------------------------
used to create, view, organize, copy, move, rename, and delete files and directories (folders).

 

| Command          | Usage                              |
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



| Command          | Usage                                                 |
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



