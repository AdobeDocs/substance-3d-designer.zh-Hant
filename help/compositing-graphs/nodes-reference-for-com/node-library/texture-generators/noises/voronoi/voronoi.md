---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/voronoi.html"
breadcrumb-title: ''
description: 利用 Voronoi 節點產生 Voronoi 圖案，以創造細胞紋理和有機材料效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Voronoi
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 沃羅諾伊
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '618'
ht-degree: 0%

---


# 沃羅諾伊

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/voronoi.png){width="200px"}

**收錄於：***材質產生器**/噪音*

**中級**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## 說明

**Voronoi** 節點會產生一個 3D Voronoi 雜訊，並利用 *Z-down 正交投影*&#x200B;映射到二維影像。

此節點可以 [Cube GBuffers](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d-gbuffers/cube-3d-gbuffers.md) 作為輸入測試，而非實際烘焙的映射（如下方範例圖片所示）。

>[!WARNING]
>
> 這種雜訊僅用於 *GPU 引擎*（例如 **Direct**&#x200B;或 **OpenGL）。**&#x200B;到 **工具>切換引擎......** 或按 **F9** 鍵選擇想要的引擎。

</td>
</tr>
</table>

## 參數

* **反布***林*\
  將輸出影像反轉。
* **比例***浮球*\
  控制 Voronoi 噪音的音階。\
  *注意*：當&#x200B;**任一&#x200B;*軸啟用*平鋪**&#x200B;時，縮放調整會被&#x200B;*階梯調整*。這是預料之中的。
* **尺寸** *Float3*\
  控制 Voronoi 在 X **、** Y **和** Z **軸上的**&#x200B;噪音大小。不均勻的數值會導致 *拉伸或壓縮* 效果。\
  *注意*：當&#x200B;**任一&#x200B;*軸啟用*平鋪**&#x200B;時，大小調整會是&#x200B;*階*&#x200B;梯式的。這是預料之中的。
* **偏移** *Float3*\
  對 X **、** Y **和** Z **軸上 Voronoi 雜訊**&#x200B;的位置&#x200B;*施加偏移*。
* **混亂** *Float3*\
  隨機偏移的強度&#x200B;*，分別施加在X **軸、**Y **軸和**Z **軸的雜訊**點*&#x200B;上。
* **失真強度***浮球*\
  控制施加在沃羅諾伊噪音上的變形效果&#x200B;*強度*。
* **失真尺度乘法***浮點*\
  控制扭曲效果中變形圖案&#x200B;*的尺度*，由變形強度&#x200B;**控制**。
* **圓弧浮***球*\
  繞&#x200B;*過噪音的每個點，使斜*&#x200B;率&#x200B;*呈現*&#x200B;凸面。\
  *注意* ：當 **Style** 參數設為 *Edge* 時，此參數不可用。
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
* **樣式***整數*&#x200B;設定&#x200B;**&#x200B;渲染 Voronoi 雜訊資料的方法，考慮雜訊是基於空間中的一組點：
  * *F1*：距離空間中最近點&#x200B;*的*&#x200B;距離
  * *F2*：距離空間中第二近點&#x200B;*的*&#x200B;距離
  * *F2-F1*- *F1\* F2 *-* F1/F2 *-*&#x200B;邊緣&#x200B;*：*&#x200B;空間中雜訊各單元* 之間的邊緣
  * *隨機顏色*：為空間中每個噪聲單元指派一個&#x200B;*隨機的平面色*
* **邊緣厚度***浮點*&#x200B;調整 Voronoi 雜訊中偵測到的格子間邊緣厚度。邊緣在 X、Y 和 Z 軸上被偵測，因此根據細胞 *深度*&#x200B;不同，某些厚度可能增長得更快。\
  *注意*：此參數僅在 Style **參數設為 *Edge* 時可用**。
* **隨機色彩種子模式***整數*\
  設定每個格子顏色選擇的隨機種子獲取方法&#x200B;**：
  * *全域隨機種子*：使用節點繼承的&#x200B;*種子*
  * *手動種子*：使用 *獨立* 種子\
    *注意*：此參數僅在樣 **式** 參數設為 *隨機顏色*&#x200B;時可用。
* **隨機顏色種子***整數*\
  每個格子顏色選擇應該使用的離散隨機種子。\
  *注意*：此參數僅在風格&#x200B;****&#x200B;參數設為&#x200B;*隨機色彩*，且&#x200B;**隨機色彩種子模式**&#x200B;參數設為&#x200B;***手動種子***&#x200B;時可用。
* **非平方展開***布林*\
  能以非平方比率補償擠壓與拉伸。

## 範例圖片

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/voronoi-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/voronoi-variant3.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/voronoi-variant5.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/voronoi-variant.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/voronoi-variant4.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/voronoi-variant6.jpg){width="256px"}

</td>
</tr>
</table>
