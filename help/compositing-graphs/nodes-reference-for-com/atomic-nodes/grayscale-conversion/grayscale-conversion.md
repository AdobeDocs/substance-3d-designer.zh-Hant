---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/grayscale-conversion.html"
breadcrumb-title: ''
description: 使用灰階轉換節點，利用各種轉換方法將色彩紋理轉換成灰階。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Grayscale conversion
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 灰階轉換
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 1%

---


# 灰階轉換

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![原子節點：灰階轉換](../../../../assets/comp_grayscaleconversion_1.png "原子節點：灰階轉換"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

透過權重每個色通道的亮度，將彩色影像轉換為灰階。

此節點可作為優化方法，從彩色影像中擷取灰階通道，方法是將所有「通道權重」值設為 0，唯獨期望通道應設為 1。

</td>
</tr>
</table>

大多數節點可設定為灰階或彩色輸出，且因簡潔與效能考量，灰階較為優先。

確實，建議一開始就使用灰階，然後在工作流程中再上色，例如使用 [漸層地圖](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/gradient-map/gradient-map.md) 節點。

這表示灰階轉換節點通常只保留在你特別想將彩色影像轉換成灰階的情況下。 在這些情況下，也可以看看 [灰階轉換進階](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/grayscale-conversion-adv/grayscale-conversion-advanced.md) 和 [色彩轉遮罩](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/color-to-mask/color-to-mask.md)。

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

## 參數

</td>
<td style="border: 0;" valign="top">

### 輸入連接器

</td>
<td style="border: 0;" valign="top">

### 輸出連接器

</td>
<td style="border: 0;" valign="top">

### 範例

</td>
</tr>
</table>

## 參數

|  |  |
| --- | --- |
| <b>通道權重</b> *Float4* | 設定每個 RGBA 通道在灰階轉換中的權重。   預設情況下，RGB 通道會平均分配。 |
| <b>壓扁阿爾法</b> *布林值* | 設定 Alpha 在最終灰階結果上的行為，因為灰階值無法包含 Alpha 資訊。   當為真&#x200B;*時*，灰階轉換會與輸入影像的 Alpha 通道相乘 |
| <b>背景值</b> *浮標* | 當輸入有 alpha 遮罩時，設定基礎背景值。 也就是說，決定哪些像素應被視為透明。   *當「Flatten alpha」設為「True」時可用。* |

## 輸入連接器

|  |  |
| --- | --- |
| <b>輸入</b> *色彩 原色* | 要處理的彩色影像。 |

## 輸出連接器

|  |  |
| --- | --- |
| <b>產出</b> *灰階* |  |

## 範例

*即將推出。*
