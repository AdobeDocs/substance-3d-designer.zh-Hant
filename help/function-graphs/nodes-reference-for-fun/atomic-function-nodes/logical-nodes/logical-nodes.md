---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/atomic-function-nodes/logical-nodes.html"
breadcrumb-title: ''
description: 存取 Substance 3D Designer 函式圖中的邏輯節點，以執行布林邏輯運算與比較。
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Logical
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 合乎邏輯
user-guide-description: ''
user-guide-title: ''
source-git-commit: f28a2ba2531cfc4456744ff151432ed8308275ec
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 0%

---


# 邏輯節點

邏輯節點用於在圖中加入多種條件：

![](logical-nodes.resources/image2015-12-23-11-23-21.png)

## And *節點*

![](logical-nodes.resources/image2015-12-23-11-30-9.png)

And 節點接收兩個布林節點作為輸入：

* 若兩個輸入皆為 True，則 And *節點的*&#x200B;輸出為 *True。*
* 在其他情況下， *And* 節點會回傳 *False*

## *Or* 節點

![](logical-nodes.resources/image2015-12-23-11-30-44.png)

Or 節點接收兩個布林節點作為輸入：

* 若至少有一個輸入為真（1），則該 Or 節點的&#x200B;*輸出為*&#x200B;真&#x200B;**
* 若兩個輸入皆為 False，Or ** 節點將回傳 *False*

## *Not* 節點

![](logical-nodes.resources/image2015-12-23-11-31-46.png)

Not 節點會接收一個布林值作為輸入：它會查看輸入值並回傳其相反值：

* *真* 輸入會產生 *假* 輸出
* *假* 輸入會得到 *真* 輸出
