---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/dripping-rust.html"
breadcrumb-title: ''
description: 使用 Dripping Rust 節點根據網格幾何和重力方向生成 Rust 滴落模式。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Dripping Rust
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 滴落的鏽蝕
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2c331b568074714ea71231410f997f965e2bcdaa
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 7%

---


# 滴落的鏽蝕

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](dripping-rust.resources/dripping-rust.png){width="128px"}

<b>收錄於：</b> 基於網格的生成器>遮罩生成器

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

根據烘焙的地圖和使用者設定產生黑白遮罩。 類似 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter) 裡[的智慧口罩](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)。

這個面罩代表鏽蝕片和斑點，漏水沿著下方延伸。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>曲率</b> <i>灰階輸入</i> | 烘焙或生成的地圖來幫助放置生鏽。 |
| <b>環境遮蔽</b> <i>灰階輸入</i> | 烘焙或生成的地圖來幫助放置生鏽。 |
| <b>職位</b> <i>灰階輸入</i> | 用於滴水導向的烘焙或生成地圖。 |
| <b>面具（選用）</b> <i>灰階輸入</i> | 遮罩槽用於遮蔽節點的效果。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>鏽蝕擴散</b> <i>0.0 - 1.0</i> | 主要控制生鏽量。 |
| <b>鏽蝕對比</b> <i>0.0 - 1.0</i> | 設定產生鏽斑的對比度（不影響滴落）。 |
| <b>擴散平滑度</b> <i>0.0 - 1.0</i> | 要施加在鏽斑上的模糊/暈染效果。 |
| <b>滴水強度</b> <i>0.0 - 1.0</i> | 設定滴落的強度與長度。 |
| <b>滴水的順滑度</b> <i>0.0 - 1.0</i> | 滴水時要有多少模糊和抹平。 |
| <b>滴注樣本量</b> <i>0 - 32</i> | 設定滴水效果的品質等級（步驟）。 會稍微影響速度。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="dripping-rust.resources/dripping-rust-ex3.gif" />
        </td>
    </tr>
</table>
