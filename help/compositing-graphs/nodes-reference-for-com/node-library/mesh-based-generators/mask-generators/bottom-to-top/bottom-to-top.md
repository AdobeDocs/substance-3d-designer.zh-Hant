---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/bottom-to-top.html"
breadcrumb-title: ''
description: 使用「從底到頂」節點，根據網格世界位置產生從底部到頂部的漸層遮罩。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Bottom To Top
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 從底部到頂部
user-guide-description: ''
user-guide-title: ''
source-git-commit: c002fea6f396f09ccb3218bd290db812d8367dc4
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 1%

---


# 從底部到頂部

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/bottom-to-top.png){width="128px"}

## 從底部到頂部

**在：***基於網格的產生器/遮罩產生器中*

**很簡單**

</td>
<td style="border: 0;" valign="top">

## 說明

根據烘焙的地圖和使用者設定產生黑白遮罩。 類似 [Painter](https://experienceleague.adobe.com/zh-hant/docs/substance-3d-painter/using/home) 裡[的智慧口罩](https://experienceleague.adobe.com/zh-hant/docs/substance-3d-painter/using/features/smart-materials-and-masks)。

這會產生從模型底部到頂部的白轉黑過渡，對於基於幾何的衰減與選擇非常有用。

## 參數

### 輸入

* **位置**： *顏色輸入*\
  烘焙位置地圖。 必備！
* **粗糙度：***灰階輸入*\
  這跟 PBR 粗糙度無關，只是用來打斷過渡的（可選）變化地圖。 只有當粗糙度設定高於0時才會出現。
* **遮罩（可選）：***灰階輸入*\
  遮罩槽用於遮蔽節點的效果。

### 參數

* **等級**： *0.0 - 1.0*\
  它會像調整亮度一樣，將結果的平均亮度在黑白之間切換。
* **對比**&#x200B;度： *0.0 - 1.0*\
  調整過渡的對比度。
* **粗糙度\_Variation**： *0.0 - 1.0*&#x200B;決定粗糙度貼圖中需要融入的程度以增加變化。 將這個值增加到 0 就會顯示地圖欄位。

## 範例圖片

![](../../../../../../assets/bottom-to-top-ex.gif)

</td>
</tr>
</table>
