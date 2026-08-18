---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/scripting/undo-and-redo.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Designer Python 腳本中實作復原與重做功能，以支援使用者操作。
helpx_creative_field: ""
helpx_description: Designer > Scripting > Undo and redo
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 還原並重做
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 0%

---


# 還原並重做

使用 <b>SDHistoryUtils.UndoGroup</b> 類別，使用者可以在&#x200B;*一個指令中將*&#x200B;所有動作&#x200B;*分組，以解除或重新執行*。

這些群組由 *使用者命名* ，並會在使用者介面的復原/重做清單中以該名稱出現。這使得大量行動更易管理。

```
import sd 

from sd.api.sdhistoryutils import * 

 

## Get the application and package manager objects.

cxt = sd.getContext() 

app = cxt.getSDApplication() 

pkgMgr = app.getPackageMgr() 

 

## Group one or more changes into an undo group.

with SDHistoryUtils.UndoGroup("My Undo Group"): 

## Create two new packages.

    pkgMgr.newUserPackage() 

    pkgMgr.newUserPackage()
```
