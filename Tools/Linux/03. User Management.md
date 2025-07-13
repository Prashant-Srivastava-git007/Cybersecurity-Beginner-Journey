# 👤 Linux User & Group Management

Managing users and groups is a core task in Linux system administration and important for controlling access in cybersecurity environments.

---

## 🆔 View User Information

```bash
id <user-name>
```
Displays the user’s UID, GID, and group memberships.

---

## ➕ Create a User

```bash
useradd <user-name>
Or with additional options:
useradd -g <group-name> -c "Description" <user-name>
```
* `-g`: Assign a primary group
* `-c`: Add a description (comment)

---

## ❌ Delete a User

```bash
userdel <user-name>
To delete the user and their home directory:
userdel -r <user-name>
```
---

## 🛠️ Modify a User

### ➕ Add a User to a New (Additional) Group

```bash
usermod -G <group-name> <user-name>
```
This adds the user to a group, but their primary group remains unchanged.

### 🔄 Change the Default (Primary) Group

```bash
usermod -g <group-name> <user-name>
```

---

## 🔐 Set or Change User Password

```bash
passwd <user-name>
```
Prompts for a new password for the user.

---

## 👥 Create & Delete Groups

### ➕ Create a Group
```bash
groupadd <group-name>
```
### ❌ Delete a Group
```bash
groupdel <group-name>
```

---

# 🧪 Lab Practice

You are the system administrator of a Linux machine.

A secret file must be accessible **only** by a new user named `agent007`.

No one else — not even other users in the same group — should be able to **read** or **modify** the file.
 
```
🕵️‍♂️ Mission Support: Classified hints and the solution are available in the `Lab` directory.
```


