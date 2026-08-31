---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/surface-brush.html"
breadcrumb-title: ''
description: 使用 Surface Brush 節點根據表面方向產生遮罩，以創造方向性的風化與磨損效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Surface Brush
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 表面刷
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 6%

---


# 表面刷

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](surface-brush.resources/surface-brush-01.png){width="128px"}

<b>收錄於：</b> 基於網格的生成器>遮罩生成器

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

根據烘焙的地圖和使用者設定產生黑白遮罩。 類似 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter) 裡[的智慧口罩](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)。

此遮罩代表了金屬刷洗在物體表面上的有趣效果，且物體幾何形狀與 AO 遮蔽。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>世界太空常態</b> <i>色彩輸入</i> |  |
| <b>曲率</b> <i>灰階輸入</i> | 烘焙貼圖用於內部效果和遮罩。 |
| <b>環境遮蔽</b> <i>灰階輸入</i> | 烘焙貼圖用於內部效果和遮罩。 |
| <b>職位</b> <i>灰階輸入</i> |  |
| <b>面具（選用）</b> <i>灰階輸入</i> | 遮罩槽用於遮蔽節點的效果。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>關卡</b> <i>0.0 - 1.0</i> | 設定全局效果等級，逐步揭示。 |
| <b>對比</b> <i>0.0 - 1.0</i> | 調整結果的對比度。 |
| <b>Scratches Lenght（長刮痕）</b> <i>0.0 - 8.0</i> | 設定刮痕的長度。 較小的數值像點狀，較高的數值則是長連續。 |
| <b>遮蔽軸</b> <i>X、Y、Z，沒有</i> | 物體的軸線應該會被刮傷。 不會改變刮痕的方向。 |
| <b>遮擋軸強度</b> <i>0.0 - 1.0</i> | 軸的強迫力，遮蔽效應。 |
| <b>遮蔽</b> <i>0.0 - 1.0</i> | AO在閉塞性刮痕上的強度。 |
| <b>銳利強度</b> <i>0.0 - 1.0</i> | 設定磨後磨刀量來處理刮痕。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="surface-brush.resources/surface-brush-02.gif" />
        </td>
    </tr>
</table>
