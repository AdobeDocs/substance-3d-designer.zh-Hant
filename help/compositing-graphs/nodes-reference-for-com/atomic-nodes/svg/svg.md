---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/svg.html"
breadcrumb-title: ""
description: 使用 SVG 節點匯入並渲染 SVG 向量圖形作為材質，以建立可縮放的圖形元素。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > SVG
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: SVG
user-guide-description: ""
user-guide-title: ""
source-git-commit: 0cb0df528e7f0eb6f3c2d51e35302744952718d5
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 0%
---

# SVG

<table>
<tr style="border: 0;">
<td width="20%" style="border: 0;" valign="top">

![原子節點：SVG](svg.resources/comp_svg_1.png "原子節點：SVG")

</td>
<td style="border: 0;" valign="top">

將 [SVG 影像](../../../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md) 渲染成點陣圖。 換句話說，就是將向量形狀映射到像素。

建立這個節點有幾種方法，且都要求你了解[連結與匯入資源](../../../../resources/importing-linking-and-new/importing-linking-and-new-resources.md)的差別。

</td>
</tr>
</table>

<div data-preserve-html="true" style="text-align: center;"><img src="svg.resources/svg-tooltip.gif" alt="SVG 工具提示" /></div>

你可以從零開始建立節點，或是把 SVG 檔丟進圖譜檢視。


>[!TIP]
>
> 產生或匯入的 SVG 影像可使用 [2D 視圖](../../../../interface/2d-view/2d-view.md)底座中的[向量編輯工具](../../../../resources/vector-graphics-svg-res/vector-editing-tools/vector-editing-tools.md)進行編輯。

>[!IMPORTANT]
>
> 此節點依賴外部資源，因此在操作時需注意幾點：
> 
> * SVG 節點可以回傳色彩或灰階，但預設仍是彩色，即使資源是灰階向量。 這會影響圖表的效能和複雜度，因此如果需要，務必切換到「灰階」 [色彩模式](#parameters) 。
> * 刪除 SVG 節點不會[刪除套件[](../../../../glossary/glossary.md)中的 SVG 資源](../../../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md)，你必須在[檔案總管](../../../../interface/the-explorer-window/the-explorer-window.md)手動刪除。
> * SVG 形狀會被 [拼](../../../../glossary/glossary.md) 貼成幾何/多邊形，然後 *光柵化* ，以便在 Substance 圖中作為點陣圖使用。 用於這些運算的技術不支援多種向量屬性，例如輪廓。 請點此](../../../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md)了解更多關於這些限制[的資訊。

>[!WARNING]
>
> SVG 形狀會被 [拼](../../../../glossary/glossary.md) 貼成幾何/多邊形，然後 *光柵化* ，以便在 Substance 圖中作為點陣圖使用。
> 
> 用於這些運算的技術不支援多種向量屬性，例如輪廓。
> 
> 請點此](../../../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md)了解更多關於這些限制[的資訊。


## 參數

|  |  |
| --- | --- |
| <b>彩色模式</b> *布林值* | 決定節點的輸出類型，可選擇以彩色或灰階返回。 |
| <b>背景色</b> *彩色/灰階* | 設定輸出影像的背景色，或用於未被向量圖形覆蓋的區域。   *當「背景](#inputs)」輸入連接時，會[被覆蓋。* |
| <b>PKG 資源路徑</b> *弦* | 節點 [所參考的 SVG 資源](../../../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md) 路徑。   建議不要手動輸入，而是從檔案總管複製資源貼到參數文字欄位，或直接從檔案總管](../../../../interface/the-explorer-window/the-explorer-window.md)拖放點陣資源[到圖形中的 SVG 節點。 |

## 向量編輯工具

向量形狀可以在 Designer 中編輯。 在本節](../../../../resources/vector-graphics-svg-res/vector-editing-tools/vector-editing-tools.md)了解更多編輯工具[的資訊。

## 輸入連接器

|  |  |
| --- | --- |
| <b>背景</b> *灰階/彩色* 原色 | 設定輸出影像的背景色，或用於未被向量圖形覆蓋的區域。   *連接時會覆蓋「[背景色](#parameters)」參數。* |


## 範例

*即將推出。*
