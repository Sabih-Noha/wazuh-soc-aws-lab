# 💣 Attack Simulations

This section documents real cyberattack simulations detected by Wazuh.

---

## 1️⃣ Linux SSH Bruteforce

**Description:** Multiple failed SSH login attempts using invalid users.

**Detection:**
- sshd: Attempt to login using a non-existent user

**MITRE:** T1110 – Brute Force

---

## 2️⃣ Privilege Escalation

**Description:** Use of sudo to gain root privileges.

**Detection:**
- Successful sudo to ROOT executed

**MITRE:** T1068 – Privilege Escalation

---

## 3️⃣ File Integrity Monitoring (FIM)

**Description:** Modification of /etc/passwd detected.

**Detection:**
- File modified: /etc/passwd

**MITRE:** T1005 – Data from Local System

---

## 4️⃣ Windows RDP Bruteforce

**Description:** Multiple failed RDP logins.

**Detection:**
- Logon failure – Unknown user or bad password

**MITRE:** T1110 – Brute Force
