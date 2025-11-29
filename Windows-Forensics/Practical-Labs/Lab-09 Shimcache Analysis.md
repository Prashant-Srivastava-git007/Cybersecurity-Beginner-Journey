# 🔍 Windows Shimcache (Application Compatibility Cache) Practical Lab

---

## 📌 Scenario

To generate realistic Shimcache artifacts, you will perform basic program execution and file operations on a Windows VM. These actions allow Windows to record executable activity in the AppCompatCache.
(This lab focuses **only** on generating artifacts, not analyzing them.)

### 🔧 Artifact-Generating Actions

**▶ 1. Run Common Executables**

Run each of the following **1–2 times**:

* `notepad.exe`
* `calc.exe`
* `mspaint.exe`
* `cmd.exe`
* `powershell.exe`
* Any `.exe` from your **Downloads** folder

These actions create new Shimcache entries.

**▶ 2. Perform Simple File Operations**

Do the following with any `.exe` file:

* Copy it from Downloads → Desktop
* Move it to another folder
* Rename it (e.g., `test.exe` → `app.exe`)

This adds additional path and file interaction artifacts.

**▶ 3. Open Executables From Different Locations**

Run `.exe` files from:

* Desktop
* Downloads
* Documents

This helps populate the Shimcache with multiple file paths.

**▶ 4. Shut Down the System**

Shimcache is written **only on shutdown**, so perform:

* **Full system shutdown**
* Wait 30–60 seconds
* Boot again

This ensures all data is saved.

---
