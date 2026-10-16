# Camera Controller Guide

## How to open

Open **Camera Controller** from the VSA sidebar.

![Camera Controller screen](../assets/screenshots/controller-overview.webp)

[🏠 Document Top](../index.md) | [⚖️ Terms of Service](./terms.md) | [🔒 Privacy Policy](./privacy.md)

---


Camera Controller sends camera parameters to VRChat over OSC (Open Sound Control). Use the top tabs to switch between:

- **VirtualLenz2 (VirtualLens2)**
- **Integral**
- **FishEye**
- **TelePortraitLens**

## VirtualLens2

The VirtualLens2 tab contains lens and camera settings. Value ranges are supplied by the connected avatar and may vary.

## Access Controller Screen

### Open from Menu

**Steps**:
1. Check sidebar menu (left side)
2. Look for the "Camera Controller" item
3. Click to open controller screen

### Keyboard Shortcut

There is no controller-specific shortcut. See [Keyboard Shortcuts](keyboard-shortcuts.md) for common shortcuts.

## Using Controller Screen

### Screen Composition

The VirtualLens2 tab contains:

- Lens settings
- Camera settings
- VirtualLens2 presets
- Connection status (shown when connected)

### Lens Settings

- **Aperture**
- **Focal length**
- **Exposure**

Adjust each item with its slider and use the item reset button to return to its default. Value ranges are supplied by the connected avatar and may vary.

### Camera Settings

- **AF mode**: Point AF, Face-detection AF, or Selfie AF
- **Grid**: None, 3×3, 3×3 plus diagonals, or 6×4
- **Information**: Toggle camera information display

### Real-time Reflection

Parameter changes are sent to the connected VRChat instance over OSC. The camera start button is unavailable until VRChat is running.

**Verification**:
1. Equip VirtualLens2 in VRChat
2. Adjust parameters in controller screen
3. Confirm reflection in VRChat screen (viewfinder)

**Notes**:
- OSC communication must be properly established

### Supported camera tabs

- **Integral**: Operate lens, focus, shutter, bokeh, aberration, and display settings. The tab provides reset and camera start/stop controls.
- **FishEye**: Toggle the lens and blur, and adjust blur amount. Focal length, FOV, and distortion are read-only.
- **TelePortraitLens**: Toggle the lens, adjust Main FOV and front/back bokeh, and control AutoFocus, AutoFocus Dof, and WorldFix.

## Integral Camera Control

Integral is a camera system for VRChat. You can operate it from the controller screen just like VirtualLens2.

### Accessing Integral Controller

From the Camera Controller screen in the sidebar menu, switch tabs to use VirtualLens2 and Integral interchangeably.

### Main Parameters

#### Lens Settings

| Parameter | Range | Description |
|-----------|-------|-------------|
| **Aperture** | 0.0 ～ 1.0 | Controls bokeh strength and brightness |
| **Zoom** | 0.0 ～ 1.0 | Camera zoom level |
| **Exposure** | 0.0 ～ 1.0 | Overall image brightness |

#### Focus Control

| Parameter | Description |
|-----------|-------------|
| **Focus Mode** | MF (Manual) / AF (Auto) / Visual AF |
| **Focus Value** | Manual focus position adjustment |
| **Pause AF** | Temporarily pause auto-focus |

#### Bokeh Shape

Select Integral's bokeh shape:

| Shape | Description |
|-------|-------------|
| **Circle** | Natural, elegant bokeh (default) |
| **Hexagon** | Geometric bokeh pattern |
| **Star** | Sparkling light effect |
| **Heart** | Cute presentation |
| **Bubble** | Transparent bubble effect |

**Bokeh Rotation**: Rotate bokeh shape to adjust angle.

#### Shutter Control

| Parameter | Description |
|-----------|-------------|
| **Shutter Speed** | Base exposure time |
| **Shutter Speed Add** | Fine-tuning adjustment |
| **Rolling Shutter** | Film camera shutter effect (OFF / Left→Right / Top→Bottom, etc.) |

#### Lens Effects

| Effect | Description |
|--------|-------------|
| **Vignetting** | Peripheral light falloff |
| **Aperture Aspect** | Adjust aperture vertical/horizontal ratio |
| **Chromatic Aberration** | Lens color separation effect |
| **Spherical Aberration** | Lens characteristic simulation |

#### Special Filters

**Cross Filter**: Adds cross-shaped light effect
- **Weight**: Filter effect strength
- **Scale**: Cross size
- **Angle**: Cross rotation angle
- **Wave amplitude / frequency**: Adjust the light wave pattern
- **Shape**: Choose 2, 4, 6, or 8 lines

#### Tilt (Tilt Shift)

Tilt lens in X/Y direction for special focus effects.

#### Composition Mode

Select image processing algorithm:

| Mode | Description |
|------|-------------|
| **Normal** | Standard image processing |
| **Lighten** | Emphasize bright areas |
| **Lighten (single)** | Single-frame lighten mode |
| **Darken** | Emphasize dark areas |
| **Darken (single)** | Single-frame darken mode |
| **Depth** | Use depth information |
| **Dither** | Dither processing |
| **Movie** | Film-style processing |

#### Curve / LUT

- **Curve**: Linear, Log, LUT1, LUT2, or LUT3
- **LUT Mix**: Amount of LUT blending

#### Other Features

| Feature | Description |
|---------|-------------|
| **Grid Display** | Show composition guide |
| **Histogram** | Check exposure |
| **Selfie Mode** | Front-facing camera |
| **Auto Level** | Off / R / Up / L |

