---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/crop.html"
breadcrumb-title: ''
description: 使用 Crop 節點將素材輸出裁剪到特定區域，以便處理掃描的材質和材質。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Crop
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 作物
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 2%

---


# 作物

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](crop.resources/crop-10.png){width="128px"}

![](crop.resources/crop-grayscale.png){width="128px"}

<b>收錄於：</b> 《材料濾>掃描處理》

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

裁切是熟悉裁切工具的參數化、非破壞性版本。 你選擇影像中的一個區域，結果會被丟棄，未被選取的區域會被丟棄。

它在許多方面都很有用，因為對原子節點執行裁切操作並不那麼簡單。 特別是在轉換非正方形影像時，這個節點非常實用。 在這種情況下，請確保輸入解析度設定正確。

非常重要的是，要輕鬆使用這個節點，你必須善用預覽與你正在編輯參數不同的節點的功能！\
簡而言之：**雙擊**&#x200B;你用來輸入的節點（原始未裁切圖片），然後&#x200B;****&#x200B;單擊緊接著的裁切節點。接著你可以修改裁切裝置，使其符合你想要裁切的區域。

</td>
</tr>
</table>

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>輸入大小</b> <i>0 - 8192</i> | 輸入影像的解析度與比例。 對於非方形影像非常重要。 |
| <b>背景</b> <i>（色彩值）/（灰階色值）</i> | 未被裁剪覆蓋區域的背景均勻值。 |
| <b>轉換</b> <i>（變換矩陣）</i> | 旋轉並縮放結果。 結果可透過直接與畫布互動來調整。 |
| <b>偏移</b> <i>0.0 - 1.0</i> | 移動或翻譯結果。 結果可透過直接與畫布互動來調整。 |
| <b>這是正常的（僅限彩色版本）</b> <i>錯誤/真實</i> | 是否應該將輸入視為法線貼圖。 |
