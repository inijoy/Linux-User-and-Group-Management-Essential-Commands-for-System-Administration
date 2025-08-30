# Linux User and Group Management & Essential Commands for System Administration

## **Overview**

### This project demonstrates **Linux system administration fundamentals**, focusing on **user and group management** along with **essential Linux commands** required for navigation, file handling, system monitoring, and networking.

As a **System Administrator** or **DevOps Engineer**, mastering these skills is crucial for:

- Securing systems.
- Ensuring proper access control.
- Managing users and groups efficiently.
- Performing system monitoring and troubleshooting.

### This hands-on project showcases real-world practices and commands with practical examples, making it beginner-friendly while also highlighting **best practices for professionals**.

 

### **Aims & Objectives**

- Understand and practice **Linux user and group management**.
- Explore **35+ essential Linux commands** in a logical order of usage.
- Learn **navigation, file operations, process management, and networking basics**.
- Follow **best practices** for system security and role-based access.

Build confidence in handling a Linux environment as a

**prerequisite for DevOps**

## **Tools Used**

- **AWS EC2 Instance** (Ubuntu 22.04 LTS – Free Tier).
- **MobaXterm** (SSH client for connecting to the instance).
- **Linux Terminal** with superuser privileges (sudo).

## **Best Practices for User & Group Management**

### 

Create groups first, then assign users to them.

 Assign permissions to groups, not individuals.

 Apply the **principle of least privilege**.

 Use sudo for administrative tasks instead of logging in as root.

Regularly audit and remove inactive accounts

## **Step 1: Creating Users Without Passwords**

Instead of setting passwords for users, the **best practice** is to create accounts without direct login passwords. This enhances security and encourages the use of **SSH keys**.

Command:

sudo adduser --disabled-password iniabasi

sudo adduser --disabled-password joy

sudo adduser --disabled-password hilary

sudo adduser --disabled-password andy

Four users created: **iniabasi, joy, hilary, andy**.

*[Insert Screenshot of user creation]*

![linux.4.png](Linux%20User%20and%20Group%20Management%20&%20Essential%20Comman%202565c4233bb6801baa3fd151cca46d95/linux.4.png)

## **Step 2: Creating Groups**

### 

Next, create two groups:

sudo groupadd devteam

sudo groupadd sysadminteam

Verify groups:

getent group devteam

getent group sysadminteam

*[Insert Screenshot of group creation]*

![linux.5.png](Linux%20User%20and%20Group%20Management%20&%20Essential%20Comman%202565c4233bb6801baa3fd151cca46d95/linux.5.png)

## **Step 3: Adding Users to Groups**

### 

Assign users to appropriate groups:

sudo usermod -aG devteam iniabasi

sudo usermod -aG devteam joy

sudo usermod -aG sysadminteam hilary

sudo usermod -aG sysadminteam andy

Verify memberships:

groups iniabasi

groups joy

groups hilary

groups andy

*[Insert Screenshot of group assignments]*

![linux.5.png](Linux%20User%20and%20Group%20Management%20&%20Essential%20Comman%202565c4233bb6801baa3fd151cca46d95/linux.5%201.png)

## **Step 4: Essential Linux Commands**

### **Navigation & Directory Handling**

pwd                 # Print current working directory

ls                  # List files and directories

ls -l               # Detailed listing with permissions

cd /etc/ssh         # Navigate to the directory

cd ..               # Move up one directory

cd ~                # Go to home directory

sudo mkdir minefile # Create new directory

sudo rmdir minefile # Remove empty directory

*[Insert Screenshot of directory operations]*

![linux.6.png](Linux%20User%20and%20Group%20Management%20&%20Essential%20Comman%202565c4233bb6801baa3fd151cca46d95/linux.6.png)

![linux.7.png](Linux%20User%20and%20Group%20Management%20&%20Essential%20Comman%202565c4233bb6801baa3fd151cca46d95/linux.7.png)

![linux.8.png](Linux%20User%20and%20Group%20Management%20&%20Essential%20Comman%202565c4233bb6801baa3fd151cca46d95/linux.8.png)

![linux.9.png](Linux%20User%20and%20Group%20Management%20&%20Essential%20Comman%202565c4233bb6801baa3fd151cca46d95/linux.9.png)

### **File Creation & Viewing**

touch notes.txt                     # Create empty file

ls -l notes.txt                     # Verify file

nano notes.txt                      # Open file in Nano editor

# Add: "My first practice notes, learning Linux commands"

cat notes.txt                       # View contents

less notes.txt                      # View file page by page

