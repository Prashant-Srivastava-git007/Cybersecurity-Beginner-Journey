# 🧪 Mini Lab – Day 12: "Suspicious Process Hunt"

🎯 **Mission**: A strange system lag has been reported. As a junior analyst, your task is to identify and terminate any suspicious process consuming excessive CPU or memory.

---

## 🛠️ Solution Steps

### ✅ Step 1: Simulate a Process

Launch any application or run a command that consumes CPU to simulate a process.

```bash
# Example: Stress the CPU (optional)
yes > /dev/null &
```

---

### 🔍 Step 2: Identify the Suspicious Process

Use one of the following to monitor system processes:

```bash
ps -u <username>       # View processes by a specific user
top                    # View real-time resource usage
htop                   # (If installed) Better UI to monitor usage
```

---

### ❌ Step 3: Terminate the Process

Once identified, kill the process using its PID (Process ID):

```bash
kill <process-id>
```
> 🔒 Use sudo if needed for elevated privileges.

---

