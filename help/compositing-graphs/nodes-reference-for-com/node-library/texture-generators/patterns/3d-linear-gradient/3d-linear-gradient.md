---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/3d-linear-gradient.html"
breadcrumb-title: ''
description: 使用 3D 線性漸層節點，根據 3D 世界位置建立線性漸層以產生空間效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > 3D Linear Gradient
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 三維線性梯度
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 1%

---


# 三維線性梯度

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3d-linear-gradient.png){width="128px"}

## 三維線性梯度

**收錄於：***貼圖產生器**/圖案*

**中級**

</td>
<td style="border: 0;" valign="top">

## 說明

根據輸入位置貼圖建立體積梯度。 有效地在三維空間中產生從黑轉白的過渡。 本作只針對 GPU 引擎使用。

還有類似效果，請參考 [3D 體積遮罩](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/3d-volume-mask/3d-volume-mask.md) 。

## 參數

* **點位置模式**： *UV 位置、世界空間位置*&#x200B;選擇漸層點是在 UV 空間（設定在 2D 視圖時效果最佳）或在 3D 座標中運作，如果你想手動輸入精確位置。
* **第一點**：\
  梯度的起點。 可以是基於位置模式的二維或三維座標。
* **第二點**：\
  梯度的終點。 可以是基於位置模式的二維或三維座標。
* **對比**&#x200B;度： *0.0 - 1.0*\
  調整結果的對比度。

## 範例圖片

![](../../../../../../assets/3d-gradient.gif)

</td>
</tr>
</table>
