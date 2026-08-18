---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/interface/the-graph-view/link-creation-modes.html"
breadcrumb-title: ''
description: 在 Substance 3D Designer 的圖形檢視中學習連結建立模式，以有效連接節點。
helpx_creative_field: ""
helpx_description: Designer > Interface > The graph view > Link creation modes
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 連結建立模式
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0b8b2d2c05587d7fe84a71bb54244a492540d6dc
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 0%

---


# 連結建立模式

在 [Substance 圖](../../../compositing-graphs/substance-compositing-graphs.md)中，你可以使用三種 <b>連結建立模式</b>之一來連接節點：

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![連結建立模式：標準](../../../assets/link-creation-mode-standard.gif "連結建立模式：標準"){zoomable="yes"}

*點擊放大*

<b>![](../../../assets/image2020-10-6-19-40-25.png)標準賽</b>（1）

不強制執行任何條件。

</td>
<td style="border: 0;" valign="top">

![連結建立模式：素材](../../../assets/link-creation-mode-material.gif "連結創建模式：素材"){zoomable="yes"}

*點擊放大*

![](../../../assets/image2020-10-6-17-11-20.png) <b>素材（</b>2）

輸入與輸出會根據其使用情況進行匹配。

如果兩者中只有一個有使用權，連線會像標準模式一樣執行。

</td>
<td style="border: 0;" valign="top">

![連結建立模式：緊湊材質](../../../assets/link-creation-mode-compact-material.gif "連結建立模式：緊湊材質"){zoomable="yes"}

*點擊放大*

![](../../../assets/image2020-10-6-19-40-46.png) <b>緊湊材料</b>（3）

和材料一樣。

屬於同一 *群* 的輸入與輸出會被合併。

</td>
</tr>
</table>

你可以隨時在圖表工具列中切換模式，點擊![](../../../assets/link-creation-mode.png) <b>連結建立模式</b>按鈕，或使用上述鍵盤快捷鍵切換。

在<b>物質模式與<b>緊湊材料</b>模式中，輸入與輸出&#x200B;*之間不匹配的使用*&#x200B;方式是被</b>禁止的連接。

## 模式

|  | <div><img data-preserve-html="true" height="23" src="../../../assets/image2020-10-6-19-40-25.png"/></div>標準 | <div><img data-preserve-html="true" height="23" src="../../../assets/image2020-10-6-17-11-20.png"/></div>緊湊 | <div><img data-preserve-html="true" height="23" src="../../../assets/image2020-10-6-19-40-46.png"/></div>緻密材料 |
| --- | --- | --- | --- |
| <b>輸入</b> | 所有輸入都是可見的 | 所有輸入都是可見的 | 每組只能輸入一個 |
| <b>輸出</b> | 所有輸出皆可見 | 所有輸出皆可見 | 每組只有一個輸出 |
| <b>連結</b> | 所有連結皆可見 | 所有連結皆可見 | 每組僅有1個連結（綠色） |
| <b>交通連接</b> | 你要一個一個連結連結 | 你根據匹配的使用情況，將連結連結成多連結材料群組。 當使用在一端時，連線為標準連線。 | 你將連結連結成單一連結的材質群組。 |

## 分組分配

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

你應該把群組指派到圖的輸入和輸出節點，這樣才能使用<b>材質</b>和<b>緊湊材質</b>模式。</b> <b></b> <b>

你可以在<b>節點的屬性</b>參數中指派一個群組，方法是在群組<b></b>屬性中填入群組名稱。群組可以是任何字串值，若連結擁有 *完全相同的*&#x200B;大小寫區分群組名稱，則會被分組。

圖的分組輸入與輸出會以視覺化方式標示，在&#x200B;*參考該圖的節點實例中以暗色膠囊* 包圍。

</td>
<td width="25.00%" style="border: 0;" valign="top">

![節點](../../../assets/link-creation-mode-group-node.png "上的群組膠囊 節點上的群組膠囊"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="25.00%" style="border: 0;" valign="top">



</td>
<td width="100.00%" style="border: 0;" valign="top">

![群組屬性](../../../assets/link-creation-mode-group.png "群組屬性"){zoomable="yes"}

*點擊放大*

</td>
<td width="25.00%" style="border: 0;" valign="top">



</td>
</tr>
</table>

## 連結匹配與使用情況

連結分組後，需將個別輸入與輸出匹配。 這是透過<b>輸入</b>節點和<b>輸出</b>節點的<b>使用</b>屬性來完成的。如果輸入與輸出 *的使用量相*&#x200B;符，就會建立連結。 若未找到匹配使用，則不建立連結。

<table>
<tr style="border: 0;">
<td width="25.00%" style="border: 0;" valign="top">



</td>
<td width="100.00%" style="border: 0;" valign="top">

![使用屬性](../../../assets/link-creation-mode-usage.png "使用屬性"){zoomable="yes"}

*點擊放大*

</td>
<td width="25.00%" style="border: 0;" valign="top">



</td>
</tr>
</table>
