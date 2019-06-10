# me_removal

This repo is for testing complete ME removal on Intel HEDT systems, some of which can boot without the ME and do not have a watchdog timer that would normally power off the system after 30 minutes.

## Confirmed Working

Please note that this has not been verified to work on any X99 or X299 boards, and may be exclusive to X79. This is why we need testers :)

### X79
- ASUS Rampage IV Extreme
- ASUS Rampage IV Gene
### X99
None tested yet
### X299
None tested yet

## Helping Test

If you have an Intel system with an X79, X99, or X299 chipset and want to test ME removal, please file an issue. You will need to be able to recover your system in the event of a bad flash. Some motherboard flashing features can provide this, but yours may not.

Supplemental BIOS patches may be required to mitigate issues caused by ME firmware removal, and these patches may not exist. The following issues have been reported:

X79:
- Onboard LAN non-functional on a cold boot (fix possible, Linux only?)
- Excessive POST times
- Reappearance of a broken MEI device on the PCI bus (fix possible)
- Onboard LAN identified as incorrect model in Windows (still works)
- Miscellaneous changes to devices in Windows device manager

The Windows MEI drivers seem to interact particularly badly with a removed ME, especially if the MEI device reappears. Uninstall them if possible.

Include in your issue:
- Board model and vendor
- BIOS version
- Operating System
