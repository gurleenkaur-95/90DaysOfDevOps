# Linux Filesystem Hierarchy and scenerio based ques 

In Linux, all files and directories appear under the root directory /, even if they are stored on different physical or virtual devices  

Linux follows a single-root hierarchical file system. Every file, directory, device, and process is part of one unified tree.  

- `/` - Root Directory (The Base of Everything)    
The root directory is the top of the file system. Every other directory exists under it. It contains essential system folders required for booting and operating the system. You normally do not store personal files here. Only the root user has permission to modify contents inside this directory. Regular users cannot make changes here.  

- `/bin` - Essential User Commands  
Contains basic commands required for system operation and user tasks. Example ls, mv, rm, cp, pwd, cat. This is a specific folder stores the ready-to-run applications and commands that keep your computer functioning. The files are written in machine code (1s and 0s) rather than human-readable text. They are compiled programs that the computer processor can understand instantly.  

- `/sbin` - System Administration Commands    
This directory contains commands mainly used by system administrators for system maintenance, booting, and repairs. Examples: systemd, reboot, shutdown, fsck (file system check), mount, iptables. These are essential for system control and maintenance. It require root privileges (sudo) to execute.  

- `/etc`- Configuration Files  
Short for "Editable Text Configuration. It is the central directory that stores all system-wide configuration files. It serves as the "control center" or settings panel for the operating system. It contains plain text files that dictate how the system, services, networks, and user accounts behave. Example Network configuration, User account settings, System startup configuration, Service configuration.  

- `/home` - User Personal Directories  
Every non-root user has a personal directory inside /home. Each user can create, delete, or modify files only in their own home directory. This directory contains Personal files, Documents, Downloads, User configurations, Desktop data.  

- `/root` - Root User Home Directory  
This is the home directory for the root (administrator) user. It is separate from /home for security and system control. Only root user has full access here.  

- `/usr` - User Applications and Programs  
It contains most installed applications and libraries. Software installed using package managers goes here.  
Subdirectories:  
/usr/bin → User programs - Stores executable programs for normal, everyday user tasks    
/usr/sbin → Admin programs - Stores system administration and maintenance utilities intended primarily for the superuser/root  
/usr/lib → Libraries for /usr/bin and /usr/sbin  
/usr/share → Shared files   

- `/var` - Variable Data (Frequently Changing)
This directory contains data that changes frequently.  
Examples:  
Log files → /var/log  
Mail data → /var/mail  
Cache → /var/cache  
Spool → /var/spool  
When debugging system issues, logs inside /var/log are very important.  

- `/tmp` - Temporary Files  
Temporary files created by programs are stored here. Files may be deleted automatically. Used by applications for temporary processing.  

- `/dev` - Device Files
In Linux, hardware devices are represented as files. This design allows Linux to treat devices like regular files.  
Examples:  
/dev/sda → Hard disk  
/dev/tty → Terminal  
/dev/null → Null device  
/dev/usb → USB device  

- `/proc` - Process and Kernel Information
/proc is a virtual file system. It does not store real files. It provides detailed information about system processes. System monitoring tools use this directory. It contains runtime system information such as: Running processes, CPU usage, Memory usage, Kernel parameters.  
Example:  
/proc/cpuinfo → CPU details  
/proc/meminfo → Memory status  

- `/sys` - System and Hardware Information
Another virtual file system used for hardware and kernel interaction. Used by system tools to manage Devices, Drivers, Kernel modules.  

- `/opt` - Optional  
Third-party software and packages not part of the default system installation are stored in /opt. It includes their configuration and data files.  

- `/lib` - Library  
It Contains the essential building blocks that the operating system needs to start up and run that means these include dynamic libraries needed during runtime Inside this, there are Shared Libraries (.so files) which is core code that basic commands (like ls to list files) need to function, and Drivers (/lib/modules) which are hidden files that help your computer talk to your hardware, like your keyboard, mouse, and screen.  

- `/boot` - 
This directory stores all files required for booting the system. The Linux boot process follows six main stages:    
1. BIOS / UEFI: Powers on the hardware, runs the Power-On Self-Test (POST), and locates the bootable storage drive.  
2. MBR / EFI: Reads the boot sector or EFI system partition to find and start the bootloader.
MBR (Master Boot Record) which is older system and EFI Partition is Modern System.  
3. GRUB: Displays the OS menu, lets you choose a kernel, and loads the core Linux system into memory.  
4. Kernel: Decompresses itself, activates core hardware drivers, and mounts the root file system.  
5. systemd: Launches as Process ID 1 (PID 1) to bring up critical background services like network and security.  
6. Login: Displays the final prompt or desktop interface for user sign-in.  

----------------------------------------------------------------------------------------------------  
    
- Scenario 1: Service Not Starting  
A web application service called 'myapp' failed to start after a server reboot.  
What commands would you run to diagnose the issue?  
STEP 1 - ```systemctl status myapp```  
WHY - to check status of myapp if it is running or not  
STEP 2- ```journalctl -u myapp -n 50```  
WHY -  it filters logs of myapp and shows last 50 log lines.  (journalctl for logs, -u for filter, myapp is service, -n 50 is for last 50 count)  
STEP 3 - ```systemctl is-enabled myapp```  
WHY - to check if it is enavled to start on boot or not  


- Scenario 2: High CPU Usage  
Your manager reports that the application server is slow.  
You SSH into the server. What commands would you run to identify  
which process is using high CPU?   
STEP 1 - ```top``` or ```htop```  
WHY - to check live CPU usage. htop is for live data and press q to quit.  
STEP 2 - ```ps aux --sort=-%cpu | head -5```  
WHY - it displays th top 4 CPU consuming processes  
STEP 3 - note the PID of the process  
  
  
- Scenario 3: Finding Service Logs  
A developer asks: "Where are the logs for the 'docker' service?"  
The service is managed by systemd.  
What commands would you use?    
STEP 1 - ```systemctl status docker```  
WHY - to check whether docker is running or not  
STEP 2 - ```journalctl -u docker```  
WHY - to check the logs of docker. add ```-n 5``` to check the laste 5 logs adn ```-f``` to see in real time. for example : journalctl -u docker -n 5 -f   


- Scenario 4: File Permissions Issue  
A script at /home/user/backup.sh is not executing.  
When you run it: ./backup.sh  
You get: "Permission denied"  
What commands would you use to fix this?  
STEP 1 - ```ls -l```  
WHY -  to check the which permissions do file have  
STEP 2 - ```Chmod 764```  
WHY - it will give read write execute permissions to user (because of 7), read write permission to group (because of 6) and read only permission to others (because of 4)  
STWP 3 - verify its permissions by ```ls -l``` and try running it.  







