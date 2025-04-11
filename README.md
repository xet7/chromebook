# Chromebook arm64

- https://web.archive.org/web/20240119035042/https://www.devkitsune.net/blog/wordpress/2024/01/04/linux-on-arm-chromebooks/
- https://news.ycombinator.com/item?id=43642351

# Chromebook amd64: Installing Debian Linux

## Why

- No new releases of ChromeOS for this hardware, got popup on ChromeOS.
- In this case, installing to Acer Chromebook 15 (CB3-532), codename BANON, 2016 Intel Braswell.
- This Chromebook has 2 GB RAM and 16 GB of internal storage. So Debian works, there is space for newest XFCE, Chrome, LibreOffice, Gimp, leaving 6 GB free disk space.

## Video of booting Debian at Chromebook

https://github.com/xet7/chromebook/releases/download/v1.0.0/chromebook-debian-boot.mp4

## What was tried, but not then used

- Installing Linux Mint, because minimum install size 15 GB, too big for internal storage.
- Win10 https://www.youtube.com/watch?v=kXnU_S5ZNJQ https://coolstar.org/chromebook/windows.html would probably require buying and installing bigger SSD/M.2 disk https://www.youtube.com/watch?v=1staB8LtmQM and maybe more RAM.
- Trying to install to external storage like SD or USB card, because it would require remembering keeping that storage plugged in.
- Did not try installing Debian that does not have non-free firmware. Preferred to have non-free firmware included, just in case.
- Did not try to install GalliumOS, it is not developed actively anymore.
- Did try to dd newest UPupBB.iso to eMMC, it did boot from there, but adding more eMMC partitions after UPupBB.iso CDROM did mess up UEFI booting. UPupBB could be confusing to non-English users because many apps there are not translated.

## Requirements

- Cross screwdriver that fits to screws at bottom of your Chromebook, if your Chromebook model requires removing write protect screw, see https://wiki.galliumos.org/Hardware_Compatibility
- USB stick that has FAT32 format, used to save ChromeOS stock firmware rom file, about 9 MB.
- USB stick that has Debian 11 with non-free firmware. Use https://www.balena.io/etcher to flash this .iso to USB stick: 
  https://cdimage.debian.org/cdimage/unofficial/non-free/cd-including-firmware/11.6.0+nonfree/amd64/iso-cd/firmware-11.6.0-amd64-netinst.iso

## Installing

1. Look what Chromebook model you have at bottom of Chromebook, and find codename from https://wiki.galliumos.org/Hardware_Compatibility

2. In this BANON case, installing to Acer Chromebook 15 (CB3-532), codename BANON, 2016 Intel Braswell.

3. In this BANON case, take screwdriver, remove all screws from bottom of Chromebook, open case, and remove write protect screw - see Banon_wp.jpg . Add botton screws back.

<img src="https://raw.githubusercontent.com/xet7/chromebook/main/Banon_wp.jpg" width="60%" alt="Banon write protect screw" />

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
