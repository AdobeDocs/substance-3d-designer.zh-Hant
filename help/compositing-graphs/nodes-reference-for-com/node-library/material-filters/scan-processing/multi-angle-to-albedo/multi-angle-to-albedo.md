---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/multi-angle-to-albedo.html"
breadcrumb-title: ''
description: 使用多角度轉反照率節點，從多角度掃描影像中擷取反照率圖，以獲得乾淨的材質色彩。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Multi-Angle to Albedo
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 多角度到阿貝多
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 1%

---


# 多角度到阿貝多

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](multi-angle-to-albedo.resources/multi-angle-to-albedo.png){width="128px"}

<b>收錄於：</b> 《材料濾>掃描處理》

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

此節點嘗試從一組在不同光照角度下拍攝的輸入照片/掃描中移除所有光照資訊。 它將所有取樣合成一張影像，應盡可能保持光線中性，因此符合PBR正確。

請記住，樣本越多，光線角度差異越大，成功率就越高。 從四個樣本開始，根據輸入的影像，應該能達到接近完美的效果。 輸入影像應該用腳架拍攝，差異極小甚至理想上完全沒有，除了光線角度不同！

>[!NOTE]
>
> 請參閱 [「多角度到法線](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-normal/multi-angle-to-normal.md) 」以了解此節點的法線貼圖版本。 如果你想預先處理輸入 [，多色均衡器](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-color-equalizer/multi-color-equalizer.md)、 [多重裁切](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-crop/multi-crop.md) 和 [多重複製補丁](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-clone-patch/multi-clone-patch.md) 都很有用，因為它們本來就是設計用來與這些節點結合的。
> 
> [部落格文章《你的智慧型手機是物質掃描器》對這個過程做了更清楚的說明。](https://www.allegorithmic.com/blog/your-smartphone-material-scanner)

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>輸入 1-8</b> <i>色彩輸入</i> | 輸入數量由樣本數量參數決定。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>樣本數量</b> <i>2 - 8</i> | 設定用於處理的樣本（輸入）數量。 |
