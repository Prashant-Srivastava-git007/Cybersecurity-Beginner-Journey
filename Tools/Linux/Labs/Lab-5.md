# 🧪 Mini Lab: The Secure Gateway

## 🎯 Mission:
Harden SSH on your Kali machine (or VM) and connect to it securely from a Windows machine.

---

## 🛡️ Steps:

### 🔧 1. Change SSH Port to `2222`

```bash
sudo nano /etc/ssh/sshd_config
```

* Find the line:
  ```
  #Port 22
  ```
* Change it to
    ```
    Port 2222
    ```

* 🔄 Then restart the SSH service:
  ```
  sudo systemctl restart ssh
  ```

  ---

### 🚫 2. Disable Root Login
  * In the same file /etc/ssh/sshd_config, find this line:
    `PermitRootLogin yes` Change it to `PermitRootLogin no`

  * 🔄 Then restart the SSH service:
  ```
  sudo systemctl restart ssh
  ```

---

### 🔐 3. Generate an SSH Key Pair (on Windows)
* On your Windows machine, open PowerShell and run:
  ```
  ssh-keygen
  ```

* Press Enter to accept default paths and skip passphrase (for lab use).

  ---

 ### 🚀 4. Copy Public Key to Linux Machine
  Still in PowerShell, run:

  ```
  type $env:USERPROFILE\.ssh\id_rsa.pub | ssh username@remote_host "mkdir -p ~/.ssh && cat >> ~/.ssh/authorized_keys"
  ```

  ---

### 🧪 5. Test Passwordless SSH Login
Try logging in without a password:
```
ssh username@ip-address -p 2222
```

---

### 🔥 6. Restrict SSH Access Using UFW
✅ Step 1: Enable UFW if it's not already active:
```
sudo apt install ufw -y
sudo ufw enable
```
✅ Step 2: Allow SSH only from your Windows IP:
```
sudo ufw allow from <your_host_ip> to any port 2222 proto tcp
```
❌ Step 3: Deny Default SSH Port:
```
sudo ufw deny 22
```
🔍 Step 4: Check UFW Rules:
```
sudo ufw status numbered
```
