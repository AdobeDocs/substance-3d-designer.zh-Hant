---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape.html"
breadcrumb-title: ''
description: 使用 Shape 節點來產生基本的幾何圖形，用於在 Substance 3D Designer 中創建圖案和貼圖。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Shape
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 形狀
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 2%

---


# 形狀

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/shape-2.png){width="128px"}

## 形狀

**收錄於：***貼圖產生器**/圖案*

**中級**

</td>
<td style="border: 0;" valign="top">

## 說明

能產生多種程序化形狀，並可修改基礎形狀。 這些形狀總是完美插值且高精度。

儘管簡單，這是一個非常有用的節點：它是大多數程序式高度圖生成的基石！ 透過將基本形狀與變換節點結合，你可以創造出比任何位圖更精確的全程序式高度圖形狀。

## 參數

* **鋪磚**： *1 - 16*\
  設定結果應該鋪磚的次數。
* **圖案**： *方形、圓盤、拋物面、鐘形、高斯分布、荊棘、金字塔、磚、漸變、波浪、半鐘形、脊狀鐘形、彎曲、膠囊、錐形*、半球**\
  選擇要使用的圖案形狀。
* **特定**&#x200B;模式： *0.0 - 1.0*\
  讓你可以改變所選圖案的形狀。 效果取決於所選的模式。
* **比例**： *0.0 - 1.0*&#x200B;可縮放整個形狀。
* **尺寸**： *0.0 - 1.0*&#x200B;允許在 X 軸或 Y 軸上進行非均勻縮放。
* **角度**： *0.0 - 1.0*&#x200B;旋轉整個形狀。
* **旋轉45°**： *假/真*&#x200B;旋轉以預設45度旋轉。
* **非平方展開**： *假/真*\
  能以非平方比率補償擠壓與拉伸。
* **非方形平鋪**&#x200B;**:** *False/True*當啟用非正方形擴展時，會用平鋪方式將形狀平鋪而不會被壓縮。

## 範例圖片

![](../../../../../../assets/shape-ex.gif)

</td>
</tr>
</table>
