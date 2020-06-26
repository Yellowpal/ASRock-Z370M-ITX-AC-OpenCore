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

系统版本：10.15.5

OpenCore：0.5.9

Lilu：1.4.5

VirtualSMC：1.1.4

WhateverGreen：1.4.0

AppleALC：1.5.0

USB：已定制，使用的都是主板上的接口，使用的SMBIOS是iMac19,1，如果需要更改SMBIOS的话请自行更改 USBPorts.kext下面info.plist中的SMBIOS或重新定制。

# 使用方式

1.  填上新的三码即可，参考：https://dortania.github.io/OpenCore-Desktop-Guide/config.plist/coffee-lake.html#platforminfo

2. ROM可填上自己网卡的MAC地址，避免冲突。

3. 以下根据自己硬件进行修改

   ## 1. 有免驱独显

    不需要进行其他修改

   ## 2. 只有核显

   1. 将DeviceProperties->Add->PciRoot(0x0)/Pci(0x2,0x0)->AAPL,ig-platform-id替换为07009B3E。
   2. 根据硬件修改SMBIOS为Macmini机型。

# 功能

1. 随航、硬解正常，FCP核显可以跑到1.1。
2. 睡眠唤醒正常。
3. 主板上的两个网口正常驱动。（未测试网络连接）
4. 其他不一一列举，如使用过程中有问题可一起探讨交流。

