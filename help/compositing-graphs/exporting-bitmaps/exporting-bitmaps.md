---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/exporting-bitmaps.html"
breadcrumb-title: ''
description: 學習如何從 Substance 合成圖中匯出材質與點陣圖，用於外部應用程式與工作流程。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Exporting Bitmaps
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 匯出點陣圖
user-guide-description: ''
user-guide-title: ''
source-git-commit: 7e53313d3c368803a95ebb1f9eee712ae2a05817
workflow-type: tm+mt
source-wordcount: '577'
ht-degree: 0%

---


# 匯出點陣圖

本頁說明 Substance 3D Designer 如何匯出至多種不同的點陣圖檔案格式，以及如何將多個 UV-Tile 分批匯出。如果你想匯 [出成 PSD 檔案](../exporting-psd-files/exporting-psd-files.md)，有專門的頁面。

![簡化](exporting-bitmaps.resources/exportflow.png "出口 簡化匯出")

## 概念匯出

匯出點陣圖時，請記住以下幾點很重要：

* 你<b> 是從圖（Graph）匯出，不是從套件（Package</b>）匯出。 套件本身不會產生影像內容。
* 匯出的位圖數量（及解析度）由 <b>圖的輸出</b> 決定。
* 所有輸出/位圖的檔案類型都設定好了。
* 匯出和出版](../publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md)是不同的[，務必清楚兩者的差異！

## 出口方法

一旦準備好匯出，有兩種方式可以進入匯出對話框：

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

在 [檔案總管](../../interface/the-explorer-window/the-explorer-window.md) 視窗中，右鍵點擊匯出圖，並選擇 **「匯出輸出為點陣圖」**

![](exporting-bitmaps.resources/export-explorer.gif)

</td>
<td style="border: 0;" valign="top">

在 [圖表檢視](../../interface/the-graph-view/the-graph-view.md)中，點擊工具按鈕 ![](exporting-bitmaps.resources/image2019-9-17-14-44-17.png) 並選擇 **「匯出輸出...」**

![](exporting-bitmaps.resources/export-graph.gif)

</td>
</tr>
</table>

## 匯出對話框

匯出對話框會提供幾個自訂匯出選項。

右側所示版本為標準對話框，解析度變更可在圖形、輸出或設定父解析度前再開啟對話框。

1. <b>目的地： </b>所有檔案要儲存的位置。
1. <b>格式：</b> 所有匯出檔案所使用的檔案類型。
1. <b>模式</b>：基於元資料關鍵字產生檔案類型的通用方法。 以下顯示基於第一個輸出的範例檔名，供驗證使用。\
   以下列出所有可用的選項：
   1. *$（graph）* - 目前圖的名稱
   1. *$（識別碼）* -目前輸出識別碼
   1. *$（描述）* - 電流輸出描述
   1. *$（label）* - 目前輸出標籤
   1. *$（user\_data）* - 自訂使用者當前輸出資料
   1. *$（group）* - 輸出輸出組
   1. *$（色彩空間）* - 目前輸出的色彩空間（僅適用於 *OCIO* 與 *Adobe ACE* [色彩管理](../../color-management/color-management.md) 模式）
1. <b>輸出：</b> 切換圖表中特定的輸出和輸出群組。 按鈕可以全部開關。 當只有一個點陣圖改變時，這很有用。
1. <b>自動匯出：</b> 切換按鈕可啟用圖表輸出的自動重新匯出，只要有變更。 只針對目前的圖表。 根據設定，可能會很重且很慢。
1. <b>匯出按鈕：</b> 匯出時使用目前設定，或關閉對話框。

![匯出輸出對話框](exporting-bitmaps.resources/fromgraph-1.png "匯出輸出對話框")

## 匯出對話框（批次/UV 圖塊）

在 Designer 中處理 UV 圖塊網格時，匯出對話框可以用稍微不同的方式，讓多個 UV 磚可以一次批量匯出。 務必了解這個工作流程，並且正確地將 Substance 圖](../../compositing-graphs/substance-compositing-graphs.md)分配[給一個或多個 UV-Tiles。\
批次分頁也是將圖表匯出到與工作解析度（父）解析度不同的快速方法。

用上面提到的方法開始對話框，只要確保你在檔案總管&#x200B;*裡右鍵點擊* UV-Tile-指派的圖表，或是你在圖譜檢視中用&#x200B;*工具按鈕開啟了該 UV-Tile 指派的圖*。

1. <b>批次分頁</b>：請確保選擇此分頁，而非標準 <b>的 From Graph </b>方法，否則選項 2-3 將無法使用。
1. <b>UV 圖塊：</b> 就像 Outputs 一樣，允許你切換開啟或關閉特定 UV 圖塊的匯出。
1. <b>[輸出大小](../../compositing-graphs/output-size/output-size.md）： </b>覆蓋匯出解析度，讓你能更精簡、更有效率地工作，同時以最大輸出速度完成。

![批次匯出輸出對話框](exporting-bitmaps.resources/batch.png "批次匯出輸出對話框")
