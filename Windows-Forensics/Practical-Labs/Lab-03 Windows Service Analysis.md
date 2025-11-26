# Windows Service Analysis Practical

---

## 📌 Scenario

During a system review, an unexpected Windows service was discovered.
This service appears to reference a non-standard executable path, suggesting that it may have been created to maintain persistence or execute unwanted programs at system startup.
The following actions were performed on the machine and now exist in its service-related artifacts.

### 🔧 Artifact-Generating Actions (Service-Based Persistence)

**Create a Fake Windows Service**
```powershell
sc create MyFakeService binPath= "C:\Windows\System32\notepad.exe" start= auto
```
**Verify the Service Exists**
```powershell
sc query MyFakeService
```
This creates a service entry that can be examined during forensic analysis to understand how service-based persistence is configured on Windows systems.

---
