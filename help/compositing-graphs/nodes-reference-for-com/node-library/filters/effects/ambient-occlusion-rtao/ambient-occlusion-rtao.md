---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/ambient-occlusion-rtao.html"
breadcrumb-title: ''
description: 使用環境遮蔽（RTAO）節點，從高度圖產生即時環境遮蔽貼圖，以達到逼真的陰影效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Ambient Occlusion (RTAO)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 環境遮蔽（RTAO）
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 0%

---


# 環境遮蔽（RTAO）

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![RTAO 節點圖示](../../../../../../assets/rt-ao.png "RTAO 節點圖示")

<b>收錄於：</b> *濾鏡/效果*

</td>
<td width="58.30%" style="border: 0;" valign="top">

## 說明

根據高度圖輸入產生環境遮蔽圖。

此濾波器相較於 HBAO 能提供更精確的結果，但因計算時間限制，不宜與 CPU（SSE）引擎搭配使用。

請參見 [環境遮蔽（HBAO）（濾波節點）](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/ambient-occlusion-hbao/ambient-occlusion-hbao-filter-node.md) 以獲得更快且簡單的替代方案。

</td>
</tr>
</table>

## 參數

<b>使用物理大小</b> *布林值*\
切換到使用實體尺寸設定來決定身高比例。

<b>物理大小</b> *Float3*（當 <b>使用物理大小</b>設為 *True*）\
根據表面的實際物理大小調整高度比例

<b>取樣&#x200B;</b>*整數*\
計算環境遮蔽所使用的光線數量。\
較高的數值能提供更平滑且精確的結果，但會犧牲性能。

<b>高度比例</b> *浮點*（當<b>使用實體尺寸</b>設為 *False* 時可用）\
乘數表示高度圖輸入的強度。

<b>分布</b> *整數*&#x200B;設定分配方法。 影響陰影區域的衰減，

<b>最大距離</b> *浮球*\
設定光線可被遮蔽的最大距離。

<b>擴散角</b> *浮球*\
設定射線的擴散角度。 值為1則是一個完整的半球。

## 範例圖片

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![RTAO 節點 - 範例 1](../../../../../../assets/image2021-6-18-11-7-48.png "RTAO 節點 - 範例 1")

</td>
<td style="border: 0;" valign="top">

![RTAO 節點 - 範例 2](../../../../../../assets/image2021-6-18-11-9-0-1.png "RTAO 節點 - 範例 2")

</td>
</tr>
</table>
