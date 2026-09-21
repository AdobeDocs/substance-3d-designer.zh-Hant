---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/voronoi.html"
breadcrumb-title: ""
description: 利用 Voronoi 節點產生 Voronoi 圖案，以創造細胞紋理和有機材料效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Voronoi
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 沃羅諾伊
user-guide-description: ""
user-guide-title: ""
source-git-commit: 0f214099ae94088d37122a5d474d3e70d4ccf46f
workflow-type: tm+mt
source-wordcount: '628'
ht-degree: 0%
---

# 沃羅諾伊

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](voronoi.resources/voronoi.png){width="200px"}

<b>收錄於：</b> 貼圖產生器>噪音

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

**Voronoi** 節點會產生一個 3D Voronoi 雜訊，並利用 *Z-down 正交投影*&#x200B;映射到二維影像。

此節點可以 [Cube GBuffers](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d-gbuffers/cube-3d-gbuffers.md) 作為輸入測試，而非實際烘焙的映射（如下方範例圖片所示）。

>[!WARNING]
>
> 這種雜訊僅用於 *GPU 引擎*（例如 **Direct**&#x200B;或 **OpenGL）。**&#x200B;到 **工具>切換引擎......** 或按 **F9** 鍵選擇想要的引擎。

</td>
</tr>
</table>

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>倒轉</b> <i>布林值</i> | 將輸出影像反轉。 |
| <b>規模</b> <i>浮標</i> | 控制 Voronoi 噪音的縮放。<br><br>*注意：當&#x200B;**在任何軸*上啟用&#x200B;*平鋪**&#x200B;時，縮放調整會是*&#x200B;階&#x200B;*梯式的。*&#x200B;這是預料之中的。 |
| <b>規模</b> <i>Float3</i> | 控制 Voronoi 在 X **、** Y **和** Z **軸上的**&#x200B;噪音大小。值不均勻會導致&#x200B;*拉伸或壓縮*&#x200B;效果。<br><br>*注意*：當&#x200B;**任一&#x200B;*軸啟用*平鋪**&#x200B;時，尺寸調整會是&#x200B;*階*&#x200B;梯式的。這是預料之中的。 |
| <b>偏移</b> <i>Float3</i> | 對 X **、** Y **和** Z **軸上 Voronoi 雜訊**&#x200B;的位置&#x200B;*施加偏移*。 |
| <b>混亂</b> <i>Float3</i> | 隨機偏移的強度&#x200B;*，分別施加在X **軸、**&#x200B;Y **軸和**&#x200B;Z **軸的雜訊**&#x200B;點*&#x200B;上。 |
| <b>失真強度</b> <i>浮標</i> | 控制施加在沃羅諾伊噪音上的變形效果&#x200B;*強度*。 |
| <b>失真尺度倍增器</b> <i>浮標</i> | 控制扭曲效果中變形圖案&#x200B;*的尺度*，由變形強度&#x200B;**控制**。 |
| <b>圓弧</b> <i>浮標</i> | 在雜訊的每個點周圍將 *斜率* 四捨五入，使其 *凸*&#x200B;起。<br><br>*注意*：當 **Style** 參數設為 *Edge* 時，此參數無法使用。 |
| <b>距離尺度</b> <i>浮標</i> | 調整 *噪音點周圍梯度* 的距離。 |
| <b>距離模式</b> <i>整數</i> | 設定計算雜訊中每個點距離梯度的方法：- 歐幾里得&#x200B;*<br>-*&#x200B;曼哈頓&#x200B;*<br>-*&#x200B;切比雪夫&#x200B;*<br>-*&#x200B;明可夫斯基 *<br><br>*** |
| <b>明可夫斯基數</b> <i>浮標</i> | 閔可夫斯基距離的階數 *p* 。 若將距離梯度分為象限，此數值對象限的影響如下：<br><br>- p 為&#x200B;** 1：直線<br> - p *小*&#x200B;於 1：凹<br> p *大於* 1：<br><br>凸 有趣值：<br><br>- *1.0*：曼哈頓距離<br> - *2.0*：歐幾里得距離<br> - *無限*：切比雪夫距離&#x200B;<br><br>*注意*：此參數僅在距離&#x200B;**模式**&#x200B;參數設為&#x200B;*明可夫斯基*。 |
| <b>風格</b> <i>整數</i> | 設定 Voronoi 雜訊資料的渲染方法，考慮雜訊基於空間中的一組點：<br><br>- *F1*：距離&#x200B;*空間中最近點<br>*&#x200B;的距離 - *F2*：距離&#x200B;*空間中第二近點*<br>的距離 - *F2-F1*<br>- *F1\* F2 *<br>-* F1/F2 *<br>-*&#x200B;邊&#x200B;*：*&#x200B;空間<br>中雜訊各格&#x200B;*子之間的邊-*&#x200B;隨機顏色&#x200B;*：**為空間中每個噪聲格指派一個*&#x200B;隨機的平面色* |
| <b>邊緣厚度</b> <i>浮標</i> | 調整偵測到 Voronoi 雜訊單元間邊緣厚度。 邊是在 X、Y 和 Z 軸偵測，因此根據格子&#x200B;*的深度*，某些厚度可能增長得更快。<br><br>*注意*：此參數僅在 Style **&#x200B;**&#x200B;參數設為 *Edge（邊緣*）時可用。 |
| <b>隨機色彩種子模式</b> <i>整數</i> | 設定每個格子顏色選擇的隨機種子獲取方法&#x200B;*：- 全域隨機種子*：使用節點<br>繼承&#x200B;*的種子*- *手動種子*：使用&#x200B;*離散*&#x200B;種子&#x200B;<br><br>*注意*：此參數僅在風格&#x200B;**&#x200B;**&#x200B;參數設為&#x200B;*隨機顏色*&#x200B;時可用。 *<br><br>* |
| <b>隨機色彩種子</b> <i>整數</i> | 每個格子顏色選擇應使用的離散隨機種子。<br><br>*注意*：此參數僅在風格&#x200B;**&#x200B;**&#x200B;參數設為&#x200B;*隨機色彩*&#x200B;且&#x200B;**隨機色彩種子模式**&#x200B;參數設為&#x200B;***手動種子***&#x200B;時可用。 |
| <b>非平方展開</b> <i>布林值</i> | 能以非平方比率補償擠壓與拉伸。 |

## 範例

<table style="table-layout:fixed">
    <tr style="border: 0;">
        <td style="border: 0;">
            <img src="voronoi.resources/voronoi-variant2.jpg" class="modal-image" alt="沃羅諾伊 - 範例1" />
        </td>
        <td style="border: 0;">
            <img src="voronoi.resources/voronoi-variant3.jpg" class="modal-image" alt="沃羅諾伊 - 範例 2" />
        </td>
        <td style="border: 0;">
            <img src="voronoi.resources/voronoi-variant5.jpg" class="modal-image" alt="Voronoi - 範例 3" />
        </td>
    </tr>
    <tr style="border: 0;">
        <td style="border: 0;">
            <img src="voronoi.resources/voronoi-variant.jpg" class="modal-image" alt="Voronoi - 範例 4" />
        </td>
        <td style="border: 0;">
            <img src="voronoi.resources/voronoi-variant4.jpg" class="modal-image" alt="Voronoi - 範例 5" />
        </td>
        <td style="border: 0;">
            <img src="voronoi.resources/voronoi-variant6.jpg" class="modal-image" alt="Voronoi - 範例 6" />
        </td>
    </tr>
</table>
