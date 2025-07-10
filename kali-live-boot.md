✅ Kali Linux Live Boot – Reset Windows Password via SAM File

# 🧪 Reset Windows Password Using Kali Linux Live Boot

This method involves booting into Kali Linux using a live USB and modifying the **SAM (Security Account Manager)** file to clear or reset user account passwords in Windows.

> ✅ No need to replace system files  
> ⚠️ Works only on **unencrypted drives** (BitLocker must be off)

---

## 🛠️ Requirements

- A **Kali Linux Live USB** (8GB+)
- A system with **boot access control**
- Basic knowledge of Linux terminal

---

## 🚀 Steps to Reset Password via Kali Live Boot

### 1️⃣ Create a Kali Linux Live USB

- Download Kali ISO: [https://www.kali.org/get-kali/](https://www.kali.org/get-kali/)
- Use [Rufus](https://rufus.ie) or BalenaEtcher to flash it:
  - Select ISO
  - Select your USB
  - Click **Start**

---

### 2️⃣ Boot Into Kali

1. Plug the USB into the target machine.
2. Restart and boot from USB (use keys like `F12`, `ESC`, or `F10` to access boot menu).
3. Select **Live System (forensic or regular mode)** and press Enter.

---

### 3️⃣ Locate the Windows Partition

- On the Kali desktop, you should see a drive icon that represents the **Windows file system** — double-click to mount it.

---

### 4️⃣ Open Terminal in the System32 Directory

Right-click inside the mounted partition window → **Open Terminal Here**

Then run:

```bash
cd Windows/System32/config
ls SAM*
````

✔️ If the `SAM` file is listed, proceed to the next step.

---

### 5️⃣ Launch chntpw to Edit SAM

```bash
sudo chntpw -i SAM
```

You'll see an interactive menu.

---

### 6️⃣ Edit User Password

1. Type `1` to **Edit user data and passwords**
2. A list of Windows users will appear with RID and usernames
3. Type the user number or name and press Enter

Now you'll see options like:

```
1 - Clear (blank) user password
2 - Unlock and enable user account
```

4. Type `1` and press Enter
5. Then type `2` and press Enter (optional but useful)
6. Press `q` to quit
7. Type `y` to **save changes**

---

### 7️⃣ Reboot and Log In

* Restart the computer and remove the USB
* The selected Windows user account should now **have no password**
* Log in directly without entering one

---

## ⚠️ Notes & Warnings

* BitLocker-encrypted drives will not allow this method.
* The `chntpw` tool only works on local (not Microsoft online) accounts.
* Always have permission before performing this on any system.

---

## 🛡️ Legal Disclaimer

This method is for:

* Password recovery for your own systems
* Digital forensics or ethical hacking education
* Cybersecurity awareness & research

❌ **Unauthorized use is illegal. Always act ethically and with permission.**

---

🔐 *Master tools. Respect boundaries. Hack ethically.*
