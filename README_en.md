# Vanilla OS China Images

[中文](./README.md)

Containerfile for Vanilla OS China images.

The images are built in parallel based on the following images :

- [vanilla-os/gnome](https://github.com/Vanilla-OS/vso-image/pkgs/container/gnome) -> gnome-china
- [vanilla-os/gnome-nvidia](https://github.com/Vanilla-OS/vso-image/pkgs/container/gnome-nvidia) -> gnome-nvidia-china
- [vanilla-os/gnome-nvidia-modern](https://github.com/Vanilla-OS/vso-image/pkgs/container/gnome-nvidia-modern) -> gnome-nvidia-modern-china
- [vanilla-os/gnome-vm](https://github.com/Vanilla-OS/vso-image/pkgs/container/gnome-vm) -> gnome-vm-china

## Changes applied to images

- Pre-mirrored Debian sources & Flathub
- Pre-installed ibus & ibus-rime
- Use localized vso-china-image by default

## Installation

To apply the localized images to your Vanilla OS, please choose the "Custom Image" option when installing your system. Then, when prompted for the image name, please enter one of the following images (mirrored by NJU):

- ghcr.nju.edu.cn/vanilla-flavors/gnome-china:latest *(For most desktop users)*
- ghcr.nju.edu.cn/vanilla-flavors/gnome-nvidia-china:latest *(For older NVIDIA GPUs)*
- ghcr.nju.edu.cn/vanilla-flavors/gnome-nvidia-modern-china:latest *(For modern NVIDIA GPUs)*
- ghcr.nju.edu.cn/vanilla-flavors/gnome-vm-china:latest *(For virtual machines)*

If you have your Vanilla OS already installed, please use `abroot rebase <image>` to apply the localized image.

DISCLAIMER: This image is NOT officially maintained by Vanilla OS.
