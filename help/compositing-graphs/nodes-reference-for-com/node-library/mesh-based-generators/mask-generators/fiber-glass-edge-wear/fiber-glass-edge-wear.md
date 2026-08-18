---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/fiber-glass-edge-wear.html"
breadcrumb-title: ''
description: 使用玻璃纖維邊緣磨損節點，根據網狀曲率在玻璃纖維邊緣生成磨損遮罩。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Fiber Glass Edge Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 玻璃纖維邊緣磨損
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 1%

---


# 玻璃纖維邊緣磨損

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/fiber-glass-edge-wear.png){width="128px"}

## 玻璃纖維邊緣磨損

**收錄於：***基於網格的生成器**/遮罩生成器*

**中級**

</td>
<td style="border: 0;" valign="top">

## 說明

根據烘焙的地圖和使用者設定產生黑白遮罩。 類似 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter) 裡[的智慧口罩](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)。

代表一種專為玻璃纖維材質設計的面具，或許可用於布料。 由於纖維非常拼貼且重複，三平面混合可選擇性啟用。

## 參數

### 輸入

* **曲率**： *灰階輸入*\
  用於邊緣高亮的烘焙地圖。 必備！
* **環境遮蔽**： *灰階輸入*\
  烘焙貼圖用於遮蔽遮蔽區域。 不是必須的，但絕對推薦。
* **垃圾搖滾輸入**： *灰階輸入*\
  可選配自訂插槽來覆蓋光纖模式。
* **遮罩（可選）：***灰階輸入*\
  遮罩槽用於遮蔽節點的效果。
* **世界空間法線**： *色彩輸入*\
  只用於三平面。
* **位置**： *顏色輸入*\
  只用於三平面。

### 參數

* **磨損程度**： *0.0 - 1.0*&#x200B;類似 [直方圖掃描](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md)，逐步揭示磨損狀況。
* **磨損對比**&#x200B;度： *0.0 - 1.0*&#x200B;設定總效果對比度。
* **邊緣平滑度**： *0.0 - 16.0*&#x200B;高亮邊緣會流失或模糊。
* **垃圾搖滾量**： *0.0 - 1.0*&#x200B;設定纖維效果在邊緣間融合多少。 把它和磨損程度一起調整，以獲得最大控制。
* **環境遮蔽遮蔽**： *0.0 - 1.0*&#x200B;設定 AO 對隱藏效果的影響程度。
* **曲率權重**： *0.0 - 1.0*&#x200B;設定曲率凸邊的影響量。
* **使用 Custom Grunge**： *False/True*&#x200B;覆蓋內建光纖並搭配自訂貼圖。
* **使用三平面**： *假/真*&#x200B;使 [三平面](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/utilities-mesh-based-gen/tri-planar/tri-planar.md) 能隱藏接縫。
* **三面融合對比**&#x200B;度： *0.0 - 1.0*&#x200B;控制三面效果的對比度。

## 範例圖片

![](../../../../../../assets/fiber-glass-edge-wear-ex.gif)

</td>
</tr>
</table>
