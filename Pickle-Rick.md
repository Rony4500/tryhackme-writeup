# 🥒 TryHackMe - Pickle Rick Walkthrough

## 📎 Room Link
[Pickle Rick](https://tryhackme.com/room/picklerick)

## 🖥 Target IP
`10.10.X.X`

---

## 🔍 Nmap Scan

```bash
nmap -sC -sV -oN pickle-nmap.txt 10.10.X.X
```

Found HTTP on port 80.

### 🔑 Login Page
Username: `RICK`  
Password: `Wubbalubbadubdub`

### 🐚 Shell Access
Used the web shell panel to run Linux commands.

---

### 🎯 Flags

- `ingredient1.txt`: Found in /home directory
- `ingredient2.txt`: Hidden file
- `ingredient3.txt`: Found in `/root/` after privilege escalation
