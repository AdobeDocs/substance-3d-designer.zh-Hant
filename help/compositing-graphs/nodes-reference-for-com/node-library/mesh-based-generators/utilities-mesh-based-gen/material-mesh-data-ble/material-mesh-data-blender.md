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
source-git-commit: fbf066c7185f74dcbf35156afc3873d192f77abc
workflow-type: tm+mt
source-wordcount: '572'
ht-degree: 7%

---


# 材質網格資料混合器

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/material-mesh-data-blender.png){width="128px"}

<b>收錄於：</b> 基於網狀的發電機>公用事業

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

這個節點的目的是讓根據烘焙資料加入細節變得更容易。 它附帶很多滑桿，可以根據任何烘焙的貼圖作為輸入，修改輸入的完整材質。 可以多試試看，因為有很多選擇。

它很適合做像是根據曲率或其他地圖加邊緣高亮、用漫反射/基色混合 AO、根據曲率和/或 AO 加入鏡面遮蔽等。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>完整資料輸入（「材料」群組）</b> | 完整的材質地圖。<br><br>這些資料會被該節點修改，然後再以輸出形式返回。 |
| <b>環境遮蔽</b> <i>灰階輸入</i> | 烘焙貼圖用於內部效果和遮罩。 |
| <b>曲率</b> <i>灰階輸入</i> | 烘焙貼圖用於內部效果和遮罩。 |
| <b>高度</b> <i>灰階輸入</i> |  |
| <b>正常</b> <i>色彩輸入</i> |  |
| <b>頂點顏色</b> <i>色彩輸入</i> |  |
| <b>世界太空常態</b> <i>色彩輸入</i> |  |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>頻道</b> | 在這個群組中切換材質通道，例如使用鏡面/光澤貼圖而非金屬/粗糙度時。 影響以下參數的可用性。 |
| <b>烘焙地圖</b> | 是否要使用列出的烘焙地圖來計算。 影響以下參數的可用性。 |
| <b>擴散性AO</b> <i>0.0 - 1.0</i> | 要多少環境遮蔽才能融入擴散效果。 |
| <b>擴散銳利邊緣</b> <i>0.0 - 1.0</i> | 曲率貼圖的多少要融入擴散。 |
| <b>頂點顏色的漫反射色彩</b> <i>0.0 - 1.0</i> | 頂點顏色烘焙的量，要融合到擴散中。 |
| <b>漫反射預照明</b> <i>0.0 - 1.0</i> | 根據世界空間法線（World Space Normals）計算的（假）預光量。 |
| <b>漫射卡通燈光平衡</b> <i>0.0 - 1.0</i> | Diffuse 在寫實與卡通燈光之間切換。 |
| <b>漫反射卡通前燈光層</b> <i>0 - 10</i> | 控制卡通燈光計算的外觀。 |
| <b>擴散卡通大綱</b> <i>0.0 - 1.0</i> | 控制卡通燈光計算的外觀。 |
| <b>底色 AO</b> <i>0.0 - 1.0</i> | 要多少環境遮蔽才能融入基色。 |
| <b>底色銳利邊緣</b> <i>0.0 - 1.0</i> | 曲率貼圖的多少要混合到基色裡。 |
| <b>頂點顏色的基底顏色</b> <i>0.0 - 1.0</i> | 頂點顏色烘焙的量，要融合到基色中。 |
| <b>正常材料強度</b> <i>0.0 - 1.0</i> | 烘焙（切線）法線貼圖的混合強度。 |
| <b>SpecularAO</b> <i>0.0 - 1.0</i> | 在鏡面鏡中融合AO的強度。 |
| <b>鏡面明亮銳利邊緣</b> <i>0.0 - 1.0</i> | 在鏡面中融合曲率強度。 |
| <b>鏡面漫畫大綱</b> <i>0.0 - 1.0</i> | 混合卡通的強度 鏡面邊緣輪廓效果，基於曲率。 |
| <b>光澤 深色銳利邊緣</b> <i>0.0 - 1.0</i> | 將曲面的強度融合在光澤感中。 |
| <b>粗糙 明亮銳利的邊緣</b> <i>0.0 - 1.0</i> | 將曲率強度與粗糙度融合。 |
| <b>粗糙卡通大綱</b> <i>0.0 - 1.0</i> | 混合卡通粗糙邊緣輪廓效果的強度，基於曲率。 |
| <b>金屬光亮銳利的邊緣</b> <i>0.0 - 1.0</i> | 融合金屬色中曲率的強度。 |
| <b>金屬卡通大綱</b> <i>0.0 - 1.0</i> | 融合卡通風格的金屬邊緣輪廓效果，基於曲率。 |
| <b>AO 物資強度</b> <i>0.0 - 1.0</i> | 將烘焙的地圖 AO 與材質生成的 AO 強度混合，該以什麼程度合併兩個 AO 地圖？ |
| <b>高度 材質強度</b> <i>0.0 - 1.0</i> | 將烘焙地圖的高度強度與材質生成的高度混合，並以多大的程度合併兩個高度圖。 |
| <b>高度材質混合類型</b> <i>強化、插值</i> | 混合模式用於結合兩個高度貼圖。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/blenddata-ex.gif" />
        </td>
    </tr>
</table>
