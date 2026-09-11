---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/fxmaps/how-it-works.html"
breadcrumb-title: ''
description: 學習 FXMaps 如何在 Substance 3D Designer 中應用功能圖到材質以產生程序效果。
helpx_creative_field: ""
helpx_description: Designer > Function graphs > FXMaps > How it works
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 運作原理
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 0%

---


# 運作原理

了解 FX-Map 圖形的運作方式，是掌握這項強大功能的關鍵。

FX-Map 圖可以包含三種 FX-Map 節點類型中的一種或多種：象限、迭代和切換。 在這些節點中，你最常用的可能是象限，迭代節點緊隨其後。

參數集節點是 FX-Maps 的主要推動者。 它建立 FX-Maps 依賴的核心區域四叉樹圖，但不會以區域圖形式顯示。 視覺上，四叉樹圖以馬可夫鏈的形式呈現。

在渲染 FX-Map 時，簡化後的 FX-Map 圖會被「展開」，看起來像那棵大樹狀的圖。 引擎「行走」整個四叉戟，從上到下，再從左到右。

FX-Map 節點不會盲目複製貼上圖片。 每張影像渲染時，會執行該影像中的任何動態函式。 這些函式會影響節點渲染的每一張影像。 因此你可以為每張影像隨機旋轉、比例因子或其他多項調整。
