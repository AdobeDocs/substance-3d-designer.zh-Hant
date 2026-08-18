---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/non-uniform-rotation.html"
breadcrumb-title: ''
description: 使用非均勻旋轉節點來套用非均勻旋轉轉換，以創造螺旋和漩渦效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Non-Uniform Rotation
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 非均勻旋轉
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 1%

---


# 非均勻旋轉

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/nonuniformrotationgrayscale.png){width="200px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/nonuniformrotationcolor.png){width="200px"}

</td>
</tr>
</table>

**收錄於：** 濾波器*/變換*

**中級**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## 說明

**非均勻旋轉**&#x200B;節點會利用&#x200B;**旋轉映射**&#x200B;輸入來旋轉&#x200B;**&#x200B;**&#x200B;輸入。

影像的數值代表&#x200B;**&#x200B;數圈。旋轉是圍繞樞 &#x200B;** 軸位置 **&#x200B; 值或 &#x200B;** 樞軸位置地圖** 輸入所指定的位置進行。\
旋轉映射輸入中的&#x200B;**正值會產生&#x200B;*順*時針**&#x200B;旋轉。

</td>
</tr>
</table>

## 參數

### 輸入

* **輸入***灰階/彩色*\
  輸入的灰階影像應該被旋轉。
* **旋轉地圖***灰階*&#x200B;用來控制旋轉量（以&#x200B;*回合*&#x200B;數計）的地圖。取樣值會與旋轉角度乘&#x200B;**數相乘**。負值則會逆 *時針* 旋轉。
* **旋轉樞軸位置貼圖***顏色*\
  用來指定旋轉 *樞軸*&#x200B;位置的影像。 **X/Y** 位置映射到&#x200B;**影像的 R/G** 通道。

### 參數

* **旋轉角度乘數***浮子*\
  調整旋轉地圖&#x200B;**輸入的**&#x200B;強度。
* **旋轉角度偏移***浮動*\
  施加指定的額外旋轉量。
* **使用 樞軸位置圖***布林值*\
  使用 *點陣圖輸入* 來指定旋轉樞軸的位置。 **X/Y** 位置映射到&#x200B;**位置映射**&#x200B;輸入的 **R/G** 通道。
* **PIvot 位置** *Float2*\
  影像旋轉的樞軸位置。
* **背景色***浮點/浮點4*\
  背景色顯示 *在影像範圍之外* ，以防鋪磚未設為 **H 和 V 平鋪**。
* **濾波模式整***數*\
  定義在像素&#x200B;*間插值時如何處理取樣結果*：
  * *最近*：會取 *樣完全相同的* 值（更快）
  * *雙線性*：會對結果套用雙線性濾波器，讓畫面更&#x200B;**&#x200B;平滑

## 範例圖片

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/nonuniformrotation-demo-02-resized.gif){width="768px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/nonuniformrotation-variant-png.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/nonuniformrotation-node.png){width="256px"}

</td>
</tr>
</table>
