---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-blend.html"
breadcrumb-title: ''
description: 使用 Normal Blend 節點將法線貼圖混合在一起，創造表面細節間的平滑過渡。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 一般混合
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 1%

---


# 一般混合

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/normal-blend.png){width="128px"}

## 一般混合

**收錄於：***濾鏡/法線貼圖*

**中級**

</td>
<td style="border: 0;" valign="top">

## 說明

法線混合允許你用可選的遮罩將兩個法線貼圖混合在一起，同時確保所有數值保持正規化狀態。 它和原子混合節點](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md)差異不大[，但增加了法線貼圖的內部計算。

法線混合並非用來合併（疊加）法線貼圖，因為上方貼圖會為下方貼圖增加細節。 為此，改用[普通聯合。](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-combine/normal-combine.md)

## 參數

### 輸入

* **NormalFG**： *色彩輸入*\
  前景/頂法線貼圖。
* **NormalBG：***色彩輸入*\
  背景/底部法線貼圖。
* **遮罩**： *灰階輸入*\
  遮罩槽用於遮蔽節點的效果。 可以用「使用遮罩」參數切換。

### 參數

* **不透明度**： *0.0 - 1.0*\
  前景與背景之間的不透明度融合
* **使用面具**： *虛假/真實*\
  切換面具地圖的使用開關。

## 範例圖片

![](../../../../../../assets/normalblend-ex.gif)

*（.gif格式引入抖動，例如，應用內結果平滑）*

</td>
</tr>
</table>
