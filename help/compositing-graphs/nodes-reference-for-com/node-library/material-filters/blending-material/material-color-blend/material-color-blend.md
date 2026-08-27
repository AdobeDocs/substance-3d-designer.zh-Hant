---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/blending-material/material-color-blend.html"
breadcrumb-title: ''
description: 使用 Material Color Blend 節點來混合材質間的色彩通道，以創造複合材質效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Blending (Material) > Material Color Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 材質顏色混合
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 2%

---


# 材質顏色混合

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](material-color-blend.resources/material-color-blend.png){width="128px"}

<b>收錄於：</b> 材料過濾器>混合

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

此節點允許透過在上方混合純色來調整多通道全材質。 這是與[材質調整混合](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/material-adjustment-blend/material-adjustment-blend.md)的主要差異，後者只允許[&#128279;](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/levels/levels.md)對通道進行等級調整，而這個節點則使用[&#128279;](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md)純色混合類型的調整。

這個節點最有用的地方，是你想在漫射色或基色中加入平面色提示，或是想用固定的實色值「平整」其他通道時。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>ColorID</b> <i>色彩輸入</i> | 遮罩槽用於遮蔽節點的效果。 |
| <b>灰階面具</b> <i>灰階輸入</i> | 遮罩槽用於遮蔽節點的效果。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>頻道</b> | 例如，當使用 Specular/Glossiness 貼圖而非金屬/粗糙度時，可以切換這組材質通道的開關。 |
| <b>彌漫</b> |  |
| <b>顏色</b> <i>（色彩值）</i> | 要在擴散通道上混合哪個色彩值。 |
| <b>不透明度</b> <i>0.0 - 1.0</i> | 融合前景與背景的不透明度。 |
| <b>混合模式</b> <i>法線、加法、減法、乘法、加法/加法、加法、最小值、切換</i> | 在操作中使用混合模式。 |
| <b>底色</b> | 在這個通道上方混合純色，並有選項，就像擴散組一樣。 |
| <b>正常</b> |  |
| <b>資料來源</b> <i>身高，面具</i> |  |
| <b>混合模式</b> <i>結合、混合</i> |  |
| <b>高度強度</b> <i>0.0 - 1.0</i> |  |
| <b>高度不透明度</b> <i>0.0 - 1.0</i> |  |
| <b>節目形式</b> <i>DirectX、OpenGL</i> |  |
| <b>鏡面鏡面</b> | 在這個通道上方混合純色，並有選項，就像擴散組一樣。 |
| <b>發射體</b> | 在這個通道上方混合純色，並有選項，就像擴散組一樣。 |
| <b>光澤</b> | 在這個通道上方混合純色，並有選項，就像擴散組一樣。 |
| <b>粗糙度</b> | 在這個通道上方混合純色，並有選項，就像擴散組一樣。 |
| <b>金屬</b> | 在這個通道上方混合純色，並有選項，就像擴散組一樣。 |
| <b>鏡面層級</b> | 在這個通道上方混合純色，並有選項，就像擴散組一樣。 |
| <b>環境遮蔽</b> | 在這個通道上方混合純色，並有選項，就像擴散組一樣。 |
| <b>高度</b> | 在這個通道上方混合純色，並有選項，就像擴散組一樣。 |
| <b>不透明度</b> | 在這個通道上方混合純色，並有選項，就像擴散組一樣。 |
| <b>色彩識別面罩</b> <i>錯誤/真實</i> | 使用色彩識別遮罩代替灰階遮罩。 請記住，這只適用於一種顏色！<br><br>啟用以下所有選項。 |
| <b>顏色</b> <i>（色彩值）</i> | 選擇哪種顏色並轉換成白色。 |
| <b>模糊感</b> <i>0.01 - 1.0</i> | 你選的顏色與鄰近顏色融合的程度。 |
| <b>填充物</b> <i>0.0 - 1.0</i> | 你選的顏色的過渡對比。 |
