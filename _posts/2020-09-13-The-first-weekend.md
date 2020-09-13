---
layout: page
title:  "my notes"
subtitle: "The first weekend"
date:   2020-09-13 21:21:21 +0530
categories: 笔记
---

- 将本地代码推送到远程版本仓库 ps：远程版本仓库=中转站（如git）
- 分支管理

## 电脑三大系统 Mac、Linux、windows
   - 三大系统都是Unix内核，Linux主要厂牌是Ubuntu/centos    

## 命令行工具（又称终端）
   - 解释命令（命令=小软件）：指示要用哪个工具去做事情
   - 
## markdow 标记语言 （速记用）

## git命令
   - git int    （初始化本地版本库）
   - git status （查看本地版本状态）
      - 本地版本库由暂存区和本地版本库组成，status查看代码是否提交，未提交至任意位置则为红色，在暂存区则为绿色，提交至本地版本库则为clean
   - git add .  （当前文件夹所有内容提交至暂存区）
   - git commit -m "第一次提交"   （提交至本地版本库）
   - git clone 克隆 
   - git push   （推送至远程版本库）ps：推送前必须clean，完整表述为"http://xxx.git.io master:master"
   - git log 更替版本库可用该命令查看 commit_id,它可以告诉我们历史记录用于回退版本库
   - git rest --hard "commit_id" 可以在历史版本库更替
   - git reflog 查看命令历史，以便回到后面的版本 
   - git checkout --文件名    可以撤销修改且无论工作区删除或修改均可一键删除
   - git 文件名  删除操作
   - git switch -c 分支名    创建并切换到已有的分支
   - git branch   可以查看分支
   - git branch 分支名       可以创建分支
   - git merge 分支名      合并分支到当前分支
   - git branch -d 分支名  删除分支
   
## URL：协议、客户端、服务端、端口
   - 客户端=发送请求的软件
   - 服务端=接受请求的软件

## 映射关系：一对一的关系
   - 去host文件寻找域名与IP的映射关系
      - host文件在 C:\windows\sys32\drivers\etc
   - 去DNS服务器中查找