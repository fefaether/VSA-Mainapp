# Settings Guide - Complete Reference

## How to open

Open **Settings** from the VSA sidebar.

![Settings screen](../assets/screenshots/settings-system.webp)

[🏠 Document Top](../index.md) | [⚖️ Terms of Service](./terms.md) | [🔒 Privacy Policy](./privacy.md)

---


The Settings panel allows you to customize VSA's appearance, behavior, integrations, update checks, and user-facing legal/support information.

The **Application Info** and **Tutorial** panel descriptions apply to development build v0.9.0. They may not appear in distributed v0.8.2.

## Accessing Settings

Click the gear icon (⚙️) in the sidebar to open the Settings screen.

The left menu normally contains 11 panels. When the cloud UI is available, **X Post** appears after **Shortcut**, for 12 panels:

1. **System** - startup and background behavior
2. **Application Info** - version and connection status
3. **Appearance** - theme, color, and language
4. **Animation** - motion and transition settings
5. **Game Settings** - watch, output, and log folders plus OSC
6. **Notification** - notification settings
7. **Shortcut** - keyboard shortcuts
8. **Favorites** - favorites management
9. **Tutorial** - start in-app tutorials
10. **Update** - update checks and release notes
11. **Other** - terms, privacy policy, licenses, external links, and important notices

When the cloud UI is available, **X Post** appears after **Shortcut**, shifting the panels that follow down by one.

## System Panel

- **Run at PC startup**: Starts VSA when you sign in to Windows.
- **Open new photos in VR preview**: Automatically shows VSA's VR capture mode when a new photo is detected.
- **VR preview curvature**: Adjusts the curvature of the photo surface shown in VR.
- **Automatically archive older photos**: Choose an age threshold of 1, 2, 3, 4, 6, or 12 months. Archives are stored in `VSA-Archive` under the current photo output folder.

Start **Photographer Mode** from the VR icon in the title bar to review newly captured photos full screen. Configure automatic VR preview display and its curvature in this System panel. See the [Photographer Mode Guide](photographer-mode.md) for the full-screen controls.

## Application Info Panel

Review the installed version, VRChat connection status, and photo-watcher status. Use **Refresh status** to retrieve the current status again.

## Appearance Panel

Configure how VSA looks and displays information.

### Theme Settings

Choose the visual theme for the application.

**Theme Options**:
- **Light**: White background with dark text (for bright environments)
- **Dark**: Dark background with light text (reduces eye strain)
- **System Linked**: Automatically follows Windows theme settings (Recommended)

**How to Change**:
1. Select your preferred theme
2. Changes apply immediately with smooth fade transition
3. Window content updates in real-time

### Language Setting

Choose the UI language for the entire application.

**Available Languages**:
- **Japanese**: Most of the interface appears in Japanese.
- **English**: Most of the interface appears in English. In-app tutorials are currently shown in Japanese.

**How to Change**:
1. Select language from dropdown
2. Application UI updates immediately
3. Most translated text updates to the selected language; some content may remain in Japanese
4. Setting persists across sessions

**Note**: Some interface text may still appear in Japanese.

### Theme Color Selector

Choose an accent color for the application interface.

**3 Preset Colors Available**:
- **Darkroom**: Graphite and amber
- **Night Scene**: Blue-black and cobalt
- **Print**: Warm white and teal ink

**How to Use**:
1. Click on desired color swatch
2. Color preview appears in real-time
3. All UI elements (buttons, accents, highlights) change immediately
4. Selection applies to entire application

**Animation Effects**:
- Color transitions include smooth animation
- Fade-in effect when selecting new color
- Multiple interactive elements animate simultaneously

## Animation Panel

Control visual effects and transitions throughout the application.

### Animation Effects Toggle

Enable or disable UI animations and transition effects.

**When Enabled**:
- Fade transitions between views
- Smooth scroll animations
- Button press animations
- Panel opening/closing animations

**When Disabled**:
- UI changes appear instantly
- No transition effects
- Faster perceived responsiveness
- Lower GPU usage

