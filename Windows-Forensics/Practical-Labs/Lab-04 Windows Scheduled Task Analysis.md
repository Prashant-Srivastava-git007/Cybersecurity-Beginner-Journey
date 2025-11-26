# Windows Scheduled Task Analysis Practical

---

## 📌 Scenario

A suspicious scheduled task was identified on a Windows system.
The task appears to run frequently and execute command-line actions that modify files on disk, suggesting potential malicious automation.
The following task configuration was created on the machine and now exists as part of its scheduled task artifacts.

### 🔧 Artifact-Generating Actions (Scheduled Task Activity)

Create a Test Scheduled Task

Task Name: `Test_Malicious_Look_Task`
Trigger: Runs every 5 minutes

Action:
* Program: `cmd.exe`
* Arguments: `/c echo Task Ran > C:\Users\Public\testtask.txt`

This task was created through Task Scheduler → Create Task.

**Allow the Task to Run**

Wait 5–10 minutes so the task executes at least once.
This simulates:
* Persistence
* A command execution
* A writable output file being generated

---
