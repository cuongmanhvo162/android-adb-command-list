### get list service specified package name

- adb shell pidof "package name"

### query registered receiver with specified intent

- adb shell cmd package query-receivers --brief -a "intent name"

### get PendingIntent and AlarmManager registered

- adb shell dumpsys alarm 

### get current activity

- adb shell dumpsys activity

### get deviceidle.xml info

- adb shell dumpsys deviceidle

### get whitelisted apps

- adb shell dumpsys deviceidle whitelist

### get latest activity

- adb shell dumpsys activity recents | find "Recent #0"

### print logcat on console

- adb locat

### save logcat to file. While it running, use Ctrl+C  to stop the logging.

- adb logcat > "filename".txt

### force stop everything associated with the app. Introduced in Honeycomb. This will completely kill all associated AlarmManager, Service, Broadcast Receiver of the app.

- adb shell am force-stop "pacekage name"

**To check connected devices when ROM is running on phone:** 

- adb devices

**To boot into bootloader mode:** 

- adb reboot bootloader

**To check connected devices when in bootloader mode:** 

- fastboot devices

**To boot into ROM:**  

- fastboot reboot

**To boot into recovery:**  

- fastboot reboot recovery