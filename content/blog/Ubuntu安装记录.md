---
title : Ubuntu安装记录
description : 记录安装 Linux 时的一些大体情况。
date : 4.28 2024 
draft : false
banner: "ubuntu.png"
params:
  author : Queso
weight: 10
tags:
  - Linux
  - Guide

---


## 前言


> 本文为了  ***防止解决的问题在忘记解决方案时再出现***  而撰写。
	
	
### 准备措施


这里采用 Ubuntu 23.10 Desktop 镜像版本，提供了图形化页面，可以根据自己的需求进行更换。

- **拔掉要安装设备的网线。**

- **一个 U盘（U盘安装），大于等于 8G**

- [最新版 Ubuntu 镜像（BT下载）](https://ubuntu.com/download/alternative-downloads)

- [VMWare（虚拟机安装）](https://customerconnect.vmware.com/en/downloads/info/slug/desktop_end_user_computing/vmware_workstation_player/17_0)

- [Rufus 4.3 (U盘烧录)](http://nigger.eastasia.cloudapp.azure.com:5244/d/Onedrive/System%20Backup/rufus-4.3.exe?sign=HhYnX8D6tmuLhwgMqWoh4sOSGsHBsACNGEA1HPt_H5A=:0)





### 安装方式：
		 
	
- 烧录 ISO U盘启动安装进硬盘
- 采用虚拟机直接安装进移动硬盘（Linux to Go）


---

### 虚拟机安装前置步骤

打开 VMware  


```

1. 创建新虚拟机 -> 稍后安装系统 -> 选择Linux 版本
    -> 选择位置 -> 一直默认到自定义硬件
	
2. CD / DVD -> 选择使用ISO映像文件 ，选中你的 ISO
	
3. USB 控制器  -> 兼容性 改为 3.1

```
完成，启动虚拟机。
	
	

---

### U盘安装前置步骤

使用 Refus 刷入镜像进入 U盘 ， 调整 BIOS 为 U盘 启动 
	
	
	
### 进入 Ubuntu 镜像烧录

进入镜像或者U盘启动后  
 
```
Try or Install Unbuntu
	
    1. 选择语言为中文
	
    2. Install Ubuntu
	
    3. 选择不连接网络
	
    4. 默认版本，其他不勾选
```
- #### 选择自定义分区 （Manual partitioning）
	
点击你要的 U盘 新建分区表 
```
1. 创建一个主分区 

  - 大小自定义 
  - 文件格式选择 Ex4
  - 挂载目录选择 /
  
2. 再创建一个 Swap 分区 

  - 大小可以选择跟你内存相同
  - 用于交换内存
  - 挂载目录选择Swap
  
3. 选择引导设备为你的硬盘或 U盘 ，安装进哪里就选哪里。

```  
  
  
下一步开始安装，记得断网不然会无法安装
		
装好后根据提示拔掉U盘，重启电脑即可
 