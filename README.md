# Dual Mouse Controller

Control a racing game using two mice — one for gas/brake and one for steering.

## How it works

- **Accelerator mouse**: move forward = gas, move backward = brake. The value stays fixed until you move again.
- **Steering mouse**: move left/right to steer. The value stays fixed until you move again.

Both mice are read independently using Windows Raw Input and mapped to a virtual joystick via vJoy.

## Requirements

- Windows 10/11
- [vJoy](https://github.com/jshafer817/vJoy/releases) (virtual joystick driver) — install this first

## How to use

1. Install vJoy and enable Device 1 with at least Axis X and Axis Y
2. Run `detectar.exe` to find the handle numbers for each of your mice
3. Run `mousesv2.exe`
4. Enter the handle numbers in the corresponding fields
5. Adjust sensitivity and threshold to your liking
6. Click **Start** and open your game
7. In the game's controller settings, map:
   - Axis X → steering
   - Axis Y → gas/brake

## Finding your mouse handles

Run `detectar.exe` and move each mouse — the handle number will appear on screen. Note which handle belongs to which mouse and enter them in the main app.

## Settings

| Setting | Description |
|---|---|
| Handle | Unique ID for each mouse device |
| Sensitivity | How much each pixel of movement affects the axis |
| Threshold | Minimum movement to register (filters out noise) |
| Invert | Reverses the direction of the axis |

Settings are saved automatically when you close the app.

## Files

- `mousesv2.exe` — main controller app
- `detectar.exe` — tool to find mouse handle numbers

## Tested with

- Logitech G502 (accelerator)
- Logitech G305 (steering)
- BeamNG.drive
