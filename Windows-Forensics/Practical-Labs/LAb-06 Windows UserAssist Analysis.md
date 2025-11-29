## 🔍 Windows UserAssist Analysis

---

## 📌 Scenario

During a forensic investigation, an analyst needs to determine which GUI applications were executed by a user, how frequently they were accessed, and when they were last run. UserAssist artifacts stored in the Windows Registry can help reconstruct user behavior and application execution history.

To simulate real-world forensic conditions, we will generate UserAssist activity on a Windows system and later analyze it using tools such as KAPE, Registry Explorer, RegRipper (userassist plugin), or UserAssistView.

### 🔧 Artifact-Generating Actions (GUI Application Execution Activity)

Perform the following actions on your Windows VM to ensure UserAssist data is generated:

**▶ Execute Common GUI-Based Applications**

Run each of the following programs 2–3 times:
* notepad.exe
* calc.exe
* mspaint.exe
* explorer.exe (open folders like Documents, Downloads, etc.)
* wordpad.exe
* Any GUI .exe file from your Downloads folder

**These actions simulate:**
* GUI application execution
* Updated execution counts
* New entries in UserAssist GUID keys
* User interaction patterns

> ⏳ Wait 1–2 Minutes UserAssist entries update after a short delay.

---
