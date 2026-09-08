---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/hald-clut.html"
breadcrumb-title: ''
description: 使用 Hald CLUT 節點，使用 Hald CLUT 格式套用色彩查找表來進行調色與校正。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Hald CLUT
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 哈爾德·克魯特
user-guide-description: ''
user-guide-title: ''
source-git-commit: 029f702d9b6a4d0dfaa83a4ae8447c02f70be355
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 3%

---


# 哈爾德·克魯特

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/hald-clut.png){width="128px"}

<b>收錄於：</b> 篩選>調整

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

會對輸入影像套用 LUT。 LUT 必須是 Hald 格式，解析度為 4096\*4096。 更多資訊請參見 <http://www.quelsolaar.com/technology/clut.html> 。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>輸入</b> <i>色彩輸入</i> | 請想像要在哪裡套用 LUT。 |
| <b>LUT</b> <i>色彩輸入</i> | LUT輸入槽。 一定是 4096x4096。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>LUT 強度由 Alpha 分類</b> <i>錯誤/真實</i> | 定義 LUT 效果是否依 alpha 通道加權。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/content-hald-clut.jpg" />
        </td>
    </tr>
</table>
