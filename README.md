# Repacking-Debian-for-ARCH

Hi There!
You've come here because the software you so darely need on your Arch computer only exists as a .deb, yes? Well fear no more, As I'll show you how to repackage this .Deb for Arch!

# What do I need prior to this?
All you need is your .deb file, incase the AUR (ArchLinux User Repository) does not have a prior repackaged repository.

# Method 1; A priorly repackaged bin is available on the AUR
_(For Demonstration purposes, we are using the GameMaker installation files. at the time of writing this, the current Gamemaker debian file is **`GameMaker-Beta-2024.1400.0.849.deb`**. The Version number will be different than yours, so please check first.

###  Install yay using pacman.
      `sudo pacman -S yay`
yay is an AUR helper used to query & install AUR packages. In case the debian package has already been repackaged and published to the AUR by someone else.

###  Find your desired file on [AUR](https://aur.archlinux.org/).
for our purposes, it is [Gamemaker-beta-bin](https://aur.archlinux.org/packages/gamemaker-beta-bin).

###  Install the package using yay.
  Raw command:
      `yay -S package-name`
  For Our Purposes: 
      `yay -S Gamemaker-beta-bin`

### press N when it asks you to show any extra files (such as the ToS).
### press Y when it asks you to install any needed repositories.

This process will take a while, depending on your Internet speed.
### once everything is installed, update everything once more using pacman or yay, to make sure no outdated repositories will hinder your repackage from running.

# You should be good to go from here! If it doesn´t show up, restart your PC and it should show up.

# FAQ
## Why can i not use the .deb file directly in Arch Linux?
.deb files are specifically made to run on **UBUNTU** distributions, while Arch Linux runs, well, **ARCH**.

## I've found an easier way to do [X]!
Great! Make your own Repository and update us here.

## "You can do [X] way easier if you do it with [Y]!"
Cool! Make your own Repository, as this is my method.
