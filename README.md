# Vanilla OS 中国镜像

[English](./README_en.md)

用于构建 Vanilla OS 中国镜像的 Containerfile。

这些镜像基于以下镜像并行构建：

- [vanilla-os/gnome](https://github.com/Vanilla-OS/vso-image/pkgs/container/gnome) -> gnome-china
- [vanilla-os/gnome-nvidia](https://github.com/Vanilla-OS/vso-image/pkgs/container/gnome-nvidia) -> gnome-nvidia-china
- [vanilla-os/gnome-nvidia-modern](https://github.com/Vanilla-OS/vso-image/pkgs/container/gnome-nvidia-modern) -> gnome-nvidia-modern-china
- [vanilla-os/gnome-vm](https://github.com/Vanilla-OS/vso-image/pkgs/container/gnome-vm) -> gnome-vm-china

## 所应用的更改

- 预置 GHCR、Docker Hub 与 Flathub 的国内镜像
- 预置 ibus-libpinyin 与 ibus-rime 输入法
- 默认使用本地化的 vso-china-image

## 安装方法

首先，您可以从 [Vanilla OS 官网](https://vanillaos.org/)或[清华大学开源软件镜像站](https://mirrors.tuna.tsinghua.edu.cn/github-release/Vanilla-OS/live-iso)获取 Vanilla OS 的安装镜像。之后，您需要将安装镜像烧录到 U 盘中，并进入 BIOS/UEFI 设置调整启动顺序，从 U 盘启动计算机。

要在 Vanilla OS 中使用本地化镜像，请在安装系统时选择“Install Custom Image (Advanced)”选项。之后，按照顺序设置您的语言（以中国大陆为例，选择 Chinese (Simplified)）、时区 (以中国大陆为例，选择 Shanghai)。随后，当提示输入镜像名称时，请输入以下镜像之一（以使用南京大学开源镜像站为例，也可以使用其他 GHCR 镜像）：

- ghcr.nju.edu.cn/vanilla-flavors/gnome-china:latest *(适合多数桌面用户)*
- ghcr.nju.edu.cn/vanilla-flavors/gnome-nvidia-china:latest *(适用于旧款 NVIDIA 显卡)*
- ghcr.nju.edu.cn/vanilla-flavors/gnome-nvidia-modern-china:latest *(适用于现代 NVIDIA 显卡)*
- ghcr.nju.edu.cn/vanilla-flavors/gnome-vm-china:latest *(适用于虚拟机)*

如果您的 Vanilla OS 已经安装完成，请使用 `abroot rebase <镜像名>` 来应用本地化镜像。

### 输入法

安装完毕开机，设置好您的用户，选择您所需要的应用程序，等待 Vanilla OS First Setup 配置完成后，请打开 GNOME 设置，找到键盘。

![GNOME Settings](images/settings.png)

点击右上角加号，搜索“中文（中国）”，点击并选择对应的输入法。

![Input methods](images/input-method.png)

该镜像预装了两种输入法：

- 智能拼音（ibus-libpinyin）：开箱即用，无须额外配置，但候选词机制可能不尽人意
- 中州韵（ibus-rime）：智能输入引擎，可以自由安装输入方案

您可以按照自己的需求自行选择。如果您选择中州韵输入法，您可以在输入框中按下 Ctrl+` or F4 来切换输入方案、简繁体等。预装的朙月拼音在大多数情况下已经足够使用，您还可以安装其他输入方案，如雾凇拼音等。

声明：该镜像并非由 Vanilla OS 官方进行维护。
