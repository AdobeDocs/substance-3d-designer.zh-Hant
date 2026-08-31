---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill-mapper.html"
breadcrumb-title: ''
description: 使用 Flood Fill Mapper 節點，利用泛洪填充演算法來映射相連區域的值，進行貼圖處理。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill Mapper
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 洪水填埋地圖儀
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '666'
ht-degree: 6%

---


# 洪水填埋地圖儀

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](flood-fill-mapper.resources/flood-fill-mapper-01.png)![](flood-fill-mapper.resources/flood-fill-mapper-02.png)

<b>收錄於：</b> 濾鏡>效應

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

洪水填充映射器允許將現有的圖案或紋理重新映射到洪水填充[&#128279;](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md)的[&#128279;](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md)每個單元上。它和其他洪水填充轉換軟體不同，比如 [隨機灰階](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-random-gra/flood-fill-to-random-grayscale.md) 或 [漸層](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-to-gradient/flood-fill-to-gradient.md) ，因為它不會產生純色或數值，而是允許你使用自己的輸入貼圖。 它可以被視為洪水填充與[圖塊取樣器](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md)或[形狀映射器的](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-mapper/shape-mapper.md)結合，因為它提供了相當多相似的控制與介面。

彩色版本有額外控制項可搭配法線貼圖 [，能補償切線空間 Normap 的旋轉](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-vector-rotation/normal-vector-rotation.md)。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>洪水填充 Bbox</b> <i>色彩輸入</i> | 標準洪水填補輸入，需輸入。 |
| <b>模式輸入 1-8</b> <i>灰階/彩色輸入</i> | 自訂圖案影像輸入。 |
| <b>分布圖</b> <i>灰階輸入</i> | ID Map 用來判斷哪個圖案會連接到哪個儲存格。 也可以來自其他洪水填水地圖，例如洪水填水到索引。 |
| <b>比例尺地圖</b> <i>灰階輸入</i> | 地圖以決定每個細胞的比例。 |
| <b>旋轉地圖</b> <i>灰階輸入</i> | 映射以決定每個細胞的旋轉。 |
| <b>亮度偏移圖</b> <i>灰階輸入</i> | 映射以設定每個格子的亮度 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>平鋪模式</b> <i>無鋪磚，H+V</i> | 設定是否使用磁磚。 只有當 Size 或 Scale AR 設定低於 1 時才會顯示。 |
| <b>模式</b> |  |
| <b>模式輸入編號</b> <i>1 - 8</i> | 設定使用數量的自訂模式輸入。 |
| <b>模式分配模式</b> <i>隨機、形狀大小、分布圖輸入</i> | 設定方法來判斷格子中顯示的圖案。 |
| <b>模式分布抖動</b> <i>0.0 - 1.0</i> | 允許圖案分布有輕微變化或偏移，且不會透過隨機種子改變所有內容。 |
| <b>規模</b> |  |
| <b>尺寸模式</b> <i>相對於質地、相對於形狀 BSphere、相對於最大形狀、相對於最小形狀，Fit 形狀 BBox</i> | 設定每個格子中圖案大小的決定方式。 |
| <b>規模</b> <i>0.0 - 1.0</i> | 允許模式的非均勻縮放。 |
| <b>規模</b> <i>0.0 - 1.0</i> | 設定效果的全域（均勻）比例。 |
| <b>比例尺地圖多重器</b> <i>0.0 - 1.0</i> | 設定可選縮尺地圖的影響。 |
| <b>量表隨機</b> <i>-1.0 - 1.0</i> | 設定圖案尺度內的隨機變化量。 |
| <b>旋轉</b> |  |
| <b>旋轉</b> <i>0.0 - 1.0</i> | 為每個格子設定全域且均勻的旋轉。 |
| <b>旋轉地圖多重接管</b> <i>0.0 - 1.0</i> | 設定可選旋轉地圖的影響。 |
| <b>旋轉隨機</b> <i>0.0 - 1.0</i> | 設定每個格子的隨機旋轉量。 |
| <b>旋轉自動比例</b> <i>錯誤/真實</i> | 設定圖案旋轉時是否應該調整縮放以符合格子內。 |
| <b>職位</b> |  |
| <b>位置偏移</b> <i>0.0 - 1.0</i> | 為每個儲存格設定全域位置偏移。 |
| <b>位置偏移對齊</b> <i>紋理、圖案</i> | 設定為將偏移 0 點對齊到圖案格子或貼圖。 |
| <b>位置偏移隨機</b> <i>0.0 - 1.0</i> | 設定每個格子的位置偏移隨機化數量。 |
| <b>彩色（僅限灰階版本）</b> |  |
| <b>亮度範圍</b> <i>0.0 - 1.0</i> | 設定貼圖的全域對比度，0 變成中間灰色。 |
| <b>亮度範圍隨機</b> <i>0.0 - 1.0</i> | 設定亮度範圍的隨機化程度。 |
| <b>亮度偏移</b> <i>-1.0 - 1.0</i> | 設定亮度的偏移，作為亮度控制。 |
| <b>亮度偏移隨機</b> <i>0.0 - 1.0</i> | 設定亮度偏移的隨機化量。 |
| <b>亮度偏移貼圖多重映射器</b> <i>0.0 - 1.0</i> | 設定可選亮度偏移貼圖的影響。 |
| <b>背景色</b> <i>（灰階）</i> | 將背景色設定在被混合的材質上。 |
| <b>彩色（僅限彩色版本）</b> |  |
| <b>是法線貼圖</b> <i>錯誤/真實</i> | 設定為將圖案輸入解讀為法線貼圖。 將補償並修正法線切線空間旋轉。 |
| <b>一般格式</b> <i>DirectX、OpenGL</i> | 切換不同的法線貼圖格式（反轉綠色通道）。 只有當 的法線貼圖為真時才會啟動。 |
| <b>HSL 調整</b> <i>-1.0 - 1.0</i> | 全球調整HSL。 |
| <b>HSL 隨機</b> <i>-1.0 - 1.0</i> | 設定每個細胞的HSL隨機化。 |
| <b>阿爾法調整</b> <i>-1.0 - 1.0</i> | 設定全域 Alpha 調整，降低 Alpha 對比度。 |
| <b>阿爾法隨機</b> <i>-1.0 - 1.0</i> | 設定每個細胞的 Alpha 調整隨機化。 |
| <b>背景色</b> <i>（色彩值）</i> | 將背景色設定在被混合的材質上。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="flood-fill-mapper.resources/flood-fill-mapper-03.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="flood-fill-mapper.resources/flood-fill-mapper-04.jpg" />
        </td>
    </tr>
</table>
