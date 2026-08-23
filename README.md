# Vanilla OS 中国镜像

[English](./README_en.md)

用于构建 Vanilla OS 中国镜像的 Containerfile。

这些镜像基于以下镜像并行构建 :

- [vanilla-os/gnome](https://github.com/Vanilla-OS/vso-image/pkgs/container/gnome) -> gnome-china
- [vanilla-os/gnome-nvidia](https://github.com/Vanilla-OS/vso-image/pkgs/container/gnome-nvidia) -> gnome-nvidia-china
- [vanilla-os/gnome-nvidia-modern](https://github.com/Vanilla-OS/vso-image/pkgs/container/gnome-nvidia-modern) -> gnome-nvidia-modern-china
- [vanilla-os/gnome-vm](https://github.com/Vanilla-OS/vso-image/pkgs/container/gnome-vm) -> gnome-vm-china

## 所应用的更改

- 预置 Debian 与 Flathub 的国内镜像
- 预置 ibus 与 ibus-rime
- 默认使用本地化的 vso-china-image

## 安装方法

要在 Vanilla OS 中使用本地化镜像，请在安装系统时选择带有“Custom Image”字样的选项。随后，当提示输入镜像名称时，请输入以下镜像之一（由南京大学镜像站提供）：

- ghcr.nju.edu.cn/vanilla-flavors/gnome-china:latest *(适合多数桌面用户)*
- ghcr.nju.edu.cn/vanilla-flavors/gnome-nvidia-china:latest *(适用于旧款 NVIDIA 显卡)*
- ghcr.nju.edu.cn/vanilla-flavors/gnome-nvidia-modern-china:latest *(适用于现代 NVIDIA 显卡)*
- ghcr.nju.edu.cn/vanilla-flavors/gnome-vm-china:latest *(适用于虚拟机)*

如果您的 Vanilla OS 已经安装完成，请使用`abroot rebase <镜像名>`来应用本地化镜像。

声明：该镜像并非由 Vanilla OS 官方进行维护。
