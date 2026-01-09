# EasyFlasher-META脱机烧录器用户使用指南

![](./assets/user_manual/产品展示.png)

## 文档修订历史

| 版本   | 日期         | 修订人 | 说明                      |     |
|:---- |:---------- |:--- |:----------------------- | --- |
| V1.0 | 2025年3月13日 | -   | 出版发布                    |     |
| V1.1 | 2025年5月24日 | -   | 1.增加在线烧录章节<br/>2.更新功能说明 |     |
| V1.2 | 2025年8月16日 | -   | 修订新版META使用说明            |     |
| V1.3 | 2025年9月9日  | -   | 新增连接模式：上电复位模式说明         |     |
| V1.4 | 2025年12月5日 | -   | 增加Keil中Reset复位方式使用说明    |     |
| V1.5 | 2026年1月6日  | -   | 增加**硬件设置**说明            |     |

## 接线说明

### 接线示例

![](./assets/user_manual/接线示例.png)

### 引脚定义

![](./assets/user_manual/引脚定义.png)

### 机台信号控制

- CTRL：外部烧录控制，拉低50ms触发一次烧录
- STA1：烧录状态，高电平表示空闲，低电平表示正在烧录
- STA2：烧录结果，高电平表示烧录成功，低电平表示烧录失败

控制时序如下图所示：

![](./assets/user_manual/机台控制信号时序图.png)

## 设备界面展示

![](./assets/user_manual/设备界面展示.png)

## 脱机烧录配置软件功能说明

![](./assets/user_manual/EasyFlasher.png)

见《[脱机烧录配置软件功能说明](../EasyFlasher/index.md)》

## 脱机烧录

![](./assets/user_manual/脱机烧录配置.png)

脱机烧录器在使用脱机烧录时，需使用配置软件生成.AKF格式的脱机文件。生成脱机文件的具体步骤如下：

1. 选型实际使用的芯片型号；
2. 进行基础设置，如连接方式、擦除方式、选项字节等；
3. 点击【添加程序段】按钮将.bin或者.hex格式的固件文件添加至上位机内；
4. 点击【生成脱机文件】按钮将.afk格式的脱机文件保存至电脑硬盘或直接保存至烧录器U盘内。
5. 将烧录器切换为【USB模式】，烧录器显示界面如下图所示，切换后电脑上弹出U盘，将脱机文件复制到此U盘内即可。

![](./assets/user_manual/USB模式.png)

## 在线烧写

将烧录器切换至【USB模式】，显示界面如下图所示。

![](./assets/user_manual/USB模式.png)

按上下按键可切换DAPLink电平电压。

支持1.8V/3.3V/5V以及外部供电输入四种模式。

当使用外部输入模式时，外部供电电压支持3.3~5V，请勿超压供电！

进入USB模式后，电脑显示一个U盘，并提供DAPLink调试器功能。

可搭配我司上位机软件DAPLinkUtility对目标芯片在线读取、烧录、配置选项字节，解锁芯片等。

DAPLinkUtility使用说明，见《[DAPLink上位机](../DAPLinkUtility/index.md)》。

## Keil在线仿真调试

### Keil配置

见《[Keil中使用DAPLink常用设置](../other/daplink_keil_settings.md)》。

### 驱动安装

见《[DAPLink驱动安装](../other/daplink_driver_install.md)》。

### 常见问题

见《[Keil中使用DAPLink常见问题](../other/daplink_keil_FAQ.md)》。

## 硬件设置（个性化功能）

> 注意：此功能需要烧录器固件版本≥V3.0.3。请检查更新固件并升级：菜单->帮助->固件升级。

见《[硬件设置](../other/hardware_settings.md)》。
