---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/scripting/plugin-basics.html"
breadcrumb-title: ''
description: 學習如何為 Substance 3D Designer 製作 Python 外掛，以擴展應用程式功能。
helpx_creative_field: ""
helpx_description: Designer > Scripting > Plugin basics
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 插件基礎
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 0%

---


# 插件基礎

外掛是一個 Python 檔案或 Python 模組，用來定義初始 <b>化 SDPlugin（）</b> 函式。

<b>當載入外掛時會呼叫初始化 SDPlugin（）</b> 函式。\
在這個函式中，你可以建立使用者介面元素、暫存器回調以及其他你可能需要的功能。

外掛可選擇性地定義 <b>一個 uninitializeSDPlugin（）</b> 函式，當外掛卸載時會被呼叫。\
你可以用這個功能釋放資源、關閉網路連線等等。

```
## Plugin entry point. Called by Designer when loading a plugin.

def initializeSDPlugin(): 

 print("Hello!") 

 

## If this function is present in your plugin,

## it will be called by Designer when unloading the plugin.

def uninitializeSDPlugin(): 

 print("Bye!")
```
