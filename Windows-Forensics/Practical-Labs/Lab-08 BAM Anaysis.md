# 🔍 Windows Background Activity Monitor (BAM) Practical Lab

---

## 📌 Scenario

To simulate real-world forensic conditions, we will generate **BAM activity** on a Windows machine. These actions will create entries showing which applications were executed and when.

### 🔧 Artifact-Generating Actions

Perform the following steps on your Windows VM to create BAM artifacts:

**▶ Run Common Applications**

Execute each program **2–3 times**:

* `notepad.exe`
* `calc.exe`
* `mspaint.exe`
* `wordpad.exe`
* `cmd.exe`
* `powershell.exe`
* Open **File Explorer** and browse Documents, Downloads, Pictures

**▶ Run Apps From Different Locations**

* Launch an `.exe` from **Downloads**
* Run any program from **C:\Program Files**
* Run a portable `.exe` from the **Desktop**

**▶ Trigger Brief Executions**

(Open & close quickly — useful for testing BAM behavior)

* Notepad
* Calculator
* Paint
* Run dialog → type `calc` → Enter → close

> ⏳ Wait 1–2 Minutes Give BAM time to write the execution data to the registry.

---
