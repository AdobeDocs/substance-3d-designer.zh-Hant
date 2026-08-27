---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape-mapper.html"
breadcrumb-title: ''
description: 使用 Shape Mapper 節點將形狀映射到貼圖上，並可自訂變換和位置。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Shape mapper
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 形狀映射器
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 1%

---


# 形狀映射器

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![形狀映射器 - 圖示](shape-mapper.resources/shape_mapper.png "形狀映射器 - 圖示"){width="200px"}

<b>收錄於：</b> 紋理產生器>圖案

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

將輸入影像投影到圓形或多邊形上。

投影會使影像變形，使其符合形狀輪廓，並使其精確地嵌入指定次數且無空隙。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>輸入</b> <i>灰階</i> | 圖案應該放在形狀上。 |

<a name="outputs"></a>

## 輸出

|  |  |
|:---|:---|
| <b>產出</b> <i>灰階</i> | 這是將圖案投影到形狀上的灰階點陣圖。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>形狀</b> <i>整數</i> | 規定圖案應依何形狀排列：<ul data-preserve-html="true"> <li data-preserve-html="true">圓形</li> <li data-preserve-html="true">多邊形</li> </ul> |
| <b>圖案數量</b> <i>整數</i> | 沿著選定形狀放置的圖案數量。 |
| <b>連結段落與圖案數量</b> <i>布林值</i>   *當「形狀」設為「多邊形」時可用* | 用<b>圖案數量</b>來表示分段</b>數量<b>。這樣可以防止圖案繞過轉角，確保外觀筆直且一致。 |
| <b>單元</b> <i>整數</i>   *當「形狀」設為「多邊形」且「與圖案數量連結分段」設為「假」時可用* | 多邊形中放置圖案的段數。   線段大小均&#x200B;**&#x200B;等，所有頂點距離中心等&#x200B;**&#x200B;距，因此線段數量增加會使多邊形收斂成圓。 |
| <b>半徑</b> <i>浮標</i> | 形狀半徑的乘數，1.0 是影像最短邊長的一半。 |
| <b>寬度</b> <i>浮標</i> | 一個乘數，表示沿形狀圖案的寬度，其中1.0是影像最短邊長的一半。 |
| <b>旋轉</b> <i>浮標</i> | 從水平右邊順時針方向旋轉的旋轉量。 |
| <b>一對二翻</b> <i>布林值</i> | 每隔一個形狀垂直翻轉一個。 |
| <b>過濾模式</b> <i>整數</i> | 對排列在形狀上的圖案所採用的過濾方法：<ul data-preserve-html="true"> <li data-preserve-html="true"><i>最近：</i> 直接套用最近投影像素的值，使畫面更清晰但帶有鋸齒。</li> <li data-preserve-html="true"><i>雙線性：</i> 應用雙線性濾波器將投影像素與鄰近像素插值，呈現更平滑但模糊的畫面。</li> </ul> |
| <b>非平方展開</b> <i>布林值</i> | 在非正方形影像中，保持產生的形狀方正，並將影像生成擴展到影像的邊界。 |

## 範例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
