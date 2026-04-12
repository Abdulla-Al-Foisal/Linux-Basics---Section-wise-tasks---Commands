# Linux-Basics---Section-wise-tasks---Commands

## Objective
The objective of this project is to gain a foundational understanding of Linux operating systems, including system navigation, file management, user administration, permissions and system monitoring. This project focuses on building practical command-line skills essential for IT support and cybersecurity roles.

### Skills Learned

•	Understanding Linux architecture and distributions 
•	Command-line navigation and file handling 
•	User and group management 
•	File permissions and security concepts 
•	System monitoring and troubleshooting 
•	Basic Linux administration skills

### Tools Used

Tools Used:
•	Linux OS -kali
•	Terminal (Bash Shell)
•	Virtual Box

## Steps

Section 1: What is Linux?

Technically, Linux is a Kernel the core component that manages hardware resources. Linux is an open-source operating system based on Unix. It is widely used in servers, cybersecurity, cloud computing and embedded systems. 

Section 2: Linux Distributions 

Linux Distributions are different versions of Linux with customized tools and interfaces.

Examples:

•	Ubuntu 
•	Kali Linux
•	CentOS / Red Hat 
•	Parrot OS
•	Rocky Linux 

Section 3: Linux vs Windows 

Topic			             Windows				          Linux Command
View Processes	     Task Manager		      	top, htop, ps aux
Manage Services   	 services.msc			      systenct1  start/stop/status
File System		       C: D: E: 			        Single tree ‘/’ hierarchy
Users 			         Local/Domain		        Strict least privilege – UID/GID
Run Admin Jobs 	     Run as Admin			      sudo  <command>


Section 4: Linux File System & Navigation


Task 1 - Explore root directory

ls / 
<img width="624" height="418" alt="image" src="https://github.com/user-attachments/assets/67722561-4d47-4ca0-82ef-b8bd07df6a99" />


Task 2 - Move between directories

cd /home
cd /var/log
cd - 
pwd     (Show current location)

<img width="624" height="434" alt="image" src="https://github.com/user-attachments/assets/f5ae0dc2-103c-4c2d-b819-ec239953e9d3" />

Important Directories
/home - user personal data
/var/log - system logs
/etc - config files
/bin , /sbin - system binaries
/tmp - temporary files

Section 5: Files & Directories Operations

Task 1 - Create a file

touch ms.txt
<img width="624" height="474" alt="image" src="https://github.com/user-attachments/assets/ac63775d-d1ee-455f-9b7f-f4b91bfd9f70" />

Task 2 - Write/Edit a file

nano ms.txt
<img width="570" height="456" alt="image" src="https://github.com/user-attachments/assets/d0f69172-02c2-4d44-bf6e-1ee0e7d3c982" />

Task 3 - View file content

cat ms.txt
head ms.txt       (Prints only first 10 lines )
tail -f /var/log/syslog   (real time logs)
less ms.txt           (scroll page wise)


Task 4 - Ctreate/Delete Drectories

mkdir ms  (root user)
sudo mkdir ms  (from sudo user)
mkdir -p parent/child      (recursive)
rm -r ms   (delete folder)
rmdir ms   (delete directory)
<img width="624" height="416" alt="image" src="https://github.com/user-attachments/assets/dfbe709a-7076-4c6b-959b-ab4888908ac4" />

Task 5 - Copy/Delete Directories

cp file1.txt file2.txt
mv file1.txt /var/log/
rm unwanted.txt

Section 6: Users, Groups & sudo Privileges

Task 1 - Identify current user & users List

whoami
cat /etc/passwd    (All User)
cat /etc/group     (All Group)
<img width="624" height="494" alt="image" src="https://github.com/user-attachments/assets/d5e4a909-e44b-4863-af1b-558af605592d" />

Task 2 - Create a user & add to sudo group

sudo adduser john
sudo usermod -aG sudo john
<img width="533" height="541" alt="image" src="https://github.com/user-attachments/assets/01dc9af0-27c5-4d68-8f15-0fff87115aa3" />

Task 3 - Switch user
su -john

Task 4 - Verify sudo access
sudo apt install nmap

Section 7 - File Permissions & Ownership

Permission Concept 
r - read 
w - write
x - execute

Task 1 - Check File Permissions
ls -l

Task 2 - Change Permissions

chmod 777 ms.txt  (rwx rwx rwx)
chmod 755 ms.txt  (rwx r-x r-x)
chmod 644 ms.txt  (rw- r-- r--)

Task 3 - Chnage ownership
sudo chown john:john ms.txt

Section 8 - System Monitoring -(CPU, RAM, DISK, NETWORK)

Cpu & Process Monitoring
top
htop
ps aux
<img width="624" height="455" alt="image" src="https://github.com/user-attachments/assets/a1097911-2e16-48b3-a52e-6b3d8720b617" />

Memory Monitoring
free -h 
<img width="624" height="458" alt="image" src="https://github.com/user-attachments/assets/17693d2c-be71-4ef0-8f15-02cc3265d26a" />


Disk Usage
df -h
du -sh /var/log/*

Network Monitoring

ip a
netstat -tulnp
ss -tulnp    
<img width="624" height="196" alt="image" src="https://github.com/user-attachments/assets/33c8765b-36bb-4f43-bc1e-243e5088efa8" />



## Outcome
After completing this project, I gained practical experience in Linux system operations, including file management, user administration, and system monitoring. I developed confidence in using the Linux command line, which is essential for roles in IT support, system administration, and cybersecurity.

