# eFinder Lite mk2


![IMG_6329](https://github.com/user-attachments/assets/0eabcc3c-f5e7-4bad-b855-3142e98c168f)

## Basics

Code for AltAz telescopes (primarily Dobsonians) to utilise plate-solving to improve pointing accuracy.

Requires:

- microSd card loaded with Raspberry Pi 64bit Bookworm OS Lite (No desktop)
- Raspberry Pi Zero 2W.
- A custom box (Raspberry Pi Zero, OLED display and switches)
- A Nexus DSC Pro with optical encoders. (Note: requires Pro version)
- USB cable from Nexus DSC Pro USB port to the Pi Zero USB OTG port.
- A Camera,the RP HQ Camera module
- Camera lens, (Recommend Arducam 25mm f1.2)

Full details at [
](https://astrokeith.com/equipment/efinder/efinder-lite)https://astrokeith.com/equipment/efinder/efinder-lite

## Compatibility

The eFinder Lite mk2 is designed to operate alongside a Nexus DSC Pro. It uses the standard LX200 protocol to communicate with the Nexus DSC Pro via its usb port.

It differs from the mk1 in ...
- The USB/UART HAT is not required
- Will only work with a Nexus DSC Pro
- Requires Nexus DSc Pro firmware later than 1.4.12
  
If the Nexus DSC is connected to a drive, GoTo++ can be enabled. Directly compatible drives are ScopeDog, SiTech & SkyTracker. ServoCat drives can be used but since the Nexus DSC usb port is used to connect to the ServoCat drive, the eFinder must be configured to connect to the Nexus DSC Pro via wifi.

A Raspberry Pi HQ camera module is strongly recommended. The Arduino clone will also work, but the config.txt file needs amending. change to camera_auto_detect=0 and add dtoverlay=IMX477

If no Nexus is found on boot, the eFinder will restart as 'eFinder Live'. This uses just plate-solving to determine telescope position and relay the solution to SkySfari or similar Apps over wifi. A gps dongle or module is required.

## Operation
Plug the eFinder into the Nexus DSC port (set to LX200, 9600, N, 1 Protocol)
Turn on the Nexus DSC which will power up the eFinder Lite.
The eFinder Lite will autostart on power up.

ssh & Samba file sharing is enabled at efinder.local, or whatever hostname you have chosen.

The eFinder.config file is accessible via a browser at "efinder.local", or whatever hostname you have chosen.

A forum for builders and users can be found at https://groups.io/g/eFinder

## Acknowledgements and Licences

The eFinder Lite uses Tetra3, Cedar-Detect & Cedar-Solve. Please refer to the licence and other notes in the Tetra3 folder

