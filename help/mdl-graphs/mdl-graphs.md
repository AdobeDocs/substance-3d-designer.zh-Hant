---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/mdl-graphs.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Designer 中建立並使用材料定義語言（Material Definition Language）圖表，以進行進階材料工作流程。
helpx_creative_field: ""
helpx_description: Designer > MDL graphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: MDL 圖
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0b8b2d2c05587d7fe84a71bb54244a492540d6dc
workflow-type: tm+mt
source-wordcount: '793'
ht-degree: 0%

---


# MDL 圖

本頁介紹 Substance 3D Designer 中的 MDL 圖表，讓您能撰寫 MDL 材料並即時預覽其行為。

![孔雀石MDL材料](../assets/mdl-malachite-example.jpg "孔雀石MDL材料")

*孔雀石與Chrysocolla、Mark Foreman**](https://www.artstation.com/oggyart)的MDL資料[可於我們的[Legacy Substance Share](https://share-legacy.substance3d.com/libraries/4043)**平台取得*

>[!WARNING]
> 
> MDL 圖形及所有相關功能於 Designer 16.0.0 版本中被移除。
> 
> 更多資訊請見： [MDL 圖表與 Iray 終止生命週期](../technical-issues/mdl-graph-iray-eol/mdl-graph-iray-eol.md)

+++目錄

* [主要 MDL 圖形概念](/help/mdl-graphs/main-mdl-graph-concepts/main-mdl-graph-concepts.md)
* [建立 MDL 圖](/help/mdl-graphs/creating-an-mdl-graph/creating-an-mdl-graph.md)
* [MDL 圖書館](/help/mdl-graphs/mdl-library/mdl-library.md)
* [MDL 圖中參數的暴露](/help/mdl-graphs/exposing-parameters-mdl/exposing-parameters-in-mdl-graphs.md)
* [物質圖表與 MDL 材料](/help/mdl-graphs/compositing-graphs-and/substance-compositing-graphs-and-mdl-materials.md)
* [匯出 MDL 內容](/help/mdl-graphs/exporting-mdl-content/exporting-mdl-content.md)
* [MDL 圖表中的警告](/help/mdl-graphs/warnings-in-mdl-graphs/warnings-in-mdl-graphs.md)
* [MDL 學習資源](/help/mdl-graphs/mdl-learning-resources/mdl-learning-resources.md)

+++

## 概觀

MDL 代表 [Materials Definition Language](http://www.nvidia.com/object/material-definition-language.html)：「由 [NVIDIA](https://www.nvidia.com/) 開發的技術，用以定義物理基礎材料以實現物理基礎渲染解決方案。」 （資料來源： [ NVIDIA MDL 文件](https://raytracing-docs.nvidia.com/mdl/index.html)）

使用此語言，完整材質定義可移植，因此可在多個應用程式與渲染器間使用，以達成一致的輸出。 Substance 3D Designer 目前 *是唯一* 提供基於圖形的 MDL 材料節點製作的應用程式，透過將 MDL 函式與值類型作為 MDL 圖中的節點公開。

在製作材質時，你可以使用 NVIDIA 自家[的 Iray](../interface/3d-view/iray/iray.md) 渲染器，內建於 Designer 中，並可於 [3D 檢視](../interface/3d-view/3d-view.md)面板中使用，以互動&#x200B;*式方式預覽材質*&#x200B;的行為。

MDL 圖與 [Substance 圖](../compositing-graphs/substance-compositing-graphs.md)互補，後者輸出 *的紋理* 可 *被 MDL 材質取樣* ，以影響其行為與外觀。

我們建議您閱讀本文件&#x200B;**&#x200B;的各章節，從下方 MDL 圖形資源的屬性開始，進行引導式學習路徑。\
急著投入嗎？ 在 MDL 學習資源](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/first-steps-with-mdl-145654095.html)區開始使用 MDL 圖表[吧！

>[!NOTE]
>
> 您可以在 NVIDIA MDL 文件中了解更多關於材料定義語言 [技術實作的資訊，該文件](https://raytracing-docs.nvidia.com/mdl/index.html)包含由 NVIDIA 撰寫與維護的 MDL 規範與 [MDL 手冊](http://mdlhandbook.com/)連結。

![MDL 圖屬性](../assets/mdl-main.png "MDL 圖屬性")

*屬性](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/parameters-ui-129368153.html)面板中的 [MDL 圖形屬性*

## MDL 圖性質

### 屬性

本節包含關於MDL資料的資訊，用於識別、分類及確定作者身份。

* <b>識別碼</b>：此資源的名稱，應在封包的父資源下唯一
* <b>顯示名稱</b>：介面中顯示的 MDL 材質名稱
* <b>圖示</b>：Designer&#39;s Library 中此圖作為縮圖的圖片
* <b>隱藏\*</b>：當設定為* True（True*）時，MDL 資料在 MDL 函式庫中不會顯示，但仍存在於內部，且可被引用
* <b>在函式庫</b>中顯示：當設定為 *True* 時，MDL 圖表會顯示在 Designer&#39;s Library 中
* <b>說明</b>：MDL 材料的描述，可顯示於參考此圖的實例節點工具提示中
* <b>Category\*</b>：MDL 圖所屬的類別——目前不影響圖在 Designer&#39;s [Library 中的排序方式](../interface/the-library/the-library.md)
* <b>在群組\*</b>中：MDL資料所屬的函式庫群組
* <b>作者/*</b>：MDL資料的作者
* <b>貢獻者\*</b>：除作者外，對MDL資料的貢獻者
* <b>關鍵字\*</b>：可用於在圖書館搜尋中尋找MDL資料的關鍵字
* <b>版權聲明\*</b>：與MDL資料的作者及使用相關的版權聲明

注意：標有星號（\*）的屬性為 MDL 註解，供 MDL 函式庫整合使用，對* Designer 無影響* 。

### 圖輸入

本節列出與 [MDL 圖中暴露參數](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/exposing-a-parameter-145654033.html) 相關的互動參數，並定義其 *預設值*。 它們可以&#x200B;**&#x200B;隨時調整和&#x200B;*重新排序*。

這些輸入的介面與行為由 *它們所連接的參數的值型態* 與 *範圍* 所定義。 例如：

* 若將 Float</b> 類型暴露於<b>軟範圍 [0.0,4.0]，則會以&#x200B;*單一滑桿*&#x200B;顯示，範圍從 0.0 到 4.0
* 一個暴露的 Color</b> 型<b>值會以顏色小工具&#x200B;*的形式顯示*，包含選取漸層和顏色縮圖

要重新排序圖形輸入，將游標放在&#x200B;*參數左側的暗色把*&#x200B;手上，點擊並&#x200B;*長按*<b>左鍵</b>，然後向上或向下拖曳游標。此自訂順序將用於在以下情境中顯示 MDL 材料的特性：

* 參考本資料 MDL 圖的實例節點
* 3D 視圖中的 [材料特性](../interface/3d-view/3d-view.md)
* 第三方 MDL 整合
