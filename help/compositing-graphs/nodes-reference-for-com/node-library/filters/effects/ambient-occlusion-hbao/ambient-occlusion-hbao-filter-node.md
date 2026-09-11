---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/ambient-occlusion-hbao-filter-node.html"
breadcrumb-title: ''
description: 使用環境遮蔽 HBAO 濾鏡節點，利用基於地平線的演算法生成環境遮蔽貼圖，呈現逼真的陰影效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Ambient Occlusion (HBAO) (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 環境遮蔽（HBAO）（濾波節點）
user-guide-description: ''
user-guide-title: ''
source-git-commit: 132a27ad47b0272a877b913eaa7957ccf8b549fd
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 5%

---


# 環境遮蔽（HBAO）（濾波節點）

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](ambient-occlusion-hbao-filter-node.resources/hbao.png){width="128px"}

<b>收錄於：</b> 濾鏡>效應

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

輸入高度圖，並產生環境遮蔽圖。 它使用基於地平線的環境遮蔽演算法，該演算法最初用於螢幕空間即時 AO 生成。 對於從程序式高度圖製作程序式AO地圖非常有用。

關於另一種更進階但較慢的 AO 版本，請參見 [環境遮蔽（RTAO）](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/ambient-occlusion-rtao/ambient-occlusion-rtao.md)

</td>
</tr>
</table>

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>使用世界單位</b> <i>錯誤/真實</i> | 切換使用世界或場景空間單元。 能提供額外參數，讓控制更精確。 |
| <b>高度深度</b> <i>0.0 - 1.0</i> | 僅在世界單位設定為 False 時使用。 控制全域縮放。 |
| <b>表面積</b> <i>0.0 - 1000.0</i> | 僅在世界單位設定為 True 時使用。 控制全域縮放。 |
| <b>身高比例（公分）</b> <i>0.0 - 1000.0</i> | 僅在世界單位設定為 True 時使用。 控制全域縮放。 |
| <b>半徑</b> <i>0.0 - 1.0</i> | 控制AO的擴散。 |
| <b>品質</b> <i>4個樣本，8個樣本，16個樣本</i> | 透過計算所用樣本數量來設定品質等級。 |
| <b>GPU 優化</b> <i>錯誤/真實</i> | 能實現內部 GPU 優化，加速處理速度。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="ambient-occlusion-hbao-filter-node.resources/image2021-6-18-11-11-11-1.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="ambient-occlusion-hbao-filter-node.resources/image2021-6-18-11-11-22.png" />
        </td>
    </tr>
</table>
