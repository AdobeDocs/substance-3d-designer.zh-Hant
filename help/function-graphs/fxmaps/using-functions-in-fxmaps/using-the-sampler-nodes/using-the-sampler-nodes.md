---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/function-graphs/fxmaps/using-functions-in-fxmaps/using-the-sampler-nodes.html"
breadcrumb-title: ''
description: 學習如何在 FXMaps 中使用取樣節點來取樣貼圖並創造程序化材質變化。
helpx_creative_field: ""
helpx_description: Designer > Function graphs > FXMaps > Using Functions in FXMaps > Using the Sampler nodes
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 使用 Sampler 節點
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 0%

---


# 使用 Sampler 節點

![](../../../../assets/sampler-graph.jpg)

取樣節點可用於取樣連接特效映射節點的影像輸入像素值。 取樣後的值可用來驅動任何參數。

## 簡單範例

在此範例中，已建立一連串象限節點以產生圖案網格。 在最後一象限的不透明度/亮度參數中建立一個函數。

![](../../../../assets/sampler-function.jpg){width="300px"}![](../../../../assets/sampler-result-1.jpg){width="300px"}

Sample 節點會將 float2 輸入作為取樣座標 （x， y）。 在此範例中，我們使用 $pos 變數：每個圖案的像素值會在第一個插入 FxMap 節點的影像輸入中取樣。

Sample Gray 節點回傳 float1 值，範圍為 0， 1。

Sample Color 節點回傳 float4（rgba） 值，範圍為 0,1。

## 進階範例

此處，我們將取樣值與常數 （0.3） 比較。 若取樣值大於 0.3，函數回傳 1，否則回傳 0。

![](../../../../assets/sampler-function-advanced.jpg){width="300px"}![](../../../../assets/sampler-result-advanced.jpg){width="300px"}

## 下載範例

[![SBS 檔案圖示](../../../../assets/sbs-1_1.png){width="64px"}](https://shared-assets.adobe.com/link/d5f9adf3-0bb5-49a1-4eb9-a0506d4f3f32)
