---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/utilities-mesh-based-generators/3d-planar-projection.html"
breadcrumb-title: ''
description: 使用 3D 平面投影節點，將貼圖投影投影到網格表面上，並使用平面投影來做貼圖貼圖。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Utilities (Mesh Based Generators) > 3D Planar Projection
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 三維平面投影
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 1%

---


# 三維平面投影

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3d-planar-gray.png)![](../../../../../../assets/3d-planar.png)

## 3D 平面投影（彩色）

**收錄於：***基於網狀的發電機**/工具*

**複合體**

</td>
<td style="border: 0;" valign="top">

## 說明

根據烘焙的網格資料（位置與世界法線貼圖）執行平面投影。 允許你在接縫間投影並放置貼紙，獨立於原始 UV 映射。

## 參數

### 輸入

* **位置映射**： *顏色輸入*&#x200B;烘焙位置映射
* **世界空間法線**： *色彩輸入*&#x200B;烘焙世界空間法線貼圖
* **投影貼圖**： *顏色輸入*&#x200B;輸入貼圖要投影到目標上。

### 參數

* **定位**
  * **專案輸入**： *UV 位置、世界空間位置*&#x200B;選擇投影位置設定為 2D/UV 或 3D/World 空間。
  * **目標紫外線位置**：\
    只有在 UV Position Input 時才會這樣，最佳方式是用來在 Position map 的 2D 視圖中選擇一個點。
  * **目標位置**：*（色彩值）*只有在世界空間位置輸入時，才能定義精確的三維座標。
  * **目標法線**： *（顏色值）*
  * **旋轉**： *0.0 - 1.0\
    會沿著投影的貼圖軸旋轉。*
  * **等級**： *0.0 - 1.0*\
    設定投影材質的全域縮放。
  * **尺寸**： *0.0 - 2.0*&#x200B;對投影材質進行非均勻縮放。
* **遮蔽**
  * **最大深度**： *0.0 - 1.0*&#x200B;控制投影材質的深度，以及何時會被切斷。
  * **深度漸入淡出**： *0.0 - 1.0*&#x200B;將截止深度的過渡設定為突然或漸淡。
  * **法線閾值：*-1.0 - 1.0*設定**&#x200B;不完全與投影法線對齊的表面的限制。
  * **正常漸移**： *0.0 - 1.0*&#x200B;未對齊的表面將過渡設定為突然或漸移。

## 範例圖片

![](../../../../../../assets/3d-planar-projection-ex.gif)

</td>
</tr>
</table>
