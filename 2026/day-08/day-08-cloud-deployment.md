# DEPLOY A REAL WEB SEREVER ON AWS CLOUD 
--------------------------------------------------------------

Step 1 : Launch an instance from AWS console  
Step 2 : Connect to instance using ssh  
Command : `ssh -i "demo-key.pem" ubuntu@ec2-35-88-107-136.us-west-2.compute.amazonaws.com`  
Step 3 : To update system  
Command : `sudo apt update` and then `sudo apt upgrade`  
Step 4 : Install Nginx  
Command : `sudo apt install nginx`  
Step 5 : Install docker  
Command : `sudo apt install docker.io`  
Step 6 : Configure security groups for web access. From the AWS console, go to the security group and add an inbound rule for port 80 (default for Nginx)    
Step 7 : Check logs of nginx servise  
Command : `journalctl -u nginx`  
Step 8 : Save the logs file first into a new folder called nginx-logs.txt  
Command :  `journalctl -u nginx > ~/nginx-logs.txt`  
Step 9 : Save logs to file into your laptop (exit ec2 and enter in new terminal) 
Commad : `scp -i "demo-key.pem" ubuntu@35.88.107.136:~/nginx-logs.txt .` 
  
## CHALLANGES FACED 
--------------------------------------------------------------
  
*Challange* : scp gave the error “No such file or directory” because nginx-logs.txt had not been created on the EC2 server.  
*Solution*: I created the log file using: journalctl -u nginx > ~/nginx-logs.txt  
Then I used scp to download the file to my local machine.  
  

## WHAT I LEARNED  
------------------------------------------------------------- 
  
- Connect to an AWS cloud instance using SSH    
- How to manage security group (adding inbound rules)  
- How to install Nginx and serve a webpage  
- The importance of reloading a service after configuration changes or adding new files  
- How to transfer files securely from the instance to the local machine using scp  