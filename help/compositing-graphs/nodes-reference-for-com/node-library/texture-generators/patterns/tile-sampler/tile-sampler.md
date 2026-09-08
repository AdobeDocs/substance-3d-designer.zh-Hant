---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/tile-sampler.html"
breadcrumb-title: ''
description: 使用 Tile Sampler 節點從輸入貼圖中取樣並排列圖塊，在 Substance 3D Designer 中創造瓦片圖案。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Tile Sampler
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 瓷磚樣本
user-guide-description: ''
user-guide-title: ''
source-git-commit: 79916cdb133abb1a43d11012c9d23c3c6d27b079
workflow-type: tm+mt
source-wordcount: '1060'
ht-degree: 5%

---


# 瓷磚樣本

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/tile-sampler.png){width="128px"}

<b>收錄於：</b> 紋理產生器>圖案

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

Tile Sampler 是終極的圖塊圖案生成節點。 它是 Tile Generator[&#128279;](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md) 的進化版、更複雜的版本。截至 2017 2.1 版本，Tile Sampler 與 [Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md) 之間的差異大幅縮小。 主要差異現在只在七個不同的地圖槽位上，可用於駕駛縮放、位置、旋轉、大小、顏色和遮罩。 它們的效果可以分開混合。

Tile Sampler 適合建立人工程序式模式，並可額外控制由外部輸入映射驅動的特定參數。

在開始使用圖塊取樣器之前，務必熟悉 [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md) 。 大多數情況下，你會發現 [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md) 就足夠了，不需要 Tile Sampler 那麼複雜。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>模式輸入 1-6</b> <i>灰階輸入 / 色彩輸入</i> | 自訂圖案影像，當「圖案」參數設為「影像輸入」時使用。<br><br>可用輸入的數量由 <b>圖案輸入數</b> 參數決定。 |
| <b>比例尺地圖輸入</b> <i>灰階輸入</i> | 用灰階地圖來驅動圖塊縮放。 |
| <b>位移圖輸入</b> <i>灰階輸入</i> | 用灰階地圖來驅動地磚位移。 |
| <b>旋轉地圖輸入</b> <i>灰階輸入</i> | 灰階地圖來驅動地磚旋轉。 |
| <b>向量地圖輸入</b> <i>色彩輸入</i> | 色彩向量映射以驅動非均勻縮放。 |
| <b>色彩映射輸入</b> <i>灰階輸入 / 色彩輸入</i> | 地圖到驅動的每格染色。 |
| <b>遮罩映射輸入</b> <i>灰階輸入</i> | 面具槽用來隱藏特定格子。 |
| <b>模式分布地圖輸入</b> <i>灰階輸入</i> | 遮罩槽用於驅動多個自訂圖案輸入。 |
| <b>背景輸入</b> <i>灰階輸入 / 色彩輸入</i> | 可選背景圖片。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>X 金額</b> <i>0 - 64</i> | 圖案的X字重複次數。 |
| <b>Y 金額</b> <i>0 - 64</i> | 該模式的Y字重複次數。 |
| <b>非平方展開</b> <i>錯誤/真實</i> | 能以非平方比率補償擠壓與拉伸。 |
| <b>模式</b> |  |
| <b>模式</b> <i>圖案輸入、方形、圓盤、拋物面、鐘形、高斯分布、荊棘、金字塔、磚塊、漸變、波浪、半鐘、脊狀鐘、新月、膠囊、錐形</i> | 選擇要使用的圖案形狀。 |
| <b>模式輸入編號</b> <i>1 - 6</i> | 可以隨機挑選的自訂圖案數量。 |
| <b>模式輸入分布</b> <i>隨機、模式號碼、分布圖</i> | 設定如何選擇多個模式輸入。 隨機指隨機選出一個，圖案編號則是它們被放入循環序列中。 分布圖使用灰階地圖輸入來驅動擺放。 |
| <b>模式輸入濾波（Engine > v4）</b> <i>雙線性 + 多元映射、雙線性、最近</i> |  |
| <b>圖案專屬</b> <i>0.0 - 1.0</i> | 讓你可以改變所選圖案的形狀。 效果取決於所選的模式。 |
| <b>模式特定隨機</b> <i>0.0 - 1.0</i> | 隨機化效應取決於所選的模式。 |
| <b>旋轉</b> <i>0, 90, 180, 270</i> | 階梯旋轉（90度）。 |
| <b>旋轉隨機</b> <i>0.0 - 1.0</i> | 每格隨機自由旋轉。 |
| <b>對稱隨機</b> <i>0.0 - 1.0</i> | 根據以下行為，設定應該隨機翻轉/鏡像的方塊數量。 |
| <b>對稱隨機模式</b> <i>水平 + 垂直，水平，垂直</i> | 決定對稱性、鏡像行為。 |
| <b>規模</b> |  |
| <b>尺寸模式</b> <i>Normal、Keep Ratio、Absolute、Pixel</i> | 設定圖案大小的一般行為。<br><br>Normal 讓你可以定義圖案元素的大小。 它會受到 X 和 Y 的數量影響。<br><br>Keep Ratio 允許你設定受 X 和 Y 數量影響的大小，但兩者之間的 X 和 Y 比例保持不變。<br><br>絕對值讓你設定一個不會受 X 和 Y 影響的絕對大小。<br><br>像素可以設定絕對像素大小，不受 X 和 Y 數量影響。 改變解析度會影響元素的大小。 |
| <b>尺寸（絕對/像素）</b> <i>0.0 - 1.0</i> | 改變磚塊的非均勻比例。 具體行為取決於尺寸模式。 |
| <b>隨機大小</b> <i>0.0 - 1.0</i> | 每格隨機比例。 |
| <b>規模</b> <i>0.0 - 10.0</i> | 設定全域圖塊比例。 |
| <b>量表隨機</b> <i>0.0 - 1.0</i> | 每格的比例隨機化。 |
| <b>比例地圖倍數</b> <i>0.0 - 1.0</i> | 融合縮放貼圖的效果。 |
| <b>比例向量地圖乘法</b> <i>0.0 - 1.0</i> | 透過比例向量貼圖的效果進行混合，以驅動非均勻縮放。 |
| <b>尺度參數化影響</b> <i>X 和 Y，X，Y</i> | 集合，軸向，尺度參數化的影響。 可以用來讓縮放貼圖只影響元素的 X 或 Y。 |
| <b>職位</b> |  |
| <b>隨機位置</b> <i>0.0 - 10.0</i> | 會隨機化兩個軸上的方塊位置。 |
| <b>偏移</b> <i>0.0 - 1.0</i> | 根據偏移類型移動格子。 |
| <b>偏移型</b> <i>水平五度、垂直五度、水平全局、垂直全局</i> | 改變偏移的運作方向。 |
| <b>全球抵消</b> <i>0.0 - 1.0</i> | 全域偏移X軸或Y軸上的所有磚塊。 |
| <b>位移地圖強度</b> <i>0.0 - 1.0</i> | 在偏移量上混合 Displacement 貼圖的強度。 |
| <b>位移角</b> <i>0.0 - 1.0</i> | 設定位移的角度。 |
| <b>向量地圖位移</b> <i>0.0 - 1.0</i> | 使用向量貼圖來驅動位移和角度。 |
| <b>旋轉</b> |  |
| <b>旋轉</b> <i>0.0 - 1.0</i> | 全域旋轉所有格子。 |
| <b>旋轉隨機</b> <i>0.0 - 1.0</i> | 每格隨機旋轉。 |
| <b>旋轉映射乘數</b> <i>0.0 - 1.0</i> | 混合旋轉對每個圖塊旋轉的效果。 |
| <b>向量映射乘法</b> <i>0.0 - 1.0</i> | 使用 Vector Map 來驅動每格旋轉。 |
| <b>顏色</b> |  |
| <b>遮罩貼圖閾值</b> <i>0.0 - 1.0</i> | 遮罩地圖的閾值，何時開始隱藏圖塊。 |
| <b>遮罩貼圖反轉</b> <i>錯誤/真實</i> | 反轉遮罩地圖效果。 |
| <b>遮罩地圖取樣技術</b> <i>圖案中心，圖案邊界盒（較慢）</i> | 隱藏應該由單一點決定還是由邊界框決定。 避免了零散像素造成的奇怪效果。 |
| <b>面具隨機</b> <i>0.0 - 1.0</i> | 隨機遮罩，與遮罩貼圖平行運作。 |
| <b>反轉面罩</b> <i>錯誤/真實</i> | 反轉隨機遮蔽。 |
| <b>混合模式</b> <i>加/字幕、最大（磚塊取樣器）/ 加/字幕、alpha 混合（磚塊取樣器顏色）</i> | 混合模式，讓磚塊與背景及彼此相接。 |
| <b>顏色</b> <i>（灰階值）/（色彩值）</i> | 實心的全域圖塊顏色。 |
| <b>顏色/亮度隨機</b> <i>0.0 - 1.0</i> | 顏色隨機化，每格。 |
| <b>色彩參數化模式</b> <i>色彩輸入、比例、線索引、行索引、圖案索引（圖塊取樣器）/色彩映射、縮放、線索引、列索引、圖案索引、圖案中心位置、圖案中心位置（RG） B球大小（B）（圖塊取樣器顏色）</i> | 設定顏色隨機化的具體參數化方式。 |
| <b>色彩參數乘法</b> <i>0.0 - 1.0</i> | 融合上述參數化效果。 |
| <b>色彩參數化影響（僅限顏色）</b> <i>RGB+Alpha，僅RGB，僅Alpha</i> | 設定參數化如何影響顏色。 |
| <b>全域不透明度（僅限灰階）</b> <i>0.0 - 1.0</i> | 設定全域圖塊不透明度。 |
| <b>背景色</b> <i>（灰階值）/（色彩值）</i> | 設定純色背景色。 |
| <b>反向渲染順序</b> <i>錯誤/真實</i> | 反轉渲染順序，從後到前。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/tilesampler-ex2.png" /><br><i>範例說明參數如何由輸入映射（圖案分布、比例、旋轉）驅動。</i>
        </td>
    </tr>
</table>
