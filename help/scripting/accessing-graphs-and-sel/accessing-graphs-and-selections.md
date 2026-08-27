---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/scripting/accessing-graphs-and-selections.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Designer Python 腳本中存取並操作圖表與節點選擇。
helpx_creative_field: ""
helpx_description: Designer > Scripting > Accessing graphs and selections
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 存取圖表與選擇
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 0%

---


# 存取圖表與選擇

<b>SDApplication</b> 類別包含一些有用的方法，讓你能存取&#x200B;*目前活躍*&#x200B;的圖表，以及&#x200B;*其中的當前選擇*。

```
import sd 

 

## Get the application and UI manager object.

ctx = sd.getContext() 

app = ctx.getSDApplication() 

uiMgr = app.getQtForPythonUIMgr() 

 

## Get the current graph.

g = uiMgr.getCurrentGraph() 

print("The current graph is %s" % g) 

 

## Get the currently selected nodes.

selection = uiMgr.getCurrentGraphSelectedNodes() 

for node in selection: 

 print("Node %s" % node)
```


特定圖視圖中顯示&#x200B;**&#x200B;的圖形可以透過 graphViewID</b> 存取<b>。

此方法在建立自訂圖形檢視工具列時非常有用。 <b>在「建立使用者介面元素](../../scripting/creating-user-interface/creating-user-interface-elements.md)」章節中的「在圖視圖</b>中建立工具列」範例[提供了更多細節。
