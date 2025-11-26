# Windows Run Key Analysis Practical

---

## 📌 Scenario

A Windows system shows signs of a potential persistence mechanism being set up.
During the initial review, an entry was found under the Run key, suggesting that a program may have configured itself to start automatically at login.
The following actions were performed on the machine and now exist as part of its registry activity history.

### 🔧 Artifact-Generating Actions (Run Key Persistence)

**Add a Custom RUN Key Entry**

```text
Registry Path:
HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Run
```
**Entry Created:**
* Name: MyUpdater
* Value: C:\Windows\System32\notepad.exe

This simulates software (or malware) establishing persistence by adding itself to the Run key.

---
