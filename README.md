cyberlinux repo
====================================================================================================

<img align="left" width="48" height="48" src="https://raw.githubusercontent.com/phR0ze/cyberlinux/master/art/logo_256x256.png">
<b><i>cyberlinux</i></b> was designed to provide the unobtrusive beauty and power of Arch Linux as a
fully customized automated offline multi-deployment ISO. Using clean declarative yaml profiles,
cyberlinux is able to completely customize and automate the building of Arch Linux filesystems
which are bundled as a bootable ISO. Many common use cases are available as deployment options
right out of the box, but the option to build your own infinitely flexible deployment is yours
for the taking.

### Disclaimer
***cyberlinux-repo*** comes with absolutely no guarantees or support of any kind. It is to be used at
your own risk.  Any damages, issues, losses or problems caused by the use of ***cyberlinux-repo*** are
strictly the responsiblity of the user and not the developer/creator of ***cyberlinux-repo***.

### Re-create the Repo Database
Creating a repo database from a directory of packages is a simple process:

1. Navigate to the repo location
   ```bash
   $ cd ~/Projects/cyberlinux-repo/cyberlinux/x86_64
   ```
2. Remove prior database files
   ```bash
   $ rm -rf cyberlinux.*
   ```
3. Re-create the database
   ```bash
   $ repo-add cyberlinux.db.tar.gz *.pkg.tar.*
   ```

Key:
* **AUR** indicates the upstream aur package was built and added to this repo
* **Repackaged** indicates the upstream bits were customized and packaged with `cyberlinux-aur/<package>`
* **Custom** indicates this package was wrote from scratch and packaged with `cyberlinux-aur/<package>`

| Package                         | Version           | Purpose                
| ------------------------------- | ------------------| ------------------------------------------------------------------
| arch-install-scripts            | 22-2              | Repackaged: patched the arch-chroot to retry umount for reduce
| arcologout                      | 1.0.1-2           | 
| awf-git                         | v1.3.1.r4.gcee91. | ?
| bindip                          | 0.0.1-1           | ?
| ccextractor                     | 0.88-1            | AUR: dependency of makemkv
| cyberlinux-grub                 | 0.0.3-1           | Custom: provides cyberlinux splash screen and boot files
| cyberlinux-keyring              | 0.0.170-2         | Custom: provides cyberlinux keyring
| cyberlinux-nvim                 | 0.0.1             | Custom: Install and configures neovim, vim-plug for cyberlinux
| cyberlinux-plank                | 0.11.4-4          | Repackaged: modified the source with better defaults 
| cyberlinux-screenfetch          | 3.8.0-2           | Custom: cyberlinux screenfetch
| epson-inkjet-printer-escpr2     | 1.0.26-1          | AUR: Driver for the Epson WorkForce 7710 inkjet all-in-one printer
| google-cloud-sdk                | 243.0.0-1         | ?
| idesk                           | 0.7.5-8           | AUR: desktop icon support
| imagescan-plugin-networkscan    | 1.1.2-1           | AUR: Scanner driver for Epson WorkForce 7710 inject all-in-on printer
| input-wacom-dkms                | 0.39.0-1          | AUR: wacom input driver
| inxi                            | 3.0.36-2          | AUR: Low level cli tool for device configuration discovery
| jd-gui                          | 1.6.3             | Repackaged: patched with dark theme and java font fix
| lib32-freetype2                 | 2.8-2             | ?
| lib32-nvidia-340xx-utils        | 340.107-4         | AUR: supports the Quadro FX 3800 and other older cards
| lib32-opencl-nvidia-340xx       | 340.107-4         | AUR: supports the Quadro FX 3800 and other older cards
| libblockdev                     | 2.22-2            | Repackaged: recompiled ABS with `--without-lvm` to remove the lvm2 dependency
| libxnvctrl-340xx                | 340.107-2         | Repackaged: provides libxnvctrl used by conky
| light                           | 1.1.2-1           | AUR: file size ui tool
| makemkv                         | 1.14.4-1          | Repackaged version making ccextractor a default dependency
| mkinitcpio-vt-colors            | 1.0.0-1           | Custom: provides kernel output coloring on boot
| mycli                           | 1.23.2-1          | AUR: A terminal client for MySQL with AutoCompletion and SyntaxHighlighting
| numix-frost-themes              | 3.6.6-1           | ?
| nvidia-340xx                    | 340.107-92        | AUR: supports the Quadro FX 3800 and other older cards
| nvidia-340xx-dkms               | 340.107-92        | AUR: supports the Quadro FX 3800 and other older cards
| nvidia-340xx-settings           | 340.107-2         | AUR: supports the Quadro FX 3800 and other older cards
| nvidia-340xx-utils              | 340.107-4         | AUR: supports the Quadro FX 3800 and other older cards
| opencl-nvidia-340xx             | 340.107-4         | AUR: supports the Quadro FX 3800 and other older cards
| openvpn-update-systemd-resolved | 1.2.6-1           | ?
| paper-icon-theme                | 1.4.0-1           | ?
| php                             | 7.1.12-2          | ?
| php-apache                      | 7.1.12-2          | ?
| php-gd                          | 7.1.12-2          | ?
| php-sqlite                      | 7.1.12-2          | ?
| pjproject                       | 2.7-1             | ?
| pnmixer                         | 0.7.2-1           | ?
| postman-bin                     | 6.1.3-2           | ?
| powerline-gitstatus             | 1.3.1-1           | Custom: provides gitstatus in PS1 using powerline
| python-cli_helpers              | 2.1.0-1           | AUR: supports `mycli`
| systemd-docker                  | 0.2.1-1           | ?
| teamviewer                      | 13.2.13582-1      | Remote desktop software - licensed for personal use only
| termcap                         | 1.3.1-6           | ?
| tiny-media-manager              | 2.9.16-1          | AUR: Kodi compatible media manager
| ttf-google-fonts-fun            | 1.0.0             | Repackaged: some of the script and sans serif fun fonts
| ttf-google-fonts-work           | 1.0.0             | Repackaged: includes the same fonts as typewolf did
| ttf-inconsolata-g               | 20090213-3        | AUR: excellent mono space coding font
| ttf-ms-fonts                    | 2.0-10            | AUR: old venerable Microsoft fonts
| ttf-nerd-fonts-symbols          | 2.0.0-2           | AUR: font symbols useful for powerine etc...
| vdhcoapp-bin                    | 1.3.0-2           | Repackaged: Video Download Helper's companion app, simply bumped the version
| virtualbox-ext-oracle           | 6.0.4-1           | AUR: extensions for virtualbox
| visual-studio-code-bin          | 1.34.0-2          | AUR: excellent development IDE
| vivaldi                         | 2.5.1525.48-1     | An advanced browser made with the power user in mind
| vpnctl                          | 0.0.62-1          | ?
| winff                           | 1.5.5+f721e4d-1   | AUR: GUI for ffmpeg
| wpa\_gui                        | 2.6-1             | Custom: A Qt frontend to wpa\_supplicant
| xcursor-numix-frost             | 0.9.9-4           | Custom: X-Cursor theme for use with numix products
| xnviewmp                        | 0.89-1            | AUR: An efficient multimedia viewer, browser and converter
| yay                             | 10.3.1-2          | AUR: Pacman wrapper and AUR helper written in go
| zoom                            | 2.8.252201.0616-1 | AUR: Video Conferencing and Web Conferencing Service

<!-- 
vim: ts=2:sw=2:sts=2
-->
