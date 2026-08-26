---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/blend.html"
breadcrumb-title: ''
description: 使用 Blend 節點，利用各種混合模式將兩個材質混合在一起，以創造合成效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 混合
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '332'
ht-degree: 0%

---


# 混合

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![原子節點：混合](../../../../assets/comp_blend_1.png "原子節點：混合"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

使用指定的混合模式及可選遮罩將兩張影像合併。

它是所有原子節點中最有用的節點，幾乎你在 Substance 3D Designer](https://www.adobe.com/products/substance3d-designer.html) 中[建立的任何圖都會使用這個節點。

</td>
</tr>
</table>

它的功能類似於 Substance 3D Painter](https://www.adobe.com/products/substance3d-painter.html) 或 [Photoshop](https://www.adobe.com/ch_fr/products/photoshop/landpa.html) 中，兩個層層疊[疊，透過你在頂層設定的混合模式來混合。

>[!TIP]
>
> 在這個專門頁面](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blending-modes-des/blending-modes-description.md)中了解混合節點[中可用的混合模式。

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">



</td>
<td width="83.33%" style="border: 0;" valign="top">



</td>
<td width="100.00%" style="border: 0;" valign="top">



</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## 輸出連接器

</td>
<td style="border: 0;" valign="top">

### 範例

</td>
</tr>
</table>

## 參數

|  |  |
| --- | --- |
| <b>不透明度</b> *浮標* | 前景圖層的不透明度與背景融合。 它獨立於不透明度輸入運作，並作為額外的乘數。 |
| <b>混合模式</b> *整數*[靜態](../../../../glossary/glossary.md) | 設定要使用的混合操作。   請參閱 [專門的混合模式](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blending-modes-des/blending-modes-description.md)頁面。 |
| <b>Alpha 混合</b> *整數*[靜態](../../../../glossary/glossary.md) | 判斷當色彩輸入具有 Alpha 通道時的混合行為：<ul data-preserve-html="true"> <li data-preserve-html="true">使用來源 alpha</li> <li data-preserve-html="true">忽略 alpha</li> <li data-preserve-html="true">純α混合</li> <li data-preserve-html="true">預乘 alpha 混合</li> </ul> |
| <b>耕作區域</b> *Float4* [靜態](../../../../glossary/glossary.md) | 允許設定自訂裁切區域，作為額外的不透明度遮罩。 裁切的區域只顯示背景。 |

## 輸入連接器

|  |  |
| --- | --- |
| <b>前景</b> *灰階/彩色* | 混合操作的頂層或前景層。 |
| <b>背景</b> *灰階/彩色* 原色 | 混合操作的底層或背景層。 |
| <b>不透明度</b> *灰階* | 可選的 Alpha 遮罩輸入。 |

>[!IMPORTANT]
>
> 混合節點有動態輸入，會根據你的連線在灰階和色彩之間切換。<b> 混合節點只能混合兩個相同類型的</b>輸入。
> 
> 將彩色與灰階輸入連接到前景與背景，會導致虛線紅色連接線，表示計算錯誤。
> 
> 這是新手用戶在彩色與灰階連線時遇到問題的首要原因：務必確保兩種連接類型相同！

## 輸出連接器

|  |  |
| --- | --- |
| <b>產出</b> *灰階/彩色* |  |

## 範例

*即將推出。*
