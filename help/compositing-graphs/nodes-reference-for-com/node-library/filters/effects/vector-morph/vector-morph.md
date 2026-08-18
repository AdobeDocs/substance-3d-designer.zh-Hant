---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/vector-morph.html"
breadcrumb-title: ''
description: 使用 Vector Morph 節點，利用向量場來實現平滑過渡，在兩個輸入間做紋理變形。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Vector Morph
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 向量變態
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 1%

---


# 向量變態

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/vector-morph-grayscale.png)![](../../../../../../assets/vector-morph.png)

## 向量變形（灰階）

**收錄於：***濾鏡/效果*

**中級**

</td>
<td style="border: 0;" valign="top">

## 說明

透過向量映射扭曲輸入影像。 這種效果類似於使用法線貼圖（Normalmap）來產生的 UV 變形，或是遊戲著色器中使用的「流程貼圖」。 輸入像素會被向量地圖的紅色和綠色值所定義的向量移動。

這個節點本身不是最難用的，但建立一個正確的向量地圖會很有保障。 我們建議你使用最高位元深度，以確保變形時的精確度。

向量變形和 [向量扭曲](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/vector-warp/vector-warp.md)非常相似：主要差別是這個變形節點不會在結果被推出畫布範圍時「循環」或「平鋪」。 相反地，它會夾住並重複邊緣。

## 參數

### 輸入

* **輸入**： *色彩/灰階輸入*&#x200B;應該是變形目標的來源輸入。
* **向量場**： *色彩輸入*&#x200B;用來驅動變形的向量貼圖。

### 參數

* **數量**： *0.0 - 1.0*&#x200B;設定扭曲效果的強度，作為向量地圖的乘數。

## 範例圖片

</td>
</tr>
</table>
