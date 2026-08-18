---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/paths-vertex-processor.html"
breadcrumb-title: ''
description: 使用 Paths 頂點處理器節點來轉換並操作路徑頂點，並有進階選項。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Paths Vertex Processor
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 路徑頂點處理器
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 0%

---


# 路徑頂點處理器

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![節點圖示](../../../../../../assets/paths-vertex-processor-icon.png "節點圖示")

<b>收錄於：</b> 樣條與路徑工具 > 路徑工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

對輸入<b>路徑</b>頂點位置施加轉換。

節點應如下使用：

1. 編輯<b>每個頂點函 </b>數參數函式;
1. 使用 <b>Get Float2</b> 節點來取得;vertex.pos **、*prev.pos* 和/或 *next.pos* 變數
1. 對這些值做一些運算（例如，乘以縮小路徑）;
1. 將你的計算結果設為輸出。

</td>
</tr>
</table>

在查詢 prev.pos 或 next.pos 之前，務必先設定正確的 <b>Previous vertices accessed <b></b> 和 Next vertices accessed</b> 值&#x200B;** **\
你也可以加入輸入影像，並從函式中取樣。 你必須先連接一個能從函數取樣的輸入。 （請注意，第一個輸入是&#x200B;*圖片 1*！）\
你也可以存取 *prev[2].pos*（Float2）、*next[2].pos*（Float2）、*vertex.corner*（bool）和 *path.id*（float）變數。

>[!TIP]
>
> 對於進階使用者， [路徑格式規範](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-format-spe/paths-format-specifications.md) 說明了路徑資料如何編碼成彩色影像，並提供直接操作這些資料的技巧。

>[!NOTE]
>
> 另 [見路徑頂點處理器](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-vertex-processor-1/paths-vertex-processor-simple.md)簡單版。

## 輸入連接器

<b>路徑</b> *顏色*\
一份編碼段路徑列表。 將此輸入連接到 Mask to Paths](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) 的結果[，或是連接到另一個&#x200B;*Path-processing* 節點。

<b>輸入 #</b> *色彩/灰階*\
應該在 <b>每個頂點函</b> 數參數函數中取樣的影像輸入。

## 輸出連接器

<b>路徑</b> *顏色*\
變形的路徑。 你可以使用[預覽路徑來了解結果代表什麼，使用其他路徑處理節點，或[輸入](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md)到路徑到樣條線（Paths to Spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md)）中，進一步以樣條線處理。

## 參數

<b>先前存取</b> *的頂點 整數*\
使用此參數後，你可以透過 <b>Per Vertex Function</b> 參數函式中的 <b>Get</b> 節點，取得路徑上&#x200B;*前一個頂點（prev.pos*）及前一個頂點（*prev[2].pos*）的位置。

<b>下一頂點存取</b> *整數*\
使用此參數後，你可以利用 <b>Per Vertex Function</b> 參數函式中的 <b>Get</b> 節點，取得路徑上下一個頂點（*next.pos*）及下一個頂點（*next[2].pos*）的位置。

<b>影像輸入計數</b> *整數*\
用於連接應在每個頂點函</b>數參數函數中<b>取樣的影像的可見 <b>Input #</b> 輸入連接器數量。\
當你完成所有想要的取樣後，可以透過將這個參數的值降回 0 來隱藏未使用的腳位。

<b>每個頂點函數</b> *Float2*\
每個頂點都套用了函數。 必須回傳新的頂點位置。\
請參閱 <b>本頁的說明</b> 部分以獲得指引。

## 範例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![節點範例 2](../../../../../../assets/PathsVertexProcessor-Demo2.gif "節點範例 2")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
