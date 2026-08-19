---
title: 舞台布景材料
description: 設定 SDF 場景材質的基色、粗糙度與金屬度。
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 0%

---


# 舞台布景材料

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![場景資料圖示](set-material.png "套裝素材")

<b>收錄於：</b> 材料>3D函數

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

設定 SDF 場景材質的基色、粗糙度與金屬度。

這些值接著可以取回 Shape splatter v2[&#128279;](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.md) 輸出中所有已濺射的 SDF 形狀。

</td>
</tr>
</table>

>[!INFO]
> 
> 欲了解更多涉及 SDF 函數的概念與工作流程，請前往專門頁面： [使用 SDF 函數](../../working-with-sdf-functions.md)

## 輸入

|                            |                                  |
|----------------------------|----------------------------------|
| <b>SDF場景</b> *浮標* | 輸入SDF場景。 |
| <b>底色</b> *Float3* | RGB 底色值要設定。 |
| <b>金屬性</b> *浮標* | 金屬度數值要設定。 |
| <b>粗糙度</b> *浮標* | 要設定的粗糙度值。 |
