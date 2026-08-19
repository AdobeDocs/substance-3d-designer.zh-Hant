---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/non-uniform-blur.html"
breadcrumb-title: ''
description: 使用非均勻模糊節點，在 X 和 Y 方向施加不同強度的模糊，以達到各向異性效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Non Uniform Blur
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 非均勻模糊
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 1%

---


# 非均勻模糊

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/non-uniform-blur-grayscale.png){width="128px"}

![](../../../../../../assets/non-uniform-blur.png){width="128px"}

## 非均勻模糊（灰階）

**收錄於：***濾鏡/模糊*

**中級**

</td>
<td style="border: 0;" valign="top">

## 說明

執行高品質模糊，強度由輸入遮罩驅動。 選項允許加入各向異性與非對稱性。

## 參數

### 輸入

* **模糊貼圖**： *灰階輸入*&#x200B;遮罩貼圖以提升效果強度。

### 參數

* **強度**： *0.0 - 50.0*&#x200B;施加模糊效果的最大強度。 被模糊地圖遮蔽，因此這個設定對該地圖的黑色區域沒有影響。
* **各向異性**： *0.0 - 1.0*&#x200B;可選擇性地為模糊效果增加方向性。 由角度參數驅動。
* **不對稱**： *0.0 - 1.0*&#x200B;可選擇性地增加取樣偏置。 由角度參數驅動。
* **角度**： *0.0 - 1.0*&#x200B;設定方向與取樣偏壓的角度。
* **樣品**&#x200B;數量： *1 - 16*&#x200B;樣本數量，決定品質。 乘以刀刃數量。
* **刀刃**： *1 -* 9\
  抽樣區域的數量決定了品質。 乘以樣本數量。

## 範例圖片

*下方範例是由模糊貼圖槽中90度的梯度斜坡驅動。*

![](../../../../../../assets/nonuniform-example.gif)

</td>
</tr>
</table>
