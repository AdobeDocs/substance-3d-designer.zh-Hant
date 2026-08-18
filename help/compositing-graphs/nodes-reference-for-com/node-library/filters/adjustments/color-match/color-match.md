---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/color-match.html"
breadcrumb-title: ''
description: 使用色彩匹配節點來匹配材質間的顏色，以創造一致的色彩調色盤並協調材質。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Color Match
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 顏色配對
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 1%

---


# 顏色配對

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/color-match-3.png){width="128px"}

## 顏色配對

**收錄於：***濾鏡/調整*

**複合體**

</td>
<td style="border: 0;" valign="top">

## 說明

嘗試將定義 *的來源色彩* 範圍與 *目標色彩* 範圍匹配，並支援輸入槽來定義來源與目標。

較簡單的版本請參見 [「替換色彩範圍](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/replace-color-range/replace-color-range.md) 」或 [「替換顏色](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/replace-color/replace-color.md)」。

## 參數

### 輸入

* **輸入**： *彩色* 輸入\
  主要輸入需修改以達成結果。
* **來源顏色**： *色彩輸入*\
  輸入槽用於來源色彩，僅在「來源色彩模式」設為 *輸入*&#x200B;時使用。
* **目標顏色**： *目標顏色的顏色輸入*&#x200B;槽，僅在「目標顏色模式」設為 *輸入*&#x200B;時使用。

### 參數

* **來源色彩模式**： *平均、參數、輸入*&#x200B;設定 來源色彩是透過平均輸入影像、參數設定，或使用輸入槽來定義。
* **來源顏色**：*（色彩值）*&#x200B;若將來源色彩模式設為 *參數*，該參數決定來源顏色。
* **目標色彩模式**： *參數，影像輸入*&#x200B;設定來源顏色是透過平均輸入影像、設定參數，或使用輸入槽來定義。
* **目標顏色**：*（顏色值）*&#x200B;如果目標顏色模式設為 *參數*，該參數決定目標顏色。
* **自訂顏色變化**：假/真\
  可增加顏色變化。
* **顏色變化**\
  若啟用，則可設定色相、色度或亮度變化。
* **使用面具**： *虛假/真實*\
  根據下方遮罩模式，切換遮罩輸入或輸出的使用。
* **遮罩模式**： *參數，輸入*&#x200B;參數模式會輸出一個遮罩，詳細說明顏色如何改變。 輸入模式讓遮罩能控制色彩匹配效果的強度。
* **面具**\
  輸出一個遮罩，顯示色彩匹配效果的精確位置，並附加平滑與模糊遮罩的控制。

## 範例圖片

|  |
| --- |
| 本頁無附帶圖片。 |

</td>
</tr>
</table>
