# Chromebook arm64

- [Linux on ARM Chromebooks](arm.md)
- https://news.ycombinator.com/item?id=43642351

# Chromebook amd64: Installing Debian Linux

## Why

- No new releases of ChromeOS for this hardware, got popup on ChromeOS.


## 1) Acer Chromebook 15 (CB3-532), codename BANON, 2016 Intel Braswell, 2 GB RAM, 16 GB internal disk.

1. Debian can be installed, there is space for newest XFCE, Chrome, LibreOffice, Gimp, leaving 6 GB free disk space. Linux Mint is too big for 16 GB internal disk.

2. Video of booting Debian at Chromebook https://github.com/xet7/chromebook/releases/download/v1.0.0/chromebook-debian-boot.mp4

3. Cross screwdriver that fits to screws at bottom of your Chromebook. This Chromebook model
   requires removing write protect screw, see https://wiki.galliumos.org/Hardware_Compatibility
4. USB stick that has FAT32 format, used to save ChromeOS stock firmware rom file, about 9 MB.

5. USB stick that has Debian. Use https://www.balena.io/etcher to flash this .iso to USB stick:
   https://cdimage.debian.org/debian-cd/current/amd64/iso-cd/debian-13.0.0-amd64-netinst.iso

6. Look what Chromebook model you have at bottom of Chromebook, and find codename from:

- [HardwareCompatibility](HardwareCompatibility.md)
- https://archive.is/aFtnj
- Old link, does not work anymore: https://wiki.galliumos.org/Hardware_Compatibility

7. In this BANON case, installing to Acer Chromebook 15 (CB3-532), codename BANON, 2016 Intel Braswell.

8. In this BANON case, take screwdriver, remove all screws from bottom of Chromebook, open case, and remove write protect screw - see Banon_wp.jpg . Add botton screws back.

<img src="https://raw.githubusercontent.com/xet7/chromebook/main/Banon_wp.jpg" width="60%" alt="Banon write protect screw" />

9. Enable Developer Mode https://mrchromebox.tech/#devmode

10. From ChromeOS login screen or guest mode, when connected to Internet via WLAN, press: `Ctrl+Alt+F2`

11. Login with username: `chronos`

