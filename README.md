# LG-Gram-15z990-Hackintosh-Sequoia
An (almost) perfect Hackintosh build for the LG Gram 15z990 using OpenCore

<img width="1920" height="1080" alt="CleanShot 2025-11-12 at 17 12 52" src="https://github.com/user-attachments/assets/23e81356-ec46-443e-b335-3c59b86f1b49" />

## Configuration
|      | Detail   |
| ---- | -----------------------------------------|
| Mac OS Version | Sequoia 15.7 (24G222)|
| Model | LG Gram 15Z990-VA50K|
| CPU  | Intel Core i5-8265U (Whiskey Lake)|
| GPU | Intel UHD Graphics 620 (Integrated)|
| Memory | 8GB DDR4 2400MHz (Pre-installed)|
| SSD | Have been changed to Intel SSDPEKNW512G8 512GB|
| Sound Card | Conexant CX8200|
| Network Card | Intel AC-9560|
| Bluetooth | Intel AC-9560|
|Thunberbolt Chipset | JHL6340 (Alpine Ridge)|

## Instructions
Do following My reference efi same as: https://github.com/dimdom69/LG-Gram-17z990-Hackintosh

## What is working
- [x] The touchpad works normally. Note that force touch must be disabled in System Preferences
- [x] Keyboard functions normally
- [x] Fn keys are functional, using a combination of SSDT patches, builtin ACPI functionality, and a helper program called [LGGramAssistant](https://github.com/lehrian/LGgramAssistant). It's possible to map other ones, but I'm lazy, so currently the ones that are mapped are:
    - **Fn+F2**: Brightness down
    - **Fn+F3**: Brightness up
    - **Fn+F4**: Sleep
    - **Fn+F6**: Toggle WiFi
    - **Fn+LShift+F6**: Toggle Bluetooth
    - **Fn+F8**: Toggle Keyboard Backlight
    - **Fn+F10**: Mute
    - **Fn+F11**: Volume Down
    - **Fn+F12**: Volume Up
- [x] The display works with graphics acceleration
- [x] Sleep/wake works, including closing the laptop lid to sleep
- [x] WiFi/Bluetooth works natively (no need for an add-in card)
- [x] The 3 USB Type A ports work both in USB3 and USB2 modes
- [x] The USB Type C port works in every possible way:
    - Thunderbolt 3 works, including hotplug, even after sleep
    - USB3/USB2 works, including hotplug, even after sleep
    - Works regardless of whether or not a device was plugged in at boot
- [x] HDMI output works
- [x] MicroSD Card reader works
- [x] Audio works, including the headphone jack (have not tested audio in through the headphone jack)
- [x] Battery reports percentage correctly
- [x] Power management seems to work correctly
- [x] Dual booting with Windows works fine, including using Boot Camp and Target Disk mode
- [x] FileVault and Secure Boot are working
- [x] Both SATA and NVMe M.2 drives seem to work fine

## What Doesn't Work
- [ ] AirDrop/Wireless Sidecar/Various other Apple Continuity things
    - This is a limitation of the OpenIntelWireless drivers
    - Only Handoff and Universal Clipboard are supported
- [ ] Hibernation (S4 sleep)
    - This is not supported at all for Hackintoshes as far as I know
- [ ] Trackpad doesn't function in the OpenCore boot picker
- [ ] Boot Chime (Don't really care enough to work on this)

## Thanks
- dimdom69 (https://github.com/dimdom69/LG-Gram-17z990-Hackintosh) my reference efi build in monterey
- Suzuke's [build for the 13z980](https://github.com/suzuke/LG-Gram-13z980-Opencore) was an invaluable starting point
- AskDavis's [build for the 17z90n](https://github.com/AskDavis/LG-Gram-17Z90N)
- Parthvsquare's [build for the 14z980](https://github.com/Parthvsquare/Opencore-LG-gram-14z980)
- EliteMacX86 for the [Thunderbolt 3 hotplug information](https://elitemacx86.com/threads/how-to-enable-thunderbolt-3-hotplug-on-macos.462/)
- The whole [Acidanthera team](https://github.com/acidanthera)!
- Many random forum posters
