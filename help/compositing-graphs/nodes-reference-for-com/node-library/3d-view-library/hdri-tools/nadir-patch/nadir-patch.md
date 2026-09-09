---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/nadir-patch.html"
breadcrumb-title: ''
description: 使用 Nadir Patch 節點來修補 HDRI 全景圖的 Nadir 區域，以修正環境地圖底部的瑕疵。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Nadir Patch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 低谷補丁
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9aaf135d4c336ea0cff865524ad1ccd5dcc225bd
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 5%

---


# 低谷補丁

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](nadir-patch.resources/panorama-nadir-patch.png){width="200px"}

<b>收錄於：</b> HDRI 工具> 3D 視圖

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

此節點提供連接球面映射影像中央基點（天頂）的功能。 它可以用來隱藏或「複製」醜陋的天底，或可見的相機或三腳架。 它的運作方式類似 [複製補丁](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md)，但可以調整球面映射影像。 使用者選擇影像中其他位置的點，即克隆並混合的底部點。 處理時不需要其他外部輸入，只需單一 HDRI，但可使用外部遮罩作為音色效果的 alpha。

效果可透過 Nadir 萃取[&#128279;](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/hdri-tools/nadir-extract/nadir-extract.md)快速檢查與驗證。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>輸入</b> <i>色彩輸入</i> |  |
| <b>遮罩輸入</b> <i>灰階輸入</i> | 可選的遮罩槽用於遮罩音色。 像個阿爾法一樣行事。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>啟用</b> <i>錯誤/真實</i> | 啟用或關閉補丁效果。 |
| <b>顯示幀輔助工具</b> <i>錯誤/真實</i> | 請顯示或隱藏輔助行，方便除錯。 |
| <b>框架厚度</b> <i>0.0 - 1.0</i> | 輔助線的厚度。 |
| <b>Patch 尺度</b> <i>0.0 - 1.0</i> | 全局且均勻的紋章比例。 影響來源和目標。 |
| <b>補丁大小</b> <i>0.0 - 1.0</i> | 貼片大小不均。 |
| <b>補丁旋轉</b> <i>0.0 - 1.0</i> | 補丁輪替。 影響來源和目標。 |
| <b>Patch Alpha</b> <i>平方形、高斯、遮罩輸入</i> | 設定用來將音色與背景融合的 alpha 值。 |
| <b>斑塊硬度</b> <i>0.0 - 1.0</i> | 設定硬度/α 對比度。 |
| <b>源旋轉偏移量</b> <i>0.0 - 1.0</i> | 只有補丁來源會輪流使用。 |
| <b>位置座標</b> |  |
| <b>來源位置</b> | 來源位置。 在2D視角下有把手。 |
| <b>音色位置</b> | 目標位置。 在2D視角下有把手。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="nadir-patch.resources/nadir-patch-ex.gif" />
        </td>
    </tr>
</table>
