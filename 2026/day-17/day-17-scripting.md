# Shell Scripting: Loops, Arguments & Error Handling
--------------------------------------------
## Task 1: For Loop  

1. Create for_loop.sh that:
- Loops through a list of 5 fruits and prints each one

Code: 
![alt text](<images/day17 task1 -1 code.png>)

Output:
![alt text](<images/day17 task1 -1.png>)

2. Create count.sh that:
- Prints numbers 1 to 10 using a for loop

Code:
![alt text](<images/day17 task1 -2 code.png>)

Output:
![alt text](<images/day17 task1 -2 .png>)

--------------------------------------------

## Task 2: While Loop 

1. Create countdown.sh that:
- Takes a number from the user
- Counts down to 0 using a while loop
- Prints "Done!" at the end

Code:
![alt text](<images/day17 task2 code.png>)

Output:
![alt text](<images/day17 task2.png>)

--------------------------------------------

## Task 3: Command-Line Arguments  

1. Create greet.sh that:
- Accepts a name as $1
- Prints Hello, <name>!
- If no argument is passed, prints "Usage: ./greet.sh "

Code: 
![alt text](<images/day17 task3 -1 code.png>)

Output:
![alt text](<images/day17 task3 -1.png>)

2. Create args_demo.sh that:
- Prints total number of arguments ($#)
- Prints all arguments ($@)
- Prints the script name ($0)

Code:
![alt text](<images/day17 task3 -2 code.png>)

Output:
![alt text](<images/day17 task3 -2.png>)

--------------------------------------------

## Task 4: Install Packages via Script  

1. Create install_packages.sh that:
- Defines a list of packages: nginx, curl, wget
- Loops through the list
- Checks if each package is installed (use dpkg -s or rpm -q)
- Installs it if missing, skips if already present
- Prints status for each package

Code:
![alt text](<images/day17 task4 code.png>)

Output:
![alt text](<images/day17 task4.png>)

--------------------------------------------

## Task 5: Error Handling

1. Create safe_script.sh that:
- Uses set -e at the top (exit on error)
- Tries to create a directory /tmp/devops-test
- Tries to navigate into it
- Creates a file inside
- Uses || operator to print an error if any step fails

Code:
![alt text](<images/day17 task5 -1 code.png>)

Output:
![alt text](<images/day17 task5 -1.png>)


2. Modify your install_packages.sh to check if the script is being run as root — exit with a message if not

Code:
![alt text](<images/day17 task5 -2 code.png>)

Output:
![alt text](<images/day17 task5 -2.png>) 

--------------------------------------------

## What I have learned :

1. The environment where I run a command matters because the available commands, permissions, file system, and behavior can be different
- **Ubuntu WSL**: My main Linux environment for practicing Linux commands and shell scripting. It behaves like a real Linux system.
- **Git Bash (MINGW64)**: Useful for Git, SSH, and SCP on Windows, but it is not a complete Linux environment.
- **PowerShell / Windows Terminal**: Mainly used to run Windows commands and start/manage WSL. It is different from Linux shells. but we can run ubuntu here by `wsl -d ubuntu` then `cd~` and we will be in linux environment.
- **EC2 Ubuntu**: A real remote Linux server in AWS, useful for practicing server-related tasks like systemctl, journalctl, Nginx, and troubleshooting.
- **/mnt/c/... in WSL**: This means I am working with files stored on the Windows C: drive, so some Linux features like chmod may behave differently.
- **/home/lenovo in WSL**: This is the Linux filesystem, where Linux permissions and commands work more naturally.

2. Difference between these operators
- **||** → run the next command if the previous command fails.
- **&&** → run the next command if the previous command succeeds.

3. Some commands that i learned-
- **Error handling**
`set -e` → stops the script when a command fails.
`exit 1` → exits with an error status.
`$?` → shows the previous command's exit status.
- **Root checking**
`$EUID` → gives the effective user ID.
`0` → root.
`$EUID -ne 0` → current user is not root.
- **Package management**
`dpkg -s package` → checks whether a package is installed.
`apt install package` → installs a package.
- **Command output**
`>/dev/null` → hides normal output.
`2>&1` → sends error output to the same place as normal output.

