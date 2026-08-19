---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-ridged-noise-fractal.html"
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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 0%

---


# 3D 有脊狀雜訊分形

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/3dridgednoisefractal.png){width="200px"}

**收錄於：***材質產生器**/噪音*

**中級**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## 說明

**3D Ridged Noise 分形**&#x200B;節點根據&#x200B;*位置圖&#x200B;**輸入在 3D 空間**&#x200B;中產生分形* Ridged 噪聲。

此節點可用 Cube 3D GBuffers[&#128279;](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d-gbuffers/cube-3d-gbuffers.md) 作為輸入，取代實際烘焙的貼圖（如下方範例圖片所示）進行測試。

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
  控制分形3D脊狀雜訊的比例。
* **尺寸** *Float3*\
  控制 X **、** Y **和** Z **軸中**&#x200B;分形 3D Ridged 雜訊的大小。不均勻的數值會導致 *拉伸或壓縮* 效果。
* **偏移** *Float3*\
  對分形三維脊狀雜訊在 X **、** Y **和** Z **軸的位置施加偏移&#x200B;**。**
* **失真強度***浮球*\
  控制 *對分形3D有脊聲所施加的扭曲效果* 強度。
* **失真尺度乘法***浮點*\
  控制扭曲效果中變形圖案&#x200B;*的尺度*，由變形強度&#x200B;**控制**。
* **最小整數層***級*\
  分形圖案中使用的最低 *重複* 程度。 更寬的最小/最大範圍會產生 *更豐富的圖案* ，並在更多頻率範圍內變化。
* **最大層級***整數*\
  分形圖案中使用的最大 *重複* 程度。 更寬的最小/最大範圍會產生 *更豐富的圖案* ，並在更多頻率範圍內變化。
* **粗糙漂***浮*\
  控制&#x200B;*分形圖案中低與高*&#x200B;重複&#x200B;*的平衡*。\
  *注意*：值為 **0** 的輸出 *與後續低值不一致* 。 這是預料之中的。
* **Lacunarity** *花車*\
  控制施加的分形圖案 *如何填滿空間*。 *較高*&#x200B;的數值會導致&#x200B;*圖案間隙*&#x200B;較少，噪音&#x200B;*密度也更*&#x200B;高。
* **全域不透明度***浮點*\
  控制&#x200B;*分形 3D Ridged 雜訊值*&#x200B;在&#x200B;***基準值**&#x200B;附近的範圍*。
* **基線***浮動*\
  對3D脊狀雜訊分布的基準亮度值施加&#x200B;*偏移*。**
* **對比***浮動*\
  調整 3D Ridged 雜訊的對比度。
* **啟用平鋪布***林*\
  調整 3D Ridged 雜訊，使其產生的圖案 *在 X、Y 和 Z 軸上重複* 出現。

## 範例圖片

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dridgednoisefractal-variant.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dridgednoisefractal-variant2.jpg){width="256px"}

</td>
</tr>
</table>