**Use Cases**:
- Enable for modern, polished feel
- Disable if animations cause discomfort or on low-end systems

## Notification Panel

Configure notification methods, event types, and notification sound.

### Notification Methods

Toggle OS notifications and in-app toast notifications independently.

- **OS notifications**: Show in the Windows notification center
- **Toast notifications**: Show a toast in the bottom-right of the app
- When both are OFF, no notifications are shown.

Allow VSA notifications in Windows settings when using OS notifications.

### Notification Types

When either notification method is enabled, configure these events independently:

- **Import complete**: When image import finishes
- **Photo import in progress**: When the game takes a photo
- **Compression complete**: When JXL compression finishes
- **Error notifications**: When an error occurs
- **VRChat startup**: When VRChat starts
- **VRChat exit**: When VRChat exits

### Sound

Turn on **Play notification sound** to play a sound when a notification is shown. There is no volume slider or notification-history setting in this panel.

Open the bell icon in the bottom status bar to review notification history. Opening it marks the current items as read; there are no per-item delete or clear-all controls.

## Shortcut Panel

Manage keyboard shortcuts for frequent operations.

### Implemented Shortcuts (9 total)

**Display Operations**:
- **Screen Size Toggle** (F10): Cycle through window sizes (1280×720 → 1600×900 → 1920×1080 → 2560×1440)
- **Fullscreen Toggle** (F11): Switch between window and fullscreen modes
- **Gallery Zoom In** (Ctrl + =): Increase thumbnail size
- **Gallery Zoom Out** (Ctrl + −): Decrease thumbnail size
- **Retouch Fit to Window** (F): Fit the retouch preview to the window
- **Retouch Zoom In** (Ctrl + ;): Increase the retouch preview size
- **Retouch Zoom Out** (Ctrl + −): Decrease the retouch preview size
- **Retouch Rotate Left**: Check the current binding in Settings > Shortcut
- **Retouch Rotate Right**: Check the current binding in Settings > Shortcut

In development build v0.9.0, a rotation key may be unassigned. Check the Shortcut panel for the current binding before using it.

### Customizing Shortcuts

**How to Change a Shortcut**:
1. Locate the shortcut you want to change
2. Click on the shortcut field (becomes highlighted)
3. Enter your new key combination:
   - Press and hold modifier keys (Ctrl, Shift, Alt, Win)
   - While holding modifiers, press your desired key
   - Release all keys
4. New combination displays in the field
5. The new binding is saved automatically; there is no Save button.

**Example Combinations**:
- Single key: `F2`
- With modifier: `Ctrl + Shift + S`
- Multiple modifiers: `Ctrl + Shift + Alt + S`

### Resetting to Defaults

**Reset All Shortcuts**:
1. Open Settings > Shortcut panel
2. Click **Reset all**
3. All shortcuts return to default values

**Warning**: This action cannot be undone. Note current customizations if needed.

See [Keyboard Shortcuts Complete List](keyboard-shortcuts.md) for detailed information.

## Game Settings Panel

The Game Settings panel in Settings contains the sidebar Game Settings **Display Settings**: watch, output, and log folders plus OSC. Switches and fields save automatically; there is no manual Save button.

Configure Steam, Virtual Desktop, and VRChat outage notifications in [Game Settings](game-config.md) > **Plugins**. Review the event history in its **Time Machine** tab.

## Favorites Panel

Choose the folder used to keep copies of favorite photos and migrate existing favorites.

### Favorites Folder Migration

**Purpose**: Copy existing favorite photos to the selected favorites folder.

**Steps**:
1. Choose a folder under **Save destination folder**
2. Click **Migrate favorite photos**
3. Review the successful and failed counts and any failed-photo details

When you mark a photo as a favorite, VSA copies the original to the configured folder. Removing one favorite with the star button in the detail sidebar deletes the tracked copy. Bulk removal in Favorites selection mode only clears favorite status and leaves both the original and the copy.

