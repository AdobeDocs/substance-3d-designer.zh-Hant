---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/substance-compositing-graph-key-concepts.html"
breadcrumb-title: ''
description: 學習Substance合成圖的關鍵概念，包括節點、連接與工作流程基礎。
helpx_creative_field: ""
helpx_description: Designer > Substance graphs > Substance graph key concepts
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 實體圖的關鍵概念
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '859'
ht-degree: 0%

---


# 實體圖的關鍵概念

本頁列出在 Substance 3D Designer 中處理 Substance 圖表時需要理解的重要概念。

## 子圖/出版

[發佈圖](../publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md) 或建立子圖是兩個非常相似且抽象的概念。 這表示任何圖或節點網絡都可以「打包」在一起，並轉化為可重複使用的獨立資源。 子圖[&#128279;](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)的建立大多是在應用程式內部完成，目的是讓某些內容能在高效且智慧的工作流程中重複使用，避免重複一組節點。發佈時還需額外匯出為 Substance 3D 資產（SBSAR）格式，讓你的節點網路圖能在應用程式外使用，例如為 Unreal Engine 製作材質時。

輸入、輸出與暴露參數在此概念中極為重要，因為它們是圖形作為子圖或已發佈 Substance 3D 資產時，仍能與其互動的唯一方式。 原因如下：

* 沒有輸出就代表你的圖表 <b>什麼都不會產生，完全</b> 沒有資料。
* 沒有暴露參數代表你的圖表 <b>無法以任何方式自訂</b> 。 你無法設定像是效果強度、影像混合的透明度、特定區域的顏色等等......
* 沒有輸入意味著在某些情況下，你無法用<b> 自己的影像資料</b>自訂圖表結果，例如烘焙的網格貼圖來產生特效、輸入影像用來模糊，或自訂遮罩來隔離影像的特定區域。

## 輸入與輸出

[輸出](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)是一個產生單一二維結果的節點。它是你的圖的終點，一個完成的結果。 只有與輸出相連的資料才能匯出到 Designer 之外，甚至用於其他圖表。

以下是你應該知道的幾件事：

* 你可以有任意多個輸出，但至少必須有一個 <b>輸出</b>。
* 輸出解析度可達<b></b>最高 8192px 寬或高，可為<b>彩色或灰階</b>，並可匯出至支援的任何檔案類型。
* 輸出可以且應該唯一 <b>命名</b> 以識別，這在匯出時很有幫助。
* 任何節點右側的每個連接器其實都是一個輸出（更多資訊請參見「子圖」）

[輸入](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md)類似於輸出，是一個空的槽位，供你或其他使用者連接自己的資料。它允許在外部使用者定義的影像資料中建立圖形，例如修改輸入影像的濾鏡（例如模糊或對比度調整）。

以下是你應該知道的幾件關於輸入的事：

* 輸入完全是 <b>可選</b>的，只有在需要時才應該加入。 沒有最低或最高金額。
* 輸入有一個固定的解析度（通常與圖表相關），你可以定義，也可以決定是灰階還是彩色。 任何連接它的東西都會被轉換成符合這個數字。
* 輸入可以是硬碟的點陣圖檔案、其他圖表、Painter 或 Alchemist 的圖層等。
* 任何節點左側的每個連接器都是一個輸入（詳見「子圖」以了解更多資訊）

## 繼承

當影像與數值從節點傳遞到其他節點時，這些影像的一些 *屬性* ——即基礎 <b>參數</b> ——也會在 *圖中傳播* ，例如解析度、精度（即位元深度）、平鋪與隨機種子。

此傳播由 [每個節點對這些屬性所套用的繼承方法](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) 所定義。 事實上，節點可以 *繼承其他節點或其所在圖的屬性* 。\
繼承方法可以包括：

* *相對於母本*
* *相對於輸入*
* *絕對* 的——即無繼承權

繼承可能抽象且難以管理，因此我們強烈建議您 [查看專門討論此事的專頁](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) 。

## 參數暴露

參數暴露是一個非常深入的概念，但可以總結為選擇圖中節點的特定屬性，並為它們建立一個專用的 UI 控制元素，當圖被用作子圖或以 Published 為 Archive 時，這個元素就能輕鬆取得。 由於你無法快速或輕鬆地選取節點並調整其屬性，目標是建立另一個主要控制面板，將所有與該圖相關的屬性歸類。

以下是你應該知道的關於暴露參數的一些事項：

* Exposed Parameters（暴露參數 <b>）會將控制項從節點移動到圖表</b>，基本上是階層結構的上一層。
* 因此，暴露的參數在節點上無法再更改，只能在圖上更改。
* Exposed Parameters可以完全自訂，包含名稱、標籤、數值、UI編輯器類型，甚至在特定條件下隱藏與顯示。

對初學者來說，Exposing Parameters是一個抽象且困難的概念，[雖然有更多專門的文件](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)，但建議在深入Exposing Parameters之前，先熟悉軟體的其他基本面向。