more notes.txt                      # Scroll through file

head bigfile.txt                    # Show first 10 lines

tail bigfile.txt                    # Show last 10 lines

tail -f /var/log/syslog             # Monitor logs live

*[Insert Screenshot of notes.txt editing]*

![linux.10.png](Linux%20User%20and%20Group%20Management%20&%20Essential%20Comman%202565c4233bb6801baa3fd151cca46d95/linux.10.png)

![linux.11.png](Linux%20User%20and%20Group%20Management%20&%20Essential%20Comman%202565c4233bb6801baa3fd151cca46d95/linux.11.png)

![linux.12.png](Linux%20User%20and%20Group%20Management%20&%20Essential%20Comman%202565c4233bb6801baa3fd151cca46d95/linux.12.png)

![linux.13.png](Linux%20User%20and%20Group%20Management%20&%20Essential%20Comman%202565c4233bb6801baa3fd151cca46d95/linux.13.png)

![linux.14.png](Linux%20User%20and%20Group%20Management%20&%20Essential%20Comman%202565c4233bb6801baa3fd151cca46d95/linux.14.png)

![linux.15.png](Linux%20User%20and%20Group%20Management%20&%20Essential%20Comman%202565c4233bb6801baa3fd151cca46d95/linux.15.png)

### **File & Directory Management**

cp notes.txt notes_backup.txt             # Copy file

mv notes.txt mynotes.txt                  # Rename file

rm notes_backup.txt                       # Delete file

rm -r testfolder                          # Delete directory & contents(This returned error because no named directory)

find /home/ubuntu -name "mynotes.txt"     # Search for file

*[Insert Screenshot of file management]*

![linux.16.png](Linux%20User%20and%20Group%20Management%20&%20Essential%20Comman%202565c4233bb6801baa3fd151cca46d95/linux.16.png)

### **System Info & Monitoring**

whoami            # Current logged-in user

who               # Show all logged-in users

uname -a          # System & kernel info

uptime            # System uptime & load

free -h           # Memory usage

df -h             # Disk usage

lsblk             # List block storage devices

top               # Live process & CPU usage

ps aux            # All running processes

*[Insert Screenshot of system monitoring]*

![linux.17.png](Linux%20User%20and%20Group%20Management%20&%20Essential%20Comman%202565c4233bb6801baa3fd151cca46d95/linux.17.png)

![linux.18.png](Linux%20User%20and%20Group%20Management%20&%20Essential%20Comman%202565c4233bb6801baa3fd151cca46d95/linux.18.png)

![linux.19.png](Linux%20User%20and%20Group%20Management%20&%20Essential%20Comman%202565c4233bb6801baa3fd151cca46d95/linux.19.png)

### **Networking & Package Management**

ping google.com                       # Test network connectivity

wget https://hijoxcloud.online        # Download file

curl https://hijoxcloud.online        # Fetch URL content

sudo apt update                       # Update package list

sudo apt install htop -y              # Install package (example: htop)

*[Insert Screenshot of package installation]*

![linux.20.png](Linux%20User%20and%20Group%20Management%20&%20Essential%20Comman%202565c4233bb6801baa3fd151cca46d95/linux.20.png)

## 

![linux.21.png](Linux%20User%20and%20Group%20Management%20&%20Essential%20Comman%202565c4233bb6801baa3fd151cca46d95/linux.21.png)

 

![linux.22.png](Linux%20User%20and%20Group%20Management%20&%20Essential%20Comman%202565c4233bb6801baa3fd151cca46d95/linux.22.png)

### **What I Learned**

- How to **create users and groups** and assign them logically.
- Importance of R**ole-Based Access Control** for Security.
- How to navigate Linux directories efficiently.
- File creation, editing, and monitoring basics.
- Essential system monitoring commands every SysAdmin/DevOps must know.
- Networking basics using ping, wget, and curl.
- Software installation and updates using apt.

## **Conclusion**

### This project provided hands-on practice with **core Linux administration skills,** a solid foundation for aspiring **System Administrators** or **DevOps Engineers**.

It demonstrates how to:

- Manage **users and groups**.
- Apply **best practices** for security.
- Use **essential Linux commands** for real-world tasks.

These skills are critical in managing servers in **cloud environments (like AWS)** and form the backbone of **DevOps workflows**.

### Next Steps (Future Enhancements):

- Automate user/group creation with **Bash scripts**.
- Implement **role-based permissions** using /etc/sudoers.
- Extend project with **file permissions (chmod, chown, chgrp)**.