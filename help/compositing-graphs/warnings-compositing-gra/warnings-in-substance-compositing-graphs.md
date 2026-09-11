---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/warnings-in-substance-compositing-graphs.html"
breadcrumb-title: ''
description: 了解物質合成圖中的警告，並學習如何解決常見問題與錯誤。
helpx_creative_field: ""
helpx_description: Designer > Substance graphs > Warnings in Substance graphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 物質圖中的警告
user-guide-description: ''
user-guide-title: ''
source-git-commit: 46563ec789547cc1add76655dbad02f5099927a6
workflow-type: tm+mt
source-wordcount: '700'
ht-degree: 0%

---


# 物質圖中的警告

本頁列出 Substance 3D Designer 中 Substance 圖表[&#128279;](../../compositing-graphs/substance-compositing-graphs.md)可能觸發的警告與錯誤訊息，並提供每種常見的故障排除步驟。

警告會顯示在總管[&#128279;](../../interface/the-explorer-window/the-explorer-window.md)面板中圖表資源[的警告圖示工具提示中，若圖已載入，則會在圖表視圖的](../../interface/the-graph-view/the-graph-view.md)左下角顯示。

## ![（錯誤）](warnings-in-substance-compositing-graphs.resources/error.svg) 未定義輸出節點

該圖沒有 [輸出](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) 節點。

**![（滴答聲）](warnings-in-substance-compositing-graphs.resources/check.svg) 解決方案**

在圖中新增一個或多個 [輸出](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) 節點，並將串流中最後一個節點的輸出連接到該節點。

>[!NOTE]
>
> 透過 [新圖](../creating-compositing-gra/creating-a-substance-compositing-graph.md) 對話框提供的圖範本已預設輸出節點可供使用。

![修正「未定義輸出節點」警告](warnings-in-substance-compositing-graphs.resources/warnings-comp-output.gif "修正「未定義輸出節點」警告"){width="512px"}

### ![（錯誤）](warnings-in-substance-compositing-graphs.resources/error.svg)*[x]* 參數的函式有一些警告

[套用到指定節點參數的函數圖](../../function-graphs/function-graphs.md)至少有一個警告。\
節點參數在節點標籤後方括號內指定，依照 Node[Parameter] 模板。

E.g. 均勻顏色[輸出顏色]，像素處理器[每個像素函數]

**![（滴答聲）](warnings-in-substance-compositing-graphs.resources/check.svg) 解決方案**

在圖譜檢視[&#128279;](../../interface/the-graph-view/the-graph-view.md)中，透過標籤和警告徽[章找到發出警告的節點，然後選擇它在屬性](../../interface/properties/properties.md)面板中顯示其屬性。找到發出警告的參數，點擊「編輯功能&#x200B;**」按鈕開啟其函式**。

接著，評估圖表視圖左下角列出的警告並解決問題。 您可以參考 [功能圖](../../function-graphs/warnings-function-graphs/warnings-in-function-graphs.md) 中的警告頁面，以了解功能圖中報告的警告故障。

![修正「參數函數有某些警告」警告](warnings-in-substance-compositing-graphs.resources/warnings-comp-param-function.gif "修正「參數函數有某些警告」警告")

### ![（錯誤）](warnings-in-substance-compositing-graphs.resources/error.svg) 參考資料中有一些警告

節點所參考的資源會有一個或多個警告。 以下是一些引用資源的節點：

* 圖 [實例](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md) 節點參考一個圖
* [位圖](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md)節點參考一個[位圖資源](../../resources/bitmap-resource/bitmap-resource.md)
* SVG [&#128279;](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/svg/svg.md) 節點參考 [SVG 資源](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md)
* 文字[&#128279;](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md)節點參考字[型資源](../../resources/font-resource/font-resource.md)

**![（滴答聲）](warnings-in-substance-compositing-graphs.resources/check.svg) 解決方案**

在 [Explorer](../../interface/the-explorer-window/the-explorer-window.md) 面板中，找到該資源所提及的資源並排除該資源所引發的所有警告：

* 關於圖表，請參考本頁其他項目
* 其他資源請參考 [「依賴](../../resources/warnings-from-dep/warnings-from-dependencies.md) 警告」頁面

![修正「參考資料有警告」](warnings-in-substance-compositing-graphs.resources/warnings-comp-referenced-data.gif "警告 修正「參考資料有警告」警告")

### ![（錯誤）](warnings-in-substance-compositing-graphs.resources/error.svg) 找不到參考資源

節點所參考的資源並未在 Substance 3D[&#128279;](https://www.adobe.com/products/substance3d/3d-augmented-reality.html) 檔案（SBS）中儲存的路徑中找到。以下是一些引用資源的節點：

* 圖 [實例](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md) 節點參考一個圖
* [位圖](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md)節點參考一個[位圖資源](../../resources/bitmap-resource/bitmap-resource.md)
* SVG [&#128279;](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/svg/svg.md) 節點參考 [SVG 資源](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md)
* 文字[&#128279;](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md)節點參考字[型資源](../../resources/font-resource/font-resource.md)

**![（滴答聲）](warnings-in-substance-compositing-graphs.resources/check.svg) 解決方案**

對於 [圖實例](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md) 節點

檢查來源圖是否存在於套件 **中，該套件位於其 Package** 屬性所儲存路徑的位置。\
如果沒有，則刪除該實例節點，並以引用有效套件的實例節點取代。 或者，你也可以重新建立實例節點參考的套件和圖表，然後在檔案總管[&#128279;](../../interface/the-explorer-window/the-explorer-window.md)面板點擊右鍵，並在情境選單中選擇&#x200B;**重新載入**&#x200B;主機套件。

對於 [點陣](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md)圖、 [SVG](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/svg/svg.md) 或 [文字](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md) 節點

在總管面板中找到參考資源，並確認它們是否存在於檔案 **路徑** 屬性中儲存的位置。\
如果沒有，請在檔案總管中點擊資源項目的右鍵，並在情境選單中選擇 **「重新定位...」** 選項，為該資源設定新的有效目標檔案。

![修正「找不到參考資源」警告](warnings-in-substance-compositing-graphs.resources/warnings-comp-referenced-resource.gif "修正「找不到參考資源」警告")

### ![（錯誤）](warnings-in-substance-compositing-graphs.resources/error.svg) 文字節點使用無效字型

[文字](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md)節點會參考無法正確載入或解析的字型。

<b>!&lbrack;（勾選）（警告-in-substance-compositing-graphs.resources/check.svg）解決方案</b>

選擇 [Text](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md) 節點，並記錄其 <b>Font</b> 屬性的值。 在你的系統中找到該字型的原始檔案，並確保它健康&#x200B;**，例如在其他應用程式中使用，例如文字編輯器。必要時用健康的字型檔案取代字型，或將文字節點切換到其他字型。
