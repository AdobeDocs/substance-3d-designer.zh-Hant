---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/material-clone-patch.html"
breadcrumb-title: ''
description: 使用 Material Clone Patch 節點來克隆並修補掃描材質中修復瑕疵的貼圖區域。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Material Clone Patch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 物質複製補丁
user-guide-description: ''
user-guide-title: ''
source-git-commit: ca90755a159a7e0297bb26d1e3522b0cfeb6f2ac
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 4%

---


# 物質複製補丁

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/clone-patch-material.png){width="128px"}

<b>收錄於：</b> 《材料濾>掃描處理》

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

這是多頻道完整素材版本的 [《Clone Patch](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md)》。 它會對材料的任何通道執行克隆補丁。 [更多資訊請參閱原版！](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md)

如果你想從材質的所有通道中移除細節，這非常有用。 輸出會針對多個聲道進行除錯影像，精確查看智慧音色區域的樣貌。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>面具</b> <i>灰階輸入</i> | 遮罩槽用於遮蔽節點的效果。 可以用「遮罩」參數切換。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>頻道</b> | 在這個群組中切換材質通道，例如使用鏡面/光澤貼圖而非金屬/粗糙度時。 |
| <b>形狀</b> <i>方形、圓盤</i> | 定印章形狀。 只當作基礎使用。 |
| <b>Edge</b> |  |
| <b>閾值（多通道）</b> <i>0.0 - 1.0</i> | 設定混合區域應該延伸到多遠。 這種現象會沿著目標區域的形狀逐步成長，因此在均勻背景下幾乎沒有影響。 要小心不要在不同頻道間調整太多，否則可能會導致視覺差異！ |
| <b>模糊</b> <i>0.0 - 2.0</i> | 若需要較柔和的過渡，則模糊印章區域的邊緣。 |
| <b>平滑度</b> <i>0.0 - 2.0</i> | 郵票形狀邊緣圓潤，使輪廓更流暢流暢。 |
| <b>網格解析</b> <i>1 - 11</i> | 設定混合分析的品質解析度。 較高的數值代表融合更準確。 |
| <b>變換</b> |  |
| <b>來源矩陣</b> <i>（變換矩陣）</i> | 變換來源（縮放與旋轉）。 無法在 Canvas 上進行，只能透過這些參數來改變。 |
| <b>來源偏移</b> <i>-0.5 - 0.5</i> | 翻譯來源位置。 無法在 Canvas 上進行，只能透過這些參數來改變。 *這個參數大概是你最想改變的！* |
| <b>目標矩陣</b> <i>（變換矩陣）</i> | 轉換目標位置（縮放與旋轉）。 也可以用 Gizmo 在畫布上來完成。 |
| <b>目標偏移</b> <i>-0.5 - 0.5</i> | 翻譯目標位置。 也可以用 Gizmo 在畫布上來完成。 |
