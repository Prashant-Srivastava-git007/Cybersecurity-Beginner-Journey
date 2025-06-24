# 🧪 Lab Practice 🛡️ Secure Backup Mission

🕵️‍♂️ **Role**: Junior Security Analyst  
🎯 **Goal**: Back up critical system configs and prepare for full recovery

---

## 🔐 Mission Brief

A malware threat has been detected.

Your task:
- Back up the `/etc/` directory (contains sensitive configs)
- Create a secure `.tar.gz` archive
- Ensure it can be restored completely if the system is compromised

---

# 🧩 Solution

Follow these steps to back up and restore a sensitive configuration directory:

---

## 🔧 Step 1: Create a Directory with Sensitive Configs

```bash
mkdir secret
```

Create some mock config files using:
```bash
nano secret/config1.txt       # Or use touch/echo as needed
```

---

## 📦 Step 2: Compress the Directory
Choose one of the following methods to archive the folder:

### 📁 Create a .zip file:

```bash
zip -r secret.zip secret/
```

### 📁 Create a .tar.gz file:

```bash
tar -czvf secret.tar.gz secret/
```

## 🚨 Step 3: Simulate a Threat
Delete the original folder to simulate data loss:

```bash
rm -r secret
```

## 💾 Step 4: Recover the Backup
### If using .zip:

```bash
unzip secret.zip
```
### If using .tar.gz:

```bash
tar -xzvf secret.tar.gz
```

---

```bash
🎯 You have now successfully created a secure backup and verified system recovery!
```
