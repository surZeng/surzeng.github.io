---
layout: post
title: "windows下android开发环境搭建（Eclipse）"
date: 2017-04-20 11:52:06 
description: "jdk, sdk, ndk"
tag: android
---


这里将配置android开发环境的步骤简单说一下。
     

# 配置 jdk 环境
* [下载合适的JDK版本](http://www.oracle.com/technetwork/java/javase/downloads/index.html)
* 安装下载下来的jdk，记下安装的路径
* 配置jdk

> 1.右键“我的电脑”或者“这台电脑”——>选择“属性”——>弹出来的页面中点击“高级系统设置”——>选择“高级”选项卡——>点击“环境变量”。

> 2.新建系统变量，变量名：JAVA_HOME， 变量值：刚才安装 jdk 的路径。

> 3.打开path系统变量，在变量值后面添加：;%JAVA_HOME%\bin;%JAVA_HOME%\jre\bin;。

> 4.新建系统变量，变量名：CLASSPATH， 变量值：.;%JAVA_HOME%\lib;%JAVA_HOME%\lib\tools.jar。


* 测试配置是否成功
```bash
>java -version
java version "1.8.0_102"
Java(TM) SE Runtime Environment (build 1.8.0_102-b14)
Java HotSpot(TM) 64-Bit Server VM (build 25.102-b14, mixed mode)
```

# 配置 sdk 环境
* [下载sdk](https://dl.google.com/android/android-sdk_r24.4.1-windows.zip)
* 选择合适的地方解压缩下载的sdk
* 配置 sdk

> 1.右键“我的电脑”或者“这台电脑”——>选择“属性”——>弹出来的页面中点击“高级系统设置”——>选择“高级”选项卡——>点击“环境变量”。

> 2.新建系统变量，变量名：ANDROID_HOME， 变量值：刚才解压 sdk 的路径。

> 3.打开path系统变量，在变量值后面添加：;%ANDROID_HOME%\platform-tools;%ANDROID_HOME%\tools;。


* 测试配置是否成功
```bash
>adb version
Android Debug Bridge version 1.0.36
Revision 0e9850346394-android
```

# 配置 NDK 环境
* [64位NDK下载](https://dl.google.com/android/repository/android-ndk-r13b-windows-x86.zip)
* [32位NDK下载](https://dl.google.com/android/repository/android-ndk-r13b-windows-x86_64.zip)
* 选择合适的地方解压缩并安装下载的ndk，记下安装的路径
* 配置 ndk

> 1.右键“我的电脑”或者“这台电脑”——>选择“属性”——>弹出来的页面中点击“高级系统设置”——>选择“高级”选项卡——>点击“环境变量”。

> 2.新建系统变量，变量名：NDK_ROOT， 变量值：刚才安装 ndk 的路径。


<br>

转载请注明：[曾剑峰的博客](https://surzeng.github.io)