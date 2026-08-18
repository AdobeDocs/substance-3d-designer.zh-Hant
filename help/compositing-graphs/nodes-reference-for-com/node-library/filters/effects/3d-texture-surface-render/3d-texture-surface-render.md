---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/3d-texture-surface-render.html"
breadcrumb-title: ''
description: 使用 3D Texture Surface Render 節點，從 3D 資料渲染表面貼圖，以建立程序化表面效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > 3D Texture Surface Render
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D 貼圖表面渲染
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '480'
ht-degree: 0%

---


# 3D 貼圖表面渲染

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesurfacerender.png){width="200px"}

**收錄於：***濾波器/效果*

**很簡單**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## 說明

**3D Texture Surface Render** 節點會渲染由 *3D 材質*&#x200B;描述的形狀表面，並利用其從 3D 距離場&#x200B;**影像輸入得到**&#x200B;的對應&#x200B;*距離場*。

該曲面在單位立方體&#x200B;*的範圍內*&#x200B;表示。光照是利用&#x200B;**&#x200B;**&#x200B;環境輸入影像映射到無限球體來計算的。

>[!NOTE]
>
> 距離欄位預期為 **4096x4096** 的紋理，描述形狀，並以 **16x16** 格子，包含 256 個切片。\
> 你可以使用 [3D Texture SDF](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-texture-sdf/3d-texture-sdf.md) 節點來計算 256 個切片的 3D 貼圖的距離場。

</td>
</tr>
</table>

## 參數

### 輸入

* **3D 距離場***灰階*\
  這張 4096x4096 的影像代表形狀距離場&#x200B;*的 256*&#x200B;個切片&#x200B;**，排列成 16x16 的格子。\
  你可以使用 [3D Texture SDF](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-texture-sdf/3d-texture-sdf.md) 節點來計算 256 個切片的 3D 貼圖的距離場。
* **環境***色彩*\
  代表環境的影像&#x200B;*應在渲染時映射到無限球體，並用於計算*&#x200B;光照&#x200B;*。*\
  當&#x200B;**背景模式**&#x200B;參數設為&#x200B;*環境**或環境*&#x200B;時，影像也用於渲染場景背景。

### 參數

* **輸出解析度** *整數 2*\
  輸出影像的解析度以 **X** 和 **Y** 表示，表示為 *二*&#x200B;的冪方。
* **攝影機位置** *Float2*\
  相機在形狀周圍的位置。\
  當節點被選中後，你可以在 2D 視圖&#x200B;**中使用位置裝置**&#x200B;來繞&#x200B;*行*&#x200B;攝影機。
* **攝影機距離***漂浮*\
  相機到形狀的距離。
* **攝影機視野***浮動*\
  相機的視野 *以度數*&#x200B;為單位。
* **阿貝多***浮動3*\
  形狀表面的反照率顏色。
* **背景模式整***數*\
  渲染場景背景的表示方法：
  * *地面輻照度*：計算出的地面平面輻照度
  * *環境*：環境影像輸入的&#x200B;**&#x200B;**&#x200B;環境色彩映射到無限球體，類似於影像的強烈模糊版本
  * *均勻顏色*：均勻地填滿背景以指定顏色
  * *環境*：**&#x200B;**&#x200B;將環境影像輸入映射到無限球面
* **背景色** *Float4*\
  用來均勻填滿渲染場景背景的顏色。\
  *注意*：此參數僅在背景 **模式** 參數設為 *統一色彩*&#x200B;時可用。
* **啟用地面平面***布林值*\
  當 *True 時*，會渲染一個地面平面。 *包圍該形狀的單位立方體*&#x200B;就位於此平面上。
* **無限平面***布林*\
  設定地面平面無限 *延伸* 至地平線。\
  *注意*：此參數僅在啟用 **地面平面** 參數設 *為 True* 時可用。
* **地面平面尺寸** *float2*&#x200B;調整地面平面大小。\
  *注意*：此參數僅在啟用 **地面平面** 參數設 *為 True* 、 **無限平面** 參數 *設為 False* 時可用。

## 範例圖片

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesurfacerender-variant.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesurfacerender-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesurfacerender-variant3.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesurfacerender-variant4.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesurfacerender-node.png){width="512px"}

</td>
</tr>
</table>
