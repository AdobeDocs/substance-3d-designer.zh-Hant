---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-perlin-noise-fractal.html"
breadcrumb-title: ''
description: 使用 3D Perlin Noise 分形節點在 3D 空間中產生分形 Perlin 噪音圖案，以創造細緻的體積紋理。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Perlin Noise Fractal
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D Perlin 雜訊分形
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 0%

---


# 3D Perlin 雜訊分形

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-perlin-noise-fractal.resources/3d-perlin-noise-fractal-01.png){width="200px"}

<b>收錄於：</b> 貼圖產生器>噪音

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

<b>3D Perlin 噪聲分形</b>節點根據<i>位置圖</b>輸入在三維空間<b>中產生分形</i> Perlin 噪聲。

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
| <b>規模</b> <i>浮標</i> | 控制分形3D佩林雜訊的比例。 |
| <b>規模</b> <i>Float3</i> | 控制 X</b>、<b>Y</b> 和 <b>Z</b> 軸分<b>形 3D Perlin 雜訊的大小。不均勻的數值會導致 <i>拉伸或壓縮</i> 效果。 |
| <b>偏移</b> <i>Float3</i> | 對分形三維Perlin雜訊在X</b>、<b>Y</b>和<b>Z</b>軸的位置施加偏移<i></i>。<b> |
| <b>失真強度</b> <i>浮標</i> | 控制對分形三維Perlin雜訊施加的扭曲效應</i>強度<i>。 |
| <b>失真尺度倍增器</b> <i>浮標</i> | 控制扭曲效果中變形圖案</i>的尺度<i>，由變形強度</b>控制<b>。 |
| <b>最低水準</b> <i>整數</i> | 分形圖案中使用的最低 <i>重複</i> 程度。 更寬的最小/最大範圍會產生 <i>更豐富的圖案</i> ，並在更多頻率範圍內變化。 |
| <b>最高等級</b> <i>整數</i> | 分形圖案中使用的最大 <i>重複</i> 程度。 更寬的最小/最大範圍會產生 <i>更豐富的圖案</i> ，並在更多頻率範圍內變化。 |
| <b>粗糙度</b> <i>浮標</i> | 控制<i>分形圖案中低與高<i>重複</i>的平衡</i>。<br><br><i>注意</i>：值為 <b>0</b> 會產生與其他低值不一致</i>的輸出<i>。這是預料之中的。 |
| <b>缺口</b> <i>浮標</i> | 控制施加的分形圖案 <i>如何填滿空間</i>。 <i>較高</i>的數值會導致<i>圖案間隙</i>較少，噪音<i>密度也更</i>高。 |
| <b>全域不透明度</b> <i>浮標</i> | 控制<i>分形三維Perlin雜訊值<i>在</i><b>基準值</b>附近的範圍</i>。 |
| <b>基線</b> <i>浮標</i> | 對3D Perlin雜訊值分布的基準亮度</i>值施加<i>偏移</i>。<i> |
| <b>對比</b> <i>浮標</i> | 調整 3D Perlin 雜訊的對比度。 |
| <b>絕對</b> <i>布林值</i> | 在 3D Perlin 雜訊中使用絕對值。 這實際上<i>是</i>反轉低於0.5</i>值<i>的值分布。 |
| <b>啟用平鋪</b> <i>布林值</i> | 調整 3D Perlin 雜訊，使其產生的圖案 <i>在 X、Y 和 Z 軸上重複</i> 出現。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-perlin-noise-fractal.resources/3d-perlin-noise-fractal-02.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-perlin-noise-fractal.resources/3d-perlin-noise-fractal-03.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-perlin-noise-fractal.resources/3d-perlin-noise-fractal-04.jpg" />
        </td>
    </tr>
</table>