12. Get script that will install UEFI with these commands: ( info from https://mrchromebox.tech/#fwscript )

```
cd /tmp

curl -LOk mrchromebox.tech/firmware-util.sh

cd

sudo bash /tmp/firmware-util.sh
```

13. Install UEFI with that script, see https://mrchromebox.tech/#fwscript . UEFI will be installed in separate BIOS storage area, not internal 16 GB eMMC disk. Insert USB stick that has FAT32 format to backup original firmware.

14. From UEFI/BIOS with Esc, select to boot from USB stick that has Debian.

15. When installing Debian, select your WLAN, force UEFI install of Debian when it asks about BIOS etc selection, unselect Gnome, select XFCE. Overwrite all of internal eMMC 16 GB disk with default partition layout, using same / for all files.
    (Sure you can also install full disk encryption if you like etc).

16. Install some software, here also LibreOffice language pack, and enable ufw firewall

```
su

apt -y install zip unzip p7zip-full gimp libreoffice libreoffice-l10-fi unp vlc ufw nano

ufw enable
```

17. If you like more Windows style look, edit and unlock toolbars, remove small toolbar, move big toolbar from top to bottom, and lock toolbars. Remove extra virtual desktops if you don't use them.

18. Use Firefox ESR to download Chrome Debian amd64 .deb package.

```
su

cd Downloads

sudo dpkg -i chrome*.deb

sudo apt -f install
```
19. If you like autologin:
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

20. After reboot, press Esc to go to UEFI, and change boot order so ChromeBook boots from UEFI. Could require moving with + key that is somewhere left from backspace, with or without shift. Save and exit.

## ASUS Chromebook C223, codename BABYMEGA, 2018 Intel Apollo Lake, about 30 GB internal disk.

1. Because there is enough disk space, installed Linux Mint. Download newest Linux Mint Mate amd64 and write it to USB stick with [Balena Etcher](https://etcher.balena.io).

2. Backup downloads folder to external harddrive or Google Drive.

3. From Chrome OS boot menu, power wash computer.

4. Enable developer mode https://docs.mrchromebox.tech/docs/boot-modes/developer.html

5. To allow installing UEFI, removed screws from bottom,also that middle screw that is hidden hidden under a sticker. I scraped the sticker off the screw.

6. It is recommended that you open the back cover with a plectrum or other plastic tool to avoid damaging the back cover, but I used a spoon anyway.
   I used the handle of the spoon to open the back cover by lifting it at the folding hinges, and I lifted the back edge out of place a little at a time with the spoon.

7. Take power cable of battery away from mainboard. Power cable has many colored wires, that go to white power plug. You need to lift what white
   part It is located here. (Sorry, I did take a photo, but photo is at phone that does not boot anymore, it needs reinstalling).

```

   THIS IS BIGGER ZOOM IMAGE OF WHITE POWER CABLE PART
   +----------------------------+-------------+------+
===| BATTERY WHITE POWER CABLE  | BLACK   | METALLIC |
===| PART DISCONNECT,           | PLASTIC | DO NOT   |
===| LIFT WITH PLASTIC,         | DO NOT  | LIFT     |
===| TO NOT GET ELECTRIC SHOCK, | LIFT    |          |
===| WHEN POWER IS ON,          |         |          |
===| LIFT TO YOURSELF DIRECTION |         |          |
===|                            |         |          |
   +-------------+--------------+---------+----------+
^
|
Many different colored wires

THE BIG WHITE POWER CABLE PART IS AT SMALLER SIZE
BELOW AT "E" PART WHERE ARROW POINTS OUT
WHERE IT IS:     |
                 |
                 |
  THIS IS BOTTOM | OF CHROMEBOOK
+-----------------++---------------+
|                |                 |
|                V                 |
|   +---------+       BATTERY      |
|   |         |==E <==WHITE POWER  |
|   |         |       CABLE, LIFT  |
|   |         |       WITH PLASTIC |
|   |         +---------------+    |
|   | Battery                 |    |
|   |                         |    |
|   +-------------------------+    |
|                                  |
+----------------------------------+
```

8. While battery power cable is disconnected, it is possible to install UEFI with install script.

9. Boot laptop to guest mode, connect to WLAN.

10. Press CTRL+ALT+F2 and login with username chronos, press enter when it asks for password https://docs.mrchromebox.tech/docs/fwscript.html

11. Type this and press Enter:

```
cd; curl -LO mrchromebox.tech/firmware-util.sh && sudo bash firmware-util.sh
```

12. Install UEFI (Full ROM) Firmware.

13. After install, put Linux Mint USB stick to Chromebook. When booting Chromebook there is white rabbit logo, press Esc to get to menu where select USB boot.

14. Install Linux mint to internal MMC drive. (Alternatively, you could install for example to microSD or SD, and set computer to boot from that at UEFI settings).

## What was tried, but not then used

- Installing Linux Mint, because minimum install size 15 GB, too big for internal storage.
- Win10 https://www.youtube.com/watch?v=kXnU_S5ZNJQ https://coolstar.org/chromebook/windows.html would probably require buying and installing bigger SSD/M.2 disk https://www.youtube.com/watch?v=1staB8LtmQM and maybe more RAM.
- Trying to install to external storage like SD or USB card, because it would require remembering keeping that storage plugged in.
- Did not try installing Debian that does not have non-free firmware. Preferred to have non-free firmware included, just in case.
- Did not try to install GalliumOS, it is not developed actively anymore.
- Did try to dd newest UPupBB.iso to eMMC, it did boot from there, but adding more eMMC partitions after UPupBB.iso CDROM did mess up UEFI booting. UPupBB could be confusing to non-English users because many apps there are not translated.
