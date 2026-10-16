# FAQ/Troubleshooting

[🏠 Document Top](../index.md) | [⚖️ Terms of Service](./terms.md) | [🔒 Privacy Policy](./privacy.md)

---


This section covers frequently asked questions and solutions for common problems.

> **Note (Integral parameters)**
> Integral is supported, but some camera parameter values may not be recorded or displayed correctly.

## Frequently Asked Questions

### Images Not Displaying

**Symptom:** Images don't appear in the gallery, or thumbnails won't load

**Solutions:**

1. **Check if folders are properly imported**
   - Open **Gallery** > **Import** and verify the folder is listed
   - Confirm folder status shows "Enabled"

2. **Check the image format**
   - Import supports PNG, JPG, JPEG, GIF, BMP, and WebP
   - Unsupported formats are skipped automatically

3. **Check if files are corrupted**
   - Verify you can open the images in an image viewer

4. **Try reloading**
   - Click the reload button (refresh icon) on the gallery screen

---

### Metadata Not Being Captured

**Symptom:** World name or username shows as "Unknown"

**Solutions:**

1. **Confirm VRChat was running**
   - VSA uses information embedded in the photo together with VRChat log/OSC data
   - Photos taken without VRChat running may not include world or user information

2. **Confirm VSA was running in background**
   - VSA must be running at the time of capture

3. **Check OSC settings**
   - Verify OSC is enabled in VRChat settings
   - Verify OSC output is enabled on the camera you use (VirtualLens2, Integral, FishEye, or TelePortraitLens)

4. **Check log files**
   - Verify VRChat log files are being output correctly
   - Location: `%LOCALAPPDATA%Low\VRChat\VRChat\`

---

### JXL Compression Not Progressing

**Symptom:** Compression process doesn't start or stops midway

**Solutions:**

1. **Check disk space**
   - Compression requires approximately 1.2x the input file size in free space

2. **Check file permissions**
   - Read permission for input folder
   - Write permission for output folder

3. **Check automatic archive status**
   - Confirm automatic archiving is enabled on the JXL Compression screen
   - Open the archive manager’s Problems tab and retry any available action

4. **Check process in Task Manager**
   - Verify VSA process is responding
   - If not responding, restart the application

---

### Gallery is Slow

**Symptom:** Scrolling is choppy, loading is slow

**Solutions:**

1. **Adjust thumbnail size**
   - Larger thumbnails require more processing power
   - Try zooming out to display smaller thumbnails

2. **Close other applications**
   - High memory usage can degrade performance

3. **Check sort mode**
   - Sorting loads all data, which may cause slowdowns

4. **Restart the application**
   - Restart VSA after processing completes and check the gallery again

---

### App Won't Start

**Symptom:** VSA doesn't start when clicked

**Solutions:**

1. **Close existing processes**
   - Check if VSA process remains in Task Manager
   - If so, end it and restart

2. **Check settings state**
   - Settings files may be corrupted
   - Do not delete the settings folder manually; if a restart does not help, contact support with logs and the symptoms

---

### Start VSA when Steam VRChat launches

On Windows Steam VRChat (App ID 438100), open Game Settings from the sidebar and enable **Start VSA with VRChat** in **Plugins**. VSA is added to Steam Launch Options and starts with VRChat. VRChat still launches if VSA cannot be started.

If Steam is running, VSA will ask you to quit Steam and retry because Steam may overwrite a file changed while it is open. Existing third-party wrappers, cmd/PowerShell commands, complex syntax, and multiple `%command%` placeholders are not changed automatically for safety. Steam-side changes take precedence.

### VRChat still launches after uninstalling VSA

The uninstaller attempts to restore VSA-managed Launch Options when they have not been changed. If Steam is running or another app changed the options, it leaves them untouched and continues uninstalling.

In that case, before uninstalling, open VRChat's Steam properties and remove only the VSA portion containing `vsa-mainapp.exe` and `--minimized`. Keep wrappers for other apps and VRChat's own arguments.

---

### Game Settings tabs are missing

Open **Game Settings** from the sidebar. The screen has **Display Settings**, **Plugins**, and **Time Machine** tabs. The similarly named Game Settings panel under Settings contains only folders and OSC.

### Notifications are not displayed

1. In Settings > **Notification**, enable **OS notifications** or **Toast notifications**.
2. Enable the notification types you want.
3. Allow VSA notifications in Windows settings when using OS notifications.
4. Turn on **Play notification sound** if you also want sound.

### A shortcut does not work

Open Settings > **Shortcut** and confirm the binding. Gallery shortcuts work in the gallery, retouch shortcuts work in retouch, and browser/OS-reserved or duplicate bindings cannot be registered.

---

### Account or Cloud Controls Are Missing

Accounts, cloud save, X posting, and event capture are being prepared for general availability and are hidden with normal settings. Local import, albums, and favorites work without an account. Keep important photos backed up separately.

## Troubleshooting

### Finding VRChat Logs

VRChat log files are located at:

```
%LOCALAPPDATA%Low\VRChat\VRChat\
```

You can access this by entering the path in Windows Explorer's address bar.

Log file names follow the format `output_log_date_time.txt`.

### Verifying OSC Communication

To check if OSC communication is working correctly:

1. Open VRChat settings
2. Navigate to the OSC section
3. Verify "OSC" is enabled
4. If needed, enable "OSC Debug Console" to monitor communication

### Photo data problems

Manual deletion or replacement of VSA-managed data can remove photos and favorites. Make a backup first, then contact support with logs and the symptoms instead of changing managed data directly.

### Checking Log Files

Check the log folder in Game Settings > **Display Settings > Log folder**. When unset, VSA uses the OS default.

When problems occur, error information is recorded in these log files.

## Contact

If the above methods don't solve your issue, please contact us through the following:

1. **GitHub Issues**
   - Bug reports and feature requests are accepted on GitHub Issues
   - Attaching log files helps identify problems more easily

2. **Attaching Log Files**
   - When contacting us, please provide the following information:
     - Detailed description of the problem
     - Steps to reproduce
     - VSA version
     - Windows version
     - Related log files

## Known Issues

The currently known limitation is that metadata may not be captured correctly in some VRChat worlds.
