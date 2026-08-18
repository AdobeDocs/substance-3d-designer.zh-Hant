---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/leaks.html"
breadcrumb-title: ''
description: 利用 Leaks 節點根據網格幾何體產生漏水圖案，以製作水漬和流體效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Leaks
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 洩漏資訊
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '333'
ht-degree: 0%

---


# 洩漏資訊

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/leaks.png){width="128px"}

## 洩漏資訊

**收錄於：***基於網格的生成器**/遮罩生成器*

**中級**

</td>
<td style="border: 0;" valign="top">

## 說明

根據烘焙的地圖和使用者設定產生黑白遮罩。 類似 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter) 裡[的智慧口罩](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)。

這個節點代表從銳利邊緣滲出的泥土和污垢條紋。 由於連續條紋是用烘焙位置產生的，它們總是向下延伸。

記得嘗試更換變化遮罩：因為它驅動連續條紋的位置，影響比其他遮罩產生器大得多。

## 參數

### 輸入

* **位置**： *灰階輸入*\
  烘焙位置圖，用於連續路線方向。 必備！
* **曲率**： *灰階輸入*\
  用於連續放置的烘焙地圖。 必備！
* **環境遮蔽**： *灰階輸入*\
  烘焙貼圖用於內部效果和遮罩。 推薦，但你也可以用純白色代替。
* **正常世界空間**： *色彩輸入*\
  烘焙世界空間法線貼圖，用於連續條紋方向。 必備！
* **變異遮罩**： *灰階輸入*\
  可選的變異遮罩，透過將覆寫設定為 True。
* **遮罩（可選）：***灰階輸入*\
  遮罩槽用於遮蔽節點的效果。

### 參數

* **等級**： *0.0 - 1.0*\
  結果的總水平。 逐漸展現效果，也影響長度。 應該設定得比較高，才能讓滴注時間長。
* **對比**&#x200B;度： *0.0 - 1.0*\
  調整結果的對比度。
* **變化**： *0.0 - 1.0*&#x200B;設定用來遮蔽連續痕跡的大規模變化量。 將此值設為 0 會導致連續完全均勻，因此請避免此操作。
* **長度**： *0.0 - 8.0*&#x200B;連續長度會滴落。 在小尺度設定過高的數值會導致明顯的階梯效應。 也可以試試看關卡。
* **遮蔽**： *X、Y、Z、*&#x200B;無 設定 AO 應該影響的方向。
* **覆蓋變異遮罩**： *False/True*&#x200B;啟用以自訂輸入槽覆蓋變異遮罩。 使用較稀疏或密度較高的遮罩會很有趣，也是控制滴落的好方法。

## 範例圖片

![](../../../../../../assets/leaks-ex.gif)

</td>
</tr>
</table>
