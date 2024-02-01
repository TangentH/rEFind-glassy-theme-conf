# rEFind-glassy-theme-conf
original repo: https://github.com/Pr0cella/rEFInd-glassy

## 使用方式

将这个仓库clone下来，然后把rEFInd-glassy文件夹复制到`/boot/efi/EFI/themes`下，然后把`refind.conf`复制到`/boot/efi/EFI/`下即可，注意备份原来的配置文件

## conf

```
timeout 5
```

5秒后，自动选择上次的OS进去

```
hideui label
```

这个配置项关闭了启动项信息的文本提示

注意不要把`banner`也加上去，因为默认的背景(banner)不是纯黑的，而是官方默认皮肤背景的灰白色，不是很好看

```
# resolution 1920 1080
```

这个配置项本来是开启的，但是发现图标会发生畸变，因此不开启了，而且发现注释掉后并不影响分辨率（应该是只影响banner的分辨率，而与icon的分辨率无关）

```
use_graphics_for osx,linux,windows
```

也就是在按下OS图标后，不会弹出一个蓝色条告诉你refind启动了哪个bootloader的信息

osx指的是苹果

```
dont_scan_dirs /EFI/Boot,EFI/Lenovo,EFI/ubuntu
scan_all_linux_kernels true
```

把复原用的/多余的bootloader过滤掉（包括grub），扫描所有linux内核（这样ubuntu可以从内核启动，而不用再从grub启动一次）



这个主题OS图标下方的三个图标分别是：

| 重启 | 关机 | 重启并且进入BIOS |
| ---- | ---- | ---------------- |

