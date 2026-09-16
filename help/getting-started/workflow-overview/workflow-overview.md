---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/getting-started/workflow-overview.html"
breadcrumb-title: ""
description: 從頭到尾學習 Substance 3D Designer 中製作程序材質的基本工作流程。
helpx_creative_field: ""
helpx_description: Designer > Getting started > Workflow overview
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 工作流程概述
user-guide-description: ""
user-guide-title: ""
source-git-commit: f475b696f2d3ff6c453c5dc27e5672d55d72116e
workflow-type: tm+mt
source-wordcount: '1169'
ht-degree: 0%
---

# 工作流程概述

Substance 3D Designer 是一款基於節點的編輯器。 這表示幾乎所有類型的專案或資源都會涉及放置節點（建構單元）並將它們連接起來，形成一連串操作（圖）。本頁說明了基於節點的工作流程概念，並總結了你可以在 Designer 中撰寫的三種主要圖形類型。

![資料流程簡化](workflow-overview.resources/graph-direction.png "資料流程簡化"){zoomable="yes"}

## 基於節點的工作流程

在 Designer 中工作與其他 2D 影像編輯軟體（如 Photoshop）不同。 你不需要手動執行動作（例如透過選單選項調整飽和度並調整滑桿），而是 <b>建立編輯或建立影像的邏輯步驟</b> 。 這是透過建立一個稱為「節點」的小積木網絡來實現的。 影像資料從<b> 左向右</b> 穿過各個組件，這些組件由連結連接，決定資訊的路徑。 每個節點若連接，都會對最終結果做出貢獻。

主要優點是你的工作流程會變得 <b>非線性</b>。 與手動執行的操作進入歷史堆疊不同，你隨時可以更換或修改節點。 如果你覺得第一次調整對比度，影響了整個影像效果，結果一直到最後，還是可以回頭調整，甚至完全刪掉，而不會失去後續所做的所有工作。

![圖實例簡化](workflow-overview.resources/sub-graph.png "圖實例")

## 圖實例工作流程

實例化圖是 Designer 中的一個關鍵流程。 它允許你透過將任何大小或類型的圖打包成新的節點建構塊來建立自己的節點。 這類節點稱為「圖實例」，這讓你更有效率、節省時間並與他人分擔工作。 例如，你有沒有發展出很棒的邊緣磨損技巧？ 用它建立一個圖實例，自己重用，或分享給社群或你的團隊！

