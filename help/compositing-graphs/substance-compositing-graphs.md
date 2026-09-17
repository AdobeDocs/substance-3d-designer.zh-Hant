---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs.html"
breadcrumb-title: ""
description: 學習 Substance 3D Designer 中的 Substance 合成圖，用於建立程序貼圖與材質工作流程。
helpx_creative_field: ""
helpx_description: Designer > Substance graphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 物質圖
user-guide-description: ""
user-guide-title: ""
source-git-commit: c460f605a97021efd2143941c28a977e12452299
workflow-type: tm+mt
source-wordcount: '345'
ht-degree: 0%
---

# 物質圖

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

[![](substance-compositing-graphs.resources/graph-5.png){width="120px"}](https://substance3d.adobe.com/)

</td>
<td width="100.00%" style="border: 0;" valign="top">

[Substance 圖](https://substance3d.adobe.com/) 是 Substance 3D Designer 中主要建立的圖形類型。 它們的目的是產生 <b>並處理不受固定解析度、顏色或形狀限制的二維影像資料</b> 。 它們是極具多功能性的影像處理與生成工具，而非靜態預設結果。

結果可以是簡單的黑白圖案、只在其他圖片上運行且不會自動產生內容的濾鏡，甚至是擁有多個通道的完整程序化素材。

Substance 圖是[支援最廣泛的圖](../getting-started/overview/overview.md)類型，可以匯出並用於各種不同的工作流程。

</td>
</tr>
</table>

## 範例

以下是一些常見的使用案例範例。

+++簡單的形狀
![Substance 圖中的簡單形狀 Substance 圖](substance-compositing-graphs.resources/simpleshape.png "中的簡單"){width="512px"}



貼紙的遮罩形狀是透過產生[一段文字](../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md) 和 [一個圓盤形狀](../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape/shape.md)， [從圓盤中提取邊緣](../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/edge-detect/edge-detect.md) ，最後 [將它們混合在一起](../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md) ，然後設定為最終 [輸出](../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)。

帶有數字或邊緣厚度的文字可以外部曝光，使圖表更具動態性。

+++

+++調整濾波器
![Substance 圖](substance-compositing-graphs.resources/simplefilter.png "中的調整濾波器 Substance 圖中的調整濾波器"){width="512px"}



濾波圖會將法線貼圖作為 [輸入](../compositing-graphs/nodes-reference-for-com/atomic-nodes/input-color/input-color.md) （並有自訂預覽）， [將其轉換為曲率](../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-smooth/curvature-smooth.md) ，然後 [調整對比](../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md) 度，產生一個凸邊遮罩作為最終 [輸出](../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)。

直方圖中設定的對比值可以被曝光，這使得這個濾波器與動態輸入槽結合使用時，既簡單又實用。

+++

+++完整內容
![Substance 圖表](substance-compositing-graphs.resources/simplematerial.png "中的完整內容 Substance 圖表中完整資料"){width="512px"}



更複雜的圖表[則結合了兩種基底材質](../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/material-blend/material-blend.md)。 一個[基底材質](../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/base-material/base-material.md) 保持簡單，另一個則用一些自訂輸入來增加趣味。 遮罩用來判斷兩種材料中哪一種在被設定為最終 [輸出](../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)前出現的位置。

本範例利用 [連結建立模式](../interface/the-graph-view/link-creation-modes/link-creation-modes.md) 來簡化使用多條連結。

+++
