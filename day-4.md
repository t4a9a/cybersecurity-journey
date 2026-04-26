# 📅 Day 3 – Nmap Scanning & Service Detection

## 🎯 Objective

Learn how to scan open ports and identify services running on a machine using Nmap.

---

## 🛠️ 1. Tool Used

* Nmap (Network Mapper)

👉 Used for:

* Discovering open ports
* Identifying services
* Scanning targets

---

## 🔍 2. Basic Scan

### Command:

```bash
nmap localhost
```

### Output:

```text
PORT     STATE SERVICE
8080/tcp open  http-proxy
```

### Understanding:

* 8080 → port number
* open → port is accessible
* service → possible service running

---

## 🔎 3. Service Detection

### Command:

```bash
nmap -sV localhost
```

### Output:

```text
8080/tcp open  http  SimpleHTTPServer 0.6 (Python 3.x)
```

### Understanding:

* Nmap detects:

  * Service type → HTTP
  * Server → Python SimpleHTTPServer
* This helps identify possible vulnerabilities

---

## 🧪 4. Full Port Scan

### Command:

```bash
nmap -p- localhost
```

### Purpose:

* Scans all 65535 ports
* Finds hidden or uncommon services

---

## 🌐 5. Practical Setup

### Started a local server:

```bash
python3 -m http.server 8080
```

### Result:

* Opened port 8080
* Created a simple web server

---

## 🔁 6. Interaction Observed

* Nmap sent requests to port 8080
* Server responded to those requests
* Logs appeared in server terminal

### Example:

```text
GET / HTTP/1.1 200
POST /sdk HTTP/1.1 501
```

---

## 🧠 Key Learnings

* Open ports indicate running services
* Nmap scans ports by sending packets
* Service detection reveals what is running
* Servers respond when scanned
* Scanning is the first step in hacking

---

## ❌ Mistakes / Confusion

* Initially confused between local scan and real network scan
* Thought `ss -tuln` could scan other systems
* Didn’t fully understand how Nmap interacts with services

---

## ✅ Outcome

* Successfully scanned localhost
* Detected running HTTP server
* Understood how Nmap works
* Observed real interaction between scanner and server

---
![alt text](/screenshots/image-7.png)