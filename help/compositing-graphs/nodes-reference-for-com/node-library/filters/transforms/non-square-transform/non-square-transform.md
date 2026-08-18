---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/non-square-transform.html"
breadcrumb-title: ''
description: 使用 Non-Square Transform 節點，對具有獨立 X 和 Y 縮放的非正方形材質套用變換。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Non-Square Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 非平方轉換
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 0%

---


# 非平方轉換

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/safe-transform.png)

![](../../../../../../assets/safe-transform-grayscale.png)

## 非平方轉換（灰階）

**收錄於：***濾波器/轉換*

**中級**

</td>
<td style="border: 0;" valign="top">

## 說明

非方形安全的 Transform 2D[&#128279;](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md) 版本。自動偵測非正方形比例，並能將正方形輸入影像轉換到非正方形畫布上。

務必完全了解 [圖參數](../../../../../../compositing-graphs/graph-parameters/graph-parameters.md)，才能充分利用這個節點，因為你需要正確設定幾個參數：

* 你的 **圖** 大小應該是非方形的，否則不需要這個節點。
* 將非正方形轉換 **節點的** 輸出大小設為「*相對於父節點*」。
* 如果你只想將輸入轉換到單一位置，請將節點的&#x200B;**平鋪模式設**&#x200B;為「*無平鋪*」。

## 參數

* **磚塊模式**： *自動、手動*&#x200B;啟用自動非正方形補償是否啟用。
* **瓦片**： *1 - 16*&#x200B;只有在瓦片模式設為手動時才能進入。 讓你能以安全的平鋪方式改變比例。
* **偏移**&#x200B;量： *0.0 - 1.0*\
  移動或翻譯結果。 雙擊滑桿以輸入負值。
* **旋轉**： *0.0 - 1.0*&#x200B;旋轉輸入影像。
* **安全旋轉（僅限方形）：***假/真*&#x200B;吸附至安全值以維持像素銳利度。
* **背景色**：*（色彩值）*用來填充影像的背景色。 只有當 [基礎參數的平鋪模式設為「*無平鋪*」](../../../../../../compositing-graphs/graph-parameters/graph-parameters.md)時才會顯示。

## 範例圖片

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/nonsquare-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
