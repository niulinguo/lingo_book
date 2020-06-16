---
description: 本文介绍 MultiDex 的使用和原理
---

# MultiDex 是什么

随着项目的不断壮大，方法数不断增加，有一天你会发现编辑器回报这样一个错：

> Cannot fit requested classes in a single dex file \(\# methods: 99953 &gt; 65536 ; \# fields: 94840 &gt; 65536\)

也许你知道这个问题改怎么解决，但是你有没有想过为什么会出现这种错误呢？

这要从 JVM 说起

不管是 .java 文件还是 .kt 文件，想让 JVM 识别，必须都要先编译成 .class 字节码文件。安卓手机运行 JVM 虚拟机，性能太差，Google 为了解决这个问题，优化了 JVM 虚拟机，也就是我们常听到的 Dalvik、ART 虚拟机。但是他们使用的不是 .class 文件而是 .dex 文件。.dex 文件是多个 .class 文件经过优化后的文件。

我们可以猜得到，这个 .dex 文件最多只能有 65535 个方法数。

有了这个限制，如何解决呢？



