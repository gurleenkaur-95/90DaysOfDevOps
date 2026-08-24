# SHELL SCRIPTING BASICS
--------------------------------------------

## Task 1: My First Script  
Create a file hello.sh
Add the shebang line #!/bin/bash at the top
Print Hello, DevOps! using echo
Make it executable and run it

![alt text](<images/day16 task1 code.png>)![alt text](<images/day16 task1.png>)

- What happens if I remove the shebang line?
Ans : If we remove the shebang line, the script no longer tells the system which interpreter should run it. The script may still run, but it can cause errors or behave differently depending on how it is executed. 


## Task 2: Variables  
Create variables.sh with:
A variable for your NAME
A variable for your ROLE (e.g., "DevOps Engineer")
Print: Hello, I am <NAME> and I am a <ROLE>

![alt text](<images/day16 task2 code.png>)
![alt text](<images/day16 task2.png>)

- Try using single quotes vs double quotes ; what's the difference?
Ans : Using double quote " " - The variables and commands are evaluated.
Using single quote ' ' - Everything inside is taken literally, no evaluation happens


## Task 3: User Input with read  
Create greet.sh that:
Asks the user for their name using read
Asks for their favourite tool
Prints: Hello <name>, your favourite tool is <tool>

![alt text](<images/day16 task3 code.png>)
![alt text](<images/day16 task3.png>)


## Task 4: If-Else Conditions  
1. Create check_number.sh that:
Takes a number using read
Prints whether it is positive, negative, or zero

![alt text](<images/day16 task4 -1 code.png>)
![alt text](<images/day16 task4 -1.png>)

2. Create file_check.sh that:
Asks for a filename
Checks if the file exists using -f
Prints appropriate message

![alt text](<images/day16 task4 -2 code.png>)
![alt text](<images/day16 task4 -2.png>)


## Task 5: Combine It All  
Create server_check.sh that:
Stores a service name in a variable (e.g., nginx, sshd)
Asks the user: "Do you want to check the status? (y/n)"
If y — runs systemctl status <service> and prints whether it's active or not
If n — prints "Skipped."

![alt text](<images/day16 task5 code.png>)
![alt text](<images/day16 task5.png>)

