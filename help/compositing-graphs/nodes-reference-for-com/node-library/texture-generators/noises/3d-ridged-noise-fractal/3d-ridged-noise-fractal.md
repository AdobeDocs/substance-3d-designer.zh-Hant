---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-ridged-noise-fractal.html"
breadcrumb-title: ''
description: 使用 3D Ridged Noise 分形節點，在 3D 空間中產生 Ridged 分形噪音圖案，創造山脈紋理。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Ridged Noise Fractal
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D 有脊狀雜訊分形
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 0%

---


# 3D 有脊狀雜訊分形

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-ridged-noise-fractal.resources/3d-ridged-noise-fractal-01.png){width="200px"}

<b>收錄於：</b> 貼圖產生器>噪音

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

<b>3D Ridged Noise 分形</b>節點根據<i>位置圖</b>輸入在 3D 空間<b>中產生分形</i> Ridged 噪聲。

此節點可用 Cube 3D GBuffers[&#128279;](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d-gbuffers/cube-3d-gbuffers.md) 作為輸入，取代實際烘焙的貼圖（如下方範例圖片所示）進行測試。

</td>
</tr>
</table>

>[!WARNING]
>
> 這種雜訊僅用於 <i>GPU 引擎</i>（例如 <b>Direct3D</b> 或 <b>OpenGL）。</b>到 <b>工具>切換引擎......</b> 或按 <b>F9</b> 鍵選擇想要的引擎。

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>倒轉</b> <i>布林值</i> | 將輸出影像反轉。 |
| <b>規模</b> <i>浮標</i> | 控制分形3D脊狀雜訊的比例。 |
| <b>規模</b> <i>Float3</i> | 控制 X</b>、<b>Y</b> 和 <b>Z</b> 軸中<b>分形 3D Ridged 雜訊的大小。不均勻的數值會導致 <i>拉伸或壓縮</i> 效果。 |
| <b>偏移</b> <i>Float3</i> | 對分形三維脊狀雜訊在 X</b>、<b>Y</b> 和 <b>Z</b> 軸的位置施加偏移<i></i>。<b> |
| <b>失真強度</b> <i>浮標</i> | 控制 <i>對分形3D有脊聲所施加的扭曲效果</i> 強度。 |
| <b>失真尺度倍增器</b> <i>浮標</i> | 控制扭曲效果中變形圖案</i>的尺度<i>，由變形強度</b>控制<b>。 |
| <b>最低水準</b> <i>整數</i> | 分形圖案中使用的最低 <i>重複</i> 程度。 更寬的最小/最大範圍會產生 <i>更豐富的圖案</i> ，並在更多頻率範圍內變化。 |
| <b>最高等級</b> <i>整數</i> | 分形圖案中使用的最大 <i>重複</i> 程度。 更寬的最小/最大範圍會產生 <i>更豐富的圖案</i> ，並在更多頻率範圍內變化。 |
| <b>粗糙度</b> <i>浮標</i> | 控制<i>分形圖案中低與高<i>重複</i>的平衡</i>。<br><br><i>注意</i>：值為 <b>0</b> 會產生與其他低值不一致</i>的輸出<i>。這是預料之中的。 |
| <b>缺口</b> <i>浮標</i> | 控制施加的分形圖案 <i>如何填滿空間</i>。 <i>較高</i>的數值會導致<i>圖案間隙</i>較少，噪音<i>密度也更</i>高。 |
| <b>全域不透明度</b> <i>浮標</i> | 控制<i>分形 3D Ridged 雜訊值<i>在</i><b>基準值</b>附近的範圍</i>。 |
| <b>基線</b> <i>浮標</i> | 對3D脊狀雜訊分布的基準亮度值施加<i>偏移</i>。</i> <i> |
| <b>對比</b> <i>浮標</i> | 調整 3D Ridged 雜訊的對比度。 |
| <b>啟用平鋪</b> <i>布林值</i> | 調整 3D Ridged 雜訊，使其產生的圖案 <i>在 X、Y 和 Z 軸上重複</i> 出現。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-ridged-noise-fractal.resources/3d-ridged-noise-fractal-02.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-ridged-noise-fractal.resources/3d-ridged-noise-fractal-03.jpg" />
        </td>
    </tr>
</table>
