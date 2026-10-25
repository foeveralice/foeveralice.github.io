---
title: "通过wireshark对qq进行流量抓包，并进行文件恢复。"
date: "2026-10-25"
layout: "single"
---
实现前提：
        在同一局域网下，qq通过我的手机发送给电脑的内容是不加密的，因此可以将传输内容还原。
实际操作：
        手机和电脑处于同一局域网，用电脑向手机发送文件，再通过wireshark抓包
![可可爱爱的alice](images/capture.png)
看到最开始的tcp层，使用跟踪tcp流。
![可可爱爱的alice](images/stream.png)
接下来提取文件。
![可可爱爱的alice](images/file.png)
提取后用010editor或其他16进制编辑器查看。
![可可爱爱的alice](images/hex.png)
可以看见很明显的exif标识的jpg文件头，将前面的内容删掉，就能还原文件。
![可可爱爱的alice](images/aaa.png)               