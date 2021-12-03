# liverazer
Pre-Built Linux USB Live Image to configure Razer Gaming Laptops/Hardware Lighting without Synapse

TL:DR - Boot this Linux Live USB to control Razer LED Lighting, pre-installed with everything you need!
Make sure to remove Synapse before starting, laptop won’t loose/forget the settings unless you run Synapse (On my Razer Blade 15 (2020) Advanced even after multiple OS re-installs, Linux and Windows).
16GB Memory Stick Required - Write with Win32DiskImager/Rufus on Windows or Etcher on Mac/Linux
DL Here: https://bit.ly/liverazer-01 (2.5GB)

—————————

Hi everyone,

So I’ve got a super early build of my “LiveRazer” project, which I’ll hopefully move to Github/Sourceforge eventually but if anyone is available to test it for now would be great!

Basically the idea of the project is to create a Live Linux USB to configure your Razer Laptop LED’s without requiring the extremely buggy/broken (Fan Speed Issue for me) Synapse 3. (Thanks Razer).

If you have Synapse installed at the minute you need to remove it or it will overwrite your Keyboard/Logo LED settings every time it starts.

Otherwise I’ve been able to completely reinstall laptop several times, Windows 10 and 11 (without Synapse) and the settings have never disappeared.

Here’s all I’ve done (basically) for now:

Installed Linux Mint XFCE 20.2 (Uma) to a 16GB USB Stick.
Set up with user “live” and password “razer”.
(I’m in the UK but just left standard US Keyboard Layout, feel free to change obviously).
Installed all the OS Updates as of 2nd December 21.
Removed as many apps as possible to reduce install size.
Installed the OpenRazer Stable PPA, Linux Kernel Headers and DKMS Modules for OpenRazer.
(Currently installed OpenRazer is 3.0, see openrazer.github.io for supported devices)
Added “live” user to Plugdev Group (sudo gpasswd -a $USER plugdev).
Installed RazerGenie (my preferred one as it seems to remember settings better switching between battery and AC adapter).
Installed Polychromatic (seems to be the most popular configuration utility).
Tested as much as possible on my Razor Blade 15 (2020) Advanced.

For anyone who wants to try it, just write the following .img to a 16GB+ Memory Stick (use Win32DiskImager in Windows, or Etcher on MacOS/Linux).
Then boot from USB (F12), you may have to disable Secure Boot but it shouldn’t have any affect on your Windows installation (I had to try booting twice before “ubuntu” appeared in the boot menu, might be a bug).
It will boot into Ubuntu, simply launch RazerGenie or Polychromatic and set up your lighting the way you want, when you reboot into Windows the settings should be saved until you run Synapse or possibly do a BIOS/Firmware upgrade.
If you loose the settings or want to change them ever, just load up the USB again and work away.

:-)

GDrive Link via Bit.ly (just so I can gauge interest with hit counter): LiveRazer-0.1-211202.7z
https://bit.ly/liverazer-01
(Image Size 14.9GB, Compressed Size 2.5GB)

(This will work on any USB stick 16GB or over but it’s definitely worth using a fairly quick one if you can, otherwise the experience might be a bit sluggish, also I’m fairly certain this will only work UEFI mode).

Please feel free to Reddit DM/email me any suggestions or issues for now, until I get the GitHub (and possibly Discord) page created:
liverazerusb@gmail.com

Thanks everyone!
Hopefully this is useful for someone.
Look forward to hearing your feedback,
Cheers,
David T
