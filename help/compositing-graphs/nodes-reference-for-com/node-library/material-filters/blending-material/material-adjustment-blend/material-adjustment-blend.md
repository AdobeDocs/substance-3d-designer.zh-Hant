---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/blending-material/material-adjustment-blend.html"
breadcrumb-title: ''
description: 使用材質調整混合節點來混合材質調整，進行複合效果的微調。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Blending (Material) > Material Adjustment Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 材料調整混合
user-guide-description: ''
user-guide-title: ''
source-git-commit: db158eba37ce52811a853adc20ca6143f96a79b6
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 2%

---


# 材料調整混合

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](material-adjustment-blend.resources/material-adjustment-blend.png){width="128px"}

<b>收錄於：</b> 材料過濾器>混合

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

此節點允許根據遮罩調整完整材料的任何通道。 它的目的是讓整個材料的工作流程更簡單且快速。

當你想調整材質的幾個通道（例如讓漫反射更亮、粗糙度變暗）時，它很有用。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>色彩識別面罩</b> <i>色彩輸入</i> | 遮罩槽用於遮蔽節點的效果。 |
| <b>灰階面具</b> <i>灰階輸入</i> | 遮罩槽用於遮蔽節點的效果。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>頻道</b> | 在此群組中切換材質通道的開關，例如使用鏡面/光澤貼圖而非金屬/粗糙度時。<br><br>這同時啟用或停用通道相關群組的外觀。 |
| <b>彌漫</b> | 在遮罩定義的區域內對擴散通道執行調整操作。 |
| <b>底色</b> | 在遮罩定義的區域內對基礎色彩通道執行調整操作。 |
| <b>正常</b> |  |
| <b>強度</b> <i>0.0 - 1.0</i> | 調低正常強度 |
| <b>鏡面鏡面</b> | 在遮罩定義的區域內對鏡面通道執行調整操作。 |
| <b>發射體</b> | 對由遮罩定義的區域內的發射通道執行調整操作。 |
| <b>光澤</b> | 在遮罩定義的光澤通道中執行調整操作。 |
| <b>粗糙度</b> | 對粗糙通道執行調整操作，範圍由遮罩定義。 |
| <b>金屬</b> | 在金屬通道中，根據遮罩定義的區域進行調整操作。 |
| <b>鏡面層級</b> | 在遮罩定義的區域內對鏡面層通道執行調整操作。 |
| <b>環境遮蔽</b> | 對環境遮蔽通道執行調整操作，範圍由遮罩定義。 |
| <b>高度</b> | 在遮罩定義的區域內對高度通道執行調整操作。 |
| <b>不透明度</b> | 在遮罩定義的區域內對不透明度通道執行調整操作。 |
| <b>色彩識別面罩</b> <i>錯誤/真實</i> | 設定使用 Color ID Mask 而非灰階遮罩。 |
| <b>模糊感</b> <i>0.01 - 1.0</i> | 若啟用 Color ID 遮罩，則決定 Color ID 選擇顏色的擴散範圍。 |
| <b>顏色</b> <i>（色彩值）</i> | 設定從 Color ID 映射和遮罩中選擇的顏色。 |
| <b>填充物</b> <i>0.0 - 1.0</i> | 決定色彩識別遮罩的混合對比度/過渡。 |
