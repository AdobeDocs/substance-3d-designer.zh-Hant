---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/text.html"
breadcrumb-title: ""
description: 使用 Text 節點生成帶有可自訂字型與樣式的文字紋理，以創造基於文字的圖案。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Text
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 文字
user-guide-description: ""
user-guide-title: ""
source-git-commit: 961ee151245fbc3266574676bd535c374bd0e3ad
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 1%
---

# 文字

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![原子節點：文字](text.resources/comp_text_1.png "原子節點：文字"){width="100%"}

</td>
<td style="border: 0;" valign="top">

文字節點提供了一種讓使用者在圖表中放置文字的方法。 使用者也可以選擇字型、對齊和旋轉等設定，來自訂文字位置。

文字節點非常強大，是唯一能輕鬆放置文字的方式。 由於放置總是在有限的方形畫布上，且字型由系統定義的外部清單驅動，使用起來有點棘手。

</td>
</tr>
</table>

<div data-preserve-html="true" align="center"><img src="text.resources/text-tooltip.gif" alt="文字提示" /></div>

僅支援 Truetype（.ttf）及部分 Opentype 字型。 如果清單中缺少字型，這大概就是原因。 <b>字型不能被當作參數來暴露。</b>

當一個以文字為基礎的圖形發佈到 sbsar 時，字型會嵌入套件中，就像點陣圖和其他資源一樣，以確保它能在所有系統和應用程式中正常運作。



## 參數

|  |  |
| --- | --- |
| <b>彩色模式</b> *布林值* | 在灰階和彩色輸出影像之間切換。 |
| <b>正文</b> *弦* | 決定了文本描述。 |
| <b>洗禮盆</b> *弦* | 用於渲染文字的字型資源。 |
| <b>字體大小</b> *浮標* | 字體大小（點數）。 |
| <b>路線</b> *整數* | 將文字對齊設定為左、中（預設）或右。 |
| <b>轉型</b> *Float4* | 2x2 轉換矩陣套用到渲染後的文字上。 |
| <b>職位</b> *Float2* | 文字在輸出影像中的位置。 |
| <b>背景</b> *浮動/漂浮4* | 輸出影像的背景色。 |
| <b>字體顏色</b> *浮動/漂浮4* | 文字的顏色。 |

## 輸入連接器

|  |  |
| --- | --- |
| <b>背景</b> *灰階/彩色* 原色 | 輸出影像的背景色。 |


## 範例

*即將推出。*
