# Android应用和开发环境
## Android 5.x平台架构与特性
![Android 5.x平台架构与特性](Android应用和开发环境.md_files\01.jpg)
### 主要组成部分
* 应用程序层：包含核心应用程序如：邮件客户端、浏览器、日历等。
* 应用程序框架：Android系统提供的API框架。Android系统上的应用程序开发便是面对应用程序框架进行开发
* 函数库：一套被不同框架使用的C/C++库集合，其中包括：
    * 系统C库
    * 媒体库
    * Surface Manager
    * LibWebCore
    * SGL
    * 3D libraries
    * FreeType
    * SQLite
* Android运行时：包含两部分
    * 核心库集：提供了Java核心库所能使用的绝大部分功能
    * ART：运行在Android系统上的Java虚拟机
* Linux内核
## 安卓开发环境的搭建
### Android Studio的安装与配置
#### Android SDK目录下的文件夹
* docs：存放Android SDK开发文件与API文档等
* extras：存放Google提供的USB驱动、Intel提供的硬件加速等附加工具包
* platform-tools：存放Android平台相关工具
* samples：存放Android示例程序
* sources：存放Android源代码
* system_images：Android系统镜像
