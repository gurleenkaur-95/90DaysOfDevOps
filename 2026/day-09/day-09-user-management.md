# LINUX USER AND GROUP MANAGEMENT 
------------------------------------------- 

## Users created 
Users are created by `sudo useradd -m <username>`  
users : tokyo, berlin, professor  
checked by `cat /etc/passwd` 

![user added](<images/day9-01 user created.jpg>)

## Home directories of users  
Checked by `ls -l /home`  

![home directories of user](<images/day9-02 home directories.jpg>)

## Group created  
Command : `sudo groupadd <groupname>` 
Groups : Developers, Admin  
Checked by `cat /etc/group`    

## Add users to groups  
Command : `sudo gpasswd -a <user> <groupname>`  

![assign users to group](<images/day9-03 add users to groups.jpg>)  

## Group changed of new file dev-project  
Command : `sudo chgrp <groupname> <filename>`  

![group changed](<images/day9-04 group chnaged.jpg>)  

## Other users can create files in new group : Shared Directory  
- Create directory: /opt/dev-project
- Set group owner to developers
- Set permissions to 775 (rwxrwxr-x)
- Test by creating files as tokyo and berlin  
To Switch into new user : `su <username>`  

 ![others](<images/day9-05 other users create file.jpg>)   


## Team workspace    
- Create user nairobi with home directory
- Create group project-team
- Add nairobi and tokyo to project-team
- Create /opt/team-workspace directory
- Set group to project-team, permissions to 775
- Test by creating file as nairobi

![shared directory](<images/day9-06 nairobi created file in team-workspace.jpg>)

