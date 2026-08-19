---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-perlin-noise.html"
breadcrumb-title: ''
description: 使用 3D Perlin Noise 節點在 3D 空間中產生平滑的 Perlin 雜訊圖案，創造自然的體積紋理。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Perlin Noise
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D Perlin 雜訊
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---


# 3D Perlin 雜訊

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/3dperlinnoise.png){width="200px"}

**收錄於：***材質產生器**/噪音*

**中級**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## 說明

**3D Perlin 噪聲**&#x200B;節點根據位置圖&#x200B;**輸入在三維空間**&#x200B;中產生 Perlin 噪聲。

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
  控制 3D Perlin 雜訊的比例。
* **尺寸** *Float3*\
  控制 X **、** Y **和** Z **軸上** 3D Perlin 雜訊的大小。不均勻的數值會導致 *拉伸或壓縮* 效果。
* **偏移** *Float3*\
  對 X **、** Y **和** Z **軸上 3D Perlin 雜訊**&#x200B;的位置&#x200B;*施加偏移*。
* **失真強度***浮球*\
  控制對 3D Perlin 雜訊施加的扭曲效果&#x200B;*強度*。
* **失真尺度乘法***浮點*\
  控制扭曲效果中變形圖案&#x200B;*的尺度*，由變形強度&#x200B;**控制**。
* **基線***浮動*\
  對3D Perlin雜訊值分布的基準亮度&#x200B;*值施加*&#x200B;偏移&#x200B;*。*
* **對比***浮動*\
  調整 3D Perlin 雜訊的對比度。
* **絕對***布林*\
  在 3D Perlin 雜訊中使用絕對值。 這實際上&#x200B;*是*&#x200B;反轉低於0.5 *值*&#x200B;的值分布。
* **啟用平鋪布***林*\
  調整 3D Perlin 雜訊，使其產生的圖案 *在 X、Y 和 Z 軸上重複* 出現。

## 範例圖片

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dperlin.gif){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dperlinnoise-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dperlinnoise-variant.jpg){width="256px"}

</td>
</tr>
</table>
