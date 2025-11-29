# 🔍 Windows UserAssist Analysis

## 📌 Scenario

In this practical, you will generate UserAssist activity to examine which GUI applications a user opened, how often they were accessed, and when they were last run. These artifacts help reconstruct user behavior during a forensic investigation.

We will later analyze the data using tools like **KAPE**, **Registry Explorer**, **RegRipper (userassist plugin)**, or **UserAssistView**.

---

## 🔧 Artifact-Generating Actions (GUI Application Execution)

Perform the following actions on your Windows VM to generate UserAssist entries:

### ▶ Run GUI Applications (2–3 times each)

* notepad.exe
* calc.exe
* mspaint.exe
* explorer.exe (browse folders)
* wordpad.exe
* Any GUI `.exe` from your **Downloads** folder

These actions create:

* Application execution records
* Updated counts
* New UserAssist entries
* User interaction traces

> ⏳ Wait 1–2 Minutes UserAssist updates after a short delay.

---