The Display / Other card also provides:

- **FixMode**: World or Avatar
- **FixWhileOpen**: Hold the value while the shutter is open
- **Timer**: Timer capture
- **Screen Info / Screen Font Size**: On-screen information and text size
- **HUD**: Head-up display
- **Layer**: Toggle Local Player, Remote Player, and UI layers

---

## OSC Communication Settings

### What is OSC?

OSC (Open Sound Control) is a protocol that transmits parameters real-time over network. Exchange numerical data between VRChat and VSA.

### Port Settings

#### Default Ports

Game Settings defaults are VSA receive (VRChat sends) `9001` and VSA send (VRChat receives) `9000`.

#### Change Port Number

**When Change Needed**:
- Port 9001 already in use by another app
- Network requires different port

**How to Change**:
1. Open sidebar Game Settings > Display Settings
2. Change "VSA receive port (VRChat sends)" or "VSA send port (VRChat receives)"
3. Verify the corresponding VRChat send and receive ports

The controller screen has no port fields; it uses the ports configured in Game Settings.

### Verify Communication Status

#### Status Display

The controller screen shows the connection indicator when connected:

- **Connected (green)**: Properly communicating with VRChat
- If connection is not established, the indicator is not shown

#### Diagnosis Method

**Steps**:
1. Equip VirtualLens2 in VRChat
2. Open controller screen
3. Wait until status becomes "Connected"
4. Change one parameter to test, confirm VRChat reflection

## Preset Management

Presets store the VirtualLens2 settings (aperture, focal length, exposure, AF mode, grid, and information). The Integral, FishEye, and TelePortraitLens tabs do not show this preset section.

### What are Presets?

Save preset settings combining camera parameters (focal distance, aperture, exposure, etc.).

### Save Preset

**Steps**:
1. Adjust each parameter to desired value
2. Click "Save" button in "Preset" section
3. Enter preset name (e.g., "Portrait", "Wide-angle")
4. Click "Save"

### Load Preset

**Steps**:
1. Click the preset-name button in the "Preset" section
2. All saved parameter values apply
3. The values are sent to VRChat automatically

### Delete Preset

**Steps**:
1. Select preset to delete
2. Click "Delete" button
3. Click "Delete" in confirmation dialog

## VRChat Side Settings

### Equip VirtualLens2 Avatar

VirtualLens2 requires equipping an avatar with a VirtualLens2 camera in VRChat.

**Verification**:
1. Equip avatar in VRChat
2. Check View > Viewfinder if VirtualLens2 viewfinder displays

### Enable OSC (VRChat Side)

**VRChat Setup**:
1. Launch VRChat
2. Open VRChat's OSC settings
3. Check "Enable OSC"
4. Verify VSA receive 9001 and VSA send 9000 (or the corresponding custom values)

### Verify VirtualLens2 Parameters

The main OSC parameters used by the VirtualLens2 tab are:

- `/avatar/parameters/VirtualLens2_Zoom` - Focal length
- `/avatar/parameters/VirtualLens2_Aperture` - Aperture
- `/avatar/parameters/VirtualLens2_Exposure` - Exposure
- `/avatar/parameters/VirtualLens2_AFMode` - AF mode
- `/avatar/parameters/VirtualLens2_Grid` - Grid
- `/avatar/parameters/VirtualLens2_Information` - Information display

Check parameter names and value ranges against the documentation for the VirtualLens2 avatar you use.

## Troubleshooting

### OSC Communication Not Established

**Symptom**: Status remains "Disconnected"

**Solutions**:
1. Verify VRChat OSC settings
   - Confirm "Enable OSC" checked
   - Confirm the VSA receive/send ports match the corresponding VRChat ports (9001/9000 by default)
2. Check firewall settings
   - Confirm firewall not blocking communication
   - Check security software settings
3. Verify port not in use
   ```
   netstat -ano | findstr ":9001 :9000"
   ```
   - If port in use by other process, change to different port
4. Restart VRChat and VSA
   - Completely close both and restart

### Parameters Not Reflecting

**Symptom**: Controller changed but VRChat doesn't reflect

**Solutions**:
1. Check communication status
   - Verify controller screen status is "Connected"
   - If "Disconnected", see "OSC Communication Not Established"
2. Verify VirtualLens2 equipped
   - Confirm correct avatar equipped in VRChat
   - Confirm VirtualLens2 viewfinder displays
3. Check parameter names
   - Verify correct parameter names configured on avatar
4. Restart VSA
   - Reset OSC connection by completely restarting VSA

### Parameter Response Slow

**Symptom**: Parameter changes delayed in VRChat reflection

**Solutions**:
1. Confirm VSA and VRChat are running on the same PC
2. Check other app loads
   - Check CPU usage not high
3. Check VRChat load
   - Many players in instance may reduce performance

### Parameter Reset Not Working

**Symptom**: Reset button clicked but value doesn't return

**Solutions**:
1. Check target parameter reset settings
   - Verify correct parameter selected
2. Check avatar settings
   - Verify VirtualLens2 reset value configured correctly on VRChat
3. Restart controller
   - Close controller screen and reopen

## Using presets

VirtualLens2 ranges depend on the connected avatar. Adjust the desired values, save them with a name, and load the preset when needed.

## Related Documentation

- [VRChat Integration](vrchat-integration.md) - General VRChat integration info
- [Game Settings Guide](game-config.md) - Detailed folders, OSC, plugins, and timeline settings
- [Keyboard Shortcuts](keyboard-shortcuts.md) - Shortcut list
