---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/utilities-mesh-based-generators/material-mesh-data-blender.html"
breadcrumb-title: ''
description: 使用 Material Mesh Data Blender 節點來混合材質網格資料，創造不同材質區域間的平滑過渡。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Utilities (Mesh Based Generators) > Material Mesh Data Blender
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 材質網格資料混合器
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '578'
ht-degree: 0%

---


# 材質網格資料混合器

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/material-mesh-data-blender.png){width="128px"}

## 材質網格資料混合器

**收錄於：***基於網狀的發電機**/工具*

**複合體**

</td>
<td style="border: 0;" valign="top">

## 說明

這個節點的目的是讓根據烘焙資料加入細節變得更容易。 它附帶很多滑桿，可以根據任何烘焙的貼圖作為輸入，修改輸入的完整材質。 可以多試試看，因為有很多選擇。

它很適合做像是根據曲率或其他地圖加邊緣高亮、用漫反射/基色混合 AO、根據曲率和/或 AO 加入鏡面遮蔽等。

## 參數

### 輸入

* **完整材料輸入（「材料」群組）：** 完整的材料地圖集。\
  這些資料會被該節點修改，然後再以輸出形式返回。
* **環境遮蔽**： *灰階輸入*\
  烘焙貼圖用於內部效果和遮罩。
* **曲率**： *灰階輸入*\
  烘焙貼圖用於內部效果和遮罩。
* **高度**： *灰階輸入*
* **一般：***色彩輸入*
* **頂點顏色**： *顏色輸入*
* **世界空間法線**： *色彩輸入*

### 參數

* **頻道**
  * 在這個群組中切換材質通道，例如使用鏡面/光澤貼圖而非金屬/粗糙度時。 影響以下參數的可用性。
* **烘焙地圖**
  * 是否要使用列出的烘焙地圖來計算。 影響以下參數的可用性。
* **擴散性AO：***0.0 - 1.0*&#x200B;環境遮蔽量，以融入擴散效果。
* **擴散銳利邊緣**：0.0 - 1.0\
  曲率貼圖的多少要融入擴散。
* **從頂點顏色**&#x200B;到漫反射色彩：0.0 - 1.0\
  頂點顏色烘焙的量，要融合到擴散中。
* **漫射預照明**：0.0 - 1.0\
  根據世界空間法線（World Space Normals）計算的（假）預光量。
* **漫射卡通燈光平衡**：0.0 - 1.0\
  Diffuse 在寫實與卡通燈光之間切換。
* **漫射卡通前燈光層**：0 - 10\
  控制卡通燈光計算的外觀。
* **漫漫漫畫大綱**：0.0 - 1.0\
  控制卡通燈光計算的外觀。
* **基礎色 AO：** 0.0 - 1.0\
  要多少環境遮蔽才能融入基色。
* **底色銳利邊緣**：0.0 - 1.0\
  曲率貼圖的多少要混合到基色裡。
* **從頂點顏色**&#x200B;開始的基底顏色：0.0 - 1.0\
  頂點顏色烘焙的量，要融合到基色中。
* **正常材料強度**：0.0 - 1.0\
  烘焙（切線）法線貼圖的混合強度。
* **SpecularAO：** 0.0 - 1.0\
  在鏡面鏡中融合AO的強度。
* **鏡面明亮銳利邊緣**：0.0 - 1.0\
  在鏡面中融合曲率強度。
* **鏡面漫畫大綱**：0.0 - 1.0\
  混合卡通的強度 鏡面邊緣輪廓效果，基於曲率。
* **光澤深銳邊緣**：0.0 - 1.0\
  將曲面的強度融合在光澤感中。
* **粗糙度 亮亮 銳利邊緣**：0.0 - 1.0\
  將曲率強度與粗糙度融合。
* **粗糙卡通大綱**：0.0 - 1.0\
  混合卡通粗糙邊緣輪廓效果的強度，基於曲率。
* **金屬明亮銳利邊緣**：0.0 - 1.0\
  融合金屬色中曲率的強度。
* **金屬卡通大綱**：0.0 - 1.0\
  融合卡通風格的金屬邊緣輪廓效果，基於曲率。
* **AO 物資強度**：0.0 - 1.0\
  將烘焙的地圖 AO 與材質生成的 AO 強度混合，該以什麼程度合併兩個 AO 地圖？
* **高度材質強度**：0.0 - 1.0\
  將烘焙地圖的高度強度與材質生成的高度混合，並以多大的程度合併兩個高度圖。
* **高度材質混合類型**：強化、插值\
  混合模式用於結合兩個高度貼圖。

## 範例圖片

![](../../../../../../assets/blenddata-ex.gif)

</td>
</tr>
</table>
