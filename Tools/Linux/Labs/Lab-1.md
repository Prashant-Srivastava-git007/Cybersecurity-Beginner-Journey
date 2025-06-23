# 🧪 Lab Practice – Secret File Access Control

You are the **system administrator** of a Linux machine.

A secret file must be accessible **only** by a new user named `agent007`.  
No one else — not even other users in the same group — should be able to **read** or **modify** the file.

---

## 🧩 Solution

### ✅ Step 1 – Create Users
Create two users: `agent007` and `intruder`.
```bash
adduser agent007
adduser intruder
```

### ✅ Step 2 – Create the Secret File
Create a file named Top-Secret.txt and add content using touch or a text editor like nano:
```bash
touch Top-Secret.txt
nano Top-Secret.txt
```

### ✅ Step 3 – Change Ownership
Assign the file ownership to agent007:
```bash
chown agent007:agent007 Top-Secret.txt
```

### ✅ Step 4 – Set File Permissions
Give full permissions only to agent007:
```bash
chmod 700 Top-Secret.txt
```
This allows only the file owner to read, write, and execute. Everyone else is denied access.

### ✅ Step 5 – Test Access with Another User
Try to access the file as intruder:
```bash
su - intruder
cat /home/agent007/Top-Secret.txt
```
Optionally, add intruder to the same group as agent007 and test again:
```bash
usermod -aG agent007 intruder
```
Even after adding to the same group, the file should remain inaccessible due to the strict 700 permission.

---

🧠 Mission Objective: Ensure only agent007 has access. Others — even in the same group — must be denied.


