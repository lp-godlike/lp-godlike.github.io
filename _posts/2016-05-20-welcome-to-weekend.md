---
layout: page
title: "first weekend"
subtitle: "This is a subtitle"
date:   2020-09-14 23:21:20 +0530
categories: junk
author: "Bart Simpson"
meta: "Springfield"
---

- 将本地代码推送到远程版本仓库 ps：远程版本仓库=中转站（如git）
- 分支管理
- 安装
   - 1：工作目录  2：压缩包目录  3：安装目录

- 电脑三大系统 Mac、Linux、windows
   - 三大系统都是Unix内核，Linux主要厂牌是Ubuntu/centos    

- 命令行工具（又称终端）
   - 解释命令（命令=小软件）：指示要用哪个工具去做事情
   - 
- markdow 标记语言 （速记用）

- git命令
   - git int    （初始化本地版本库）
   - git status （查看本地版本状态）
      - 本地版本库由暂存区和本地版本库组成，status查看代码是否提交，未提交至任意位置则为红色，在暂存区则为绿色，提交至本地版本库则为clean
   - git add .  （当前文件夹所有内容提交至暂存区）
   - git commit -m "第一次提交"   （提交至本地版本库）
   - git clone 克隆 
   - git push   （推送至远程版本库）ps：推送前必须clean，完整表述为"http://xxx.git.io master:master"
  
- URL：协议、客户端、服务端、端口
   - 客户端=发送请求的软件
   - 服务端=接受请求的软件

- 映射关系：一对一的关系
   - 去host文件寻找域名与IP的映射关系
      - host文件在 C:\windows\sys32\drivers\etc
   - 去DNS服务器中查找