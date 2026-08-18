---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/safe-transform.html"
breadcrumb-title: ''
description: 使用安全轉換節點來套用轉換，同時保留貼圖邊界並避免產生瑕疵。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Safe Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 安全變形
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 1%

---


# 安全變形

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/safe-transform.png)

![](../../../../../../assets/safe-transform-grayscale.png)

## 安全變形（灰階）

**收錄於：***濾波器/轉換*

**中級**

</td>
<td style="border: 0;" valign="top">

## 說明

Transform 2D[&#128279;](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md) 的平鋪安全版本。它允許你在不破壞平鋪的情況下縮放、旋轉和偏移，也不會因為小幅偏移和旋轉而損失像素細節（銳利度或銳利度）。

當需要最大控制或完美銳利度時，對轉換噪音非常有用。

## 參數

* **圖塊**： *1 - 16*&#x200B;透過平鋪來縮小輸入。
* **偏移模式**： *手動，隨機*&#x200B;切換成隨機偏移，而非手動定義的。
* **偏移**&#x200B;量： *0.0 - 1.0*\
  移動或翻譯結果。 確保像素是被吸附而非插值。
* **旋轉**： *0.0 - 1.0*&#x200B;沿著角度旋轉輸入。
* **圖塊安全旋轉**： *False/True（假/真*） 決定旋轉的行為，是否應該吸附到不會模糊像素的安全值。
* **對稱性**： *無，X，Y，X+Y*
* **背景色**： *（色彩值）（僅限彩色版本）*
* **Mipmap 模式**： *自動，手動*&#x200B;決定 mipmapping 模式。 把這個設定設為手動模式，效果會更銳利。
* **Mipmap 等級**： *0 - 10*&#x200B;當 Mipmap 模式設為手動時，可以選擇不同的 Mipmap 模式。

## 範例圖片

|  |
| --- |
| 本頁無附帶圖片。 |

</td>
</tr>
</table>
