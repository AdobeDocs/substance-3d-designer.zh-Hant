---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/atomic-function-nodes/control-nodes.html"
breadcrumb-title: ''
description: Substance 3D Designer 功能圖中的存取控制節點，以控制流程與執行邏輯。
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Control
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 控制
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '557'
ht-degree: 0%

---


# 控制節點

本頁描述功能圖[&#128279;](../../../../function-graphs/the-function-graph/the-function-graph.md)中用於控制&#x200B;*執行*&#x200B;流程的節點。

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![如果......否則節點](https://helpx.adobe.com/content/dam/substance-3d-designer/function-graphs/nodes/atomic-function-nodes/control/IfElse_Node.jpg "如果......否則節點")

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 如果......否則

類似於程式語言，If...Else 節點引入了根據預先定義條件過濾結果的可能性。

</td>
</tr>
</table>

你會將此節點與[邏輯節點](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/logical-nodes/logical-nodes.md) 及 [比較節點](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/comparison-nodes/comparison-nodes.md) 結合使用，幫助你建立檢查條件。

+++輸入連接器
<b>狀況</b> *布林值*\
控制節點輸出的條件。

<b>如果</b> *變異型別*&#x200B;如果 <b>條件</b> 為 *真*，節點輸出的值。

<b>否則</b> *變異型別*&#x200B;如果 <b>條件</b> 為 *False*，節點輸出的值。

+++

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![序列節點](https://helpx.adobe.com/content/dam/substance-3d-designer/function-graphs/nodes/atomic-function-nodes/control/Sequence_Node.jpg "序列節點")

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 序列

確保圖的某一部分在另一部分之前被計算完成。

</td>
</tr>
</table>

這對於控制變數的狀態至關重要，無論是在變數的建立、讀取和更新。

你可以在本 [文件中的「使用集合/序列節點」](../../../../function-graphs/fxmaps/using-functions-in-fxmaps/using-the-set-sequence/using-the-set-sequence-nodes.md) 頁面中了解更多關於序列節點的資訊。

+++輸入連接器
<b>在</b> *變數類型*\
圖中應該先計算的部分

<b>最後</b> *變數類型*\
圖中最後計算的部分

+++

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![白色迴路節點](https://helpx.adobe.com/content/dam/substance-3d-designer/function-graphs/nodes/atomic-function-nodes/control/WhileLoop-Node.jpg "白色迴路節點")

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 雖然環路

執行 <b>一次 Init</b> 分支，然後遍 <b>歷 Exit 條件。</b> 環 <b>形車體</b> 分支至 <b>出口點。</b> 分支返回 *True*。

迴圈完成後，節點會輸出迴圈本體</b>最後一次迭代的<b>結果。

</td>
</tr>
</table>

迴圈有隱含的最大迭代次數，可透過將其設為 -1 來停用。

變數在迭代過程中會保留其值，並可在退出條件（Exit Cond.）下存取。\
這表示你可以在每次迭代中加入索引值，並在退出條件下檢查其值，以控制你需要的迴圈數量。

>[!IMPORTANT]
>
> 連接出口 <b>條件的節點。</b> 迴 <b>圈體</b> 分支無法連接到圖的其他分支。

+++輸入連接器
<b>開始。</b> *變數類型*\
圖中在第一次迭代之前計算的部分——也就是迴圈的起點。

<b>離開指揮部。</b> *布林值*\
這個條件必須成立，才能讓循環停止。 每次迭代都會重新計算。\
*注意：* 最大迭代次數仍限制於 <b>最大迭代</b> 數參數。

<b>環形車身</b> *變數類型*\
這個圖是從迴圈中受益的。 每次迭代都會重新計算。

+++

+++參數
<b>Max。 迭代</b> *整數*\
節點執行的最大迭代次數。\
當以下條件中任一先達成時，節點停止迭代：達到此最大數值或退出條件變為真。\
這個最大值可以透過將值設為 *-1* 來停用。 此時，只有退出條件能停止迭代。

設定『最大值』。 迭代到 -1 能提升小迴圈中的效能，因為少了一個計數器需要追蹤和更新。

不過，要注意節點的配置方式，因為有可能產生 <b>無限迴圈</b> ，導致 Designer 變得無反應。

+++

看看這個關於 While 迴圈節點的教學：
