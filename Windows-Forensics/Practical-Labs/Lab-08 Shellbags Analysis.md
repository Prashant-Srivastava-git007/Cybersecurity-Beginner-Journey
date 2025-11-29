# 🗂️ Windows Shellbags Practical Lab

---

## 📌 Scenario

Shellbags record folders viewed in Windows Explorer, including deleted or external folders. To create realistic forensic artifacts, perform the actions below on your Windows VM.

### 🔧 Artifact-Generating Actions

**▶ 1. Browse Local Folders**

Open File Explorer and visit several folders such as:

* Documents
* Downloads
* Desktop
* System32
* Program Files

**▶ 2. Change Folder View Modes**

In different folders, switch between:

* Details
* List
* Large Icons

This updates Shellbag view settings.

**▶ 3. Create & Delete Test Folders**

* Create a folder (e.g., `C:\Shellbag_Test`)
* Add a few subfolders inside
* Open each folder
* **Delete the entire structure**

This generates Shellbags for **deleted folders**.

**▶ 4. Optional: External or Network Access**

If available:

* Open folders on a USB drive
* Or access a network share (`\\IP\Share`)

This creates entries for removable/network paths.

> ⏳ Wait 1–2 minutes This ensures all Shellbag entries are written to the registry.

---
