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
 
 ***sleep 500***


