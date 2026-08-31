---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/clone-patch.html"
breadcrumb-title: ''
description: 使用 Clone Patch 節點來克隆並修補掃描材料中的區域，以移除瑕疵和瑕疵。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Clone Patch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 複製人補丁
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '456'
ht-degree: 3%

---


# 複製人補丁

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](clone-patch.resources/clone-patch-01.png){width="128px"}

![](clone-patch.resources/clone-patch-02.png){width="128px"}

<b>收錄於：</b> 《材料濾>掃描處理》

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

Clone Patch 是一個程序化、參數化的「Clone Stamp」節點。 它將輸入的一個區域複製到另一個區域，隱藏可能不想要的細節。 雖然它不如在筆刷應用中使用熟悉工具那麼快速簡單，但它確實提供了非破壞性且能在節點式工作流程中運作的關鍵優勢。 此外，此節點會對目標區域與來源區域進行智慧分析，並嘗試根據對比度、明暗度與形狀盡可能融合。

這主要是針對那些偶爾想手動修正特定區域的時刻，以防有不需要的細節。

請注意，這並不像一般簡單的「印章」刷子那樣運作。 你混合區域的形狀是根據你處理區域的形狀和明暗來決定的，這代表這是一個相當沉重且需要耐心的節點，但效果非常出色。

另一個重要的是，你可以用小工具移動目標區域，但來源區域必須透過更改「來源矩陣」參數來設定。

>[!NOTE]
>
> 如果你想要完整材質（通常情況如此），請參考 [Material Clone Patch](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/material-clone-patch/material-clone-patch.md)。
> 
> 如果你想同時對多個輸入執行此操作（且不讓它成為材質），請參見 [多重複製補丁](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-clone-patch/multi-clone-patch.md)。

</td>
</tr>
</table>

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>是正常的（僅限顏色）</b> <i>錯誤/真實</i> | 設定輸入是否為法線貼圖，以及混合是否應以此方式處理。 |
| <b>形狀</b> <i>方形、圓盤</i> | 定印章形狀。 只當作基礎使用。 |
| <b>Edge</b> |  |
| <b>門檻</b> <i>0.0 - 1.0</i> | 設定混合區域應該延伸到多遠。 這種效果會沿著目標區域的形狀逐步成長，對於均勻背景<i>幾乎沒有影響。</i> |
| <b>模糊</b> <i>0.0 - 2.0</i> | 若需要較柔和的過渡，則模糊印章區域的邊緣。 |
| <b>平滑度</b> <i>0.0 - 2.0</i> | 郵票形狀邊緣圓潤，使輪廓更流暢流暢。 |
| <b>網格解析</b> <i>1 - 11</i> | 設定混合分析的品質解析度。 較高的數值代表融合更準確。 |
| <b>變換</b> |  |
| <b>來源矩陣</b> <i>（變換矩陣）</i> | 變換來源（縮放與旋轉）。 無法在 Canvas 上進行，只能透過這些參數來改變。 |
| <b>來源偏移</b> <i>-0.5 - 0.5</i> | 翻譯來源位置。 無法在 Canvas 上進行，只能透過這些參數來改變。 <i>這個參數大概是你最想改變的！</i> |
| <b>目標矩陣</b> <i>（變換矩陣）</i> | 轉換目標位置（縮放與旋轉）。 也可以用 Gizmo 在畫布上來完成。 |
| <b>目標偏移</b> <i>-0.5 - 0.5</i> | 翻譯目標位置。 也可以用 Gizmo 在畫布上來完成。 |
