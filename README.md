# AnalogMouse

Control racing games using two mice — one for gas/brake and one for steering, with full analog input via vJoy.

## How it works

- **Accelerator mouse**: move forward = gas, move backward = brake. The value stays fixed until you move again.
- **Steering mouse**: move left/right to steer. The value stays fixed until you move again.
- Both mice are read independently using Windows Raw Input and mapped to a virtual joystick via vJoy.

## Requirements

- Windows 10/11
- [vJoy](https://github.com/jshafer817/vJoy/releases) — install this first and enable Device 1 with at least Axis X and Axis Y

## How to use

1. Install vJoy and enable Device 1 with Axis X and Axis Y checked
2. Run `AnalogMouse.exe`
3. Click **Detect** next to each mouse field and move that mouse — the handle is assigned automatically
4. Adjust sensitivity, threshold, and curve to your liking
5. Click **Start** and open your game
6. In the game's controller settings, map:
   - Axis X → steering
   - Axis Y → gas/brake

## Features

### Auto mouse detection
Click the **Detect** button next to each mouse field and move that mouse. The handle is assigned automatically — no need to find numbers manually or run a separate tool.

### Profiles
Save unlimited configurations for different games. Each profile stores handles, sensitivity, threshold, invert settings, and curves. Switch between profiles instantly with the profile buttons at the top.

### Sensitivity curves
Choose between three response curves for each axis:
- **Linear** — direct 1:1 response
- **Exponential** — slow near center, fast at extremes (good for steering)
- **Logarithmic** — fast near center, gradual at extremes (good for throttle)

A live preview of the curve is shown next to the settings.

### Visual axis bars
Real-time bar indicators show the current value of each axis — green for gas, red for brake, blue for steering.

### Dual cursor overlay
Click the **Dual Cursors** button to show two colored arrows on screen — red for the accelerator mouse and blue for the steering mouse — moving independently on the desktop. Each cursor supports left and right click. Click the button again to close the overlay.

### Hotkeys
Assign custom keys to start, stop, and reset axes without clicking buttons. Click a hotkey field and press any key to assign it.

| Action | Default key |
|---|---|
| Start | F5 |
| Stop | F6 |
| Reset axes | F7 |

### Auto-reconnect detection
If a mouse disconnects while running, the app detects it automatically and shows a warning.

### Invert axes
Flip the direction of either axis independently.

### Swap mice
Instantly swap the accelerator and steering mouse handles with one click.

### Language
Switch between Spanish and English at any time with the language button.

## Settings explained

| Setting | Description |
|---|---|
| Handle | Unique ID for each mouse — assigned automatically via Detect button |
| Sensitivity | How much each pixel of movement affects the axis |
| Threshold | Minimum movement to register (filters hand tremor) |
| Curve | Response curve: Linear, Exponential, or Logarithmic |
| Invert | Reverses the direction of the axis |

## In-game setup (BeamNG example)

1. Open Options → Controls
2. Select the vJoy device
3. Map Axis X → steering
4. Map Axis Y → gas/brake
5. Set linearity to 1 and adjust sensitivity from the AnalogMouse app

## Windows security warning

When you first run the .exe, Windows may show a security warning. This is normal for unsigned applications.

1. Click **More info**
2. Click **Run anyway**

## Changelog

### v2.0
- Merged mouse detection into the main app — no separate tool needed
- Added unlimited profiles
- Added sensitivity curves with live preview
- Added real-time axis bar indicators
- Added reset hotkey (F7)
- Added swap mice button
- Added auto-reconnect detection
- Major stability improvements

### v1.0
- Initial release
- Two separate executables: main controller + handle detector

## Coming soon

- Analog Keyboard Input — use keyboard keys as analog axes with configurable ramp speed
