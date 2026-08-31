---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/atomic-function-nodes/get-nodes.html"
breadcrumb-title: ''
description: 存取 Substance 3D Designer 功能圖中的節點，以擷取變數值與資料。
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Variables
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 變數
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '477'
ht-degree: 1%

---


# 變數

變數是一種儲存值的方式，以便<b>之後<b>取得（Get</b>）和/或修改（<b>Set</b>）。</b>

![Substance 函數圖 - 取得 float](get-nodes.resources/get-nodes-01.gif "Substance 函數圖 - 取得 float"){zoomable="yes"}

Get 節點的本質作用是抓取一個動態變數，然後從 Get 節點的輸出中回傳，用於函式。 這些 Get 節點構成圖參數中定義[的輸入參數與[參數函式](../../../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)之間的](../../../../compositing-graphs/graph-parameters/graph-parameters.md)連結。

每次使用「取得」節點時，你必須從下拉選單中選擇一個可用的值。 取得節點會 <b>擷取對應類型的</b>值。 這表示你只會在 Get 節點的選單中看到有效選項，無法選擇無效選項。 如果變數無法使用，代表類型不匹配

有許多 <b>「系統」變數</b>：預先定義的特殊變數，你無法自行宣告。 這些變數非常重要，且在下方節點會列出可用的系統變數。

當參數被 [暴露](../../../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)時，會對其套用一個參數函式，該函式僅包含正確類型的 Get 節點。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## 取得

</td>
<td style="border: 0;" valign="top">

### 場景

</td>
<td style="border: 0;" valign="top">

### 定義為

</td>
</tr>
</table>

## 取得

<table>
<tr style="border: 0;">
<td width="25.00%" style="border: 0;" valign="top">

![取得 float2 - 圖示](get-nodes.resources/get-nodes-02.png "取得 float2 - 圖示"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

這些節點讓你能取得目前作用域&#x200B;*中存在*&#x200B;的變數值。

被擷取變數的名稱會在屬性（Properties）底座中設定。

</td>
</tr>
</table>

「取得」節點，以下是你需要注意的限制：

* <b>它們是有型</b>別的，因此你需要確保變數的值與節點類型相同。 主機會回報類型不符。
* <b>它們不會檢查該變數</b> 是否存在於當前範圍內。 未發現變數會在控制台中回報。
* 在使用像 Sequence 這類控制流程節點的複雜函式中，要注意 <b>設定和取得變數</b>的順序。 當 Designer 偵測到「Get before Set」的狀況時，會在控制台中回報。

>[!NOTE]
>
> 內建變數
> 
> 多個「Get」節點會根據當前情境提供內建變數，以存取現有值——例如：像素處理器中的當前像素位置、節點目前的平鋪模式等
> 
> 所有內建變數都列在這個 [專屬頁面](../../../../function-graphs/variables/system-variables/system-variables.md)中。

### 取得節點

+++花車
![取得浮動 - 圖示](get-nodes.resources/get-nodes-03.png "取得浮動 - 圖示"){width="200px"}



Get Float

![取得 float2 - 圖示](get-nodes.resources/get-nodes-02.png "取得 float2 - 圖示"){width="200px"}



取得 Float2

![取得 float3 - 圖示](get-nodes.resources/get-nodes-04.png "取得 float3 - 圖示"){width="200px"}



取得 Float3

![取得 float4 - 圖示](get-nodes.resources/get-nodes-05.png "取得 float4 - 圖示"){width="200px"}



取得 Float4

+++

+++整數
![取得整數 - 圖示](get-nodes.resources/get-nodes-06.png "取得整數 - 圖示"){width="200px"}



取得整數

![取得整數2 - 圖示](get-nodes.resources/get-nodes-07.png "取得整數2 - 圖示"){width="200px"}



取得 Integer2

![取得整數3 - 圖示](get-nodes.resources/get-nodes-08.png "取得整數3 - 圖示"){width="200px"}



取得整數3

![取得整數4 - 圖示](get-nodes.resources/get-nodes-09.png "取得整數4 - 圖示"){width="200px"}



取得 Integer4

+++

+++其他
![取得布林值 - 圖示](get-nodes.resources/get-nodes-10.png "取得布林值 - 圖示"){width="200px"}



取得布林值

![取得字串 - 圖示](get-nodes.resources/get-nodes-11.png "取得字串 - 圖示"){width="200px"}



抓繩子

+++

## 場景

<table>
<tr style="border: 0;">
<td width="25.00%" style="border: 0;" valign="top">

![集合：節點圖示](get-nodes.resources/get-nodes-12.png "設定：節點圖示"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

文字

</td>
</tr>
</table>

## 定義為

<table>
<tr style="border: 0;">
<td width="25.00%" style="border: 0;" valign="top">

![定義：節點圖示](get-nodes.resources/get-nodes-13.png "定義：節點圖示"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

文字

</td>
</tr>
</table>
