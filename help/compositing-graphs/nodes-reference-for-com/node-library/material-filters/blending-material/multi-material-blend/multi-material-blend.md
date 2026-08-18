---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/blending-material/multi-material-blend.html"
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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 1%

---


# 多材料混合

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/multi-material-blend.png){width="128px"}

## 多材料混合

**收錄於：***材質濾鏡/混合*

**中級**

</td>
<td style="border: 0;" valign="top">

## 說明

這個節點會根據材質 ID / 顏色 ID 映射組合多個材質，該貼圖可以從網格烘焙出來。 它最多需要 16 種不同的完整素材，並且在 Channels 群組中啟用的頻道類型。

節點在貼圖完整道具時非常有用，因為它允許材質完整參數化，同時動態組合所有材質。 非常適合貼圖製作簡單到複雜的道具，且有適當的 ID 烘焙，甚至能製作完全符合團隊標準的「模板」物質。

請記得，使用這個時，材料1、槽位1永遠是預設材質，且會出現在沒有其他材質的地方。 這就是為什麼你無法為它設定顏色。 如果你想保守一點，可以 [像插入設定成粗黑的基底材質](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/base-material/base-material.md) 。

## 參數

### 輸入

* **1-16 個滿材料欄位**&#x200B;欄位數量由 **材料** 下拉選單決定。
* **色彩識別**&#x200B;碼： *色彩輸入*\
  烘焙色彩識別地圖。

### 參數

* **材料**： *2、3、4、5、6、7、8、9、10、11、12、13、14、15、16*&#x200B;設定可混合的材料數量上限。
* **頻道**\
  在這個群組中切換材質通道，例如使用鏡面/光澤貼圖而非金屬/粗糙度時。
* **材料 2-16**&#x200B;每啟用一個材料，會顯示一組。
  * **顏色**：*（顏色值）*從ID映射中選擇與此材質槽相符的顏色。
  * **模糊度**： *0.01 - 1.0*&#x200B;滲透到鄰近顏色中。
  * **填充：***0.0 - 1.0*&#x200B;過渡的硬度：遮罩對比度。

## 範例圖片

|  |
| --- |
| 本頁無附帶圖片。 |

</td>
</tr>
</table>
