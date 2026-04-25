# 📅 Day 2 – Kali Linux Basics & Terminal Fundamentals

## 🎯 Objective

Learn basic Linux terminal commands, file handling, permissions, and system awareness.

---

## 🖥️ 1. Terminal Basics

| Command | Description                |
| ------- | -------------------------- |
| `pwd`   | Print current directory    |
| `ls`    | List files and directories |
| `cd`    | Change directory           |
| `mkdir` | Create a new directory     |
| `touch` | Create a new file          |
| `rm`    | Delete file                |

---

## 📂 2. File Management

| Command          | Description         |
| ---------------- | ------------------- |
| `cp file1 file2` | Copy file           |
| `mv file1 file2` | Move or rename file |

### Example:

```bash
mkdir hacking
cd hacking
touch file.txt
cp file.txt backup.txt
mv backup.txt renamed.txt
rm renamed.txt
```

---

## 🔍 3. Searching

### grep (search inside file)

```bash
echo "hello world" > file.txt
grep hello file.txt
```

### find (search file in system)

```bash
find / -name file.txt 2>/dev/null
```

---

## 🔐 4. File Permissions

Command:

```bash
ls -l
```

Example output:

```
-rwxr-xr-- 1 user user file.txt
```

### Meaning:

* `r` = read
* `w` = write
* `x` = execute


### Change permission:

```bash
chmod +x file.txt
```

---

## 🌐 5. Network Information

Command:

```bash
ip a
```

### Purpose:

* View IP address
* Identify network interface (eth0 / wlan0)

---

## 🛠️ 6. First Tool Exposure

Used:

* Nmap (network scanning tool)

Command:

```bash
nmap localhost
```

### Purpose:

* Scan open ports on a machine

---

## 🧠 Key Learnings

* Terminal gives full control over the system
* File management is essential for lab work
* Permissions are important for security and exploitation
* Basic networking info helps in future scanning
* Tools like Nmap are used to discover targets

---

## ⚠️ Challenges Faced

* Understanding file permissions
* Remembering commands
* Navigating directories efficiently

---

## ✅ Outcome

* Learned basic Linux commands
* Understood file handling and permissions
* Ran first network scan
* Gained confidence using terminal

---

## Mistakes i made:
forgot how to write in txt file.
how to find something in txt file
and still a little bit confused about how to find in the whole system