---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/histogram-scan.html"
breadcrumb-title: ''
description: 使用直方圖掃描節點來掃描並分析貼圖直方圖，進行色彩校正與調整。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Histogram Scan
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 直方圖掃描
user-guide-description: ''
user-guide-title: ''
source-git-commit: f320cf6842ff56ac24912ceda264f30c28317c05
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 1%

---


# 直方圖掃描

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/histogram-scan-1.png){width="128px"}

## 直方圖掃描

**收錄於：***濾鏡/調整*

**很簡單**

</td>
<td style="border: 0;" valign="top">

## 說明

這是一個非常簡單但實用的節點，提供一種直覺的方式來重新映射輸入灰階影像的對比度和亮度。 可以用來動態地「增大」或「縮減」遮罩。

[點此觀看Substance Academy關於組織圖操作的影片。](https://www.youtube.com/watch?v=p9wcmJBFyGA&t=427s)

## 參數

* **位置**： *0.0 - 1.0*&#x200B;類似亮度控制，會移動結果的中點。 當用於梯度輸入時，這會使轉換點膨脹並縮小。\
  重要提示：預設值為 0 代表最終結果永遠是黑色，試著從 0.5 開始試試看！
* **對比**&#x200B;度： *0.0 - 1.0*\
  調整結果的對比度。 可以用來設定過渡的硬度。
* **反轉位置**： *假/真*&#x200B;會反轉最終結果。

## 範例圖片

![](../../../../../../assets/histogram-scan.gif)

![](../../../../../../assets/histogram-scan2.gif)

![](../../../../../../assets/histogram-scan3.gif)

</td>
</tr>
</table>
