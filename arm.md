# Linux on ARM Chromebooks

From https://www.devkitsune.net/blog/wordpress/2024/01/04/linux-on-arm-chromebooks/

by DevKitsune. Posted on January 4, 2024.

Recently I came into possession of a mostly functional
Samsung Chromebook Plus (kevin) which uses a
Rockchip RK3399 ARM CPU.

I have messed around with Linux on Chromebooks before.
In early high school I used Crouton on a cheap
x86 Acer Chromebook and more recently I have used
MrChromebox.tech’s Firmware script to install
Coreboot UEFI on a cheap x86 Lenovo Chromebook
which enables the installation of most normal
desktop Linux distros on Chromebooks
(I ended up installing Xubuntu) none of these
shenanigans have felt particularly worth documenting.
hey are fairly widely know and are covered by
comprehensive guides and documentation from
the people who actually created these tools.

But Linux on ARM Chromebooks is a little bit stranger.
Of course I am still standing on the shoulders of
people much smarter then myself who actually did
the work of creating these distributions and
writing documentation for them, but the documentation
is a bit more scattershot and the options for Linux
on an ARM Chromebook are less straight forward then
simply using a UEFI bootloader and installing your
favorite distro.

## Arch Linux ARM

https://archlinuxarm.org/platforms/armv8/rockchip/samsung-chromebook-plus

Arch Linux ARM got off to a good start.
It was the first distro I found and it had a page
dedicated to my Chromebook model with fairly
comprehensive documentation on how to install,
however things got rocky quickly.

The first issue I ran into was that attempting to
run “wifi-menu” as described in the installation
instructions yielded an error. After some googling
I discovered this could be resolved by downloading
the Marvell wifi package and manually extracting it
the second partition under /lib/firmware/mrvl on
the SD Card that the OS was installed on.

It’s possible that if you used the specific
ARMv8 Rockchip Chromebook image available in their
download page this issue would be resolved, however
the instructions specific to my Chromebook did not
specify to use this image, and instead use the
generic aarch64 image so that was the image I used.

## Link to the WiFi package

https://archlinuxarm.org/packages/any/linux-firmware-marvell

Once the WiFi was working I was easily able to get
the Arch install online. I then ran `pacman -Syu`
and installed XFCE4, and LightDM.

After all this was done I rebooted…. and the Arch
install would no longer boot, instead hanging at
a black screen. My best guess as to what happened
was the system upgrades preformed by pacman broke
something but at this point I was thoroughly
fed up with Arch and decided I would much prefer
something Debian based with all the familiarity
and stability that comes with that.

## PrawnOS (Debian Based – Very FOSS)

I don’t want to be too mean to the guy who created
PrawnOS. Clearly he cares deeply about what he does
and has put a lot of work into building a well
documented and easy to install Debian distro for
ARM Chromeooks but he is also kind of a GNU simp
and FOSS bro. His whole goal with this project
is not to worry about trivial things like having
the WiFi function, and is instead to create
a fully FOSS Debian and he will not be distracted
from that mission by people asking him if they
could please have functional WiFi, or at least
a way to easily enable it.

If you actually want an OS that doesn’t recommend
difficult hardware modifications as the best way
to get WiFi working on your ultra portable
ARM laptop this is not the OS for you.

I tried to make it work. I tried to swap the kernel
for one that was the same version but with WiFi
support using the built in tool to flash the
kernel partition and this resulted in the same
black screen hang up that Arch ran into after
the upgrades.

## Cadmium (Debian Based – IMO the best, but no longer actively supported)

As cliche as it is third try’s the charm I guess.

Cadmium was the third ARM Chromebook distro I tried,
and the first one to just work properly despite
being no longer actively supported.

Its still an extremely up to date Debian base,
using Debian 13 (trixie) and kernel 5.1.3.0 and
the installation process was super easy just like PrawnOS.
Unlike PrawnOS (and Arch) however WiFi worked
out of the box on Cadmium. Also unique to Cadmium is
support for the stylus pen that the Chromebook Plus
includes, which once again worked flawlessly out of the box.

I installed Cadmium with the Sway DE – its worth
noting that because Chromebooks lack a super key
Cadmium’s Sway has been configured to use the
alt key in place of the super key…. this should
not have been hard to figure out but it isn’t
noted anywhere and took me just a little bit
too long to figure out.

Regardless I ended up replacing Sway with XFCE
which is my preferred DE. I run into some weird
visual artifacts with Firefox in both Sway
(which uses Wayland) and XFCE (which uses Xorg)
however these visual artifacts don’t occur in
Chromium nor any other program I have tried,
and overall Cadmium seems much more stable and
mature then the other options for Linux on
ARM Chromebooks.

I was even able to do some light 3D gaming in
Minecraft without issue. I was able to use the
stylus to take notes in Xournal++ and overall
think that if my Chromebook Plus had a properly
functioning keyboard that it would have made
quite the nice little Linux PC. Still it was
fun to play with regardless and if you have
an old ARM Chromebook sitting around I highly
recommend installing CadmiumOS.
