---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/nadir-patch.html"
breadcrumb-title: ''
description: 使用 Nadir Patch 節點來修補 HDRI 全景圖的 Nadir 區域，以修正環境地圖底部的瑕疵。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Nadir Patch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 低谷補丁
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---


# 低谷補丁

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/panorama-nadir-patch.png){width="200px"}

## 低谷補丁

**收錄於：***3D 視圖/HDRI 工具*

**複合體**

</td>
<td style="border: 0;" valign="top">

## 說明

此節點提供連接球面映射影像中央基點（天頂）的功能。 它可以用來隱藏或「複製」醜陋的天底，或可見的相機或三腳架。 它的運作方式類似 [複製補丁](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md)，但可以調整球面映射影像。 使用者選擇影像中其他位置的點，即克隆並混合的底部點。 處理時不需要其他外部輸入，只需單一 HDRI，但可使用外部遮罩作為音色效果的 alpha。

效果可透過 Nadir 萃取[&#128279;](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/hdri-tools/nadir-extract/nadir-extract.md)快速檢查與驗證。

## 輸入

* **輸入**： *彩色輸入*
* **遮罩輸入**： *灰階輸入*\
  可選的遮罩槽用於遮罩音色。 像個阿爾法一樣行事。

## 參數

* **啟用**： *假/真*\
  啟用或關閉補丁效果。
* **顯示幀輔助：***False/True*\
  請顯示或隱藏輔助行，方便除錯。
* **框架厚度**： *0.0 - 1.0*\
  輔助線的厚度。
* **補丁等級**： *0.0 - 1.0*\
  全局且均勻的紋章比例。 影響來源和目標。
* **補丁大小**： *0.0 - 1.0*\
  貼片大小不均。
* **音色輪替**： *0.0 - 1.0*\
  補丁輪替。 影響來源和目標。
* **Patch Alpha**： *光滑方形、高斯、遮罩輸入*\
  設定用來將音色與背景融合的 alpha 值。
* **貼片硬度**： *0.0 - 1.0*\
  設定硬度/α 對比度。
* **源旋轉偏移**&#x200B;量： *0.0 - 1.0*\
  只有補丁來源會輪流使用。
* **位置座標**
  * **資料來源位置**：\
    來源位置。 在2D視角下有把手。
  * **補丁位置**：\
    目標位置。 在2D視角下有把手。

## 範例圖片

![](../../../../../../assets/nadir-patch-ex.gif)

</td>
</tr>
</table>
