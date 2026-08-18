---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/extend-shape.html"
breadcrumb-title: ''
description: 使用 Extend Shape 節點將形狀延伸到邊界之外，以建立擴展遮罩和圖案效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Extend Shape
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 延伸形狀
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 0%

---


# 延伸形狀

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/extendshapegrayscale.png){width="200px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/extendshapecolor.png){width="200px"}

</td>
</tr>
</table>

**收錄於：** 濾鏡*/效果*

**很簡單**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## 說明

**延伸形狀**&#x200B;節點會將輸入&#x200B;**的一段&#x200B;****&#x200B;延伸到固定方向和距離。

**Show 助手**&#x200B;參數讓你能視覺化延伸段和延伸方向。

</td>
</tr>
</table>

## 參數

* **模態***整數*&#x200B;定義&#x200B;*了用於應用擴展的參數*：
  * *雙向：由伸展位置&#x200B;**與**伸展角&#x200B;**指定的輸入**截面&#x200B;**，向相反方向延伸*****延伸****
  * *單向*：由&#x200B;**伸延位置**&#x200B;與&#x200B;**伸展角**&#x200B;指定的輸入&#x200B;**截面**，在延伸距離&#x200B;***上以單一方向延伸***
  * *起始/結束位置*：延伸&#x200B;*向量*&#x200B;由起始位置&#x200B;**與**&#x200B;結束位置&#x200B;**定義**。輸入在起始位置&#x200B;**的**&#x200B;垂直&#x200B;*截面會在此向量*&#x200B;上延伸&#x200B;*至&#x200B;**終點位置*******
* **伸展距離***浮點*&#x200B;由伸展位置&#x200B;**與**&#x200B;伸展角&#x200B;**指定**&#x200B;的延伸段距離。距離以影像跨度的比例&#x200B;*表示*。
* **延伸位置***浮點*&#x200B;指應延伸的截面影像中的位置。該值以 *中心偏*&#x200B;移表示。
* **伸縮角***浮點*&#x200B;指應伸長的截面角度，前提是起始點為&#x200B;*垂直截面*。
* **起始位置** *float2*&#x200B;擴展向量&#x200B;*的*&#x200B;起始位置。
* **端位置** *Float2*&#x200B;延伸向量&#x200B;*的*&#x200B;端點位置。
* **開始亮度偏移***浮點*&#x200B;對影像&#x200B;*中延伸段落前*&#x200B;的區域施加亮度偏移。此亮度偏移會 *沿截面* 插值至影像後面區域的亮度。\
  *注意*：此參數僅在 **該節點的灰階** 版本中提供。
* **結束亮度偏移***浮動*&#x200B;對影像在延伸部分後&#x200B;*的*&#x200B;區域施加亮度偏移。此亮度偏移會 *沿截面* 插值至影像前方區域的亮度。\
  *注意*：此參數僅在 **該節點的灰階** 版本中提供。
* **Lum。 偏移忽略黑色像素** *布林值*&#x200B;當設定為 *True（True*）時，起始亮度偏移&#x200B;****&#x200B;與結束亮度偏移&#x200B;**中指定的&#x200B;****&#x200B;亮度偏移只會套用在&#x200B;*非黑色*&#x200B;像素上，也就是數值高於 0 的像素。\
  *注意*：此參數僅在 **該節點的灰階** 版本中提供。
* **濾波模式***整數*&#x200B;定義了在插&#x200B;*值像素時如何處理取樣結果*：
  * *最近*：會取 *樣完全相同的* 值（更快）
  * *雙線性*：會對結果套用雙線性濾波器，讓畫面更&#x200B;**&#x200B;平滑
* **顯示輔助布***林*&#x200B;將&#x200B;*延伸區*&#x200B;段視覺化為帶有箭頭的覆蓋層，顯示&#x200B;*延伸方向*。

## 範例圖片

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/extendshape.gif){width="512px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/extendshape-variant.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/extendshape-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/extendshape-node.png){width="360px"}

</td>
</tr>
</table>
