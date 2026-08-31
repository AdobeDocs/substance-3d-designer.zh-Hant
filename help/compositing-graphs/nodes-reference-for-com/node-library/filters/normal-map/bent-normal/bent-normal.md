---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/bent-normal.html"
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
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 1%

---


# 彎曲正常

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![彎曲的 法線節點圖示](bent-normal.resources/bent-normal-01.png "彎曲的法線 節點圖示")

<b>收錄於：</b> 法線貼圖>濾波器

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

根據高度圖輸入產生彎曲法線貼圖。 彎曲法線貼圖是法向[&#128279;](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md)與環境遮蔽（RTAO）[&#128279;](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/ambient-occlusion-rtao/ambient-occlusion-rtao.md)的特殊版本，能產生帶有嵌入環境遮蔽的法線貼圖。\
這可以在即時引擎中使用，將環境遮蔽（Ambient Occlusion）內建於法線貼圖中，例如為了更精確地反映金屬的遮蔽反射。

由於計算時間，此節點不應與 CPU（SSE）引擎搭配使用。

</td>
</tr>
</table>

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>使用物理尺寸</b> <i>布林值</i> | 切換到使用實體尺寸設定來決定身高比例。 |
| <b>實體尺寸</b> <i>Float3</i> | （可用時間 <b>使用物理尺寸</b> 設為 <i>True</i>）根據表面的真實物理尺寸調整高度比例。 |
| <b>取樣</b> <i>整數</i> | 計算彎曲法線的射線數量。<br>較高的數值能提供更平滑且精確的結果，但性能會有所損失。 |
| <b>身高比例</b> <i>浮標</i> | （當使用物理尺寸設為 False 時可用）高度圖輸入強度的乘數。 |
| <b>分布</b> <i>整數</i> | 設定分配方式。 影響陰影區域的衰減。 |
| <b>最大距離</b> <i>浮標</i> | 設定光線可被遮蔽的最大距離。 |
| <b>擴散角</b> <i>浮標</i> | 設定射線的擴散角度。 值為1則是一個完整的半球。 |
| <b>一般格式</b> <i>整數</i> | 將輸出的綠色通道反轉。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="bent-normal.resources/bent-normal-02.jpg" />
        </td>
    </tr>
</table>
