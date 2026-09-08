---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-select.html"
breadcrumb-title: ''
description: 使用 Edge Select 節點生成遮罩，選擇網格邊緣以創造基於邊緣的風化與磨損效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Select
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 邊緣選擇
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f071c204e1a6c09a04372b7bdaf7cd044080fcc
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 6%

---


# 邊緣選擇

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/edge-select.png){width="128px"}

<b>收錄於：</b> 基於網格的生成器>遮罩生成器

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

根據烘焙的地圖和使用者設定產生黑白遮罩。 類似 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter) 裡[的智慧口罩](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)。

這個遮罩是根據曲率選擇任何邊的最佳方式。 凸、凹面在任何層次或對比度下都可以被隔離，這提供了一個極佳的捷徑，避免透過 [層級節點](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/levels/levels.md)手動完成這些操作。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>曲率</b> <i>灰階輸入</i> | 烘焙地圖用於高亮邊緣。 必備！ |
| <b>面具（選用）</b> <i>灰階輸入</i> | 遮罩槽用於遮蔽節點的效果。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>關卡</b> <i>0.0 - 1.0</i> | 設定凸與凹邊的總高亮數量。 |
| <b>對比</b> <i>0.0 - 1.0</i> | 調整凸與凹的高光對比度。 |
| <b>凸面</b> |  |
| <b>凸邊寬度</b> <i>0.0 - 1.0</i> | 設定凸邊的高亮寬度。 要注意，稍微增加柔軟度可能會導致邊緣變薄。 |
| <b>凸軟度</b> <i>0.0 - 1.0</i> | 將凸邊的過渡軟度設定。 |
| <b>凸強度</b> <i>0.0 - 1.0</i> | 設定凸邊的邊緣高亮強度。 設為 0 以表示不高亮。 |
| <b>凹面</b> |  |
| <b>凹邊寬度</b> <i>0.0 - 1.0</i> | 設定凹邊的高亮寬度。 要注意，稍微增加柔軟度可能會導致邊緣變薄。 |
| <b>凹軟</b> <i>0.0 - 1.0</i> | 將過渡部分的柔和度設定為凹面邊緣。 |
| <b>凹面強度</b> <i>0.0 - 1.0</i> | 將凹面邊緣的高亮亮度設定為最大。 設為 0 以表示不高亮。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/edge-select-ex.gif" />
        </td>
    </tr>
</table>
