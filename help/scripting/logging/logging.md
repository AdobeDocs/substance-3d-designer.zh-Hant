---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/scripting/logging.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Designer Python 插件中實作日誌功能，用於除錯與監控。
helpx_creative_field: ""
helpx_description: Designer > Scripting > Logging
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 正在記錄
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 4%

---


# 正在記錄

我們建議使用標準 Python 的日誌模組來進行日誌記錄。

<b>sd</b> 模組包含輔助類別，用以將日誌重新導向到 Designer 的主控台。

## 登入設計師的控制台面板

```
import logging 

import sd 

 

 

## Create a logger.

logger = logging.getLogger("MyLogger") 

 

 

## Add a handler to redirect logging to Designer's console panel.

ctx = sd.getContext() 

logger.addHandler(ctx.createRuntimeLogHandler()) 

 

 

## Do not propagate log messages to Python's root logger.

logger.propagate = False 

 

 

## Set the default log level if needed.

logger.setLevel(logging.DEBUG) 

 

 

## Use the logger

logger.info("Info message") 

logger.warning("Warning message") 

logger.error("Error message")
```
