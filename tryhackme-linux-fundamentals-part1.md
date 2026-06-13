# Linux Fundamentals Part 1 - TryHackMe Writeup

**Room:** Linux Fundamentals Part 1  
**Difficulty:** Info  
**Category:** Linux Basics  
**Date Completed:** 2025  
**Platform:** TryHackMe

## Challenge Description
Embark on the journey of learning the fundamentals of Linux. Learn to run some of the first essential commands on an interactive terminal.

## Essential Linux Commands

### 1. Navigation
```bash
pwd          # Print working directory
ls           # List files
cd           # Change directory
cd ..        # Go back one directory
cd ~        # Go to home directory
```

### 2. File Operations
```bash
cat          # Display file contents
less         # View file contents page by page
head         # View first lines
tail         # View last lines
```

### 3. File Manipulation
```bash
cp           # Copy files
mv           # Move/rename files
rm           # Remove files
mkdir        # Create directory
touch        # Create empty file
```

### 4. Permissions
```bash
chmod        # Change permissions
chown       # Change ownership
```

### 5. System Info
```bash
whoami      # Current user
uname -a    # System information
hostname    # Hostname
```

## Directories Explained
- `/` - Root directory
- `/home` - User home directories
- `/etc` - Configuration files
- `/var` - Variable files (logs, etc)
- `/tmp` - Temporary files
- `/bin` - Essential binaries
- `/sbin` - System binaries

## Learning Points
- Linux is essential for cybersecurity
- Command line is powerful
- File permissions matter for security

---
*Writeup by @zudio-infosec*  
*For more: github.com/zudio-infosec/ctf-writeups*