---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/blending-material/multi-material-blend.html"
breadcrumb-title: ''
description: 使用多材質混合節點將多種材質混合在一起，創造複雜的材質組合。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Blending (Material) > Multi-Material Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 多材料混合
user-guide-description: ''
user-guide-title: ''
source-git-commit: ca90755a159a7e0297bb26d1e3522b0cfeb6f2ac
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 7%

---


# 多材料混合

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/multi-material-blend.png){width="128px"}

<b>收錄於：</b> 材料過濾器>混合

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

這個節點會根據材質 ID / 顏色 ID 映射組合多個材質，該貼圖可以從網格烘焙出來。 它最多需要 16 種不同的完整素材，並且在 Channels 群組中啟用的頻道類型。

節點在貼圖完整道具時非常有用，因為它允許材質完整參數化，同時動態組合所有材質。 非常適合貼圖製作簡單到複雜的道具，且有適當的 ID 烘焙，甚至能製作完全符合團隊標準的「模板」物質。

請記得，使用這個時，材料1、槽位1永遠是預設材質，且會出現在沒有其他材質的地方。 這就是為什麼你無法為它設定顏色。 如果你想保守一點，可以 [像插入設定成粗黑的基底材質](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/base-material/base-material.md) 。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>1-16 個完整材料欄位</b> | 槽位數量由 <b>材料</b> 下拉選單決定。 |
| <b>色彩識別</b> <i>色彩輸入</i> | 烘焙色彩識別地圖。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>材料</b> <i>2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16</i> | 設定最多可混合不同材料的數量。 |
| <b>頻道</b> | 在這個群組中切換材質通道，例如使用鏡面/光澤貼圖而非金屬/粗糙度時。 |
| <b>材料2-16</b> | 每個啟用的材料都會出現一個群組。 |
| <b>顏色</b> <i>（色彩值）</i> | 從ID地圖中選擇與此材料槽相符的顏色。 |
| <b>模糊感</b> <i>0.01 - 1.0</i> | 滲透到鄰近的顏色中。 |
| <b>填充物</b> <i>0.0 - 1.0</i> | 過渡的硬度：遮罩對比度。 |
