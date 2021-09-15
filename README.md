# ASRock-Z370M-ITX-AC-OpenCore
i7 8700 ES + ASRock-Z370M-ITX-AC + RX570 + OpenCore

# 配置

| 项目 | 配置               |
| ---- | ------------------ |
| CPU  | i7 8700 es QN8H    |
| 主板 | 华擎Z370M-ITX      |
| 显卡 | 蓝宝石RX570 ITX 4G |
| 网卡 | BCM94360CS2        |
| 内存 | 光威 8G 2666 * 2   |
| 电源 | 台达1U 400W        |
| 硬盘 | 海力士PC401 256G   |
| 散热 | ID-COOLING IS-40X  |
| 机箱 | K39+显卡延长线     |

# 版本

系统版本：macOS Big Sur 11.5.2

OpenCore：0.7.3

Lilu：1.5.6

VirtualSMC：1.2.7

WhateverGreen：1.5.3

AppleALC：1.6.4

USB：已定制，使用的都是主板上的接口，使用的SMBIOS是iMac19,1，如果需要更改SMBIOS的话请自行更改 USBPorts.kext下面info.plist中的SMBIOS或重新定制。

# 使用方式

1. 填上新的三码即可，参考：https://dortania.github.io/OpenCore-Desktop-Guide/config.plist/coffee-lake.html#platforminfo

2. ROM可填上自己网卡的MAC地址，避免冲突。

1. 非4K屏如果觉得开机图标太大可将NVRAM->Add->4D1EDE05-38C7-4A6A-9CC6-4BCCA8B38C14->UIScale值设置为01（标准分辨率）。

3. 以下根据自己硬件进行修改

   ## 1. 有免驱独显

    不需要进行其他修改

   ## 2. 只有核显

   将DeviceProperties->Add->PciRoot(0x0)/Pci(0x2,0x0)->AAPL,ig-platform-id替换为07009B3E。

# 功能

1. 随航、硬解正常，FCP核显可以跑到1.1。
2. 睡眠唤醒正常。
3. 主板上的两个网口正常驱动。
4. 其他不一一列举，如使用过程中有问题可一起探讨交流。

