# FILE OWNERSHIP  
--------------------------------------------

## User Created   
- tokyo
- berlin 
- professor
- nairobi 


## Groups Created    
- tech-team
- vault-team
- heist-team 


## Files and Directories Created   
- devops-file.txt
- app-logs/
- bank-heist/access-codes.txt
- bank-heist/blueprints.pdf
- bank-heist/escape-plan.txt
- heist-project/plans/strategy.conf
- heist-project/vault/gold.txt
- project-config.yml
- team-notes.txt  


## Understanding Ownership    
- Create file devops-file.txt
- Check current owner: ls -l devops-file.txt
- Change owner to berlin
- Verify the changes

![alt text](<images/ex-1 - task 1 of day 11.png>) 


## Basic chown Operations  
- Create file devops.txt
- Check current owner: ls -l devops.txt
- Change owner to tokyo (create user if needed)
- Change owner to berlin
- Verify the changes

![alt text](<images/day-11-01 task2.jpg>)


## Basic chgrp Operations  
- Create file team-notes.txt
- Check current group: ls -l team-notes.txt
- Create group: sudo groupadd heist-team
- Change file group to heist-team
- Verify the change

![alt text](<images/day11-03 task4.jpg>)


##  Combined Owner & Group Change  
Using chown you can change both owner and group together:
- Create file project-config.yaml
- Change owner to professor AND group to heist-team (one command)
- Create directory app-logs/
- Change its owner to berlin and group to heist-team 

![alt text](<images/day11-03 task4.jpg>)


## Recursive Ownership  
- Create directory structure:
mkdir -p heist-project/vault
mkdir -p heist-project/plans
touch heist-project/vault/gold.txt
touch heist-project/plans/strategy.conf
- Create group planners: sudo groupadd planners
- Change ownership of entire heist-project/ directory:
Owner: professor
Group: planners
- Use recursive flag (-R)
- Verify all files and subdirectories changed: ls -lR heist-project/

![alt text](<images/day11-04 task5 part 1.jpg>)
![alt text](<images/day11-05 task 5 part 2.jpg>)


## Practice Challenge  
- Create users: tokyo, berlin, nairobi (if not already created)
- Create groups: vault-team, tech-team
- Create directory: bank-heist/
Create 3 files inside:
touch bank-heist/access-codes.txt
touch bank-heist/blueprints.pdf
touch bank-heist/escape-plan.txt
- Set different ownership:
access-codes.txt → owner: tokyo, group: vault-team
blueprints.pdf → owner: berlin, group: tech-team
escape-plan.txt → owner: nairobi, group: vault-team
- Verify: ls -l bank-heist/

![alt text](<images/day11-06 task6.jpg>)  




