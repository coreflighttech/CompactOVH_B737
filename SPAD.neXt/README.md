CORE FLIGHT TECHONOLOGIES COMPACT 737 OVERHEAD PANEL firmware for SPAD.neXt SERIAL V2

# r07 Main release (2026/04/11)

[CFT_737_OVH_COMPACT_SPAD_1L2P_R07_115200.ino.exe](https://github.com/coreflighttech/CompactOVH_B737/blob/main/SPAD.neXt/CFT_737_OVH_COMPACT_SPAD_1L2P_R07_115200.ino.hex)

# d_r07 No EGT auto calibration release (2026/04/11)

[CFT_737_OVH_COMPACT_SPAD_1L2P_D_R07_115200.ino.exe](https://github.com/coreflighttech/CompactOVH_B737/blob/main/SPAD.neXt/CFT_737_OVH_COMPACT_SPAD_1L2P_D_R07_115200.ino.hex)

Use this firmware if requested by CFT support.  
It has no auto calibration and Vcc check at start.

# How to install the firmware

-> https://github.com/coreflighttech/Uploader  
- Select B737 MCP in Xloader "Device" pull down list as both devices are driven by the same Arduino type.)
- Be sure to plug the external power supply of the overhead.
- Use powered USB hub or free mothernoard USB port.
  
# How to use

Serial COM port has to be set to 115200 bauds in SPAD serial device settings (default bitrate)

SPAD should automaticaly load the overhead user interface from SPAD on-line database.

Internal devices features
- Set backlight display brightness by pressing and turning "FLT ALT" encoder
- Set digits displays brightness by pressing and turning "LAND ALT" encoder

- Force EGT calibration and display firmware version by pressing "FLT ALT" and "LAND ALT" encoder buttons 
- Force EGT calibration by sending -999 as temperature value (SPAD calibration triggering)	
- Set a user °C offset by pressing "FLT ALT" and turning "LAND ALT" encoders
- Use EGT_OFFSET variable to set °C offset within SPAD -1000 to 1000 (DEVICE:1L2P/CFT737OVHCOMPACT/EGT_OFFSET)

To manage brightness from SPAD, use these variables:
 - DISPLAY_BRI : Displays brightness from 0 to 15 (DEVICE:1L2P/CFT737OVHCOMPACT/DISPLAY_BRI)
 - BACKLIGHT_BRI : Backlight brightness from 0 to 255 (DEVICE:1L2P/CFT737OVHCOMPACT/BACKLIGHT_BRI)

SPAD test snippet for PMDG 737 #16524


# Firmware history

- r01 Initial release (2026/04/02)
- r02 Adding EGT tools (2026/04/02)
- r03 EGT fine tuning (2026/04/03)
- r04 Check Vcc power at start (2026/04/03)
- r05 Internal deadlock reset feature (2026/04/04)
- r06 Auto previous display recover after internal display usage (2026/04/04)
- d_r06	No Arduino Vcc warning, no auto calibration at start, manual calibration extended range (-1000 to 1000 °C) (2026/04/10
- r07 Check stepper zero pin, manual calibration extended range (-1000 to 1000 °C) (2026/04/11)
- d_r07	Same as r07 but no auto calibration at start and no Arduino Vcc warning, use only if needed (2026/04/11)
- r08 EGT settper timeouts added, manual calibration updated (2026/04/16 tests in progress)
