---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/physical-sun-sky.html"
breadcrumb-title: ''
description: 使用 Physical SunSky 節點生成物理精確的太陽與天空照明環境，提供逼真的材質預覽。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Physical SunSky
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 實體 SunSky
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 9%

---


# 物理太陽/天空

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](physical-sun-sky.resources/physical-sun-sky-01.png){width="200px"}

<b>收錄於：</b> HDRI 工具> 3D 視圖

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

基於 Hosek-Wikie 天窗模型的實體太陽與天空實作。 為人工 HDRI 提供了極佳的基礎。

</td>
</tr>
</table>

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>太陽位置</b> | 距離 = [0,1]x[0,1]（經緯角） |
| <b>濁度</b> <i>1.0 - 10.0</i> | 混濁度範圍為1到10 |
| <b>阿貝多</b> <i>0.0 - 1.0</i> | 阿貝多的範圍從0到1。 |
| <b>底色</b> <i>（色彩值）</i> | 地面平面的顏色。 |
| <b>曝光（EV）</b> <i>-1.0 - 4.0</i> | 結果輸出的曝光值。 |
| <b>太陽大小</b> <i>0.0 - 4.0</i> | 太陽的比例尺，任何與1不同的數值都是物理上不正確的。 價值有微妙的影響！ |
| <b>太陽強度</b> <i>0.0 - 1.0</i> | 太陽盤的強度。 太陽盤相當小，因此效應不會立刻顯現。 |
| <b>天空強度</b> <i>0.0 - 1.0</i> | 天空的強度。 也會影響天空中太陽的耀眼，而不是光碟本身。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="physical-sun-sky.resources/physical-sun-sky-02.gif" />
        </td>
    </tr>
</table>
