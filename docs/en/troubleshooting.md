# Troubleshooting Detailed Guide

[🏠 Document Top](../index.md) | [⚖️ Terms of Service](./terms.md) | [🔒 Privacy Policy](./privacy.md)

---


This guide provides solutions for problems that may occur in the VSA application. It is organized to help you resolve issues systematically, with specific symptoms and step-by-step solutions provided for each problem.

## Common Problems and Solutions

### Import-Related Issues

#### Photos Are Not Automatically Imported

**Symptom**: Screenshots taken in VRChat are not automatically imported into VSA

**Possible Causes**:
- VSA is not running or the watch folder is incorrect
- Folder path is incorrect

**Solution (Step-by-Step)**:

**Step 1: Check Monitoring Status**
1. Leave VSA running
2. Check that the sidebar reports folder monitoring
3. Take a screenshot in VRChat

**Step 2: Verify Folder Path**
1. Open Game Settings > Display Settings
2. Check the "Watch folder" setting
3. Default path is typically `C:\Users\[YourUsername]\Pictures\VRChat`
4. Verify the path is correct and re-select if necessary

**Step 3: Verify VRChat**
1. Confirm that screenshots are actually being taken in VRChat
2. Open Windows Explorer and check if photo files exist in the specified folder
3. Verify that the filename and capture time match

**Step 4: Restart the Application**
1. Completely close VSA
2. Close VRChat as well
3. Restart VSA
4. Launch VRChat
5. Take a screenshot

