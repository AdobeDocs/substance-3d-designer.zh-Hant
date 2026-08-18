---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/caustics.html"
breadcrumb-title: ''
description: 利用焦散節點生成腐蝕光模式，創造水下和折射光效效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Caustics
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 焦散
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 0%

---


# 焦散

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/rt-caustics-grayscale.png){width="128px"}

**收錄於：***材質產生器**/噪音*

**複合體**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## 說明

根據高度圖和光線方向產生投影焦散。有灰階和彩色兩種版本，差異很細微，但彩色版本會加入色彩散射效果。 光線是從單一點投射，沒有使用環境貼圖。

</td>
</tr>
</table>

## 參數

* **輸出色彩空間**： *Raw，sRGB*\
  設定輸出色彩空間。
* **光子網格大小**： *自動、512、1024、2048、4096*\
  透過調整格線大小來設定品質，但預設是匹配輸入。 可以用來加快計算速度。
* **表面高度等級**： *0.0 - 1.0*\
  乘數來決定高度的解讀方式。
* **地面高度位置**： *0.0 - 1.0*\
  設定折射面與投影的距離。
* **表面IOR**： *1.0 - 2.0*\
  設定折射率，彩色版本會增加更多色散。
* **光子大小**： *1.0 - 50.0*\
  光子大小會影響效果的清晰度。
* **色散**： *0.0 - 0.01（僅限彩色版本）*\
  只影響色彩擴散。 當 IOR 低時看不到。
* **抖動**： *0.0 - 1.0*\
  在鑄造光子粒子中加入不規則抖動。
* **燈光位置**：\
  移動燈光位置。 也是用 2D 視角的裝置來完成的。
* **背景色**： *（色彩值）（僅限彩色版本）*\
  改變背景顏色。 灰階版本僅限黑色。
* **非平方展開**： *假/真*\
  以非平方比率補償擠壓與拉伸。

## 範例圖片

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/rt-caustics-grayscale-1.png" width="300px"/></div> |
| --- |
|  |
