---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/blending-material/material-color-blend.html"
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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '466'
ht-degree: 0%

---


# 材質顏色混合

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/material-color-blend.png){width="128px"}

## 材質顏色混合

**收錄於：***材質濾鏡/混合*

**中級**

</td>
<td style="border: 0;" valign="top">

## 說明

此節點允許透過在上方混合純色來調整多通道全材質。 這是與[材質調整混合](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/material-adjustment-blend/material-adjustment-blend.md)的主要差異，後者只允許[](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/levels/levels.md)對通道進行等級調整，而這個節點則使用[](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md)純色混合類型的調整。

這個節點最有用的地方，是你想在漫射色或基色中加入平面色提示，或是想用固定的實色值「平整」其他通道時。

## 參數

### 輸入

* **ColorID**： *色彩輸入*\
  遮罩槽用於遮蔽節點的效果。
* **灰階遮罩**： *灰階輸入*\
  遮罩槽用於遮蔽節點的效果。

### 參數

* **頻道**
  * 例如，當使用 Specular/Glossiness 貼圖而非金屬/粗糙度時，可以切換這組材質通道的開關。
* **彌漫**
  * **色彩**：*（色彩值）*要在漫射通道上方混合哪個顏色值。
  * **不透明度**： *0.0 - 1.0*\
    融合前景與背景的不透明度。
  * **混合模式**： *正常、加法、減法、乘法、加壓、最大、最小、切換*&#x200B;混合模式，用於操作中。
* **底色**
  * 在這個通道上方混合純色，並有選項，就像擴散組一樣。
* **正常**
  * **資料來源**： *身高、面具*
  * **混合模式**： *合併、混合*
  * **身高強度**： *0.0 - 1.0*
  * **高度不透明度**： *0.0 - 1.0*
  * **格式**： *DirectX、OpenGL*
* **鏡面鏡面**
  * 在這個通道上方混合純色，並有選項，就像擴散組一樣。
* **發射體**
  * 在這個通道上方混合純色，並有選項，就像擴散組一樣。
* **光澤**
  * 在這個通道上方混合純色，並有選項，就像擴散組一樣。
* **粗糙度**
  * 在這個通道上方混合純色，並有選項，就像擴散組一樣。
* **金屬**
  * 在這個通道上方混合純色，並有選項，就像擴散組一樣。
* **鏡面層級**
  * 在這個通道上方混合純色，並有選項，就像擴散組一樣。
* **環境遮蔽**
  * 在這個通道上方混合純色，並有選項，就像擴散組一樣。
* **高度**
  * 在這個通道上方混合純色，並有選項，就像擴散組一樣。
* **不透明度**
  * 在這個通道上方混合純色，並有選項，就像擴散組一樣。
* **色彩識別遮罩**： *虛假/真實*&#x200B;使用 彩色識別遮罩代替灰階遮罩。 請記得這只適用於一種顏色！\
  啟用以下所有選項。
* **顏色**：*（顏色值）*選擇並轉換成白色的顏色。
* **模糊度**： *0.01 - 1.0*&#x200B;你選擇的顏色與鄰近顏色融合的程度。
* **填充**： *0.0 - 1.0*&#x200B;你選擇顏色的過渡對比度。

## 範例圖片

|  |
| --- |
| 本頁無附帶圖片。 |

</td>
</tr>
</table>
