---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/exposure-preview.html"
breadcrumb-title: ''
description: 使用曝光預覽節點，在最終渲染前預覽 HDRI 環境中的曝光調整。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Exposure Preview
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 曝光預覽
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9aaf135d4c336ea0cff865524ad1ccd5dcc225bd
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 7%

---


# 曝光預覽

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](exposure-preview.resources/hdr-exposure-preview.png){width="200px"}

<b>收錄於：</b> HDRI 工具> 3D 視圖

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

輔助節點用來預覽曝光步驟。 使用者設定最小值與最大值，節點會產生更大且多張原始輸入不同曝光版本的影像。 不同版本總是水平堆疊，數量取決於節點或圖的解析度。

</td>
</tr>
</table>

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>最大曝光（EV）</b> <i>-8.0 - 8.0</i> | 最上面最亮影像的最大曝光。 |
| <b>最小曝光（EV）</b> <i>-8.0 - 8.0</i> | 底部最暗的影像曝光最低。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="exposure-preview.resources/exp-preview-ex.png" />
        </td>
    </tr>
</table>
