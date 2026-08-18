---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/utilities-mesh-based-generators/tri-planar.html"
breadcrumb-title: ''
description: 使用三平面節點從三個正交平面投影貼圖，實現複雜幾何體的無縫貼圖。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Utilities (Mesh Based Generators) > Tri Planar
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 三平面
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 0%

---


# 三平面

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/triplanar-1.png){width="128px"}

![](../../../../../../assets/triplanar-grayscale.png){width="128px"}

## 三平面（灰階）

**收錄於：***基於網狀的發電機**/工具*

**複合體**

</td>
<td style="border: 0;" valign="top">

## 說明

這個進階節點根據烘焙的「世界空間法線位置」資料，執行三面投影映射。 這表示它基本上會完全將 UV 座標轉換成（大致上）無接縫的貼圖，基於網格本身。

這是避免接縫的好方法，不用每次都重新烘烤（烘焙師也可以做到類似效果）。 缺點是這個節點相當重，因此速度不快。

請記得烘焙必須精準度高：8位元烘焙效果不會很好。

## 參數

### 輸入

* **位置**： *顏色輸入*\
  烘焙位置地圖。 理想狀況是 16 位元或更高的精度。
* **世界空間法線**： *色彩輸入*\
  烘焙世界空間法線貼圖，理想上是 16 位元或更高的精度。
* **輸入 X**：*色彩輸入（灰階輸入）*輸入映射，透過三平面投影將 UV 重新映射到世界空間。 當影像輸入設為 1 時，用於所有軸;若設定為 3，則用於 X 軸。
* **輸入 Y**：*色彩輸入（灰階輸入）*只有當影像輸入設定為 3 時才會這樣。 輸入映射，將 UV 重新映射到 Y 軸的世界空間。
* **輸入 Z**：*色彩輸入（灰階輸入）*僅當影像輸入設定為 3 時。 輸入映射，將 UV 重新映射到 Z 軸的世界空間。

### 參數

* **投影**： *所有軸，只有 X軸，只有 Y軸，只有* Z 設定要混合的軸。
* **影像輸入**： *1 個輸入，3 個輸入*\
  設定是用一張地圖代表所有軸線，還是每個軸線用一張特定的地圖。
* **混合模式**： *線性、進階*&#x200B;提升準確度與精確度。
* **混合對比**&#x200B;度： *0.001 - 1.0*&#x200B;過渡對比，介於平滑或強烈過渡之間。
* **正規化因子**： *0.0 - 1.0*\
  透過恢復混合區域的對比度損失，改善投影的混合效果。
* **貼圖平鋪**： *0.0 - 10.0*&#x200B;將輸入貼圖平鋪的次數。
* **全球旋轉**： *0.0 - 1.0*\
  所有軸的全域旋轉。
* **修正鏡像投影**： *False/True，*&#x200B;設定如何處理鏡像投影。
* **旋轉X**： *0.0 - 1.0*&#x200B;投影X軸上的個別旋轉。
* **旋轉Y**： *0.0 - 1.0*&#x200B;投影Y軸的個別旋轉。
* **旋轉Z**： *0.0 - 1.0*&#x200B;投影Z軸上的個別旋轉。
* **偏移 X**： *0.0 - 1.0*&#x200B;投影 X 軸偏移。
* **隨機偏移X**： *0.0 - 1.0*\
  允許X軸偏移的隨機化。
* **偏移Y**： *0.0 - 1.0*&#x200B;投影Y軸偏移。
* **隨機偏移Y**： *0.0 - 1.0*\
  允許Y軸偏移的隨機化。
* **偏移Z**： *0.0 - 1.0*&#x200B;投影Z軸偏移。
* **隨機偏移Z**： *0.0 - 1.0*\
  允許 Z 軸偏移的隨機化。

## 範例圖片

</td>
</tr>
</table>
