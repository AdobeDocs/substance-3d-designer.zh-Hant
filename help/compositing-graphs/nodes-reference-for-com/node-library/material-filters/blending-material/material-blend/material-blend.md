---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/blending-material/material-blend.html"
breadcrumb-title: ''
description: 使用 Material Blend 節點，利用遮罩將整個材質混合在一起，創造複合材質效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Blending (Material) > Material Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 材料混合
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '458'
ht-degree: 6%

---


# 材料混合

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](material-blend.resources/material-blend.png){width="128px"}

<b>收錄於：</b> 材料過濾器>混合

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

Material Blend 是多通道、全材質的原子混合節點[&#128279;](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md)等價物。它會在兩個完整材質（可能的通道）之間混合，這些材質基於灰階遮罩，或是可選地基於 Color ID 遮罩中的單一顏色。

如果你想混合兩個材質，並且有灰階貼圖但沒有完整的 Color ID 烘焙，這個節點很有用。 如果你有 Color ID 烘焙，想要混合超過兩種材質，我們建議你使用 [Multi-Material Blend](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/multi-material-blend/multi-material-blend.md)。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>ColorID</b> <i>色彩輸入</i> | 可選的烘焙色彩識別地圖。 |
| <b>灰階面具</b> <i>灰階輸入</i> | 遮罩槽用於遮蔽節點的效果。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>頻道</b> | 例如，當使用 Specular/Glossiness 貼圖而非金屬/粗糙度時，可以切換這組材質通道的開關。 |
| <b>彌漫</b> |  |
| <b>不透明度</b> <i>0.0 - 1.0</i> | 前景與背景之間的不透明度融合 |
| <b>混合模式</b> <i>法線、加法、減法、乘法、加法/加法、加法、最小值、切換</i> |  |
| <b>底色</b> |  |
| <b>不透明度</b> <i>0.0 - 1.0</i> | 前景與背景之間的不透明度融合 |
| <b>混合模式</b> <i>法線、加法、減法、乘法、加法/加法、加法、最小值、切換</i> |  |
| <b>正常</b> |  |
| <b>不透明度</b> <i>0.0 - 1.0</i> | 前景與背景之間的不透明度融合 |
| <b>鏡面鏡面</b> |  |
| <b>不透明度</b> <i>0.0 - 1.0</i> | 前景與背景之間的不透明度融合 |
| <b>混合模式</b> <i>法線、加法、減法、乘法、加法/加法、加法、最小值、切換</i> |  |
| <b>發射體</b> |  |
| <b>不透明度</b> <i>0.0 - 1.0</i> | 前景與背景之間的不透明度融合 |
| <b>混合模式</b> <i>法線、加法、減法、乘法、加法/加法、加法、最小值、切換</i> |  |
| <b>光澤</b> |  |
| <b>不透明度</b> <i>0.0 - 1.0</i> | 前景與背景之間的不透明度融合 |
| <b>混合模式</b> <i>法線、加法、減法、乘法、加法/加法、加法、最小值、切換</i> |  |
| <b>粗糙度</b> |  |
| <b>不透明度</b> <i>0.0 - 1.0</i> | 前景與背景之間的不透明度融合 |
| <b>混合模式</b> <i>法線、加法、減法、乘法、加法/加法、加法、最小值、切換</i> |  |
| <b>金屬</b> |  |
| <b>不透明度</b> <i>0.0 - 1.0</i> | 前景與背景之間的不透明度融合 |
| <b>混合模式</b> <i>法線、加法、減法、乘法、加法/加法、加法、最小值、切換</i> |  |
| <b>鏡面層級</b> |  |
| <b>不透明度</b> <i>0.0 - 1.0</i> | 前景與背景之間的不透明度融合 |
| <b>混合模式</b> <i>法線、加法、減法、乘法、加法/加法、加法、最小值、切換</i> |  |
| <b>環境遮蔽</b> |  |
| <b>不透明度</b> <i>0.0 - 1.0</i> | 前景與背景之間的不透明度融合 |
| <b>混合模式</b> <i>法線、加法、減法、乘法、加法/加法、加法、最小值、切換</i> |  |
| <b>高度</b> |  |
| <b>不透明度</b> <i>0.0 - 1.0</i> | 前景與背景之間的不透明度融合 |
| <b>混合模式</b> <i>法線、加法、減法、乘法、加法/加法、加法、最小值、切換</i> |  |
| <b>不透明度</b> |  |
| <b>不透明度</b> <i>0.0 - 1.0</i> | 前景與背景之間的不透明度融合 |
| <b>混合模式</b> <i>法線、加法、減法、乘法、加法/加法、加法、最小值、切換</i> |  |
| <b>色彩識別面罩</b> <i>錯誤/真實</i> | 使用色彩識別遮罩代替灰階遮罩。 請記得這只適用於一種顏色！ |
| <b>顏色</b> <i>（色彩值）</i> | 選擇哪種顏色並轉換成白色。 |
| <b>模糊感</b> <i>0.01 - 1.0</i> | 你選的顏色和鄰近顏色融合的程度。 |
| <b>填充物</b> <i>0.0 - 1.0</i> | 你選的顏色的過渡對比。 |
