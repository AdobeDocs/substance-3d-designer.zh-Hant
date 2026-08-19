---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/bent-normal.html"
breadcrumb-title: ''
description: 使用 Bent Normal 節點來產生 Bent 法線貼圖，以考慮環境光遮蔽和間接光照。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Bent Normal
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 彎曲正常
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---


# 彎曲正常

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![彎曲的 法線節點圖示](../../../../../../assets/rt-bent-normal.png "彎曲的法線 節點圖示")

<b>收錄於：</b> *濾波器/法線貼圖*

</td>
<td width="58.30%" style="border: 0;" valign="top">

## 說明

根據高度圖輸入產生彎曲法線貼圖。 彎曲法線貼圖是法向[&#128279;](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md)與環境遮蔽（RTAO）[&#128279;](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/ambient-occlusion-rtao/ambient-occlusion-rtao.md)的特殊版本，能產生帶有嵌入環境遮蔽的法線貼圖。\
這可以在即時引擎中使用，將環境遮蔽（Ambient Occlusion）內建於法線貼圖中，例如為了更精確地反映金屬的遮蔽反射。

由於計算時間，此節點不應與 CPU（SSE）引擎搭配使用。

</td>
</tr>
</table>

## 參數

<b>使用物理大小</b> *布林值*\
切換到使用實體尺寸設定來決定身高比例。

<b>物理大小</b> *Float3* （當 <b>使用物理大小</b> 設為 *True*）\
根據表面的實際物理大小調整高度比例。

<b>取樣</b> *整數*\
計算彎曲法線所需的射線數量。\
較高的音效能提供更平順且精準的結果，但性能會有所下降。

<b>高度比例</b> *浮點（當使用實體尺寸設為 False 時可用）*\
乘數表示高度圖輸入的強度。

<b>分布整</b> *數*\
設定分配方式。 影響陰影區域的衰減。

<b>最大距離</b> *浮球*\
設定光線可被遮蔽的最大距離。

<b>擴散角</b> *浮球*\
設定射線的擴散角度。 值為1則是一個完整的半球。

<b>標準格式</b> *整數*\
將輸出的綠色通道反轉。

## 範例圖片

![彎曲的法線節點 - 範例 1](../../../../../../assets/bent-normal-ex-1.jpg "彎曲的法線節點 - 範例 1")
