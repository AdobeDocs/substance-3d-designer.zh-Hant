---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/bottom-to-top.html"
breadcrumb-title: ''
description: 使用「從底到頂」節點，根據網格世界位置產生從底部到頂部的漸層遮罩。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Bottom To Top
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 從底部到頂部
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2c331b568074714ea71231410f997f965e2bcdaa
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 4%

---


# 從底部到頂部

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](bottom-to-top.resources/bottom-to-top.png){width="128px"}

<b>收錄於：</b> 基於網格的生成器>遮罩生成器

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

根據烘焙的地圖和使用者設定產生黑白遮罩。 類似 [Painter](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/home) 裡[的智慧口罩](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/features/smart-materials-and-masks)。

這會產生從模型底部到頂部的白轉黑過渡，對於基於幾何的衰減與選擇非常有用。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>職位</b> <i>色彩輸入</i> | 烘焙位置地圖。 必備！ |
| <b>粗糙度</b> <i>灰階輸入</i> | 這跟 PBR 粗糙度無關，只是用來打斷過渡的（可選）變化地圖。 只有當粗糙度設定高於0時才會出現。 |
| <b>面具（選用）</b> <i>灰階輸入</i> | 遮罩槽用於遮蔽節點的效果。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>關卡</b> <i>0.0 - 1.0</i> | 它會像調整亮度一樣，將結果的平均亮度在黑白之間切換。 |
| <b>對比</b> <i>0.0 - 1.0</i> | 調整過渡的對比度。 |
| <b>Roughness_Variation</b> <i>0.0 - 1.0</i> | 決定要在粗糙度貼圖中融合多少以增加變化。 將這個值增加到 0 就會顯示地圖欄位。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="bottom-to-top.resources/bottom-to-top-ex.gif" />
        </td>
    </tr>
</table>
