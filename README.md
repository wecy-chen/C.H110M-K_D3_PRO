# C.H110M-K_D3_PRO
台式电脑EFI文件
## 电脑配置
	电脑型号               七彩虹 C.H110M-K D3 PRO 台式电脑
	操作系统               Windows 10 专业版 64位（Version 1909 / DirectX 12）
	处理器                英特尔 Core i5-7400 @ 3.00GHz 四核   代号 Kaby Lake
	主板                   七彩虹 C.H110M-K D3 PRO（100 Series/C230 Series 芯片组 Family - A143）
	显卡                   英特尔 HD Graphics 630 ( 128 MB / 英特尔 )
	内存                   16 GB ( 金士顿 DDR3 1600MHz / 金泰克 DDR3 1600MHz )
	主硬盘                 西数 WDC WD10EZEX-08WN4A0 ( 1 TB )
	显示器                 冠捷 AOC2180 2180W ( 20.7 英寸  )
	声卡                   瑞昱 ALC662 @ 英特尔 High Definition Audio 控制器    alc-layout-id 5注入
	网卡                   瑞昱 RTL8168/8111/8112 Gigabit Ethernet Controller / 精英

## 适用版本bigSur11.6
	OCC版本 0.7.0 
	以下正常
	1.显卡
	2.网卡
	3.声卡
	4.usb3.0端口


##  开启日志
 1. Target设置67  boot-args 启动参数-v
 2. DisableWatchDog设true AppleDebug设true ApplePanic设true


 ## cfg
 CFGLOCK.efi会自动找到CFG LOCK的参数，如Offset: 003E，值为1，1即可开启，输入Y，即可改为0，即关闭。
 关闭CFG LOCK后，取消AppleCpuPmCfgLOCk和AppleXcpmCfgLOCk

## ControlMsrE2

CFG-锁已经启用
`This firmware has LOCKED MSR 0xE2 register!`

CFG-锁被禁用。
`This firmware has UNLOCKED MSR 0xE2 register!`

## DP

`DeviceProperties`

默认 00001259
```
<key>PciRoot(0x0)/Pci(0x1F,0x3)</key>
  <dict>
      <key>alc-layout-id</key>
      <data>BQAAAA==</data>
  </dict>
  <key>PciRoot(0x0)/Pci(0x1b,0x0)</key>
  <dict>
      <key>layout-id</key>
      <data>BQAAAA==</data>
  </dict>
  <key>PciRoot(0x0)/Pci(0x2,0x0)</key>
  <dict>
      <key>AAPL,ig-platform-id</key>
      <data>AAASWQ==</data>
      <key>framebuffer-patch-enable</key>
      <data>AQAAAA==</data>
      <key>framebuffer-stolenmem</key>
      <data>AAAwAQ==</data>
  </dict>
```

新

id 07009B3E  接口00080000  CON0总线ID01 



