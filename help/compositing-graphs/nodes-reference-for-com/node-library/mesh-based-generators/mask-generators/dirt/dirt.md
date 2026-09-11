---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/dirt.html"
breadcrumb-title: ''
description: 使用 Dirt 節點根據網格曲率、位置和遮蔽產生 dirt 累積遮罩。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Dirt
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 汙垢
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2c331b568074714ea71231410f997f965e2bcdaa
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 6%

---


# 汙垢

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](dirt.resources/dirt.png){width="128px"}

<b>收錄於：</b> 基於網格的生成器>遮罩生成器

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

根據烘焙的地圖和使用者設定產生黑白遮罩。 類似 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter) 裡[的智慧口罩](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)。

此遮罩代表遮蔽與凹陷邊緣與角落的泥土，基於烘焙的 AO 與曲率。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>曲率</b> <i>灰階輸入</i> | 烘焙貼圖用於內部效果和遮罩。 必備！ |
| <b>環境遮蔽</b> <i>灰階輸入</i> | 烘焙貼圖用於內部效果和遮罩。 必備！ |
| <b>Grunge的參與</b> <i>灰階輸入</i> | 自訂 grunge 地圖輸入，可選，並由參數啟用。 |
| <b>面具（選用）</b> <i>灰階輸入</i> | 遮罩槽用於遮蔽節點的效果。 |
| <b>世界太空常態</b> <i>色彩輸入</i> | 只用於三平面。 |
| <b>職位</b> <i>色彩輸入</i> | 只用於三平面。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>泥土等級</b> <i>0.0 - 1.0</i> | 主要控制土壤量。 |
| <b>泥土對比</b> <i>0.0 - 1.0</i> | 控制面罩內髒污的主要對比度。 |
| <b>垃圾搖滾量</b> <i>0.0 - 1.0</i> | 這也決定了泥土有多髒。 設定為 0，讓土壤變得非常光滑。 |
| <b>邊緣遮罩</b> <i>0.0 - 1.0</i> | 根據曲率圖，需要從凸起邊緣去除多少土。 |
| <b>使用自訂垃圾搖滾</b> <i>錯誤/真實</i> | 啟用自訂 grunge 地圖輸入，取代內建 Grunge。 |
| <b>垃圾搖滾等級</b> <i>1 - 16</i> | 設定 Grunge 細節的平鋪比例。 |
| <b>使用三平面</b> <i>錯誤/真實</i> | 使用 [三平面投影](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/utilities-mesh-based-gen/tri-planar/tri-planar.md) 來做垃圾搖滾地圖，去除接縫。 |
| <b>三面融合對比</b> <i>0.001 - 1.0</i> | 設置三平面投影的對比度。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="dirt.resources/dirt-ex.gif" />
        </td>
    </tr>
</table>
