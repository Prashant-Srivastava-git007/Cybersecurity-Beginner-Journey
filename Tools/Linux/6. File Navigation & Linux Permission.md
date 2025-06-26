# 🗂️ File System Navigation & Linux Permissions (Advanced)

---

## 🔍 Locate – Searching Files Faster

The `locate` command is used to **quickly find files** on a Linux system. It is faster than `find` because it searches a pre-built database.

### 📌 Usage:
- `locate <file-name>`  
  → Searches for the file across the system.

- `locate -c <file-name>`  
  → Returns the **count** of matching files with that name.

### ⚠️ Troubleshooting:
- If `locate` doesn't work, first run:

  → This updates its file database:
```bash
 sudo updatedb  
```

* If not installed:
```bash
 sudo apt install mlocate
```

---

## 🔐 UMASK – Changing Default File Permissions
`umask` is used to define the default permissions assigned to new files or directories when they are created.

### 🧪 Check Current Default Permissions:

* `umask`

  → Returns an octal value.

* `umask -S`

  → Shows symbolic (readable) permission format.

### 🧠 How It Works:
The actual default permissions = `777 - umask_value`

---

### 🛠 Change Default Permissions Temporarily:
```bash
umask u+<permissions>,g+<permissions>,o+<permissions>
```
⚠️ These changes last only for the current shell session.
> ⚠️ **Note:** This symbolic syntax is supported only in certain shells like zsh and may not work in bash. So the octal method is safer and more portable.

* Use the **octal format**:
```bash
umask 027
```

### 💡 Make UMASK Changes Permanent

To apply default permissions permanently, add the umask command in shell configuration files:

|         File       |        Scope      |
|--------------------|-------------------|
| `/etc/bash.bashrc` | Global (all user) |
| `~/.bachrc`        | Current user only |

---

## 📂 Bonus Tip: Viewing File Metadata

Use the `stat` command to view detailed metadata about a file:

```bash
stat <file-name>
```

This shows:
* Access and modification time
* Owner and group
* Permissions in both symbolic and octal forms
