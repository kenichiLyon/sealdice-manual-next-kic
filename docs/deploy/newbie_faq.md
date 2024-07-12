---
lang: zh-cn
title: 计算机小白常见问题
---

# 计算机小白常见问题

::: info 本节内容

本节为计算机小白指南中的第三部分。

本节旨在帮助先前未曾接触过计算机以及服务器，或者对计算机及服务器知之甚少的用户快速查询一些常见问题以及对应的答案。本节不能代替权威解释或各项目的官方文档。

关于如何正确地提问，请看 [如何正确提问](./newbie_question)；关于如何快速学习相关背景知识，请看 [如何高效学习](./newbie_learn.md)；关于特定的名词术语解释，请看 [名词/术语速查表](./newbie_terms.md)。

:::

## 部署海豹核心为什么要解压压缩包？怎么样解压压缩包？

如果直接在解压缩应用（如 `7zip`、`WinRar` 等）中双击运行压缩包内的 `sealdice-core.exe` 文件，意味着只有 `sealdice-core.exe` 这一个文件被解压出来了，而其他文件仍然在压缩包之中。海豹核心检测不到其他必要的文件，那么，就无法正常运行。因此，需要把压缩包解压之后再双击运行海豹核心。

解压压缩包需要解压缩的应用，上面已经陈述了一些应用，使用百度搜索一下，下载安装就可以了。

一般而言，用鼠标右击压缩包，再用鼠标左键单击弹出菜单中带有`解压到`字样的选项就能解压这个压缩包。

::: tip 一个建议

解压缩软件时常不会自动帮你创建文件夹，你可能需要自己新建文件夹。这个操作非常简单。

在希望解压的文件夹下单击鼠标右键，在弹出的菜单中找到`新建文件夹`这个选项，左键单击它，然后输入你想要的文件夹名字，再按下键盘上的`Enter`，就新建了一个文件夹。

:::

而如果你想要指定这个压缩包解压到指定的文件夹，你可以右键单击压缩包后选择`解压到…`，在弹出的界面上找到你希望压缩包解压到那里的文件夹，之后双击那个文件夹，最后点击确定，压缩包便解压到了你指定的文件夹。

## 内存不足到底指的是哪里的内存不足？如何解决内存不足？

对于内存不足的情况，需要**具体问题具体分析**。

### 对于海豹核心的日志界面中「There is not enough space on the disk」的报错

翻译一下这里的报错：「在磁盘中没有足够的空间」。

很显然，这里的内存不足代指的是**磁盘可存储的空间不足**，这时候通常通过删除磁盘内部分不需要的文件，腾出空间就可以解决。

### 如果出现莫名其妙的程序中断……

如果你在资源有限的小型计算机/服务器上部署海豹，并且你的海豹是公骰（存在大量用户）或加载了大量牌堆、自定义回复和/或插件，那么有可能出现海豹核心突然中断运行的情况。如果通过日志，排除了程序内部错误的可能性，那就有可能是由内存不足引起的。此处，内存指代的是「运行内存」。

可以在海豹运行时，通过 WebUI「日志」导航栏顶部的内存占用、Windows 平台下的任务管理器、Linux 平台下的 `htop` 等工具对海豹核心的内存使用量和占用比例进行监测，如果确实存在占用过高的情况，可以考虑减少用户群体、移除不常用的自定义回复/牌堆/插件、关闭其他未在使用的进程或更换资源更为充足的平台来解决问题。

::: warning 注意：不要随意关闭你不认识的进程

只有在你完全确定某进程的用途与功能时，才能尝试关闭此进程。失误中断系统进程可能导致系统崩溃或其他隐患。

:::

## 什么是开源，什么是开源程序？

开源，即 Open Source，简言之，就是把程序的源代码放在公共平台（如 GitHub 等）并附加开源许可协议的行为，任何人都可以在开源许可协议允许的范围内下载、修改以及使用这份源代码。

开源程序，顾名思义就是开放了源代码在公共平台的程序。SealDice 就作为一个开源程序活动在大家的视线中。

## 为什么我在 SealDice 用户群问问题会被要求发送截图？为什么不能拍屏？

所有 SealDice 用户群的群员、管理、甚至是开发者，都不具备未卜先知的能力，要求你发送截图也只是为了更好地了解你的问题究竟出在哪里。知道问题出在哪里之后，排查问题或复现 bug 就会更简单。这不仅方便了群员和管理回答你的问题，也有助于你**更快地**解决问题。

不提倡拍屏而是提倡截图的原因是，拍摄屏幕时会出现各种各样的问题：因拍摄角度而看不到部分信息、屏幕因反射光线而不能让摄像头拍到真正的图片（俗称反光），而截图能避免这些问题，给解决带来更高的效率。

::: warning 注意：请做好截图保护！

如果需要发送截图，请在没有**必须要展示**的情况下隐藏好截图内可能存在的敏感信息，比如：IP 地址、端口号、文件夹内布局、密码/auth/key/salt 等。

最好的方式是通过在图片上加马赛克进行遮挡（俗称打码），不建议进行剪裁，除非敏感信息的范围过大。

:::

## 什么是 GitHub？怎么提 issue？

GitHub 是多数开源程序发布代码的地方，SealDice 开发者们平时也通过 GitHub 查看用户的需求和 bug 反馈，同时对程序进行修改，并且在 GitHub 上同步发布更新。

所以，我们希望你如果真的非常需要加入功能、或者反馈 bug，可以自己试试看除了在 SealDice 用户群中向管理说明以外，额外地再提交一份 issue 到海豹的 GitHub 的代码仓库中，这会让开发者们可能记住这个问题，同时在程序中修复它。

对于如何提 issue、怎么样提 issue 不会被关闭，以及如何在 GitHub 上下载文件之类的问题，百度应该是你更好的选择。