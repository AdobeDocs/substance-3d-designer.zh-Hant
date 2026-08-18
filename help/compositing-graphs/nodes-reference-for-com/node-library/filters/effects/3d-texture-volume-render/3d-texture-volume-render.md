---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/3d-texture-volume-render.html"
breadcrumb-title: ''
description: 使用 3D 材質體積渲染節點，從 3D 資料渲染體積材質，來創造雲霧和霧的效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > 3D Texture Volume Render
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D 貼圖體積渲染
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 0%

---


# 3D 貼圖體積渲染

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturevolumerender.png){width="200px"}

**收錄於：***濾波器/效果*

**很簡單**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## 說明

**3D 紋理體積渲染**&#x200B;節點會根據&#x200B;**&#x200B;**&#x200B;3D 有符號距離場**&#x200B;影像輸入，渲染由 *3D 紋理*&#x200B;描述的形狀體積。

體積在單位立方&#x200B;*體的範圍內*&#x200B;表示。照明是利用 *定向光* 和 *半球形天窗*&#x200B;計算的。

>[!NOTE]
>
> 有符號距離欄位預期為 **一個 4096x4096** 的紋理，描述形狀，並以 **16x16** 格網，包含 256 個切片。\
> 你可以使用 [3D Texture SDF](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-texture-sdf/3d-texture-sdf.md) 節點來計算 256 個切片的 3D 貼圖的有符號距離場。

</td>
</tr>
</table>

## 參數

### 輸入

* **3D 有號距離場灰***階*\
  這張4096x4096的影像代表形狀有符號距離場&#x200B;*的256*&#x200B;個切片&#x200B;**，排列成16x16格子。\
  你可以使用 [3D Texture SDF](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-texture-sdf/3d-texture-sdf.md) 節點來計算 256 個切片的 3D 貼圖的有符號距離場。
* **密度***灰階*\
  4096x4096 的影像代表形狀密度&#x200B;*的 256*&#x200B;切片&#x200B;**，排列成 16x16 格子。密度以灰階值映射，從0（完全透明）到1（完全不透明）。\
  你可以使用 [3D 體積遮罩](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/3d-volume-mask/3d-volume-mask.md) 或 3D 雜訊節點（[例如 3D Perlin 雜訊](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/3d-perlin-noise/3d-perlin-noise.md)、 [3D Voronoi](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/3d-voronoi/3d-voronoi.md)、 [3D Ridged Noise Fractal](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/3d-ridged-noise-fractal/3d-ridged-noise-fractal.md) 等），結合 [3D 紋理位置](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-texture-position/3d-texture-position.md) 節點作為位置輸入，產生一個包含 256 片的 3D 貼圖體積遮罩。

### 參數

* **輸出解析度** *整數 2*\
  輸出影像的解析度以 **X** 和 **Y** 表示，表示為 *二*&#x200B;的冪方。
* **攝影機位置** *Float2*\
  相機在形狀周圍的位置。\
  當節點被選中後，你可以在 2D 視圖&#x200B;**中使用位置裝置**&#x200B;來繞&#x200B;*行*&#x200B;攝影機。
* **燈光位置***浮點2*\
  指 *的是* 形狀周圍方向光的位置。\
  選中節點後，你可以在 2D 視圖&#x200B;**中使用位置裝置**&#x200B;繞&#x200B;*光源旋轉*。
* **攝影機距離***漂浮*\
  相機到形狀的距離。
* **攝影機視野***浮動*\
  相機的視野 *以度數*&#x200B;為單位。
* **吸收***浮球*\
  調整光線通過體積時&#x200B;**&#x200B;吸收的量。
* **羽毛***漂浮*\
  將密度&#x200B;**輸入所提供的**&#x200B;值乘以&#x200B;*內*&#x200B;距離場值。\
  這有效地調整了從體積外界向內的漸變漸變&#x200B;*寬*&#x200B;度。
* **光色模式***整數*\
  設定取得方向光顏色的方法：
  * *溫度（開爾文）：*&#x200B;顏色由光溫決定，數值越 *低* ， *顏色越* 暖
  * *RGB 顏色*：使用 RGB 值定義顏色
* **光溫（開爾文）***浮球*\
  光線的定向溫度，影響其 *顏色*。 數值越 *低* ， *顏色越暖* 。\
  實用價值：\
  1800 K - 燭光\
  2800 K - 白熾燈泡\
  5500 K - 日光\
  6200 K - 自然白\
  7000 K - 陰天天空\
  *注意*：此參數僅在光 **色模式** 參數設為 *溫度（開爾文）*&#x200B;時可用。
* **淺色***浮車3*\
  方向燈的顏色。\
  *注意*：此參數僅在光 **色模式** 參數設為 *RGB 色彩*&#x200B;時可用。
* **光強***浮球*\
  方向光的強度。
* **環境色彩***漂浮3*\
  環境天窗的顏色。
* **環境強度***浮球*\
  環境天窗的強度。
* **阿貝多***浮動3*\
  體積的反照率顏色。
* **背景模式整***數*\
  根據背景色&#x200B;**來渲染場景**&#x200B;背景的陰影方法：
  * *陰*&#x200B;影：顏色會受到方向光 *的顏色* 和 *強度*&#x200B;影響- *恆定色彩*：顏色會均勻地被均勻地施加 *，不受* 光線方向影響
* **背景色** *Float4*\
  用來填滿渲染場景背景的顏色。
* **抖動***浮動*\
  調整藍噪&#x200B;*的強度*，用來平滑陰影。
* **啟用地面平面***布林值*\
  當 *為真*&#x200B;時，會渲染一個 *無限的* 地面平面。 *包圍該形狀的單位立方體*&#x200B;就位於此平面上。
* **無限平面***布林*\
  設定地面平面無限 *延伸* 至地平線。\
  *注意*：此參數僅在啟用 **地面平面** 參數設 *為 True* 時可用。
* **地面平面尺寸** *float2*&#x200B;調整地面平面大小。\
  *注意*：此參數僅在啟用 **地面平面** 參數設 *為 True* 、 **無限平面** 參數 *設為 False* 時可用。

## 範例圖片

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturevolumerender-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturevolumerender-variant5.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturevolumerender-variant3.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturevolumerender-variant.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturevolumerender-variant4.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturevolumerender-node.png){width="512px"}

</td>
</tr>
</table>
