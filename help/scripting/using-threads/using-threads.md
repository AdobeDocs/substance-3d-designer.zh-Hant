---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/scripting/using-threads.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Designer Python 腳本中使用執行緒來進行平行處理與效能。
helpx_creative_field: ""
helpx_description: Designer > Scripting > Using threads
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 使用執行緒
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 0%

---


# 使用執行緒

外掛<b>可以利用 Python 的執行緒模組&#x200B;*或* Qt 來建立執行緒</b>，針對 Python 執行緒相關類別。

這對於在 Designer 執行時進行背景處理或 I/O 操作非常有用。

值得注意的是，Designer Python API *中的大多數類別與方法只能* 從 <b>主應用程式執行緒</b>呼叫。 因此，如果你想對目前在 Designer 中開啟的任何圖形做任何修改，必須從主應用程式執行緒中進行修改。

一個可能的解決方案是使用 <b>QThread</b> 與 <b>Queued 連線</b>，如下範例所示：

```
import time 

from PySide2 import QtCore 

 

 

## Our thread object.

class TimerThread(QtCore.QThread): 

    tick = QtCore.Signal() 

 

    def run(self): 

        for i in range(0, 7): 

            print("Emitting signal from thread %s" % QtCore.QThread.currentThread()) 

            self.tick.emit() 

            time.sleep(0.5) 

 

 

## Our receiver object, created on the main thread.

class Receiver(QtCore.QObject): 

    def __init__(self, parent=None): 

        super(Receiver, self).__init__(parent) 

 

    def onTick(self): 

## This is called on the main thread. It is safe to use the sd API here.

        print("Tick received in thread %s" % QtCore.QThread.currentThread()) 

 

 

timer = TimerThread() 

receiver = Receiver() 

 

## Use QtCore.Qt.QueuedConnection to make sure that slots are called on the main thread.

## You can also use QtCore.Qt.BlockingQueuedConnection if you need to block while the slot is called.

timer.tick.connect(receiver.onTick, QtCore.Qt.QueuedConnection) 

 

## Start out thread.

timer.start()
```
