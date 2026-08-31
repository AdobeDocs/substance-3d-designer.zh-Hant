---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/caustics.html"
breadcrumb-title: ''
description: 利用焦散節點生成腐蝕光模式，創造水下和折射光效效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Caustics
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 焦散
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 5%

---


# 焦散

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](caustics.resources/caustics-01.png){width="128px"}

<b>收錄於：</b> 貼圖產生器>噪音

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

根據高度圖和光線方向產生投影焦散。有灰階和彩色兩種版本，差異很細微，但彩色版本會加入色彩散射效果。 光線是從單一點投射，沒有使用環境貼圖。

</td>
</tr>
</table>

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>輸出色彩空間</b> <i>Raw，sRGB</i> | 設定輸出色彩空間。 |
| <b>光子網格尺寸</b> <i>自動、512、1024、2048、4096</i> | 透過調整格線大小來設定品質，但預設是匹配輸入。 可以用來加快計算速度。 |
| <b>地表高度尺度</b> <i>0.0 - 1.0</i> | 乘數來決定高度的解讀方式。 |
| <b>地面高度位置</b> <i>0.0 - 1.0</i> | 設定折射面與投影的距離。 |
| <b>表面 IOR</b> <i>1.0 - 2.0</i> | 設定折射率，彩色版本會增加更多色散。 |
| <b>光子大小</b> <i>1.0 - 50.0</i> | 光子大小會影響效果的清晰度。 |
| <b>擴散</b> <i>0.0 - 0.01（僅彩色版本）</i> | 只影響色彩擴散。 當 IOR 低時看不到。 |
| <b>抖動</b> <i>0.0 - 1.0</i> | 在鑄造光子粒子中加入不規則抖動。 |
| <b>燈光位置</b> | 移動燈光位置。 也是用 2D 視角的裝置來完成的。 |
| <b>背景色</b> <i>（彩色值）（僅彩色版本）</i> | 改變背景顏色。 灰階版本僅限黑色。 |
| <b>非平方展開</b> <i>錯誤/真實</i> | 以非平方比率補償擠壓與拉伸。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="caustics.resources/caustics-02.png" />
        </td>
    </tr>
</table>
