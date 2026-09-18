# 🐧 Linux Command Line & System Administration Lab

<div align="center">

![Linux](https://img.shields.io/badge/Linux-System%20Administration-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![Bash](https://img.shields.io/badge/Bash-Command%20Line-4EAA25?style=for-the-badge&logo=gnubash&logoColor=white)
![Red Hat](https://img.shields.io/badge/RHEL-Linux%20Engineering-EE0000?style=for-the-badge&logo=redhat&logoColor=white)

### Linux • Infrastructure • Operations • Cloud

**A hands-on Linux engineering lab focused on command-line administration, system operations, troubleshooting, permissions, process management, and security fundamentals.**

</div>

---

## 📌 Project Overview

This repository documents my hands-on development of **Linux command-line and system administration skills** relevant to production infrastructure, operations, and cloud engineering environments.

The project focuses on administering Linux systems from the command line, including:

- File system navigation
- File and directory administration
- Linux permissions and ownership
- Process management
- System monitoring
- Text processing
- User and group administration
- `sudo` privilege management
- Linux troubleshooting
- Command-line security challenges

The module concludes with **Levels 1–20 of the OverTheWire Bandit game**, applying Linux command-line concepts through practical security challenges.

---

## 🎯 Module Goals

By completing this module, I aim to demonstrate the ability to:

- 🗂️ Navigate the Linux file system confidently from the command line
- 📁 Create, modify, move, copy, and remove files and directories
- 🔐 Manage Linux file ownership and permissions
- ⚙️ Understand processes and perform basic system monitoring
- 🔎 Search and manipulate data using essential Linux utilities
- 👥 Manage users, groups, and `sudo` privileges
- 🛡️ Apply Linux knowledge to security-oriented challenges
- 🚩 Complete **OverTheWire Bandit Levels 1–20**

---

## 🗂️ Linux File System Navigation

Understanding the Linux file system is foundational to Linux and infrastructure engineering.

### Commands Practiced

```bash
pwd
ls
ls -la
cd
tree
file
stat
du
df
```

### Skills Demonstrated

- Navigate directories using absolute and relative paths
- Identify hidden files
- Inspect file metadata
- Understand Linux directory structures
- Examine disk and directory usage
- Locate files from the command line

---

## 📁 File & Directory Management

This section focuses on managing files and directories efficiently from the terminal.

### Examples

```bash
# Create a file
touch example.txt

# Create a directory
mkdir linux-lab

# Copy a file
cp example.txt backup.txt

# Move a file
mv backup.txt ./linux-lab/

# Remove a file
rm example.txt

# Create nested directories
mkdir -p projects/linux/scripts
```

### Core Commands

```text
touch
mkdir
cp
mv
rm
rmdir
ln
file
stat
```

---

## 🔐 Linux Permissions & Ownership

Linux permissions are essential for maintaining secure multi-user systems.

### Permission Model

```text
             User      Group     Others
               ↓         ↓         ↓
             rwx       r-x       r--
              │         │         │
              │         │         └── Other users
              │         └──────────── Group permissions
              └────────────────────── User/Owner permissions
```

### Permission Values

```text
r = Read      = 4
w = Write     = 2
x = Execute   = 1
```

### Commands Practiced

```bash
# View permissions
ls -l

# Set numeric permissions
chmod 755 script.sh

# Add execute permission for the owner
chmod u+x script.sh

# Change ownership
chown user:group file.txt
```

### Engineering Focus

Proper permission management helps prevent:

- Unauthorized file access
- Accidental modification
- Improper privilege assignment
- Insecure application configurations
- Unnecessary exposure of sensitive files

---

## ⚙️ Process Management

Linux engineers need to understand what is running on a system and how processes consume system resources.

### Process Inspection

```bash
ps aux
ps -ef
top
pgrep ssh
```

### Process Control

```bash
kill <PID>

kill -15 <PID>

kill -9 <PID>
```

### Skills Practiced

- Identify running processes
- Locate processes by name
- Understand process IDs
- Monitor CPU utilization
- Monitor memory utilization
- Terminate problematic processes
- Investigate system activity

---

## 📊 System Monitoring

System monitoring helps identify resource constraints and operational problems before they develop into larger production issues.

### Commands Practiced

```bash
uptime
free -h
df -h
du -sh /var/log
top
ps aux
```

### Areas Monitored

```text
                Linux System
                     │
          ┌──────────┼──────────┐
          │          │          │
          ▼          ▼          ▼
         CPU       Memory      Disk
          │          │          │
          └──────────┼──────────┘
                     │
                     ▼
                 Processes
                     │
                     ▼
                 System Load
```

---

## 🔎 Linux Search & Text Processing

One of the most powerful aspects of Linux is the ability to combine small command-line utilities into larger troubleshooting and automation workflows.

### `grep`

Search files and command output for patterns.

```bash
grep "error" application.log

grep -i "failed" application.log

grep -R "ERROR" /var/log/
```

---

### `find`

Locate files and directories.

```bash
find /var/log -name "*.log"

find . -type f

find . -type d
```

---

### `awk`

Process and extract structured text.

```bash
awk '{print $1}' file.txt

awk -F: '{print $1}' /etc/passwd
```

---

### `sed`

Perform text transformations.

```bash
sed 's/old/new/g' file.txt
```

---

### Essential Linux Toolkit

```text
grep
awk
sed
find
sort
uniq
cut
head
tail
wc
xargs
```

These utilities are especially useful for:

- Log analysis
- Production troubleshooting
- Searching configuration files
- Data extraction
- Automation
- System administration
- Incident investigation

---

## 👥 User & Group Administration

Linux systems frequently support multiple users, applications, administrators, and service accounts.

### User Management

```bash
useradd username

passwd username

usermod username

userdel username

id username
```

### Group Management

```bash
groupadd developers

usermod -aG developers username

groups username
```

### Important System Files

```text
/etc/passwd
/etc/group
/etc/shadow
```

### Skills Demonstrated

- Create and manage users
- Create and manage groups
- Assign group memberships
- Inspect user identities
- Understand Linux account files
- Manage access to system resources

---

## 🔑 Sudo & Privilege Management

Administrative privileges should be granted carefully and according to the principle of least privilege.

### Commands Practiced

```bash
sudo command

sudo -l

sudo -u username command
```

### Principle of Least Privilege

> Users should receive only the permissions necessary to perform their required tasks.

Understanding `sudo` administration is important for maintaining secure Linux infrastructure and controlling administrative access.

---

## 🛡️ OverTheWire Bandit Challenge

The final portion of this module applies Linux knowledge through **OverTheWire Bandit Levels 1–20**.

Bandit provides command-line security challenges that require Linux navigation, file discovery, permissions, text processing, remote access, and problem-solving skills.

### Concepts Reinforced

```text
Linux Navigation
       │
       ▼
File Discovery
       │
       ▼
Permissions
       │
       ▼
Text Processing
       │
       ▼
Command Pipelines
       │
       ▼
Remote Access
       │
       ▼
Security Fundamentals
```

### 🚩 Bandit Progress

| Challenge | Status |
|:---|:---:|
| Bandit 0 → 1 | ⬜ |
| Bandit 1 → 2 | ⬜ |
| Bandit 2 → 3 | ⬜ |
| Bandit 3 → 4 | ⬜ |
| Bandit 4 → 5 | ⬜ |
| Bandit 5 → 6 | ⬜ |
| Bandit 6 → 7 | ⬜ |
| Bandit 7 → 8 | ⬜ |
| Bandit 8 → 9 | ⬜ |
| Bandit 9 → 10 | ⬜ |
| Bandit 10 → 11 | ⬜ |
| Bandit 11 → 12 | ⬜ |
| Bandit 12 → 13 | ⬜ |
| Bandit 13 → 14 | ⬜ |
| Bandit 14 → 15 | ⬜ |
| Bandit 15 → 16 | ⬜ |
| Bandit 16 → 17 | ⬜ |
| Bandit 17 → 18 | ⬜ |
| Bandit 18 → 19 | ⬜ |
| Bandit 19 → 20 | ⬜ |

> **Security Note:** Passwords, credentials, flags, and challenge secrets are intentionally excluded from this repository.

---

## 📂 Repository Structure

```text
linux-system-administration-lab/
│
├── README.md
│
├── 01-file-system/
│   ├── navigation.md
│   └── exercises.md
│
├── 02-files-permissions/
│   ├── permissions.md
│   └── exercises.md
│
├── 03-process-management/
│   └── processes.md
│
├── 04-system-monitoring/
│   └── monitoring.md
│
├── 05-text-processing/
│   ├── grep.md
│   ├── awk.md
│   ├── sed.md
│   └── find.md
│
├── 06-users-groups/
│   └── administration.md
│
├── 07-bandit/
│   └── progress.md
│
└── scripts/
    └── README.md
```

---

## 🧠 Skills Demonstrated

This project develops and demonstrates practical experience with:

| Area | Skills |
|---|---|
| 🐧 Linux | Command Line, File Systems, Administration |
| 📁 Files | Creation, Movement, Search, Management |
| 🔐 Security | Permissions, Ownership, Sudo |
| ⚙️ Processes | Process Inspection & Management |
| 📊 Monitoring | CPU, Memory, Disk, System Load |
| 🔎 Text Processing | grep, awk, sed, find |
| 👥 Identity | Users, Groups, Privileges |
| 🛡️ Security Labs | OverTheWire Bandit |
| 🔧 Operations | Troubleshooting & Investigation |
| 🤖 Automation | Command Pipelines & CLI Tools |

---

## ☁️ Why This Matters for Infrastructure Engineering

Linux is foundational to modern infrastructure.

The skills developed in this repository directly support work involving:

```text
                    Linux Engineering
                           │
          ┌────────────────┼────────────────┐
          │                │                │
          ▼                ▼                ▼
       Cloud          Automation       Operations
    Infrastructure        │                │
          │               │                ├── Monitoring
     ┌────┴────┐      ┌────┴────┐           │
     │         │      │         │           └── Troubleshooting
     ▼         ▼      ▼         ▼
    AWS      Azure   Bash     Python
          │
          ▼
 Configuration Management
          │
          ▼
       Ansible
          │
          ▼
      Containers
       ┌────┴────┐
       │         │
       ▼         ▼
     Docker   Kubernetes
```

The goal is not simply to memorize Linux commands.

The goal is to understand **how Linux systems behave, how to investigate problems, how permissions and processes interact, and how to operate systems reliably from the command line.**

---

## 🏗️ Real-World Engineering Relevance

The concepts practiced in this lab form the foundation for more advanced infrastructure engineering tasks such as:

```text
Linux Fundamentals
        │
        ├──► RHEL Administration
        │
        ├──► AWS EC2 Linux Administration
        │
        ├──► Ansible Automation
        │
        ├──► Docker
        │
        ├──► Kubernetes
        │
        ├──► Linux Security Hardening
        │
        ├──► Monitoring & Observability
        │
        ├──► CI/CD
        │
        └──► Cloud Infrastructure
```

Strong Linux fundamentals make it easier to troubleshoot and operate infrastructure at every layer of the stack.

---

## 🎯 Learning Outcomes

Upon completion of this project, I will have strengthened my ability to:

- Operate Linux systems confidently through the CLI
- Navigate complex file system structures
- Manage files, directories, ownership, and permissions
- Investigate and control running processes
- Monitor basic system resource utilization
- Search logs and files efficiently
- Process command output using standard Linux utilities
- Administer users and groups
- Work with elevated privileges safely
- Combine commands using Linux pipelines
- Apply Linux concepts to security challenges
- Troubleshoot Linux systems methodically

---

## 🔄 Engineering Workflow

```text
Observe
   │
   ▼
Investigate
   │
   ▼
Identify
   │
   ▼
Troubleshoot
   │
   ▼
Resolve
   │
   ▼
Validate
   │
   ▼
Document
   │
   ▼
Automate
```

This workflow reflects the mindset I apply to Linux and infrastructure operations: **understand the system first, resolve the issue, validate the result, and automate repeatable work whenever possible.**

---

## 🚀 Future Enhancements

Future additions to this repository may include:

- Bash scripting exercises
- Linux service management
- `systemd` administration
- Log analysis with `journalctl`
- Package management
- SSH administration
- Linux networking
- Storage and LVM
- Firewall configuration
- SELinux
- Cron and scheduled tasks
- Ansible automation
- Linux security hardening
- AWS EC2 Linux administration
- Advanced troubleshooting labs

---

## 👨‍💻 Author

### Chaanyah Laborde

**🐧 Linux Engineer | ⚙️ Operations Engineer | 🏗️ Infrastructure Engineer | ☁️ Cloud Engineer**

I focus on building, operating, securing, troubleshooting, and automating reliable Linux and cloud infrastructure.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Chaanyah_Laborde-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/claborde/)

---

<div align="center">

## 🐧 Linux at the Core. ☁️ Cloud at Scale. ⚙️ Automation by Default.

**Master the command line. Understand the system. Engineer reliable infrastructure.**

⭐ **Linux • Cloud • Infrastructure • Operations**

</div>
