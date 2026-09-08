---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/properties.html"
breadcrumb-title: ''
description: 使用 Substance 3D Designer 中的屬性面板來檢視和編輯節點屬性及圖形參數。
helpx_creative_field: ""
helpx_description: Designer > Interface > Properties
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 屬性
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 0%

---


# 屬性

本頁介紹 <b>Substance 3D Designer 的屬性 </b>面板、其版面設計，以及你可以在其中找到的不同展開、分類和參數。 它專注於 Substance 圖](../../compositing-graphs/substance-compositing-graphs.md)的[性質。[功能圖](../../function-graphs/function-graphs.md) 和 [FX-Map](../../function-graphs/fxmaps/fxmaps.md) 圖的版面配置較為簡單。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## 概觀

<b>屬性</b>面板是一個情境感應面板，會根據你在圖景檢視](../../interface/the-graph-view/the-graph-view.md)和[檔案總管](../the-explorer-window/the-explorer-window.md)視窗中的選擇[而改變。

</td>
<td style="border: 0;" valign="top">

![物業碼頭](../../assets/image2020-11-9-13-49-48.png "物業碼頭")

</td>
</tr>
</table>

它讓你可以更改選取節點和資源的屬性，加上 [圖視圖](../../interface/the-graph-view/the-graph-view.md)，這大概是你在 Designer 中第二常用的 UI 面板。

屬性面板會根據你的選擇分為幾個不同的推出模式，例如：

* <b>基礎參數</b>，以及<b>節點的輸入</b>或<b>特定參數</b>
* <b>大多數節點與套件的屬性</b>與<b>元資料</b>

物質生態系統的一項關鍵功能「 [參數揭露](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)」是透過屬性面板完成的。

>[!NOTE]
>
> 大多數數值領域都支援 *基本的數學公式* 作為輸入——例如， `17+3.5`， `7/3`， `(4+2)*3`， ， 按下 *Enter* 鍵驗證公式，結果會被輸入欄位。 若公式無效，欄位會回復到先前的值。\
> 應用程式其他部分的某些數值欄位，例如 [Expose 參數](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md) 對話框，也支援此功能。

## 節點與實體圖

節點圖與 [實體圖](../../compositing-graphs/substance-compositing-graphs.md) 擁有一組略有重疊的屬性類別，且其功能相似。

<b>節點與圖形之間的基礎參數</b> 與 <b>屬性</b> 是相同的。

節點提供<b>特定參數</b>或<b>實例參數</b>（視其為[原子節點](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/atomic-nodes.md)或[實例](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)而定），以及<b>用於處理[值](../../compositing-graphs/values-compositing-graphs/values-in-substance-compositing-graphs.md)的輸入值</b>。

[輸入](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md)與 [輸出](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)原子節點是例外，因為它們具備 <b>整合屬性</b> 與 <b>可見性</b> 條件。 這兩組屬性也可以在圖屬性的輸入與輸出中中央存取。

圖表還有幾個額外的分類。 <b>輸入參數</b>列出[暴露的參數](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)，<b></b>輸入與<b>輸出</b>列出輸入與輸出節點的所有屬性。[你可以在專門頁面找到所有圖屬性的詳細說明。](../../compositing-graphs/graph-parameters/graph-parameters.md)

## 資源與套件

屬性面板也會回應檔案總管](../the-explorer-window/the-explorer-window.md)中的[選擇變更。它可以作為選擇圖表的另一種方式（而不是雙擊空白區域），也能讓你更改 Package 和 [Resource](../../resources/resources.md)屬性。

套件包含 **資訊**、 **屬性** 和 **元資料** 區塊。 [套件的元資料會在專屬頁面上描述。](../../package-metadata/package-metadata.md)

資源具有其特定類型的屬性，詳 [述於專屬頁面](../../resources/resources.md)中。
