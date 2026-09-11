---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/fxmaps.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Designer 中使用 FXMaps 來將功能圖套用到材質上，以進行程序式圖案生成。
helpx_creative_field: ""
helpx_description: Designer > Function graphs > FXMaps
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: FXMaps
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '799'
ht-degree: 0%

---


# FXMaps

**FX-Map 節點允許建立程序影像**。 這是物質技術中最強大的特性之一。

FX-Map 代表一種特殊類型的圖，稱為馬可夫鏈。 馬可夫鏈代表一個簡單的核心過程：反覆複製並細分一個影像。 在每個步驟中，影像都可以隨意旋轉、平移和混合。 結果可以是從簡單的模式到複雜的噪音。 FX-Maps 是許多使用 Substance 3D Designer 安裝樣品物質的基礎。

## 建立 FX-Map 圖表

如果你想看 FX-Map 圖，只要在 Substance 圖](../../compositing-graphs/substance-compositing-graphs.md)中加入[一個 FX-Map 節點](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md)[，然後右鍵點擊該節點，按 CMD + E（OS X）或 CTRL + E（Windows）即可開啟該圖。這個 FX-Map 圖表會出現在圖表面板的新分頁中;你可以點擊分頁在這張圖表和 Substance 圖表之間切換。

## FX-Maps 是做什麼用的？

FX-Map 最常見的用途是產生重複的圖案，如條紋和磚塊，以及噪音，如 Perlin、Brownian 和 Gaussian 噪音。 噪音特別有助於創造有機且自然的質感，如泥土、灰塵、混凝土、石頭表面、液體濺濺等。

FX-Map 圖的運作方式與 Substance 圖不同：在 Substance 圖中，每個節點獨立，對自己在整體圖中的位置毫無知覺，也不在意影像資料的來源或目的地。

我們將在下一章更詳細地探討這三個 FX-Map 圖形節點，簡而言之，每個 FX-Map 節點提供三種操作之一：

### 象限

此步驟將圖中影像分割成四個象限。 這是最常見的節點類型。 一連串象限節點可以創造非常複雜的影像，以及複雜的圖案。

事實上，象限節點代表四叉樹圖中的一個層級或 **八度**。 FX-Map 圖透過將樹中的每個層級用單一象限來隱藏這種樹狀結構：每次你將一個象限節點連接到另一個象限節點時，實際上是在建立一個完整的樹狀層級。

這種「作弊」技巧的原因是為了省去每個節點在樹的每一層都獨立表示的需求：在四層深度後，你還需要使用 4 x 4 x 4 x 4 節點，也就是 256 個獨立節點！ 相反地，每個象限節點「知道」自己在樹中的哪一層，並相應地生成影像。

這對許多讀者來說可能不太合理，但我們稍後會更詳細地說明。

### 反覆迭代

以設定的迭代次數重複傳入右側連接器的影像。

此節點最常與一個或多個動態函數圖形搭配使用，在每次迭代中以某種方式移動或旋轉輸入影像。

### 切換

它會接收兩個輸入，並根據其選擇器設定在其中一個輸入間切換。 與迭代節點相同，選擇器設定通常由動態函數選擇。

## FX-Maps 系統變數

FX-Maps 支援系統變數。 這些變數總是以美元符號（“$”）開頭，具體如下：

| 名稱 | 特殊性 | 資料型別 | 目的 |
| --- | --- | --- | --- |
| $time | - | float1 | 此變數回傳自 Substance 渲染引擎啟動以來的時間（秒數）。它非常適合需要隨時間移動的物質。 (E.g. 時鐘的指針。）在某些應用程式中，包括 Substance Player，使用 $time 的 Substance 會在使用者介面中顯示時間軸。 |
| $depth | - | float1 | 回傳 FX-Map 節點的八度（電平）數。 這允許節點根據它所代表的四叉樹層級來調整行為。 |
| $depthpow 2 | - | float1 | 如上所述，但回放時將2提升為八度（電平）的冪次方。 這是一個輔助值，對某些常見計算非常有用。 |
| $number | 只迭代節點 | float1 | 回傳抽圖的編號。 此可由控制迭代節點的動態函數圖存取，在每個迭代步驟中修改其行為。（注意$number從 0 開始計數，而非 1。） |
| $size | - | float2 | 回傳目前節點的大小（以像素為單位）。 |
| $sizelog 2 | - | float2 | 如上所述，但回傳大小為2的冪次方值（例如：2048\*2048影像，$sizelog 2回傳11）。 |
| $pos | 僅限象限節點 | float2 | 回傳圖案的出生位置。 結果總是介於 0 到 1 之間。 |
