---
lang: zh-cn
title: 如何正确提问
---

# 如何正确提问

::: info 本节内容

本节为计算机小白指南中的第一部分。

本节旨在帮助先前未曾接触过计算机以及服务器，或者对计算机及服务器知之甚少的用户问出更加明晰高效的问题，减少因沟通产生的不必要的麻烦。

关于如何快速学习相关背景知识，请看 [如何高效学习](./newbie_learn.md)；关于一些小白常见的问题，请看 [计算机小白常见问题](./newbie_faq.md)；关于特定的名词术语解释，请看 [名词/术语速查表](./newbie_terms.md)。

:::

## 前言

自近期用户量剧增后，SealDice 用户群的社区氛围似乎又有些不尽如人意，预料之中而情理之外的事情又再次发生了，我们觉得，用户需要这样一个科普性质的界面。**如果在不知道如何在用户群提问能尽量干脆利落，或者不清楚某些术语该怎么说的情况下，能想到这个系列就最好了**。

当然，我们没有资格教屏幕前的你如何做人，这篇科普也一样，只是给你一个或许更好的建议，是否跟着这么做，取决于你。

## 提问的智慧

在计算机技术领域内，[《提问的智慧》](https://github.com/ryanhanwu/How-To-Ask-Questions-The-Smart-Way/blob/main/README-zh_CN.md)一文广为流传。如果你想认真地学习如何问出一个好问题，强烈建议全文阅读此文章。在用户群的群文件中，也提供了此文章的文件。

当然，海豹用户群的群员们并不会如此严苛，如果你暂时没有时间完整地阅读上述文章，那么认真读完本节也足够你在海豹用户群中问出一个好问题。

## 提问前，你该这样做

### 尝试自行排查问题

对于屏幕前或许没有编程经验的你，可以通过平日里学的「五要素」法则来思考遇到的程序错误问题。下面是一个可行的思考过程。

- **Where**
- 我是在哪里做了一些事情让我的骰子出现问题了？是在服务器还是在我自己的电脑上？
- **When**
- 我在什么时候做了这些事情让骰子出现问题了？
- **What**
- 我做了什么让我的骰子出现了问题？
- **Why**
- 为什么我这么做会让骰子出现问题？
- **How**
- 我怎么做才能去修复这个问题？

通过这样的思考过程，你即使猜测不出问题所在，也可以很好地根据这五个要素的思考过程组织问题，让回答者清晰地知道你的操作流程，更快地找到问题所在，为你解决问题。

### 尝试阅读本手册以找到答案

阅读本手册，尤其是 [计算机小白常见问题](./newbie_faq.md) 和 [常见问题](../use/faq.md) 两个页面。使用页面左上角的搜索按钮有助于提高你的信息效率。

### 尝试浏览用户群内的信息以找到答案

用户群的群公告、群精华消息和历史聊天记录中，有可能找到你问题的答案。

### 尝试上网搜索以找到答案

关于如何高效地进行搜索可以参考 [如何高效学习](./newbie_learn.md) 一节中，[高效搜索](./newbie_learn#高效搜索) 小节。

### 记住你做了什么

你在解决问题时所做的努力——无论仅仅是搜索还是尝试了具体的操作、无论是有效的还是无效的，都将帮助回答者更有效地了解你的背景信息。因此，记住你所做的，并按照下文中的指导，附加在问题中。

## 提问时，你该这样做

本部分中将会为一些涉及的要素提供正例与反例，**正例并不意味着一个好问题（它是一个好问题的一部分）**，但反例显然不应该出现在你的问题里。另一方面，如果你的问题并不涉及某个的要素，那就不要强行加入这个要素。

### 清晰说明你的意图和/或困难

如果你想要让海豹实现某些功能，那么请尽可能清晰完整地描述你想实现的功能。如果你在实现某功能的过程中遇到了麻烦，或者一些你认为本该正常运行的功能表现得不正常，那么请尽可能详细地描述你遇到的困境。

以下是一些合适的措辞：

> 我希望写一个插件，在用户不使用指令前缀的情况下，也能正常响应用户的命令，并实现接入 ChatGPT API 的功能。
> - - -
> 我的骰子突然不响应指令了，具体来说，在我的 xxx 群里可以正常使用，但是我私聊它就不行。

以下是一些典型的反例：

> 呜呜我的骰子怎么不能用了——
> - - -
> 很急！来个大佬救救！

### 描述问题发生前，你做了什么

一个问题可能是也可能不是由用户错误的操作引起的，所以，为了帮助回答者分析定位问题，你应该描述在问题发生之前你做了什么。

以下是一些合适的措辞：

> 我在本地的 Windows 上通过 WinSCP 使用 SSH 协议连接到了我在腾讯云的服务器上，服务器运行的是 Ubuntu 系统。我直接把 data 文件夹拖到了 sealdice-core 同一个目录内，然而在服务器无法启动海豹。
> - - -
> 我在群里 xx 写的 xx 牌堆的基础上修改了牌堆。原本的文件上传到海豹后，可以正确识别。但是我修改之后，上传到海豹，牌堆列表里并没有出现那个文件。我修改的部分是这样的：<屏幕截图>

反例：不提供此类信息。

::: warning 注意：在提供代码相关的信息时，请使用屏幕截图

通常来说，代码都遵守着相应的格式规范。直接将代码复制到聊天窗口中会极大地破坏这种代码规范，严重影响代码的可读性。因此，不要将代码内容复制到聊天窗口中，请使用屏幕截图。

[为什么我在 SealDice 用户群问问题会被要求发送截图？为什么不能拍屏？](./newbie_faq#为什么我在-sealdice-用户群问问题会被要求发送截图-为什么不能拍屏)

:::

### 提供问题发生时，程序的日志

如果你不清楚什么是日志，请看 [名词/术语速查表](./newbie_terms) 中的 [日志](./newbie_terms#日志) 部分。海豹的日志中包含了大量的有效信息，许多问题的直接原因本身就记录在日志中。即使你不能完全理解日志的内容，它也将极大地帮助回答者排查你所遇到的问题。因此，除非你非常确定你遇到的问题与海豹本身的运行无关，或未反映在日志中，请务必提供日志截图。

每行日志的开头都带有时间戳，请确保你发送的日志是问题发生那一刻前后一段时间内的日志。例如，你在 WebUI 查看日志，而你一遇到问题就立刻开始写求助消息，那么此时问题所对应的日志通常位于页面底端，你应该下拉页面，确保截图中呈现了对应的日志。

以下是一些合适的措辞：

> 我发出指令但是骰子在私聊中没有回复我，日志是这样的：<日志截图>
> - - -
> 我修改过的牌堆上传到海豹之后，点击重载牌堆，日志是这样显示的：<日志截图>

反例：不提供日志。

::: warning 注意：在提供日志时，请使用屏幕截图

通常来说，日志中每条记录都相对较长。在一些情况下，日志还会使用特定格式输出堆栈信息。直接将日志复制到聊天窗口中会严重影响日志的可读性。因此，不要将日志内容复制到聊天窗口中，请使用屏幕截图。

[为什么我在 SealDice 用户群问问题会被要求发送截图？为什么不能拍屏？](./newbie_faq#为什么我在-sealdice-用户群问问题会被要求发送截图-为什么不能拍屏)

:::

### 描述问题发生后，你尝试过的解决方案

正如上文中提到的，无论是试图实现一个功能，还是在使用中遇到了不符合预期的事件，你都应该尝试根据参考信息自行解决问题。在提问时，即使你的尝试没有效果，也应该把你尝试过的方法描述出来。你尝试过的方法可能就是排查问题的手段之一，通过你提供的这些信息，回答者可以更加高效的帮助你定位问题。

以下是一些合适的措辞：

> 我试过对我的海豹骰进行重启，还有撤去一些自定义回复文件以及 JSON 牌堆文件，但是基本对数据库文件夹的异常磁盘占用问题没有效果。
> - - -
> 我试过重启海豹（但是没有重启分离部署的 Lagrange），海豹依然不会在私聊中回复我。

反例：不提供此类信息。

### 提供其他有价值的背景信息

海豹核心的版本号、连接的社交平台、连接 QQ 平台时使用的连接方式（内置客户端或分离部署）以及你的操作系统等，都有可能和你所遇到的问题有关。因此，与其提问后再被要求补充这些信息，不如一开始就将它们包含在你的问题之中。

以下是一些合适的措辞：

> 我使用的是 <Badge type="tip" text="vA.B.C" /> 版本的海豹骰，部署在 Windows 11 系统上。私聊不回复的问题是在 QQ 平台发生的。我是通过分离部署连接的 QQ，使用的 QQ 后端是 NapCat。

反例：不提供此类信息。

## 提问后，你该这样做

### 如果问题解决了……

如果回答者提供的解决方案解决了你的问题，你应该做出反馈。

首先，一个有效的问题解决方案可以扩充海豹社区对问题的经验。通过明确地告诉大家问题已经解决，你正在为建设海豹社区做出有力的贡献。

另外，对回答者表示感谢是最基本的礼貌，也是维护海豹社区良好氛围的行为。

### 如果问题没能解决……

问出下一个问题吧。别忘了回顾一遍本节内容，你的追问同样应该是一个良好的问题，这样才有助于问题的快速解决。

当然，那些已经描述过的且未发生改变的信息没有必要再重复一遍。如果你不确定某些信息是否应该重新描述，那就再说一遍，啰嗦总好过一个信息不完整的问题。

另一方面，你也应该额外补充一些信息，尤其是用你自己的话描述一遍你是如何执行回答者所给出的解决方案的。很多时候一个解决方案是有效的，但由于沟通上的歧义或误解，导致它没能被正确执行。因此，再和大家说说你是怎么做的吧。

## 其他事项

### 保持耐心，对回答问题者表现出友善和配合的态度

群员、管理和开发者们都有自己的生活，SealDice 也只是兴趣的一部分。所以，在你的问题看起来没有获得回答的时候，保持耐心。当有群员或管理进一步地询问相关问题，也希望你能友善且相对客观地叙述问题，而不是对他们发泄自己的主观情绪，同时，配合他们进行操作，这样，问题才能更快速地解决。

### 如果有需要，可以去 GitHub 代码仓库上提交 issue

如果你想要问的问题是新的、程序上的需求（例如希望加入一个新的接口），或者你的问题明确了是一个 bug，你希望 SealDice 开发组尽快满足这个需求或修复这个 bug，你可以通过在 GitHub 的 [sealdice/sealdice-core](https://github.com/sealdice/sealdice-core) 仓库中提交一个 issue，开发组的开发者们会通过讨论进行回复，并且，如果确定需要通过你的反馈对程序进行改动，也会更方便开发者们归档问题和修改程序。

## 结语

以上就是提问的智慧中我们总结出的，要在 SealDice 用户社区里**更快地解决问题**，**应该怎么做**的办法。希望通过这样的办法，能让你更有效率地解决在部署 SealDice 的过程中遇到的问题。

**也希望你通过本系列科普有所收获。**