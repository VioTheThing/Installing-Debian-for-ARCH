#      Repacking-Debian-for-ARCH

| Mind helping out a small, Indie Developer? You can help with as much as [tipping to buy a coffee!](https://ko-fi.com/hikkz) |
|      :---:      |

**Hi There!**
You've come here because the software you so darely need on your Arch computer only exists as a .deb, yes? Well fear no more, As I'll show you how to repackage this .Deb for Arch!

##      What do I need prior to this?
All you need is;

- your .deb file
> [!NOTE]
> incase the AUR (ArchLinux User Repository) does not have a prior repackaged repository.
  
- **SUDO privileges**
- **ROOT privileges**

#      Method 1; A priorly repackaged bin is available on the AUR
> [!NOTE]
> For Demonstration purposes, we are using the GameMaker installation files. at the time of writing this, the current Gamemaker debian file is **`GameMaker-Beta-2024.1400.0.849.deb`**. The Version number will be different than yours, so please check first.

###      1. Install yay using pacman.
      `sudo pacman -S yay`
> [!NOTE]
> yay is an AUR helper used to query & install AUR packages. In case the debian package has already been repackaged and published to the AUR by someone else.

###      2. Find your desired file on [AUR](https://aur.archlinux.org/).
for our purposes, it is [Gamemaker-beta-bin](https://aur.archlinux.org/packages/gamemaker-beta-bin).

###      3. Install the package using yay.

> [!NOTE]
> This process will take a while, depending on your Internet speed.

  Raw command:
  
      `yay -S package-name`
      
  For Our Purposes: 
  
      `yay -S Gamemaker-beta-bin`

> [!IMPORTANT]
> press N when it asks you to show any extra files (such as the ToS).

> [!IMPORTANT]
> press Y when it asks you to install any needed repositories.

> [!WARNING]
> ## Once everything is installed, update everything once more using pacman or yay, to make sure no outdated repositories will hinder your repackage from running.

###      You should be good to go from here!
> [!NOTE]
> **If it doesn´t show up, restart your PC and it should show up.**


#      METHOD 2
> [!NOTE]
>  Let's assume the Debian package hasn't been repackaged as an Arch package in AUR yet.

> [!IMPORTANT]
> While there is nothing bad that can **HARM** your computer using this Method, I cannot guarantee that this will work 100%.

> [!TIP]
> What do I need for this?
- yay
- debtap

###      1. Download your desired .debian file.
> [!NOTE]
> For our purposes, this is the latest, official GameMaker debian file.  the current Gamemaker debian file is **`GameMaker-Beta-2024.1400.0.849.deb`**. The Version number will be different than yours, so please check first.

###      2. Install yay using pacman.
      `sudo pacman -S yay`
> [!NOTE]
> yay is an AUR helper used to query & install AUR packages. In case the debian package has already been repackaged and published to the AUR by someone else.

###      3. Install debtap using yay.
      `yay -S debtap`

###      4. Create an equivalent package using debtap
> [!TIP]
> ### you **NEED** Root privileges for this. This is **NOT** optional.

> [!NOTE]
> Raw Command:

      `sudo debtap -U`
      `debtap package_name.deb`

>[!NOTE]
> For our purposes:

      `sudo debtap -U`
      `debtap GameMaker-Beta-2024.1400.0.849.deb`
>[!NOTE]
> This will create a PKG file on your PC.

###      5. install using Pacman
> [!NOTE]
> Raw Command:

      `sudo pacman -U package_name.PKG`
      
> [!NOTE]
> For our purposes:

      `sudo pacman -U GameMaker-Beta-2024.1400.0.849.PKG`

> [!NOTE]
> This should now install GameMaker.


#      METHOD 3 (NOT RECOMMENDED)
> [!CAUTION]
> This method attempts to install the package using the debian packaging format on Arch, which is not recommended due to possible danger of corrupting your installation. **If using this method it is recommended to be ready with a rescue disc image of Arch & backup of the user data/space. YOU HAVE BEEN WARNED.**

> [!TIP]
> What do I need for this?
- yay
- dpkg

> [!WARNING]
> On a serious note; the **general consensus** with using **DPKG** is:
> **It most probably won´t work and you really shouldn´t do it, unless you know what you do. And even then, don´t do it.**

###      1. Download your desired .debian file.
> [!NOTE]
> For our purposes, this is the latest, official GameMaker debian file.  the current Gamemaker debian file is **`GameMaker-Beta-2024.1400.0.849.deb`**. The Version number will be different than yours, so please check first.

###      2. Install yay using pacman.
      `sudo pacman -S yay`
> [!NOTE]
> yay is an AUR helper used to query & install AUR packages. In case the debian package has already been repackaged and published to the AUR by someone else.

###      3. Install dpkg using yay.
      `yay -S dpkg`

###      4. Install the .deb file using dpkg

> [!NOTE]
> Raw Command:

      ` sudo dpkg -i package_name.deb`
> [!NOTE]
> For our purposes:

      `sudo dpkg -i GameMaker-Beta-2024.1400.0.849.deb`

> [!NOTE]
> This should now install your desired .debian.
      



#      FAQ
##      Why can i not use the .deb file directly in Arch Linux?
- .deb files are specifically made to run on **UBUNTU** distributions, while Arch Linux runs, well, **ARCH**.

##      I've found an easier way to do [X]!
- Great! Make your own Repository and update us here.

##      "You can do [X] way easier if you do it with [Y]!"
- Cool! Make your own Repository and update us here.

##      "Can you help me with [XY]?"
- No.
