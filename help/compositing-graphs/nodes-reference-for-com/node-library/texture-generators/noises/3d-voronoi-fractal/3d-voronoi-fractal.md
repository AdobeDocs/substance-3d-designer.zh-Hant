---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-voronoi-fractal.html"
breadcrumb-title: ''
description: 使用 3D Voronoi 分形節點，根據 3D 位置產生分形 Voronoi 圖案，用於體積紋理。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Voronoi Fractal
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D 沃羅諾伊分形
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '733'
ht-degree: 0%

---


# 3D 沃羅諾伊分形

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-voronoi-fractal.resources/3dvoronoifractal.png){width="200px"}

<b>收錄於：</b> 貼圖產生器>噪音

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

<b>3D Voronoi 分形</b>節點根據<i>位置圖</b>輸入在三維空間<b>中產生分形</i> Voronoi 雜訊。

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
| <b>規模</b> <i>浮標</i> | 控制分形 3D Voronoi 雜訊的縮放。<br><br><i>注意：當<b>任一</i>軸啟用<i>平鋪</b>時，縮放調整會逐步<i>調整</i></i>。這是預料之中的。 |
| <b>規模</b> <i>Float3</i> | 控制分形 3D Voronoi 雜訊在 <b>X</b>、 <b>Y</b> 和 <b>Z</b> 軸的大小。 值不均勻會導致<i>拉伸或壓縮</i>效果。<br><br><i>注意</i>：當<b>任一</i>軸啟用<i>平鋪</b>時，尺寸調整會是<i>階</i>梯式的。這是預料之中的。 |
| <b>偏移</b> <i>Float3</i> | 對分形三維 Voronoi 雜訊在 X</b>、<b>Y</b> 和 <b>Z</b> 軸的位置施加偏移<i></i>。<b> |
| <b>混亂</b> <i>Float3</i> | 隨機偏移的強度<i>，分別施加在X</b>軸、<b>Y</b>軸和<b>Z</b>軸的雜訊<b>點</i>上。 |
| <b>失真強度</b> <i>浮標</i> | 控制對分形3D沃羅諾伊雜訊施加的扭曲效果</i>強度<i>。 |
| <b>失真尺度倍增器</b> <i>浮標</i> | 控制扭曲效果中變形圖案</i>的尺度<i>，由變形強度</b>控制<b>。 |
| <b>最低水準</b> <i>整數</i> | 分形圖案中使用的最低 <i>重複</i> 程度。 更寬的最小/最大範圍會產生 <i>更豐富的圖案</i> ，並在更多頻率範圍內變化。 |
| <b>最高等級</b> <i>整數</i> | 分形圖案中使用的最大 <i>重複</i> 程度。 更寬的最小/最大範圍會產生 <i>更豐富的圖案</i> ，並在更多頻率範圍內變化。 |
| <b>粗糙度</b> <i>浮標</i> | 控制<i>分形圖案中低與高<i>重複</i>的平衡</i>。<br><br><i>注意</i>：值為 <b>0</b> 會產生與其他低值不一致</i>的輸出<i>。這是預料之中的。<br><br><i>註 2</i>：此參數僅在混合 <b>模式</b> 參數設為 <i>Add</i> 時可用。 |
| <b>缺口</b> <i>浮標</i> | 控制施加的分形圖案 <i>如何填滿空間</i>。 <i>較高</i>的數值會導致<i>圖案間隙</i>較少，噪音<i>密度也更</i>高。 |
| <b>全域不透明度</b> <i>浮標</i> | 控制 <i>分形三維Perlin噪聲值的範圍</i> ，範圍從0開始。 |
| <b>圓弧</b> <i>浮標</i> | 在雜訊的每個點周圍將 <i>斜率</i> 四捨五入，使其 <i>凸</i>起。<br><br><i>注意</i>：當 <b>Style</b> 參數設為 <i>Edge</i> 時，此參數無法使用。 |
| <b>距離尺度</b> <i>浮標</i> | 調整 <i>噪音點周圍梯度</i> 的距離。 |
| <b>距離模式</b> <i>整數</i> | 設定計算雜訊中每個點距離梯度的方法：- 歐幾里得</i><br>-<i>曼哈頓</i><br>-<i>切比雪夫</i><br>-<i>明可夫斯基 <i><br><br><i></i></i> |
| <b>明可夫斯基數</b> <i>浮標</i> | 閔可夫斯基距離的階數 <i>p</i> 。 若將距離梯度分為象限，此數值對象限的影響如下：<br><br>- p 為</i> <i>1：直線<br> - p <i>小</i>於 1：凹<br> p <i>大於</i> 1：<br><br>凸 有趣值：<br>- <i>1.0</i>：曼哈頓距離<br> - <i>2.0</i>：歐幾里得距離<br> - <i>無限</i>：切比雪夫距離<br><br><i>注意</i>：此參數僅在距離<b>模式</b>參數設為<i>明可夫斯基</i>。 |
| <b>混合模式</b> <i>整數</i> | 設定在三維空間中混合重疊格</i>子值<i>的方法：<br><br>- <i>加</i>法：將數值<br>相加- <i>最大</i>值：<i>保留最高</i>值<br>- <i>最小</i>值：保留<i>最低</i>值 |
| <b>風格</b> <i>整數</i> | 設定分形三維沃羅諾伊雜訊資料渲染方法<i>，考慮雜訊基於三維空間中的一組點：<br><br>- <i>F1</i>：三<i>維空間<br>中最近點</i>的距離 - <i>F2</i>：三<i>維空間<br>中第二近點</i>的距離 - <i>F2-F1</i><br>- <i>F1\*F2</i><br>- <i>F1/F2</i><br>- <i>邊</i>：<i>三維空間<br>中雜訊各單元</i>之間的邊- <i>隨機顏色</i>：</i> 在三維空間中，為雜訊的每個單元指派一個<i>隨機的平面色</i> |
| <b>邊緣厚度</b> <i>浮標</i> | 調整分形三維Voronoi雜訊單元間邊緣的厚度。 邊是在 X、Y 和 Z 軸偵測，因此根據格子<i>的深度</i>，某些厚度可能增長得更快。<br><br><i>注意</i>：此參數僅在 Style <b></b> 參數設為 <i>Edge（邊緣</i>）時可用。 |
| <b>啟用平鋪</b> <i>布林值</i> | 調整分形 3D Voronoi 雜訊，使其產生的圖案 <i>在 X、Y 和 Z 軸重複</i> 出現。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-voronoi-fractal.resources/3dvoronoifractal-variant6.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-voronoi-fractal.resources/3dvoronoifractal-variant2.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-voronoi-fractal.resources/3dvoronoifractal-variant4.jpg" />
        </td>
    </tr>
    <tr style="border: 0; background: transparent">
        <td style="border: 0; background: transparent">
            <img src="3d-voronoi-fractal.resources/3dvoronoifractal-variant5.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-voronoi-fractal.resources/3dvoronoifractal-variant.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-voronoi-fractal.resources/3dvoronoifractal-variant3.jpg" />
        </td>
    </tr>
</table>
