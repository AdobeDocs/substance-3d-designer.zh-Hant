---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/warnings-in-function-graphs.html"
breadcrumb-title: ''
description: 了解 Substance 3D Designer 功能圖中的警告，並學習如何解決常見問題。
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Warnings in function graphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 函數圖中的警告
user-guide-description: ''
user-guide-title: ''
source-git-commit: 81c39001686736d41614fd59247d53e6d8438def
workflow-type: tm+mt
source-wordcount: '450'
ht-degree: 0%

---


# 函數圖中的警告

本頁列出了 Substance 3D Designer 中功能圖[&#128279;](../../function-graphs/function-graphs.md)可能觸發的警告與錯誤訊息，並提供每種的常見故障排除步驟。

警告會顯示在總管[&#128279;](../../interface/the-explorer-window/the-explorer-window.md)面板中圖表資源[的警告圖示工具提示中，若圖已載入，則會在圖表視圖的](../../interface/the-graph-view/the-graph-view.md)左下角顯示。\
若函數應用&#x200B;*於 Substance 圖[&#128279;](../../compositing-graphs/substance-compositing-graphs.md)中的參數*，任何警告都會引發「該參數的[x]參數函數有部分錯誤&#x200B;*」的警告*。

## ![（錯誤）](warnings-in-function-graphs.resources/error.svg) 未定義輸出節點

該函式沒有定義輸出節點。

<table>
<tr style="border: 0;">
<td width="58.30%" style="border: 0;" valign="top">

**![（滴答聲）](warnings-in-function-graphs.resources/check.svg) 解決方案**

在圖表中選擇任何輸出與此函式預期類型相符的節點（如果有），然後點擊 RMB，並在情境選單中選擇 **「設定為輸出節點** 」選項。\
函數圖的輸出節點以 *橘色*&#x200B;呈現。

>[!NOTE]
>
> 如果函式有預期的輸出值類型，圖視圖[&#128279;](../../interface/the-graph-view/the-graph-view.md)左下角會有註解告訴你該類型。

</td>
<td width="41.60%" style="border: 0;" valign="top">

![](warnings-in-function-graphs.resources/warnings-func-output.gif)

</td>
</tr>
</table>

### ![（錯誤）](warnings-in-function-graphs.resources/error.svg) 當前輸出節點回傳的 *值為 x*

函式的輸出節點回傳的值類型與該函式的預期輸出值類型不符。

<table>
<tr style="border: 0;">
<td width="58.30%" style="border: 0;" valign="top">

**![（滴答聲）](warnings-in-function-graphs.resources/check.svg) 解決方案**

在圖表中選擇任何輸出與此函式預期類型相符的節點，然後點選右鍵，在情境選單中選擇 **「設定為輸出節點** 」選項。\
函數圖的輸出節點以 *橘色*&#x200B;呈現。

>[!NOTE]
>
> 如果函式有預期的輸出值類型，圖視圖[&#128279;](../../interface/the-graph-view/the-graph-view.md)左下角會有註解告訴你該類型。

</td>
<td width="41.60%" style="border: 0;" valign="top">

![](warnings-in-function-graphs.resources/warnings-func-output-type.gif)

</td>
</tr>
</table>

### ![（錯誤）](warnings-in-function-graphs.resources/error.svg) 有些 Get 節點沒有變數名稱

一個或多個 [Get](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/get-nodes/get-nodes.md) 節點的 Get...</b> 屬性留<b>空，因此不指變數。

<table>
<tr style="border: 0;">
<td width="58.30%" style="border: 0;" valign="top">

**![（滴答聲）](warnings-in-function-graphs.resources/check.svg) 解決方案**

輸入一個與函式作用域&#x200B;*中變數*&#x200B;名稱相符的字串，進入 **Get 節點的 Get...** 屬性，觸發此警告。

>[!NOTE]
>
> 輸入字串會 *顯示在節點*&#x200B;中，這讓找到空白值的節點變得容易。

</td>
<td width="41.60%" style="border: 0;" valign="top">

![](warnings-in-function-graphs.resources/warnings-func-empty-get.gif)

</td>
</tr>
</table>

### ![（錯誤）](warnings-in-function-graphs.resources/error.svg) 有些集合節點沒有變數名稱

一個或多個 [Set](../../function-graphs/fxmaps/using-functions-in-fxmaps/using-the-set-sequence/using-the-set-sequence-nodes.md) 節點的 Set **屬性留**&#x200B;空，因此不指任何變數。

<table>
<tr style="border: 0;">
<td width="58.30%" style="border: 0;" valign="top">

**![（滴答聲）](warnings-in-function-graphs.resources/check.svg) 解決方案**

將任何字串輸入 **Set 節點的 Set** 屬性，觸發此警告。

>[!NOTE]
>
> 輸入字串會 *顯示在節點*&#x200B;中，這讓找到空白值的節點變得容易。

>[!NOTE]
>
> 如果字串 *與函式作用域中任何可用變數不* 符，則 *會在該範圍內建立* 一個新的變數，並以該字串命名。

</td>
<td width="41.60%" style="border: 0;" valign="top">

![](warnings-in-function-graphs.resources/warnings-func-empty-set.gif)

</td>
</tr>
</table>
