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


