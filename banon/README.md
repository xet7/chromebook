# Installing Debian Linux to Chromebook amd64

## Why

- No new releases of ChromeOS for this hardware, got popup on ChromeOS.
- In this case, installing to Acer Chromebook 15 (CB3-532), codename BANON, 2016 Intel Braswell.
- This Chromebook has 2 GB RAM and 16 GB of internal storage. So Debian works, there is space for newest XFCE, Chrome, LibreOffice, Gimp, leaving 6 GB free disk space.
- Installing Linux Mint (minimum install size 15 GB) or Win10 would probably require buying bigger SSD/M.2 disk and maybe more RAM.
- Trying to install to external storage would require remembering keeping that storage plugged in.

## Requirements

- Cross screwdriver that fits to screws at bottom of your Chromebook, if your Chromebook model requires removing write protect screw, see https://wiki.galliumos.org/Hardware_Compatibility
- USB stick that has FAT32 format, used to save ChromeOS stock firware rom file, about 9 MB.
- USB stick that has Debian 11 with non-free firmware. Use https://www.balena.io/etcher to flash this .iso to USB stick: 
  https://cdimage.debian.org/cdimage/unofficial/non-free/cd-including-firmware/11.6.0+nonfree/amd64/iso-cd/firmware-11.6.0-amd64-netinst.iso

## Installing

1. Look what Chromebook model you have at bottom of Chromebook, and find codename from https://wiki.galliumos.org/Hardware_Compatibility

2. In this BANON case, installing to Acer Chromebook 15 (CB3-532), codename BANON, 2016 Intel Braswell.

3. In this BANON case, take screwdriver, remove all screws from bottom of Chromebook, open case, and remove write protect screw - see Banon_wp.jpg . Add botton screws back.

4. Enable Developer Mode https://mrchromebox.tech/#devmode

5. From ChromeOS login screen or guest mode, when connected to Internet via WLAN, press: `Ctrl+Alt+F2`

6. Login with username: `chronos`

7. Get script that will install UEFI with these commands: ( info from https://mrchromebox.tech/#fwscript )

```
cd /tmp

curl -LOk mrchromebox.tech/firmware-util.sh

cd

sudo bash /tmp/firmware-util.sh
```

8. Install UEFI with that script, see https://mrchromebox.tech/#fwscript . UEFI will be installed in separate BIOS storage area, not internal 16 GB eMMC disk. Insert USB stick that has FAT32 format to backup original firmware.

9. From UEFI/BIOS with Esc, select to boot from USB stick that has Debian.

10. When installing Debian, select your WLAN, force UEFI install of Debian when it asks about BIOS etc selection, unselect Gnome, select XFCE. Overwrite all of internal eMMC 16 GB disk with default partition layout, using same / for all files.
    (Sure you can also install full disk encryption if you like etc).

11. Install some software, here also LibreOffice language pack, and enable ufw firewall

```
su

apt -y install zip unzip p7zip-full gimp libreoffice libreoffice-l10-fi unp vlc ufw nano

ufw enable
```

12. If you like more Windows style look, edit and unlock toolbars, remove small toolbar, move big toolbar from top to bottom, and lock toolbars. Remove extra virtual desktops if you don't use them.

13. Use Firefox ESR to download Chrome Debian amd64 .deb package.

```
su

cd Downloads

sudo dpkg -i chrome*.deb

sudo apt -f install
```
14. If you like autologin:
```
su

nano /etc/lightdm/lightdm.conf
```
There add your Linux username, that will autologin:
```
autologin-user=YOUR-USERNAME-HERE
autologin-user-timeout=0
```
Save and exit: `Ctrl-x Enter Ctrl-x`

15. After reboot, press Esc to go to UEFI, and change boot order so ChromeBook boots from UEFI. Could require moving with + key that is somewhere left from backspace, with or without shift. Save and exit.
