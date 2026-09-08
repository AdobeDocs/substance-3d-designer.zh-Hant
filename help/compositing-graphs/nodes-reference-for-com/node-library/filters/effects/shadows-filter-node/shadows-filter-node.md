---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/shadows-filter-node.html"
breadcrumb-title: ''
description: 使用陰影濾鏡節點從輸入材質產生陰影效果，為材質增添深度與真實感。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Shadows (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 陰影（濾波節點）
user-guide-description: ''
user-guide-title: ''
source-git-commit: a4ccdbff5343e3ece0312bd9b3318fb236f07308
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 8%

---


# 陰影（濾波節點）

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/shadows-1.png){width="128px"}

<b>收錄於：</b> 濾鏡>效應

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

一個純灰階的 [Shape Drop Shadow](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/shape-drop-shadow/shape-drop-shadow.md) 節點版本。 它只接收黑白二進位圖形作為輸入，且只回傳陰影。

如果你只想做陰影，不想用更完整的節點，例如自己建置材質或烘焙光照時，這會很有用。

</td>
</tr>
</table>

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>影子距離</b> <i>0.0 - 1.0</i> | 控制影子應該落下的距離。 |
| <b>光線角度</b> <i>0.0 - 1.0</i> | 控制光的入射角。 |
| <b>邊緣 柔和</b> <i>0.0 - 1.0</i> | 決定陰影邊緣的硬度或軟度。 |
| <b>取樣</b> <i>1 - 16</i> | 為邊緣柔和度設定品質。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/shadow-ex.png" />
        </td>
    </tr>
</table>
