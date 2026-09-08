---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/atlas-splitter.html"
breadcrumb-title: ''
description: 使用圖集分割器節點將材質圖集分割成獨立材質，以便處理掃描材質。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Atlas Splitter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Atlas 分裂器
user-guide-description: ''
user-guide-title: ''
source-git-commit: ca90755a159a7e0297bb26d1e3522b0cfeb6f2ac
workflow-type: tm+mt
source-wordcount: '386'
ht-degree: 0%

---


# Atlas 分裂器

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![節點圖示](../../../../../../assets/atlas-splitter.png "節點圖示")

<b>收錄於：</b> 材料濾鏡/掃描處理

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

它會根據圖譜影像輸入，將所有獨立元素拆分成 *獨立材質*。

它也可以用來重新組織並移動所有元素到格子中。

該節點作為洪水填充[&#128279;](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md)節點的進階應用。

</td>
</tr>
</table>

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>格狀視圖</b> <i>布林值</i> | 以格子形式顯示所有偵測到的形狀。 |
| <b>網格不透明度</b> <i>浮標</i> | 當網格視圖為真時，設定格線的不透明度。 除錯選項 |
| <b>網格選擇不透明度</b> <i>浮標</i> | 若格網視圖為真，則設定格子選取的不透明度高亮。 除錯選項 |
| <b>自動秤</b> <i>布林值</i> | 自動將形狀縮放到格子格子裡。 |
| <b>自動裁切</b> <i>布林值</i> | 自動依最大形狀裁剪輸出尺寸，以減少空隙。 |
| <b>形狀選擇</b> <i>整數</i> | 在格狀視圖中，會指定要標示哪個格子，而在格子視圖之外，這會設定回傳哪個格子。 |
| <b>忽略小於</b> <i>浮標</i> | 忽略對角線大小小於指定值的形狀。 |
| <b>自動旋轉</b> <i>布林值</i> | 會自動根據包圍框大小比例旋轉形狀。 |
| <b>旋轉</b> <i>浮標</i> | 全域形狀旋轉角 |
| <b>輸入標準格式</b> <i>整數</i> | 設定輸入格式為正常。 設定錯誤格式會導致錯誤結果。 |
| <b>降階不透明度遮罩</b> <i>整數</i> | 將不透明度遮罩降階以消除潛在雜訊或孤立像素。 它能防止偵測到不需要的形狀，並提升效能。 |
| <b>膨脹寬度</b> <i>浮標</i> | 在除了法線和高度以外的所有聲道上，根據不透明度遮罩套用一個放大效果。 |
| <b>啟用額外輸入</b> <i>布林值</i> | 讓 USer 1 和 User 2 的輸入和設定都能使用，適用於未涵蓋的額外地圖。 |
| <b>自訂背景色</b> <i>布林值</i> | 讓你可以選擇自訂背景色，而不是放大該圖層內容。 |
| <b>底色 Bg 色</b> <i>Float3</i> | 為基礎色自訂 BG 顏色。 |
| <b>普通背景色彩</b> <i>Float3</i> | 法線貼圖自訂 BG 顏色。 |
| <b>金屬色 Bg</b> <i>浮標</i> | 為金屬色自訂背景顏色。 |
| <b>粗糙度 Bg 色彩</b> <i>浮標</i> | 粗糙度自訂背景顏色 |
| <b>高度 Bg 顏色</b> <i>浮標</i> | 自訂身高背景顏色 |
| <b>使用者 1 背景色彩</b> <i>浮標</i> | 自訂 BG 顏色用於自訂 User 1 地圖 |
| <b>使用者 2 Bg Color</b> <i>浮標</i> | 自訂 BG 顏色用於自訂 User 1 地圖 |
