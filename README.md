![Screen Shot 2565-04-01 at 12 03 48](https://user-images.githubusercontent.com/43199445/161198228-d321dda5-2876-49d1-9d82-17700ddab588.png)



# Huananzhi X99-8M-F(B85) + Intel Xeon E5-2670 v3 + RX 460 4GB
Latest working macOS: Monterey 12.3
OpenCore version: 0.7.9

## Here is my PC specifications
  - Mainboard: Huananzhi X99-8M-F(B85)
  - CPU: Intel Xeon E5-2670v3
  - GPU: MSI AERO RX460 4GB
  - SSD: SATA 128gb (MacOS BigSur 12.3) + Samsung NVME 970 Evo 256GB (Windows 11)
  - HDD : Toshiba 1TB
  - Ram: KINGMAX Zeus 16GB x 2 2666mhz
  - PSU: Coolermaster Elite 500w

## Installations (Windows):
  - Download MacOS Image (12.0.1): https://drive.google.com/file/d/1KrvUYpbIXtJ3hR7tZpKWnGz5_kwFEtLD/view?usp=sharing and create bootable usb using balenaEtcher https://www.balena.io/etcher/
  - Mount EFI folder of boot drive by using Mini Partion Wizard https://www.partitionwizard.com/free-partition-manager.html. Select EFI folder from boot drive and then right click choose Change Volume Letter option and click Ok and Apply
  - Copy EFI folder from the repository to EFI folder in boot drive by using Explorer++ (Administator permission is require) https://explorerplusplus.com/download
  - Restart to BIOS and setup following this https://dortania.github.io/OpenCore-Install-Guide/config-HEDT/haswell-e.html#intel-bios-settings  ![Screen Shot 2565-04-01 at 12 21 04](https://user-images.githubusercontent.com/43199445/161199876-94898eb0-7311-47e4-afa6-a884343dee14.png)
  - Save change bios and boot to usb boot drive to start MacOS installation process

## Notes:
- The MacOS Image version is 12.0.1 after installing sucessfully, I can update to version 12.3 via OTA without any issue
- BIOS config for Above 4G decoding can make your PC not booting when enable it. If you got this issue, then reset your bios by remove your CMOS Battery or using the Clear BIOS jumper. And then re-config your bios setting and skip this setting option.
- Drive for install Hackintosh should be formatted with APFS format

## What works
- macOS Monterey
- HDMI/DP/DVI
- All USB ports
- Ethernet
- Bluetooth Usb Dongle
- Monitor with high refresh rate 144hz is working fine

# What not works
- Audio :( still find the ways to fix it

# References
Please read carefully if you wanna try it by yourself:
- Collect file: https://dortania.github.io/OpenCore-Install-Guide/ktext.html#firmware-drivers
- Setup config.plist file: https://dortania.github.io/OpenCore-Install-Guide/config-HEDT/haswell-e.html#starting-point
- Bios: https://dortania.github.io/OpenCore-Install-Guide/config-HEDT/haswell-e.html#intel-bios-settings
- Fix bluetooth usb dongle: https://dortania.github.io/OpenCore-Install-Guide/extras/monterey.html#bluetooth 
