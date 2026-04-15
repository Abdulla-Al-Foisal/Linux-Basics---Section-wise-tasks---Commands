# Linux-Basics---Section-wise-tasks---Commands

## Objective
The objective of this project is to gain a foundational understanding of Linux operating systems, including system navigation, file management, user administration, permissions and system monitoring. This project focuses on building practical command-line skills essential for IT support and cybersecurity roles.

### Skills Learned

•	Understanding Linux architecture and distributions <br>
•	Command-line navigation and file handling <br>
•	User and group management <br>
•	File permissions and security concepts <br>
•	System monitoring and troubleshooting <br>
•	Basic Linux administration skills <br>

### Tools Used

Tools Used: <br>
•	Linux OS -kali <br>
•	Terminal (Bash Shell)  <br>
•	Virtual Box   <br>

## Steps

Section 1: What is Linux?

Technically, Linux is a Kernel the core component that manages hardware resources. Linux is an open-source operating system based on Unix. It is widely used in servers, cybersecurity, cloud computing and embedded systems. 

Section 2: Linux Distributions 

Linux Distributions are different versions of Linux with customized tools and interfaces.

Examples:

•	Ubuntu <br>
•	Kali Linux <br>
•	CentOS / Red Hat  <br>
•	Parrot OS <br>
•	Rocky Linux <br>

Section 3: Linux vs Windows 

| Topic | Windows | Linux Command |
| :--- | :--- | :--- |
| **View Processes** | Task Manager | `top`, `htop`, `ps aux` |
| **Manage Services** | `services.msc` | `systemctl start/stop/status` |
| **File System** | C: D: E: | Single tree `/` hierarchy |
| **Users** | Local/Domain | Strict least privilege – UID/GID |
| **Run Admin Jobs** | Run as Admin | `sudo <command>` |

Section 4: Linux File System & Navigation


Task 1 - Explore root directory

ls / <br>
<img width="624" height="418" alt="image" src="https://github.com/user-attachments/assets/67722561-4d47-4ca0-82ef-b8bd07df6a99" />


Task 2 - Move between directories

cd /home  <br>
cd /var/log   <br>
cd -    <br>
pwd     (Show current location) <br>

<img width="624" height="434" alt="image" src="https://github.com/user-attachments/assets/f5ae0dc2-103c-4c2d-b819-ec239953e9d3" />

Important Directories <br>
/home - user personal data   <br>
/var/log - system logs  <br>
/etc - config files <br>
/bin , /sbin - system binaries <br>
/tmp - temporary files 

Section 5: Files & Directories Operations

Task 1 - Create a file

touch ms.txt  <br>
<img width="624" height="474" alt="image" src="https://github.com/user-attachments/assets/ac63775d-d1ee-455f-9b7f-f4b91bfd9f70" />

Task 2 - Write/Edit a file

nano ms.txt   <br>
<img width="570" height="456" alt="image" src="https://github.com/user-attachments/assets/d0f69172-02c2-4d44-bf6e-1ee0e7d3c982" />

Task 3 - View file content

cat ms.txt   <br>
head ms.txt       (Prints only first 10 lines ) <br>
tail -f /var/log/syslog   (real time logs)   <br>
less ms.txt           (scroll page wise) 


Task 4 - Ctreate/Delete Drectories

mkdir ms  (root user) <br>
sudo mkdir ms  (from sudo user)   <br>
mkdir -p parent/child      (recursive)  <br>
rm -r ms   (delete folder)   <br>
rmdir ms   (delete directory)   <br>
<img width="624" height="416" alt="image" src="https://github.com/user-attachments/assets/dfbe709a-7076-4c6b-959b-ab4888908ac4" />

Task 5 - Copy/Delete Directories

cp file1.txt file2.txt   <br>
mv file1.txt /var/log/   <br>
rm unwanted.txt  

Section 6: Users, Groups & sudo Privileges

Task 1 - Identify current user & users List <br>

whoami   <br>
cat /etc/passwd    (All User)   <br>
cat /etc/group     (All Group)   <br>
<img width="624" height="494" alt="image" src="https://github.com/user-attachments/assets/d5e4a909-e44b-4863-af1b-558af605592d" />

Task 2 - Create a user & add to sudo group

sudo adduser john   <br>
sudo usermod -aG sudo john   <br>
<img width="533" height="541" alt="image" src="https://github.com/user-attachments/assets/01dc9af0-27c5-4d68-8f15-0fff87115aa3" />

Task 3 - Switch user <br>
su -john <br>

Task 4 - Verify sudo access  <br>
sudo apt install nmap

Section 7 - File Permissions & Ownership

Permission Concept <br>
r - read  <br>
w - write <br>
x - execute

Task 1 - Check File Permissions <br>
ls -l <br>

Task 2 - Change Permissions <br> 

chmod 777 ms.txt  (rwx rwx rwx)   <br>
chmod 755 ms.txt  (rwx r-x r-x) <br>
chmod 644 ms.txt  (rw- r-- r--)  <br>

Task 3 - Chnage ownership <br>
sudo chown john:john ms.txt 

Section 8 - System Monitoring -(CPU, RAM, DISK, NETWORK)

<b>Cpu & Process Monitoring </b><br>
top  <br>
htop <br>
ps aux <br>
<img width="624" height="455" alt="image" src="https://github.com/user-attachments/assets/a1097911-2e16-48b3-a52e-6b3d8720b617" />

<b>Memory Monitoring </b> <br>
free -h   <br>
<img width="624" height="458" alt="image" src="https://github.com/user-attachments/assets/17693d2c-be71-4ef0-8f15-02cc3265d26a" />


<b>Disk Usage  </b> <br>
df -h <br>
du -sh /var/log/* <br>

<b>Network Monitoring </b> <br>

ip a <br>
netstat -tulnp <br>
ss -tulnp    <br> 
<img width="624" height="196" alt="image" src="https://github.com/user-attachments/assets/33c8765b-36bb-4f43-bc1e-243e5088efa8" />



## Outcome
After completing this project, I gained practical experience in Linux system operations, including file management, user administration, and system monitoring. I developed confidence in using the Linux command line, which is essential for roles in IT support, system administration, and cybersecurity.

