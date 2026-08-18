---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/function-graphs/fxmaps/using-functions-in-fxmaps/iterate-and-number-variable.html"
breadcrumb-title: ''
description: 學習如何在 FXMaps 中使用迭代和數字變數來創造循環模式和程序變化。
helpx_creative_field: ""
helpx_description: Designer > Function graphs > FXMaps > Using Functions in FXMaps > Iterate and number variable
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 迭代與數值變數
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 0%

---


# 迭代並$number變數

![](../../../../assets/iterate-1.jpg)

迭代節點會依照迭代值指定的時間，將連接到正確輸出的節點渲染出來。

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c0_image" src="../../../../assets/1-iteration.png"/></div> | 1 次迭代：高斯圖案被渲染一次 |
| --- | --- |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r1-column-c0_image" src="../../../../assets/10-iterations.png"/></div> | 10 次迭代：高斯圖案在同一位置渲染 10 次 |

使用迭代節點時，可以用 $number 變數取得目前的迭代值。 $number 是一個浮動值，起始數為 0。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../assets/position-function.jpg){width="300px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../assets/10-iterations-position-function.png){width="300px"}

</td>
</tr>
</table>

這個函式設定在 Pattern Offset 參數中，會執行 10 次，每個 pattern 一次。

第一個圖案的 $number 值為 0，然後在 （0， 0） 座標渲染。 第二個圖案的$number值為1，接著在（0.1， 0）座標（1 x 0.1 = 0.1）渲染，依此類推，針對接下來的圖案。

下載範例： [iterate\_node.sbs](https://helpx.adobe.com/content/dam/help/en/substance-3d/documentation/sddoc/files/102400023/102367299/1/1423458106000/iterate-node.sbs)
