---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/blending-material/material-blend.html"
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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '469'
ht-degree: 0%

---


# 材料混合

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/material-blend.png){width="128px"}

## 材料混合

**收錄於：***材質濾鏡/混合*

**複合體**

</td>
<td style="border: 0;" valign="top">

## 說明

Material Blend 是多通道、全材質的原子混合節點[&#128279;](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md)等價物。它會在兩個完整材質（可能的通道）之間混合，這些材質基於灰階遮罩，或是可選地基於 Color ID 遮罩中的單一顏色。

如果你想混合兩個材質，並且有灰階貼圖但沒有完整的 Color ID 烘焙，這個節點很有用。 如果你有 Color ID 烘焙，想要混合超過兩種材質，我們建議你使用 [Multi-Material Blend](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/multi-material-blend/multi-material-blend.md)。

## 參數

### 輸入

* **ColorID**： *色彩輸入*\
  可選的烘焙色彩識別地圖。
* **灰階遮罩**： *灰階輸入*\
  遮罩槽用於遮蔽節點的效果。

### 參數

* **頻道**
  * 例如，當使用 Specular/Glossiness 貼圖而非金屬/粗糙度時，可以切換這組材質通道的開關。
* **彌漫**
  * **不透明度**： *0.0 - 1.0*\
    前景與背景之間的不透明度融合
  * **混合模式**： *正常、加法、減法、乘法、加/加、加/壓、最大、最小、切換*
* **底色**
  * **不透明度**： *0.0 - 1.0*\
    前景與背景之間的不透明度融合
  * **混合模式**： *正常、加法、減法、乘法、加/加、加/壓、最大、最小、切換*
* **正常**
  * **不透明度**： *0.0 - 1.0*\
    前景與背景之間的不透明度融合
* **鏡面鏡面**
  * **不透明度**： *0.0 - 1.0*\
    前景與背景之間的不透明度融合
  * **混合模式**： *正常、加法、減法、乘法、加/加、加/壓、最大、最小、切換*
* **發射體**
  * **不透明度**： *0.0 - 1.0*\
    前景與背景之間的不透明度融合
  * **混合模式**： *正常、加法、減法、乘法、加/加、加/壓、最大、最小、切換*
* **光澤**
  * **不透明度**： *0.0 - 1.0*\
    前景與背景之間的不透明度融合
  * **混合模式**： *正常、加法、減法、乘法、加/加、加/壓、最大、最小、切換*
* **粗糙度**
  * **不透明度**： *0.0 - 1.0*\
    前景與背景之間的不透明度融合
  * **混合模式**： *正常、加法、減法、乘法、加/加、加/壓、最大、最小、切換*
* **金屬**
  * **不透明度**： *0.0 - 1.0*\
    前景與背景之間的不透明度融合
  * **混合模式**： *正常、加法、減法、乘法、加/加、加/壓、最大、最小、切換*
* **鏡面層級**
  * **不透明度**： *0.0 - 1.0*\
    前景與背景之間的不透明度融合
  * **混合模式**： *正常、加法、減法、乘法、加/加、加/壓、最大、最小、切換*
* **環境遮蔽**
  * **不透明度**： *0.0 - 1.0*\
    前景與背景之間的不透明度融合
  * **混合模式**： *正常、加法、減法、乘法、加/加、加/壓、最大、最小、切換*
* **高度**
  * **不透明度**： *0.0 - 1.0*\
    前景與背景之間的不透明度融合
  * **混合模式**： *正常、加法、減法、乘法、加/加、加/壓、最大、最小、切換*
* **不透明度**
  * **不透明度**： *0.0 - 1.0*\
    前景與背景之間的不透明度融合
  * **混合模式**： *正常、加法、減法、乘法、加/加、加/壓、最大、最小、切換*
* **色彩識別遮罩**： *虛假/真實*&#x200B;使用 彩色識別遮罩代替灰階遮罩。 請記得這只適用於一種顏色！
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
