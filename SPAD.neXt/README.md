CORE FLIGHT TECHONOLOGIES COMPACT 737 OVERHEAD PANEL firmware for SPAD.neXt SERIAL V2

# r06 Public Release (2026/04/04)

<i>CFT_737_OVH_COMPACT_SPAD_1L2P_R06_115200.ino.exe</i>

Serial COM port has to be set to 115200 bauds in SPAD serial device settings (default bitrate)

SPAD should automaticaly load the overhead user interface from SPAD on-line database.

Internal devices features
- Set backlight display brightness by pressing and turning "FLT ALT" encoder
- Set digits displays brightness by pressing and turning "LAND ALT" encoder

- Force EGT calibration and display firmware version by pressing "FLT ALT" and "LAND ALT" encoder buttons 
- Force EGT calibration by sending -999 as temperature value (SPAD calibration triggering)	
- Set a user °C offset by pressing "FLT ALT" and turning "LAND ALT" encoders
- Use EGT_OFFSET variable to set °C offset within SPAD -127 to 127 (DEVICE:1L2P/CFT737OVHCOMPACT/EGT_OFFSET)

To manage brightness from SPAD, use these variables.
 - DISPLAY_BRI : Displays brightness from 0 to 15 (DEVICE:1L2P/CFT737OVHCOMPACT/DISPLAY_BRI)
 - BACKLIGHT_BRI : Backlight brightness from 0 to 255 (DEVICE:1L2P/CFT737OVHCOMPACT/BACKLIGHT_BRI)

SPAD test snippet for PMDG 737 #16524

How to install firmware -> https://github.com/coreflighttech/Uploader

# Previous firmware

- r01 Initial release (2026/04/02)
- r02 Adding EGT tools (2026/04/02)
- r03 EGT fine tuning (2026/04/03)
- r04 Check Vcc power at start (2026/04/03)
- r05 Internal deadlock reset feature (2026/04/04)
- r06 Auto previous display recover after internal display usage (2026/04/04)

