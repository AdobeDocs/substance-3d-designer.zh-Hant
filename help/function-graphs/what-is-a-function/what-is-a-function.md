---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/what-is-a-function.html"
breadcrumb-title: ''
description: 了解 Substance 3D Designer 中有哪些函式，以及如何利用它們來建立可重複使用的節點網路。
helpx_creative_field: ""
helpx_description: "Designer > Function graphs > What is a function "
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: '什麼是函數 '
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 0%

---


# 什麼是函數？

Substance 3D Designer 中的函式允許使用者使用您在程式語言中會找到的邏輯來產生結果。

但 Designer 中的函式並非使用程式碼行，而是維持相同的節點方式。 乍看之下，函數圖看起來和一般圖非常相似。

![](what-is-a-function.resources/what-is-a-function-01.png)

你可以在兩種主要情況下遇到函式：

* 用以控制參數的結果
* 如果你編輯像素處理器

## 控制參數的結果

在 Substance 3D Designer 中，任何參數都可以由函式控制。

![](what-is-a-function.resources/what-is-a-function-02.png)

因此你可以想像圖中各部分之間的規則與依賴關係，以獲得唯一的結果。

例如，你可以決定混合節點的不透明度為曲速節點強度的一半：

![](what-is-a-function.resources/what-is-a-function-03.gif)

事實上，你可能已經在不自覺中創建了函式：

如果你暴露了一個參數，你就自動建立了一個函式和一個變數：該函式包含一個 get float 節點，該節點會捕捉新建立變數的值：

![](what-is-a-function.resources/what-is-a-function-04.gif)
