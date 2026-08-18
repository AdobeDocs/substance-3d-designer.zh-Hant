---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-select.html"
breadcrumb-title: ''
description: 使用 Edge Select 節點生成遮罩，選擇網格邊緣以創造基於邊緣的風化與磨損效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Select
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 邊緣選擇
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 1%

---


# 邊緣選擇

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/edge-select.png){width="128px"}

## 邊緣選擇

**收錄於：***基於網格的生成器**/遮罩生成器*

**中級**

</td>
<td style="border: 0;" valign="top">

## 說明

根據烘焙的地圖和使用者設定產生黑白遮罩。 類似 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter) 裡[的智慧口罩](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)。

這個遮罩是根據曲率選擇任何邊的最佳方式。 凸、凹面在任何層次或對比度下都可以被隔離，這提供了一個極佳的捷徑，避免透過 [層級節點](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/levels/levels.md)手動完成這些操作。

## 參數

### 輸入

* **曲率**： *灰階輸入*\
  烘焙地圖用於高亮邊緣。 必備！
* **遮罩（可選）：***灰階輸入*\
  遮罩槽用於遮蔽節點的效果。

### 參數

* **等級**： *0.0 - 1.0*\
  設定凸與凹邊的總高亮數量。
* **對比**&#x200B;度： *0.0 - 1.0*\
  調整凸與凹的高光對比度。
* **凸面**
  * **凸邊寬度**： *0.0 - 1.0*&#x200B;設定凸邊的高亮寬度。 要注意，稍微增加柔軟度可能會導致邊緣變薄。
  * **凸柔和度**： *0.0 - 1.0*&#x200B;凸邊的過渡軟度設定。
  * **凸強度**： *0.0 - 1.0*&#x200B;設定凸邊中邊緣高亮的最大強度。 設為 0 以表示不高亮。
* **凹面**
  * **凹邊寬度**： *0.0 - 1.0*&#x200B;凹邊的高亮寬度設定。 要注意，稍微增加柔軟度可能會導致邊緣變薄。
  * **凹面柔和度**： *0.0 - 1.0*&#x200B;凹面邊緣的過渡軟度設定。
  * **凹面強度**： *0.0 - 1.0*&#x200B;為凹面邊緣設定邊緣高亮的最大強度。 設為 0 以表示不高亮。

## 範例圖片

![](../../../../../../assets/edge-select-ex.gif)

</td>
</tr>
</table>