See [Favorites Guide](favorites-guide.md) for complete favorites information.

## Tutorial Panel

Select a tutorial in Settings > Tutorial to start its in-app walkthrough. A check mark indicates a completed tutorial. Tutorial content is currently shown in Japanese.

## Update Panel

Check the installed version, check for updates, and open release notes.

### Check for Updates

Click **Check for updates** to look for a newer version. When one is available, review the details and download it to restart VSA.

### Version Information and Release Notes

**Current Version Display**:
- Shows installed VSA version
- Format: X.X.X

Click **Release notes** to open the notes for the current version. External links such as GitHub Releases and documentation are in the **Other** panel.

## Other Panel

The Other panel collects user-facing documents and notices.

### Terms, Privacy, and Licenses

You can open:

- Terms of Service
- Privacy Policy
- License information
- The latest privacy policy URL used for Google OAuth publishing settings

### External Links

You can open:

- Documentation home
- GitHub Releases

### Important Notices

The panel summarizes:

- The correct app name is **Virtual Snap Archive**. VSA is unofficial and is not affiliated with, endorsed by, or supported by VRChat Inc., VirtualLens2, Integral, or their respective rights holders.
- Core local features are free. Cloud storage and X API features may require payment beyond the free allowance.
- External communication occurs when using VSA accounts, cloud storage, X posting, Turnstile, update checks, or server status features.
- Local file access is centered on the watched folders, export destinations, and managed app data that the user selects or configures.
- Windows installers may be unsigned and may trigger SmartScreen or security software warnings.

## Returning Settings to Defaults

There is currently no single button that resets every setting. Use the reset action provided by the relevant screen:

- Game Settings: reset the output or log folder individually
- Shortcut: **Reset all** returns all 9 shortcuts to their defaults (no confirmation dialog)
- Other settings: select the desired values manually

Do not delete or replace VSA-managed data manually. If the problem persists, contact support with the log and symptoms.

## Saving Settings

Settings are saved automatically when a panel value changes. Folder selections and migration results are reported in the app; there is no general Save button. Do not edit or replace settings files manually.

## Example Configurations

### Working in a dark environment

1. Set the theme to **Dark**.
2. Choose a darker theme color preset if desired.
3. Disable animations if performance is limited.

### Reducing load on an older PC

1. Disable animations.
2. Disable automatic VR preview opening if it is not needed.
3. Enable automatic archiving of older photos when storage management is a priority.

### Customizing shortcuts

1. Open the **Shortcut** panel.
2. Select the shortcut to change.
3. Enter the new key combination.
4. The accepted combination is saved automatically; there is no Save button.

## Troubleshooting

### A setting does not take effect

Restart VSA after changing the setting. If the value still has no effect, use the reset action in the relevant panel and try again.

### A setting does not persist

Check write permission for `%APPDATA%\\VSA\\` and available disk space. If the problem continues, contact support with the log and the steps that reproduce it.

## Settings Storage

Settings are saved automatically as each panel changes. Do not edit or replace settings files manually. If a setting does not persist, verify folder permissions and free disk space, then contact support with the log and symptoms.

## Tips

- **Performance**: Disable animations if VSA feels slow on older hardware
- **Notifications**: Disable non-critical notifications to reduce distractions
- **Shortcuts**: Create shortcuts for operations you perform frequently
- **Backup**: Back up the configured photo and favorites folders when you need a local copy
- **Theme**: Use System-Linked theme for automatic light/dark switching

## Related Documentation

- [Keyboard Shortcuts Complete List](keyboard-shortcuts.md) - All shortcut details
- [Favorites Guide](favorites-guide.md) - Favorites feature overview
- [Game Settings Guide](game-config.md) - VRChat integration settings
- [Terms of Service](terms.md) - Usage terms
- [Privacy Policy](privacy.md) - Data handling
- [License Information](../license.md) - Licenses and third-party software
- [Troubleshooting Guide](troubleshooting.md) - Settings-related issues
