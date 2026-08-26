---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/atomic-function-nodes/sampler-nodes.html"
breadcrumb-title: ''
description: 在 Substance 3D Designer 功能圖中存取取樣節點，取樣貼圖並提取色彩值。
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Samplers
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 取樣器
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 0%

---


# 取樣節點

![取樣節點取](../../../../assets/image2016-1-12-14-45-43.png "樣器節點")

這些節點會在輸入影像中取樣給定的二維座標：

<b>Sample Gray</b> 在灰階影像中，從輸入 <b>位置</b> 取樣一個亮度值，並以 <b>Float</b> 值輸出。

<b>樣本色彩</b>取樣於彩色影像中輸入位置</b>取樣 RGBA 值<b>，並輸出為 <b>Float4</b> 值，其中 R、G、B 與 A 分量分別映射至 X、Y、Z 和 W 分量。

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

座標從輸入的左上角開始，水平和垂直範圍介於 0 到 1。

超出此範圍的位置則依據所選 <b>定的位址模式</b> （見下文）處理。

</td>
<td width="33.33%" style="border: 0;" valign="top">

![像素座標](../../../../assets/samplercoords.png "像素座標")

</td>
</tr>
</table>

>[!NOTE]
>
> <b>Position</b> 輸入應該是 Float2 值，影像的 X 和 Y 座標分別對應到 X 和 Y 分量

## 參數

+++輸入影像
讓你可以選擇要用哪個節點輸入來取樣。

該清單會根據目前連接的輸入動態調整。 這表示在連接節點輸入時會新增條目。

輸入的編號從 0 開始，因此連接到節點第一個輸入的影像會被列為 *輸入影像 0*。

+++

+++過濾模式
讓你可以定義當取樣影像中的像素因解析度差異而無法完全對應到輸出影像時，如何處理插值。

<b>最近的</b>\
像素會依照原樣&#x200B;*映射到目標*，並匹配到對應座標。若目標解析度較低，該像素可能會被完全忽略。 若目標解析度較高;則會映射至涵蓋其跨度的所有像素。 輸出會 *更* 清晰，會看起來有點 *鋸齒*。

<b>雙線性濾波</b>\
對來源影像施加濾波處理，使其像素映射到目標解析度 *，以平滑* 像素間的過渡。 輸出較 *為平滑* ，且看起來會稍微 *模糊*。

+++

+++位址模式
控制 [0;1] 範圍外的位置值如何處理。

<b>重複</b>\
隨著值增加，迴圈超過[0;1]範圍。\
例如：3.4 是 0.4，-1.7 是 0.3。

<b>夾具到邊緣</b>\
將數值從 [0;1] 範圍到最接近的極限。\
例如：0.3.4 是 1，-1.7 是 0。

+++
