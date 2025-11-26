# Windows File System Analysis Practical

---

## Artifact Creation for Hands-On Analysis

### 📝 Scenario

Unusual activity has been detected on a Windows workstation.
Several file operations—creation, modification, renaming, movement, and deletion—were carried out within a short timeframe.
These actions are expected to leave traces in artifacts such as $MFT and $J, which can later be used to reconstruct the exact sequence of events.

---

## 🔧 Steps to Generate Artifacts

```powershell
# Create working directory
mkdir C:\LabTest

# Create two files (docx + text)
echo "secret1" > C:\LabTest\report.docx
echo "secret2" > C:\LabTest\data.txt

# Rename a file
Rename-Item C:\LabTest\report.docx final_report.docx

# Move the file into a new folder
mkdir C:\LabTest\Archive
move C:\LabTest\final_report.docx C:\LabTest\Archive

# Delete a file
del C:\LabTest\data.txt

# Create and update a log file
echo "Stage 1" > C:\LabTest\activity.log
echo "Stage 2" >> C:\LabTest\activity.log
echo "Stage 3" >> C:\LabTest\activity.log

# Rename the log file twice
Rename-Item C:\LabTest\activity.log activity_v1.log
Rename-Item C:\LabTest\activity_v1.log activity_final.log

```

---
