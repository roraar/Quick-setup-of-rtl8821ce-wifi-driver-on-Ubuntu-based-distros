# Quick setup of rtl8821ce wifi driver with DKMS

Every time i reinstall my laptop's OS (Ubuntu-based), I have to do a few lines of code in the terminal to get the wifi driver to work.

This is just a simple bash-script that does it all in one go.

The code was originally gotten from this forumpost: https://forums.linuxmint.com/viewtopic.php?t=290073

# On Arch based systems

Don't run the shell-script on arch. You CAN use the AUR to do this, but I prefer to do this manually. It's essentially the same steps as in the script, but with a different syntax. 

Do the following in terminal:

* sudo pacman -Syu git dkms

When finished, also install llinux headers for the current running kernel:

* uname -r (will give you running kernel version)
* sudo pacman -Syu linux-headers

Afterwards, simply follow the same procedure as in the shell script:

* git clone https://github.com/tomaspinho/rtl8821ce.git
* cd rtl8821ce
* sudo ./dkms-install.sh

reboot and done!
