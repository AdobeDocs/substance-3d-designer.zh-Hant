---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/physical-sun-sky.html"
breadcrumb-title: ''
description: 使用 Physical SunSky 節點生成物理精確的太陽與天空照明環境，提供逼真的材質預覽。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Physical SunSky
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 實體 SunSky
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 1%

---


# 物理太陽/天空

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/panorama-physical-sun-sky.png){width="200px"}

## 物理太陽/天空

**收錄於：***3D 視圖/HDRI 工具*

**中級**

</td>
<td style="border: 0;" valign="top">

## 說明

基於 Hosek-Wikie 天窗模型的實體太陽與天空實作。 為人工 HDRI 提供了極佳的基礎。

## 參數

* **太陽位置**：\
  距離 = [0,1]x[0,1]（經緯角）
* **濁度**： *1.0 - 10.0*\
  混濁度範圍為1到10
* **反照率**： *0.0 - 1.0*\
  阿貝多的範圍從0到1。
* **底色**： *（顏色值）*\
  地面平面的顏色。
* **曝光（EV）：***-1.0 - 4.0*\
  結果輸出的曝光值。
* **太陽大小**： *0.0 - 4.0*\
  太陽的比例尺，任何與1不同的數值都是物理上不正確的。 價值有微妙的影響！
* **太陽強度**： *0.0 - 1.0*\
  太陽盤的強度。 太陽盤相當小，因此效應不會立刻顯現。
* **天空強度**： *0.0 - 1.0*&#x200B;天空強度。 也會影響天空中太陽的耀眼，而不是光碟本身。

## 範例圖片

![](../../../../../../assets/sky-ex.gif)

</td>
</tr>
</table>