**If Still Not Resolved**:
Refer to [Checking Log Files](#how-to-check-log-files) to examine detailed errors.

#### Thumbnails Are Not Displayed

**Symptom**: Thumbnails in the gallery appear gray or are not displayed at all

**Possible Causes**:
- Thumbnail generation is in progress
- Thumbnail generation failed

**Solution (Step-by-Step)**:

**Step 1: Wait for Processing to Complete**
1. Display the gallery
2. Check the "Processing..." indicator at the top of the screen
3. Wait until the indicator disappears (may take several minutes)

**Step 2: Try Scrolling**
1. Scroll up and down in the gallery
2. Thumbnails will be loaded dynamically while scrolling

**Step 3: Restart the Application**
1. Completely close VSA
2. Wait a few seconds
3. Restart VSA
4. Display the gallery

**Step 4: Contact Support with Logs**
If the problem persists, provide the log and reproduction steps to support.

### Gallery Display-Related Issues

#### Gallery Performance Is Slow

**Symptom**: Photo display or scrolling is slow, or the application freezes occasionally

**Possible Causes**:
- Large number of photos being loaded
- Thumbnail size is too large
- Animation settings are enabled
- Insufficient memory

**Solution (By Priority)**:

**Solution 1: Reduce Thumbnail Size**
1. Display the gallery
2. Drag the zoom slider in the toolbar to the left
3. This will reduce the thumbnail size
4. Check if scroll speed improves

**Solution 2: Disable Animations**
1. Open Settings
2. Select the "Animation" panel
3. Disable animation effects
4. Screen effects will be lighter

**Solution 3: Delete Unnecessary Photos**
1. Select unnecessary photos in the gallery
2. Click the Delete button
3. Reducing total file count will reduce processing load

**Solution 4: Restart the Application**
1. Completely close VSA
2. Wait a few seconds
3. Restart VSA
4. Memory will be reset

**Solution 5: Check PC Memory**
1. Open Task Manager (Ctrl + Shift + Esc)
2. Click on the "Performance" tab
3. Check memory usage
4. If usage is 90% or higher, your PC has insufficient memory
5. Close other applications

#### Photos Are Not Displayed

**Symptom**: Nothing is displayed in the gallery, or "No photos" is shown

**Possible Causes**:
- Import has not completed
- Folder path is incorrect
- Photo files have been deleted

**Solution (Step-by-Step)**:

**Step 1: Verify Import Folder**
1. Open Game Settings > Display Settings
2. Check the "Watch folder" path
3. Open that folder in Windows Explorer
4. Verify that photo files exist (`.png` or `.jpg` files)

**Step 2: Check Import Process**
1. Open the Import Folder view
2. Check the processing indicator
3. Wait until the indicator disappears

**Step 3: Manual Reload**
1. Display the gallery
2. Click the "Reload" button (⟲) in the toolbar
3. This will refresh the photo list

**Step 4: Check Settings and Logs**
1. Open Game Settings > Display Settings and verify the watch folder
2. Capture a new photo and wait for import to finish
3. If the problem persists, contact support with the log and symptoms

### JPEG XL Compression-Related Issues

#### Compression Does Not Start

**Symptom**: Older photos are not processed after automatic archiving is enabled

**Possible Causes**:
- Automatic archiving is disabled
- No photos are older than the selected threshold
- The photo output folder, archive destination, or free disk space has a problem

**Solution (Step-by-Step)**:

**Step 1: Verify Automatic Archiving**
1. Open the JXL Compression screen
2. Confirm automatic archiving is enabled and the age threshold is appropriate

**Step 2: Check the Destination and Problem Status**
1. Confirm VSA can read and write the photo output folder and its `VSA-Archive` subfolder
2. Check available disk space
3. Open the archive manager’s Problems tab and retry the available action

**Step 3: Manually Run Compression**
1. Open the JPEG XL Compression view
2. Click "Select Folder" to choose the folder to compress
3. Click the "Run Compression" button
4. Verify that manual execution works

#### Image Quality Degrades After Compression

**Symptom**: After JPEG XL compression, images appear corrupted or colors have changed

**Solution**:

VSA's JPEG XL compression uses **lossless (reversible) compression**, so image quality should not degrade. The following causes are possible:

**Cause 1: Original Image Is Already Compressed**
- Images output by VRChat are already compressed, so no visual changes from further compression are expected
- This is normal behavior

**Cause 2: File Is Corrupted**
1. Check detailed logs (Developer Mode)
2. If errors exist, redo the compression
3. If the same error occurs, the original file may be corrupted

### VRChat Integration-Related Issues

#### Metadata Cannot Be Retrieved

**Symptom**: World name, user name, capture time, and other photo metadata are not displayed

**Possible Causes**:
- VRChat logs cannot be read
- Log folder path is incorrect
- VRChat is an old version

**Solution (Step-by-Step)**:

**Step 1: Verify the Log Folder**
1. Open Game Settings > Display Settings
2. Confirm that "Log folder" points to the VRChat log folder

**Step 2: Verify VRChat Logs**
1. Launch VRChat and enter a world
2. Check that a log is created in `C:\Users\[Username]\AppData\LocalLow\VRChat\VRChat`
3. Restart VRChat if no log is created

**Step 3: Check Log Folder**
1. Verify the log folder path shown in Game Settings
2. Open that folder in Windows Explorer
3. Verify that log files such as `output_log_*.txt` exist
4. If not, reconfigure the log folder path

**Step 4: Take New Screenshots**
1. After completing all settings, take new screenshots
2. Metadata will not be applied to existing photos
3. Verify that metadata is applied to new photos

#### OSC Communication Cannot Be Established

**Symptom**: Camera parameters (such as VirtualLens2) cannot be retrieved

**Possible Causes**:
- OSC receive and send ports are not paired correctly
- OSC is disabled on VRChat side
- Firewall is blocking
- Port number is in use

**Solution (Step-by-Step)**:

**Step 1: Verify Port Number**
1. Open Game Settings > Display Settings
2. Check "VSA receive port (VRChat sends)" (default: 9001)
3. Check "VSA send port (VRChat receives)" (default: 9000)
4. Verify the corresponding VRChat send and receive ports

**Step 2: Enable OSC on VRChat Side**
1. Launch VRChat
2. Open the Settings menu
3. Check "Enable OSC"
4. Restart VRChat

**Step 3: Check Firewall Settings**
1. Open Windows Security Center
2. Click on "Firewall & network protection"
3. Click on "Advanced settings"
4. Verify that the OSC ports (9001, 9000, etc.) are allowed in both "Inbound rules" and "Outbound rules"
5. If communication is blocked, contact support with the log and symptoms

**Step 4: Check for Port Conflicts**
1. Open Command Prompt (Windows + R → cmd)
2. Run the following command:
   ```
   netstat -ano | findstr ":9001 :9000"
   ```
3. Verify that no other processes are using the port
4. If in use, change to a different port number

**Step 5: Restart VSA**
1. Completely close VSA
2. Wait a few seconds
3. Restart VSA
4. Use the camera in VRChat

#### VRChat Launch Is Not Detected

**Symptom**: VSA does not detect when VRChat is launched (notification does not appear)

**Possible Causes**:
- VSA is not running or process detection failed
- VRChat process detection failed

**Solution**:

**Step 1: Verify Monitoring Status**
1. Leave VSA running
2. Check the folder-monitoring status in the sidebar

**Step 2: Restart VRChat**
1. Completely close VRChat
2. Restart VSA as well
3. Launch VRChat

### Account or Cloud Controls Are Missing

Accounts, cloud save, X posting, and event capture are being prepared for general availability and are hidden with normal settings. A missing menu alone does not indicate a connection failure. Local photo management works without an account. Keep important photos backed up separately.

### Notification-Related Issues

#### Notifications Are Not Displayed

**Symptom**: Settings show notifications are enabled, but desktop notifications do not appear

**Possible Causes**:
- VSA is not allowed in Windows notification settings
- Focus Assist is enabled
- Windows notification sounds or VSA notification sounds are disabled

**Solution (Step-by-Step)**:

**Step 1: Check Windows Notification Settings**
1. Open Windows Settings (Windows + I)
2. Click on "System"
3. Click on "Notifications"
4. Verify that VSA is included in the allowed apps list
5. If not, add it from "Allowed notifications"

**Step 2: Check Focus Assist**
1. Open Windows Action Center (Win + A)
2. Verify that "Focus Assist" is not turned "On"
3. If on, turn it off

**Step 3: Check Notification Settings**
1. Open VSA Settings
2. Select the "Notifications" panel
3. Verify that **OS notifications** or **Toast notifications** is enabled
4. Verify that individual notification types are enabled

**Step 4: Check Notification Sound**
1. In Settings > Notification, verify that **Play notification sound** is enabled
2. Verify that Windows notification sounds and the VSA app are not muted

### Performance-Related Issues

#### Application Startup Is Slow

**Symptom**: VSA takes tens of seconds or more to start

**Possible Causes**:
- Large number of photos
- Slow disk access

**Solution (By Priority)**:

**Solution 1: Delete Unnecessary Photos**
1. Select old photos in the gallery
2. Click the Delete button
3. This reduces the amount of work at startup
4. Verify if startup speed improves

#### Memory Usage Is High

**Symptom**: VSA memory usage keeps increasing or your PC becomes slow

**Possible Causes**:
- Large number of photos being loaded

**Solution (By Priority)**:

**Solution 1: Reduce Thumbnail Size**
1. Display the gallery
2. Drag the zoom slider to the left
3. Reduce thumbnail size
4. Check if memory usage decreases

**Solution 2: Close Photo Details Sidebar**
1. Close the open photo details panel
2. Check if memory usage decreases

**Solution 3: Restart the Application**
1. Completely close VSA
2. Wait a few seconds
3. Restart VSA
4. Memory will be reset

## How to Check Log Files

By examining VSA's detailed logs, you can more accurately identify the cause of problems.

### Log File Location

```
%APPDATA%/VSA/logs/
```

**Shortcut**:
1. Windows Key + R
2. Type `%APPDATA%` and press Enter
3. Double-click the `VSA` folder
4. Double-click the `logs` folder

### Log File Structure

Log files rotate daily:

```
logs/
├── vsa-mainapp.log
└── vsa-mainapp.log.2026-08-31
```

**To open the latest log file**: Open `vsa-mainapp.log`.

### How to Read Log Files

Log files are text files that can be opened in Notepad or VSCode.

**How to Identify Log Levels**:

| Log Level | Symbol | Meaning |
|-----------|--------|---------|
| ERROR | [ERROR] | Critical error (problem has occurred) |
| WARN | [WARN] | Warning (caution needed) |
| INFO | [INFO] | Normal information (reference info) |
| DEBUG | [DEBUG] | Debug information (for developers) |

**How to Check for Errors**:
1. Open the latest log file in a text editor
2. Use Ctrl + F to search for "ERROR"
3. Check the error message
4. Take action based on the error message

**Example**:
```
ERROR Failed to connect to screenshot folder: Access Denied
```

This error indicates that there are no access permissions to the screenshot folder.

## Managed Data or Settings Problems

The current public build does not provide a supported procedure to delete, replace, or rebuild VSA-managed data or settings manually. Incorrect changes can remove photos or favorite state.

1. Completely close and restart VSA
2. Check permissions and free space for the watch, output, and log folders
3. If the problem persists, contact support with the log, VSA version, and reproduction steps

## How to Contact Support

If the above solutions do not resolve your issue, you can contact support.

### Information Required for Inquiry

Please provide the following information:

**1. Environment Information**:
- VSA version (check in Settings > Update)
- Windows version (Windows + R → winver)
- PC specifications (CPU, memory, disk)

**2. Problem Details**:
- Specific symptoms occurring
- When the problem started occurring
- Steps to reproduce the problem

**3. Error Messages**:
- Take a screenshot of any displayed error messages

**4. Log Files**:
- Latest log file (`%APPDATA%/VSA/logs/vsa-mainapp.log`)

### Contact Methods

**GitHub Issues**:
- [VSA-MainApp Issues](https://github.com/fefaether/VSA-Mainapp/issues)
- GitHub account is required
- Provide detailed information according to the template

**Email**:
- virtualsnaparchive@gmail.com
- Include detailed inquiry and the above information

## Related Information

- [FAQ](faq.md) - Frequently Asked Questions
- [Game Settings Guide](game-config.md) - Configuration Troubleshooting
- [Settings Screen Complete Guide](settings-guide.md) - Settings Details
- [Favorites Guide](favorites-guide.md) - Cloud save and favorites troubleshooting
