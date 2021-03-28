# Hackintosh_i5-6500_B250M_HD530_EFI

| 名称 | 型号版本 |
|  ----  | ----  |
| 主板 | Gigabyte B250M-D3H |
| CPU	| Intel i5 6500 | 
| 核显	| Intel HD Graphics 530|
| 独显	| 无|
| 网卡	| i219-v |
| 引导	| OpenCore 0.6.6|
| 机型	| Macmini8,1 |
| 平台ID | 0x193B0005|
| 显示器| 4k(3840 × 2160) |

### 核显驱动

显示器为4k显示器，主板Gigabyte B250M-D3H支持4k@60分辨率的DP口显示输出。

B250系主板一般配7代 intel cpu，如 i5-7500，核显型号为 HD 630。GitHub上有很多现成的EFI可以直接使用。我这里6500核显为 HD 530，直接使用EFI，黑屏，无法启动。

仿冒ID：12345678 可以启动，也可以支持到4K，但是显存显示为31MB，特别卡，无法使用。

正确的设置方法为：

 - 机型设置为：Macmini8,1。如果为iMac 17/18 均会出现紫屏现象。
 - 仿冒ID：0x193B0005

以上设置已经配置在 EFI 文件中，同型号HD 530 直接使用即可，不需要另外设置。

![](https://github.com/wonpn/Hackintosh_i5-6500_B250M_HD530_EFI/blob/main/info.png)

### 支持情况

 ✅ 4k60 显示
 
 ✅ 核显显存 1536MB
 
 ✅ Audio 正常
 
 ✅ 有线网卡 正常
 
 ✅ 睡眠唤醒 正常
 
### 存在的问题

 ❌ VedioProc 显示不支持硬件解码，剪辑软件很卡。（Chrome 播放 4K 视频、本地 4K 视频播放正常）
 
 ❌ Chrome 播放4K高码率视频回卡屏，系统假死。关闭 chrome 的“硬件加速”选项可以解决该问题。
