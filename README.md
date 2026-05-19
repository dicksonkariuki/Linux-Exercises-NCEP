# Linux-Exercises-NCEP
This repository contains Linux practical exercises for Cloud &amp;DevOps Engineers
# Task 1 Create Project Structure
Create this structure:
/home/ubuntu/devops-project
├── logs
├── backups
├── scripts
├── configs
└── temp

***/home/ubuntu/mkdir -p devops-projects/{logs,backups,scripts,configs,temp}***

# Task 2 add files 

***touch app.log***

***touch deploy.sh***

***touch app.conf***

# Task 3 add sample content

***INFO server started***

***WARNING disk almost full***

***ERROR database connection failed***

***INFO user login successful***
# Task 4 copy backup 

***cp app.conf backups***

# Part 2 File Viewing and Log Investigation
# Task 5 Investigating logs  

Using Linux commands:
Find:
ERROR entries
WARNING entries
In the app.log created above

***grep "ERROR" app.log***

***grep "WARNING" app.log***

# Task 6 — Monitor Logs Live
Use a command that continuously watches:
app.log

***tail -f app.log***

***less +f app.log*** (for scrolling many logs)

# Part 3 Permissions & Ownership

Task 7 — Script Permissions
Make:
deploy.sh

executable.

***chmod +x deploy.sh***

Task 8 — Secure Config File (configs/app.conf)
Set permissions so:
owner can read/write
nobody else has access

***chmod 600 configs/app.conf***

Task 9 — Explain Permissions
Explain:

***755-owner can read write execute,group can read and execute ,others can read and execute***

***644-Owner can read and write,group can read,others can read***

***600-Owner can read write,group & others no permissions***

# Part 4 Process Management
Task 10 — Start Background Process
Run:
sleep 500

in the background.

***sleep 500***

Task 11 — Identify Process
Find:
PID
process name
Of the above process
 
 *** ps aux | greep sleep***

 ***PID 3471***

 ***sleep 500***

 Task 12 — Terminate Process
Stop the above process safely.

***kill 3471***

Task 13 — Monitor System
Use commands to:
check running processes
identify CPU usage
identify memory usage

***top ,htop,psaux***

***free -h***

# Part 5 Networking and Connectivity 

Task 14 — Find Server IP
Display:
IP address
hostname

***ip -a***

***whoami***

Task 15 — Test Connectivity
Verify internet access of your  linux machines.

***ping host***

Task 16 — Verify Listening Ports
Confirm:
SSH service
web server
are listening on ports.

***sudo ss -tlnp | grep :22***

***sudo ss -tlnp | grep -E ':80|:443'***

# Part 6 SSH & SCP
Task 17 — Remote Access (Local to Remote)

Use AWS Educate Account (Sign up if you don't have one)
Create an EC2 Linux instance (ubuntu)
Create a Security Group allowing SSH (port 22)
.pem key pair downloaded

Also note its public ip
From your linux pc:
Securely (using the downloaded .pem) SSH into EC2 linux instance.
ssh -i your-key.pem ubuntu@public-ip

***ssh -i "dickson.pem" ubuntu@ec2-3-137-171-248.us-east-2.compute.amazonaws.com***

Task 18 — Secure File Transfer
Recursively upload the above working folder to the remote EC2 instance.

scp -i your-key.pem -r /path/to/local-folder ubuntu@ec2-public-ip:/home/ubuntu

Task 19 — Retrieve File (Remote to Local)
Download the following file from the remote EC2 instance to a new local folder
app.log

Hint
scp -i your-key.pem user@ec2-ip:/path/to/remote/file /path/to/local/destination 

# Part 7 Disk & System Information
Task 20 — Check System Resources
Display:
RAM usage
disk usage
uptime
Linux version

***free -h (RAM usage)

***du sh (disk usage for specific directory)***

***uptime***

***uname -a***







