# Windows Prefetch Analysis

---

## 📌 Scenario

A forensic investigation requires confirming whether certain applications were executed on a Windows system. Prefetch artifacts can help determine when, how often, and from where applications were run. To simulate real-world forensic conditions, we will generate Prefetch activity and analyze it using tools such as KAPE and PECmd.

### 🔧 Artifact-Generating Actions (Application Execution Activity)

Perform the following actions on your Windows VM to ensure Prefetch files are generated:

**Execute Common Windows Applications**

Run each of the following programs 2–3 times:
* notepad.exe
* calc.exe
* cmd.exe
* mspaint.exe
* write.exe

**This simulates:**
* Application execution activity
* Updated execution counts
* Prefetch file creation and modification

---
