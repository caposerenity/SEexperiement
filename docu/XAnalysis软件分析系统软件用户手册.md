# XAnalysis软件分析系统软件用户手册

## 更新历史

| 修改人员 | 日期      | 变更原因 | 版本号      |
| -------- | --------- | -------- | ----------- |
| 李甘霖   | 2020.6.19 | 最初草稿 | V1.0.0 草稿 |

## 目录

[TOC]



# 1.引言

## 1.1编写目的

指导用户正确配置、使用XAnalysis软件分析系统，并在系统出现故障时，作为系统恢复参考手册

## 1.2项目背景

系统名称：XAnalysis软件分析系统1.0.0

开发者：南京大学软件工程大实验课程项目五组

## 1.3 定义

## 1.4参考资料

1. IEEE标准
2. 本系统用户手册需求规格说明文档
3. 软件工程与计算（卷二）软件开发的技术基础

# 2. 软件概述

## 2.1目标

对于c++项目文件有缺陷分析需求的用户

## 2.2功能

参考《XAnalysis软件分析系统用例文档》

## 2.3 性能

### a.数据精确度

本系统允许输入的数值为0-999999999的所有小数和整数

### b.时间特性

一般操作相应时间<=2秒，特殊操作（如统计、查询、分析、文件上传等）<=10秒

### c.灵活性

灵活性：系统能适应如下变化，并能及时投入部署和运行

- 客户端操作系统变化
- 部分硬件变化（如打印机）
- 网络环境的变化（如区域网升级、重新分配IP地址等）
- 系统数据库版本的变化

# 3. 运行环境

## 3.1硬件

普通PC机，内存2G以上

## 3.2支持软件

运行环境：windows 10

数据库：SQL server 2005以上

# 4. 使用说明

使用过程：

![image-20200715122219921](C:\Users\李甘霖\AppData\Roaming\Typora\typora-user-images\image-20200715122219921.png)

## 4.1安装和初始化

服务器安装：

- 服务器推荐配置：CPU： Intel Xeon 四核 2.0Ghz以上  内存：2.0GB以上
- 在项目文件夹中，使用"npm run serve"命令运行前端，使用"mvn run"命令运行后端

客户端安装：

- 本系统基于Web app进行开发，在服务器运行良好的情况下，客户仅需访问网页即可对本系统进行操作

## 4.2输入

### 4.2.1数据背景

数据输入类型可为:C文件、C++文件或包含前两类文件的项目文件夹

### 4.2.2数据格式

对于C文件和C++文件的格式要求为：能够通过编译器编译，无语法错误

## 4.3输出

### 4.3.l 数据背景

本系统所有输出数据皆以页面展示方式呈现，无与其他系统的数据交互

### 4.3.2数据格式

无

## 4.4出错和恢复

- 用户提交数据格式错误，系统显示上传文件失败
- 用户提交文件中含有语法错误，系统提示代码分析失败后自动恢复，用户可再次提交

# 5. 运行说明

## 5.1运行步骤

- 项目首页：

  ![image-20200715133043736](C:\Users\李甘霖\AppData\Roaming\Typora\typora-user-images\image-20200715133043736.png)

  点击账号状态栏，选择“登录”，跳转进入登录对话框

  ![image-20200715133306739](C:\Users\李甘霖\AppData\Roaming\Typora\typora-user-images\image-20200715133306739.png)

  完成登录后可点击“点击进入静态分析之旅”，跳转进入文件上传页面

- 文件上传页面

  ![image-20200715134340574](C:\Users\李甘霖\AppData\Roaming\Typora\typora-user-images\image-20200715134340574.png)

  点击“上传文件”后，选择需要上传的CPP文件，点击“打开”，系统将自动将该文件传输到服务器端

- 结果展示页面：

  系统将展示缺陷检测结果页面，不同的缺陷类型对应不同颜色高亮显示，用户可根据颜色匹配代码的缺陷产生原因

  ![image-20200715134544301](C:\Users\李甘霖\AppData\Roaming\Typora\typora-user-images\image-20200715134544301.png)

- 检测结果页面：

  检测结果完成后，点击“检测记录”按钮，系统将展示检测所有检测记录，点击某项检测记录可进入到该项检测结果详情界面

  ![image-20200715134759048](C:\Users\李甘霖\AppData\Roaming\Typora\typora-user-images\image-20200715134759048.png)

## 5.2操作信息

用户操作目的：

- 用户登录获得系统检测页面开放权限
- 用户上传文件进行缺陷检测活动

本系统是基于Web app的开发方式，用户仅需操作浏览器系统基本操作即可与本系统进行完整交互

式及格式说明；f.其他事项。

### 5.2.3输入／输出文件

【给出建立或更新文件的有关信息，如：】

a.文件的名称及编号；b.记录媒体；C。存留的目录；d.文件的支配

【说明确定保留文件或废弃文件的准则，分发文件的对象，占用硬件的优先

级及保密控制等.】

# 6. 程序文件（或命令文件）和数据文件一览

![image-20200715132044394](C:\Users\李甘霖\AppData\Roaming\Typora\typora-user-images\image-20200715132044394.png)