關於實體圖](../../compositing-graphs/substance-compositing-graphs.md)中圖實例[的更多資訊，文件[中有專門的章節](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)。

![圖參數簡化](workflow-overview.resources/parameters-5.png "圖參數"){zoomable="yes"}

## 自訂參數

操作鏈中的任何節點都會有某種控制：按鈕、滑桿、設定，影響最終結果。 如果你建立子圖，或想將你的Substance File匯出到其他應用程式，你可以為檔案建立自己的「控制面板」，讓任何使用該圖的人都能用完全獨特的控制面板調整和修改它，展現無限的可能性。 [在這裡](../../compositing-graphs/compositing-graph-key-con/substance-compositing-graph-key-concepts.md)了解自訂參數的基本概念，或者更深入 [地開始揭露參數](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)。

## 圖類型

以下有Substance 3D Designer中可編輯的三種圖表類型摘要，以及相關文件章節的連結。

<table>
<tr style="border: 0;">
<td style="border: 0; width: 20%; vertical-align: top">

![](workflow-overview.resources/graph-5.png){width="120px"}

</td>
<td style="border: 0; vertical-align: top">

### 物質圖

[Substance 圖](https://substance3d.adobe.com/) 是 Substance 3D Designer 中主要建立的圖形類型。 它們的目的是產生 <b>並處理不受固定解析度、顏色或形狀限制的二維影像資料</b> 。 它們是極具多功能性的影像處理與生成工具，而非靜態預設結果。

結果可以是簡單的黑白圖案、只在其他圖片上運行且不會自動產生內容的濾鏡，甚至是擁有多個通道的完整程序化素材。

Substance 圖是 [支援最廣泛的圖](../../getting-started/overview/overview.md)類型，可以匯出並用於各種不同的工作流程。

</td>
</tr>
</table>

#### 範例

以下是一些常見的使用案例範例。

+++ 簡單的形狀

![Substance 圖中的簡單形狀 Substance 圖](workflow-overview.resources/simpleshape.png "中的簡單"){width="512px" zoomable="yes"}

貼紙的遮罩形狀是透過產生[一段文字](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md) 和 [一個圓盤形狀](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape/shape.md)， [從圓盤中提取邊緣](../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/edge-detect/edge-detect.md) ，最後 [將它們混合在一起](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md) ，然後設定為最終 [輸出](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)。

帶有數字或邊緣厚度的文字可以外部曝光，使圖表更具動態性。

+++

+++ 調整濾波器

![Substance 圖](workflow-overview.resources/simplefilter.png "中的調整濾波器 Substance 圖中的調整濾波器"){width="512px" zoomable="yes"}

濾波圖會將法線貼圖作為 [輸入](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md) （並有自訂預覽）， [將其轉換為曲率](../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-smooth/curvature-smooth.md) ，然後 [調整對比](../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md) 度，產生一個凸邊遮罩作為最終 [輸出](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)。

直方圖中設定的對比值可以被曝光，這使得這個濾波器與動態輸入槽結合使用時，既簡單又實用。

+++

+++ 完整內容

![Substance 圖表](workflow-overview.resources/simplematerial.png "中的完整內容 Substance 圖表中完整資料"){width="512px" zoomable="yes"}

更複雜的圖表 [則結合了兩種基底材質](../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/material-blend/material-blend.md)。 一個 [基底材質](../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/base-material/base-material.md) 保持簡單，另一個則用一些自訂輸入來增加趣味。 遮罩用來判斷兩種材料中哪一種在被設定為最終 [輸出](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)前出現的位置。

本範例利用 [連結建立模式](../../interface/the-graph-view/link-creation-modes/link-creation-modes.md) 來簡化使用多條連結。

+++

<table>
<tr style="border: 0;">
<td style="border: 0; width: 20%; vertical-align: top">

![](workflow-overview.resources/function-1.png){width="120px"}

</td>
<td style="border: 0; vertical-align: top">

### 實體函數圖

函式 <b>處理的是單一值</b> （整數、浮點數、向量），而非影像資料（整組像素）。 函數也是帶有節點網路的圖，但 [所用](../../function-graphs/nodes-reference-for-fun/function-nodes-overview/function-nodes-overview.md) 節點與介面不同 [於一般的實體圖](../../compositing-graphs/substance-compositing-graphs.md)。 工作流程完全基於 <b>數學運算</b> ，不會顯示任何圖片預覽縮圖，因此在使用 Substance 3D Designer 時，是 <b>更進階的方式</b> 。

函式可用於多種不同情境，主要包括修改暴露參數[](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)的行為、撰寫像素處理器](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md)或[FX-Maps](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md)的行為[，以及在Substance圖中使用[值](../../compositing-graphs/values-compositing-graphs/values-in-substance-compositing-graphs.md)。

</td>
</tr>
</table>

#### 範例

以下是 Substance 函數圖常見使用案例中的一些範例。

+++ 簡單函數

![簡單函數圖簡單函數圖](workflow-overview.resources/lerpfunction.png ""){width="256px" zoomable="yes"}

在暴露參數的情境下，這是一個簡單的函數。 它會得到一個名為「強度」的輸入浮點數值，該值從 0 到 1（一個容易理解的範圍），並重新映射到 0.1 到 0.8 的設定範圍。 這表示如果使用者將強度設為 0，內部會使用 0.1;如果 UI 設為 1，則會使用 0.8，中間的任何值則會線性插值。 這種函式在暴露參數](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)時很常見[，但會使用自訂函數。

此函式也可寫成 *lerp（0.1， 0.8， Intensity），* 以類似 HLSL 或 GLSL 的偽代碼形式。

+++

+++ 進階功能

![進階功能](workflow-overview.resources/pixel-function.png "進階功能"){width="512px" zoomable="yes"}

這個進階功能展示了像素處理器的 [內部運作，該處理器](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md) 旨在根據第二個灰階遮罩輸入的強度調整色彩貼圖輸入的色調。

它會用系統的「$pos」變數取樣兩個輸入，然後剝離 Alpha，將色彩值轉換成 HSL，並透過與取樣的灰階值相乘來修改 Hue 成分。 接著重新組合向量，將 HSL 轉回 RGB，並加入 Alpha 作為最終輸出。

在偽程式碼中，這會是一個更複雜的函式，無法在單一行中呈現。

+++
