---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/bitmap.html"
breadcrumb-title: ""
description: 使用 Bitmap 節點匯入並使用 bitmap 影像作為 Substance 合成圖中的貼圖。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Bitmap
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 位圖
user-guide-description: ""
user-guide-title: ""
source-git-commit: b2c99a199364ff62b5790b72bcfef02a35d58ca2
workflow-type: tm+mt
source-wordcount: '453'
ht-degree: 0%
---

# 位圖

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![原子節點：點陣](bitmap.resources/comp_bitmap.png "圖原子節點：點陣圖"){width="20%"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

將 [點陣圖資源](../../../../resources/bitmap-resource/bitmap-resource.md) 載入圖中。

這個節點用來將點陣[&#128279;](../../../../glossary/glossary.md)圖匯入你的圖表，或是建立新的點陣圖以配合[點陣圖繪製工具](../../../../resources/bitmap-resource/bitmap-painting-tools/bitmap-painting-tools.md)使用。

建立這個節點有幾種方法，且都要求你了解[連結與匯入資源的差別。](../../../../resources/importing-linking-and-new/importing-linking-and-new-resources.md)

</td>
</tr>
</table>

<div data-preserve-html="true" style="display: block; margin: auto;"><img src="bitmap.resources/bitmap-tooltip.gif" alt="點陣圖提示" /></div>

你可以從零開始建立節點，或是將 [支援格式的點陣](../../../../glossary/glossary.md) 圖放入圖譜檢視中。


>[!TIP]
>
> 產生或匯入的 8 位元點陣圖可用 2D 視圖[&#128279;](../../../../interface/2d-view/2d-view.md)底座中的[點陣繪圖工具](../../../../resources/bitmap-resource/bitmap-painting-tools/bitmap-painting-tools.md)繪製。

>[!IMPORTANT]
>
> 此節點依賴外部資源，因此在操作時有幾點需要注意：
> 
> * 點陣節點可以回傳彩色或灰階，但即使資源是灰階點陣圖，預設仍為彩色。 這會影響圖表的效能和複雜度，因此如果需要，務必切換到「灰階」 [色彩模式](#parameters) 。
> * 刪除點陣圖節點不會[刪除套件](../../../../glossary/glossary.md) [中的點陣資源](../../../../resources/bitmap-resource/bitmap-resource.md)，你必須在[檔案總管](../../../../interface/the-explorer-window/the-explorer-window.md)中手動刪除。
> * 另一方面，刪除 [檔案總管中的位圖資源](../../../../resources/bitmap-resource/bitmap-resource.md) 時要小心：該資源仍能在該工作階段的圖表中運作，因為它被存放在快取中，但下次載入 [套件](../../../../glossary/glossary.md)時該資源會被標記為遺失。
> * 當 Substance 圖被 [煮熟](../../../../glossary/glossary.md)時，點陣解析度會固定在圖中解析度，而非基於原始大小。 建議確保點陣圖節點的「輸出大小」 [基參數](../../../../glossary/glossary.md) 使用「絕對」 [繼承方法](../../../../glossary/glossary.md)，節點後 [接一個設定為「相對於父節點」（即主機圖解析度）的二維](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md) 轉換節點。


## 參數

|  |  |
| --- | --- |
| <b>彩色模式</b> *布林值* | 決定節點的輸出類型，可選擇以彩色或灰階返回。 |
| <b>PKG 資源路徑</b> *弦* | 節點 [所參考的點陣資源](../../../../resources/bitmap-resource/bitmap-resource.md) 路徑。   建議不要手動輸入，而是從檔案總管複製資源貼到參數文字欄位，或直接 [從檔案總管](../../../../interface/the-explorer-window/the-explorer-window.md) 拖放點陣資源到圖表中的點陣節點。 |
| <b>調整尺寸方法</b> *整數* | 在放大或縮小點陣圖時，應該使用的重取樣方法：<ul data-preserve-html="true"> <li data-preserve-html="true"><i>平滑拉伸：</i> 對拉伸影像的來源像素進行 [雙線性濾波](../../../../glossary/glossary.md) 插值。</li> <li data-preserve-html="true"><i>最近拉伸：</i> 拉伸影像，並使用最近來源像素的顏色。</li> </ul> |

## 點陣圖繪製工具

點陣圖可以在 Designer 中編輯。 在本節[&#128279;](../../../../resources/bitmap-resource/bitmap-painting-tools/bitmap-painting-tools.md)了解更多編輯工具的資訊。


## 範例

*即將推出。*
