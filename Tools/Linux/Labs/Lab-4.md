# 🧪 Mini Lab: Partition Hardening Simulation

## 🎯 Your Mission

Secure the `/tmp` directory so it **cannot be used to execute malicious files**.

---

## 🧰 Steps to Complete the Lab

### ✅ Step 1: Check if `/tmp` is already mounted

Use the following command:

```bash
mount | grep /tmp
```

* If the output shows /tmp is mounted, move to the next step.
* If nothing appears, you'll need to mount it manually or configure it in /etc/fstab.

### 🔒 Step 2: Remount /tmp with Secure Flags

To harden /tmp, use the following command:

```
sudo mount -o remount,noexec,nosuid,nodev /tmp
```

---

| Flag     | Purpose                                                |
| -------- | ------------------------------------------------------ |
| `noexec` | Prevents execution of binary or script files           |
| `nosuid` | Blocks set-user-ID (SUID) and set-group-ID (SGID) bits |
| `nodev`  | Disables device file creation                          |

---

### 🧪 Step 3: Test It — Try Executing a Script from /tmp

Let’s simulate a small test to confirm /tmp is hardened.

```
echo -e '#!/bin/bash\necho hacked!' > /tmp/hack.sh
chmod +x /tmp/hack.sh
./tmp/hack.sh
```

### 🛑 Expected Result:

You should get a permission denied error, which confirms the script execution was blocked:

---

## 📌 Conclusion
> By applying the correct mount flags, you've secured a critical part of your Linux system.
This protects against many types of malware, privilege escalation, and DoS attacks commonly launched via the /tmp directory.
