# 🛡️ Linux Logs & System Monitoring (Forensics Foundation)

System logs are critical for monitoring events, processes, and messages from applications, the operating system, and other system components. These logs help track user activities, detect anomalies, and troubleshoot issues.

---

## 📁 Linux Log Directory: `/var/log/`

This is the main directory where most system logs are stored. To navigate:

```bash
cd /var/log
ls -l
```

---

## 🔍 Common Log Files

| File/Directory  | Description |
|-----------------|-------------|
| `boot.log` | 	Contains messages related to the system boot process. Useful for analyzing boot-time issues. |
| `cron` | Stores logs related to scheduled cron jobs. Helps confirm if automated scripts executed. |
| `secure` | Logs authentication events like login attempts and sudo usage. Crucial for security auditing. |
| `maillog` | 	Contains logs from mail services (e.g., Postfix, Sendmail). Important for mail server setups. |
| `httpd` | 	Contains logs for the Apache HTTP server (if installed). Useful for web diagnostics. |
| `messages` | 	Stores general system messages, kernel logs, and hardware info. Good for overall system tracking. |

> Note the structure of log file can be vary based on Linux distribution.

---

## 🔎 Log Monitoring Commands

| Command | Use                            |
|---------|--------------------------------|
| `cat <file>` or `less <file>` | View the full content of a log file |
| `tail -f <log>` | 	Monitor logs live in real time |
| `dmesg` | displays kernel and hardware-related messages in real time |
| `jrounalctl -xe` | 	View system logs with detailed info via systemd |
| `grep "Failed" auth.log` | 	Filter for failed login attempts or errors |

---

## ⚙️ Important Tools for Log Monitoring

| Tool | Description |
|------|-------------|
| `journalctl` | 	Reads logs collected by systemd. Allows powerful filtering and real-time analysis. |
| `awk` | Used for extracting patterns or fields from logs. Useful in scripting log parsers. |
| `tail` | Monitors the end of files in real-time. Common for watching growing log files. |
| `logwatch` | 	Generates daily summaries from system logs. Great for system health reports. |
| `kibana` | A visual interface for logs (with Elasticsearch). Helps create dashboards from log data. |

---

## 💻 Sample Commands to Practice

```bash
cd /var/log                     # Navigate to system logs
ls -l                           # List log files
cat auth.log                   # View authentication log
tail -f syslog                 # Monitor syslog in real time
journalctl -xe                # Analyze detailed logs using systemd
dmesg | less                   # View kernel-related logs
grep "Failed" auth.log         # Search for failed logins
```

---

> 🧠 Pro Tip: Logs are the digital footprints of everything happening in your system. Understanding them is foundational for both cybersecurity and system administration.
