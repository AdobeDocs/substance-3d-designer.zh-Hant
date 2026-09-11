---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/fiber-glass-edge-wear.html"
breadcrumb-title: ''
description: 使用玻璃纖維邊緣磨損節點，根據網狀曲率在玻璃纖維邊緣生成磨損遮罩。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Fiber Glass Edge Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 玻璃纖維邊緣磨損
user-guide-description: ''
user-guide-title: ''
source-git-commit: 78cf3f307bd33c6d8b399043ff1c5e5d1764b606
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 5%

---


# 玻璃纖維邊緣磨損

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](fiber-glass-edge-wear.resources/fiber-glass-edge-wear.png){width="128px"}

<b>收錄於：</b> 基於網格的生成器>遮罩生成器

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

根據烘焙的地圖和使用者設定產生黑白遮罩。 類似 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter) 裡[的智慧口罩](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)。

代表一種專為玻璃纖維材質設計的面具，或許可用於布料。 由於纖維非常拼貼且重複，三平面混合可選擇性啟用。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>曲率</b> <i>灰階輸入</i> | 用於邊緣高亮的烘焙地圖。 必備！ |
| <b>環境遮蔽</b> <i>灰階輸入</i> | 烘焙貼圖用於遮蔽遮蔽區域。 不是必須的，但絕對推薦。 |
| <b>垃圾搖滾輸入</b> <i>灰階輸入</i> | 可選配自訂插槽來覆蓋光纖模式。 |
| <b>面具（選用）</b> <i>灰階輸入</i> | 遮罩槽用於遮蔽節點的效果。 |
| <b>世界太空常態</b> <i>色彩輸入</i> | 只用於三平面。 |
| <b>職位</b> <i>色彩輸入</i> | 只用於三平面。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>磨損程度</b> <i>0.0 - 1.0</i> | 就像 [直方圖掃描](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md)一樣，逐漸揭示磨損。 |
| <b>戴對比</b> <i>0.0 - 1.0</i> | 設定整體效果對比。 |
| <b>邊緣平滑度</b> <i>0.0 - 16.0</i> | 場景從高亮邊緣流失或模糊。 |
| <b>垃圾搖滾量</b> <i>0.0 - 1.0</i> | 這樣可以設定纖維效果要在邊緣間融合多少。 把它和磨損程度一起調整，以獲得最大控制。 |
| <b>環境遮蔽</b> <i>0.0 - 1.0</i> | 設定 AO 對隱藏效果的影響幅度。 |
| <b>曲率權重</b> <i>0.0 - 1.0</i> | 曲率凸邊的影響量。 |
| <b>使用自訂垃圾搖滾</b> <i>錯誤/真實</i> | 用自訂地圖覆蓋內建光纖。 |
| <b>使用三平面</b> <i>錯誤/真實</i> | 使 [三平面](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/utilities-mesh-based-gen/tri-planar/tri-planar.md) 能隱藏接縫。 |
| <b>三面融合對比</b> <i>0.0 - 1.0</i> | 控制三平面效應的對比度。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="fiber-glass-edge-wear.resources/fiber-glass-edge-wear-ex.gif" />
        </td>
    </tr>
</table>
