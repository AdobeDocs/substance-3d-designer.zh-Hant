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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '740'
ht-degree: 0%

---


# 3D 沃羅諾伊分形

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/3dvoronoifractal.png){width="200px"}

**收錄於：***材質產生器**/噪音*

**中級**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## 說明

**3D Voronoi 分形**&#x200B;節點根據&#x200B;*位置圖&#x200B;**輸入在三維空間**中產生分形* Voronoi 雜訊。

此節點可用 Cube 3D GBuffers](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d-gbuffers/cube-3d-gbuffers.md) 作為輸入，取代實際烘焙的貼圖（如下方範例圖片所示）進行測試[。

>[!WARNING]
>
> 這種雜訊僅用於 *GPU 引擎*（例如 **Direct3D** 或 **OpenGL）。**&#x200B;到 **工具>切換引擎......** 或按 **F9** 鍵選擇想要的引擎。

</td>
</tr>
</table>

## 參數

* **反布***林*\
  將輸出影像反轉。
* **比例***浮球*\
  控制分形3D沃羅諾伊噪音的比例。\
  *注意*：當&#x200B;**任一&#x200B;*軸啟用*平鋪**&#x200B;時，縮放調整會被&#x200B;*階梯調整*。這是預料之中的。
* **尺寸** *Float3*\
  控制分形 3D Voronoi 雜訊在 **X**、 **Y** 和 **Z** 軸的大小。 不均勻的數值會導致 *拉伸或壓縮* 效果。\
  *注意*：當&#x200B;**任一&#x200B;*軸啟用*平鋪**&#x200B;時，大小調整會是&#x200B;*階*&#x200B;梯式的。這是預料之中的。
* **偏移** *Float3*\
  對分形三維 Voronoi 雜訊在 X **、** Y **和** Z **軸的位置施加偏移&#x200B;**。**
* **混亂** *Float3*\
  隨機偏移的強度&#x200B;*，分別施加在X **軸、**Y **軸和**Z **軸的雜訊**點*&#x200B;上。
* **失真強度***浮球*\
  控制對分形3D沃羅諾伊雜訊施加的扭曲效果&#x200B;*強度*。
* **失真尺度乘法***浮點*\
  控制扭曲效果中變形圖案&#x200B;*的尺度*，由變形強度&#x200B;**控制**。
* **最小整數層***級*\
  分形圖案中使用的最低 *重複* 程度。 更寬的最小/最大範圍會產生 *更豐富的圖案* ，並在更多頻率範圍內變化。
* **最大層級***整數*\
  分形圖案中使用的最大 *重複* 程度。 更寬的最小/最大範圍會產生 *更豐富的圖案* ，並在更多頻率範圍內變化。
* **粗糙漂***浮*\
  控制&#x200B;*分形圖案中低與高*&#x200B;重複&#x200B;*的平衡*。\
  *注意*：值為 **0** 的輸出 *與後續低值不一致* 。 這是預料之中的。\
  *註 2*：此參數僅在混合 **模式** 參數設為 *Add* 時可用。
* **Lacunarity** *花車*\
  控制施加的分形圖案 *如何填滿空間*。 *較高*&#x200B;的數值會導致&#x200B;*圖案間隙*&#x200B;較少，噪音&#x200B;*密度也更*&#x200B;高。
* **全域不透明度***浮點*\
  控制 *分形三維Perlin噪聲值的範圍* ，範圍從0開始。
* **圓弧浮***球*\
  繞&#x200B;*過噪音的每個點，使斜*&#x200B;率&#x200B;*呈現*&#x200B;凸面。\
  *注意*：當 **Style** 參數設為 *Edge* 時，此參數無法使用。
* **距離刻度***浮點*\
  調整 *噪音點周圍梯度* 的距離。
* **距離模式***整數*\
  設定計算雜訊中每一點周圍距離梯度&#x200B;*的方法*：
  * *歐幾里得*
  * *曼哈頓*
  * *切比雪夫*
  * *明可夫斯基*
* **明可夫斯基數字***花車*\
  閔可夫斯基距離的階數 *p* 。 若將距離梯度劃分為象限，該數值對這些象限的影響如下：
  * p 恰好&#x200B;*是* 1：直線
  * p 小&#x200B;**&#x200B;於 1：凹面
  * p 大&#x200B;**&#x200B;於 1：凸\
    有趣的價值觀：\
    *- 1.0*：曼哈頓距離\
    *- 2.0*：歐幾里得距離\
    *- 無限大*：切比雪夫距離\
    *注意*：此參數僅在距離 **模式** 參數設為 *Minkowski* 時可用。
* **混合模式***整數*\
  設定了將三維空間中重疊格&#x200B;*子值*&#x200B;混合的方法：
  * *加*&#x200B;法：將數值相加
  * *Max*：保留 *最高* 價值
  * *最小*&#x200B;值：保留 *最低* 值
* **風格***整數*&#x200B;設定&#x200B;*渲染分形三維沃羅諾伊雜訊資料*&#x200B;的方法，考慮雜訊基於三維空間中的一組點：
  * *F1*：三維空間中距離最近點&#x200B;*的*&#x200B;距離
  * *F2*：三維空間中第二接近點&#x200B;*的*&#x200B;距離
  * *F2-F1*- *F1\* F2 *-* F1/F2 *-*&#x200B;邊緣&#x200B;*：*&#x200B;三維空間中雜訊各單元* 之間的邊
  * *隨機顏色*：為三維空間中每個噪聲單元指派一個&#x200B;*隨機的平面色*
* **邊緣厚度***浮動*&#x200B;調整分形3D Voronoi雜訊單元間邊緣的厚度。邊緣在 X、Y 和 Z 軸上被偵測，因此根據細胞 *深度*&#x200B;不同，某些厚度可能增長得更快。\
  *注意*：此參數僅在 Style **參數設為 *Edge* 時可用**。
* **啟用平鋪布***林*\
  調整分形 3D Voronoi 雜訊，使其產生的圖案 *在 X、Y 和 Z 軸重複* 出現。

## 範例圖片

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dvoronoifractal-variant6.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dvoronoifractal-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dvoronoifractal-variant4.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dvoronoifractal-variant5.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dvoronoifractal-variant.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dvoronoifractal-variant3.jpg){width="256px"}

</td>
</tr>
</table>
