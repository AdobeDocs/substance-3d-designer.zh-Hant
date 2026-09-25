---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/getting-started/overview.html"
breadcrumb-title: ""
description: 了解 Substance 3D Designer 的概覽，並了解其在製作程序材質與貼圖方面的功能。
helpx_creative_field: ""
helpx_description: Designer > Getting started > Overview
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 概觀
user-guide-description: ""
user-guide-title: ""
source-git-commit: aeb517a0def4b5bc2de723633f8932dfc03f052c
workflow-type: tm+mt
source-wordcount: '930'
ht-degree: 0%
---

# 概觀

[Substance 3D Designer](https://www.adobe.com/tw/products/substance3d-designer.html) 是一款用於在節點介面中建立 2D 材質、材質與濾鏡的應用程式，重點在於程序生成、參數化及非破壞性工作流程。 它是 Substance 3D 生態系統中運行時間最長的應用程式，而用它製作的資源也最具多樣性與動態性。

以下是它與其他應用的比較：

|                                          | <div><img alt="Substance 3D 取樣圖示" class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell_position-par_dx_table_row-r0-column-c1_position_position-par_image_713298714" src="overview.resources/sa-appicon-noshadow-256.png" title="Substance 3D 取樣圖示" width="64px"/></div>  Substance 3D 取樣器 | <div><img alt="Substance 3D Painter 圖示" class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell_position-par_dx_table_row-r0-column-c2_position_position-par_image" src="overview.resources/pt-appicon-noshadow-256.png" width="64px"/></div>  Substance 3D 畫家 | <div><img alt="Substance 3D Designer 圖示" class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell_position-par_dx_table_row-r0-column-c3_position_position-par_image" src="overview.resources/ds-appicon-noshadow-256.png" title="Substance 3D Designer 圖示" width="64px"/></div>  Substance 3D Designer |
|------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **學習曲線** | 低 | 中 | 高 |
| **作者資料** | 是的 | 是的 | 是的 |
| **作者 3D 模型** | 不 | 有限\* | 有限\* |
| **作者過濾器、模式與效果** | 不 | 限制 | 是的 |
| **匯出參數內容** | 不 | 不 | 是的 |

\*：僅位移，請參見 <b>3D 視圖[&#128279;](../../interface/3d-view/3d-view.md)區塊中的場景匯出</b>功能。

簡言之，Substance 3D Designer 應該被視為目前最技術性、最先進的貼圖應用程式。

它讓你能為幾乎任何使用情境或情境撰寫內容。 這表示你不只侷限於單一輸出類型——例如UV映射網格的獨特材質或材質——而是能創造更廣泛的內容。

例如，Painter 和 Sampler 中大部分的程序式智慧內容都是從 Designer 撰寫並匯出的。 像是筆刷 Alpha、產生器、濾鏡和基底材質，都可以在 Designer 裡創作。

## 工作流程

Substance 3D Designer 是一款基於節點的編輯器，允許你以多種不同複雜度的方式製作內容。 [工作流程會在專門頁面](../../getting-started/workflow-overview/workflow-overview.md)中進一步說明，但以下是使用該軟體的好處：

**[非線性](../../compositing-graphs/substance-compositing-graphs.md)：** 你可以同時撰寫多個材質輸出。 編輯一個遮罩或滑桿，任何連接的輸出都會自動重新計算。 不再需要另外製作像是底色、粗糙度、法線等貼圖。

**[非破壞性](../../compositing-graphs/compositing-graph-key-con/substance-compositing-graph-key-concepts.md)：** 你可以逆轉任何動作 *而不* 損失任何工作。 這樣可以更快地反覆迭代和實驗，找到更有效率的工作流程。

**[整合烘焙](../../bakers/bakers.md)：** 在軟體內直接存取先進且極速的網狀烘焙工具。 你不再需要在獨立軟體中進行烘焙，也不必進行冗長的匯入和匯出流程。

**[參數](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)化：** 你幾乎可以透過一個滑桿或下拉選單來控制材質的任何面向。 這讓你能在單一資產上加入無限的控制與變化。

## 檔案類型

這個應用程式及其生態系統使用了四種不同的檔案類型。 說明一下：這些是從 Substance 3D Designer</b> 匯出的檔案類型<b>，可以匯入部分或所有其他 Substance 3D 應用程式。

<table>
<tr style="border: 0;">
<td style="border: 0;">

![](overview.resources/ds-sbs-48.png)

### 物質3D檔案

*(\*.SBS）*

Substance 檔案是 **Designer 的主要原始檔案** 。 當你打開一個 Substance 檔案時，你可以 **檢視並編輯圖**&#x200B;中的所有節點。 它們以套件形式呈現，可以包含任意數量的資源，如圖表、函式、位圖、網格等。它們較難分享，計算速度較慢。 它們只能在 Substance 3D Designer 和 Substance Player 中開啟。

</td>
<td style="border: 0;">

![](overview.resources/sbsar-48.png)

### Substance 3D 資產

*(\*.SBSAR）*

Substance Archives 是<b> 經過編譯、優化的</b> Substance 檔案。 它們計算起來快得多，且可以輕鬆分享，不會有參考問題。 參數仍可調整，但編輯圖表時會 <b>被鎖定</b>。 Substance Archives 可用於所有 Substance 3D 應用程式，以及任何具備 [Substance 3D 整合](https://experienceleague.adobe.com/zh-hant/docs/substance-3d/ecosystem/home) （部分包含外部外掛）的應用程式，例如 Autodesk 3DS Max 與 Maya、Unreal Engine 或 Unity Engine。

</td>
<td style="border: 0;">

![](overview.resources/bmp-96.png){width="48px"}

### 靜態檔案

*(\*.TGA、\*.BMP、\*.PNG、\*。FBX、\*。OBJ等...*

Substance 3D Designer 始終支援匯出為靜態檔案格式。 2D 影像可以匯出成點陣圖檔案，3D 模型可以匯出成常見的 3D 檔案類型。 匯出為靜態檔案時， **所有動態功能都會消失**。 影像被鎖定在解析度上，3D 模型被鎖定在多邊形數量上。

</td>
</tr>
</table>

這通常表示你在 Designer 裡工作時會保持作品的 SBS 格式，如果目標支援 SBSAR（例如 Painter），則匯出成 SBSAR，若不需要或不支援 SBSAR，則使用靜態點陣檔案。

## 資源類型

Substance 3D 檔案可以包含多種資源，這些資源服務於不同的用途。 有些資源只能在 Designer 裡面撰寫，有些則來自外部應用程式。

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;">

[![](overview.resources/graph-5.png){width="150px"}](../../compositing-graphs/substance-compositing-graphs.md)

</td>
<td width="100.00%" style="border: 0;">

### 物質圖

Substance 圖允許你產生並處理 *2D 影像資料* ，然後輸出到一個或多個貼圖輸出。 在許多使用案例中，專案會圍繞一個或多個 Substance 圖表展開。

[請前往專門討論物質圖表的章節。](../../compositing-graphs/substance-compositing-graphs.md)

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;">

[![](overview.resources/function-1.png){width="150px"}](../../function-graphs/function-graphs.md)

</td>
<td width="100.00%" style="border: 0;">

### 實體函數圖

<b>函式</b> 則是更高層次的抽象與複雜度：你 *不是處理影像資料（像素值集合），而是處理單一值* （整數、浮點數、向量）。 函式用於你想執行更複雜操作或想微調特定行為時。 函數通常無法獨立運作，且不會在 Substance 圖的上下文之外使用。

[請前往專門討論實體函數圖的章節。](../../function-graphs/function-graphs.md)

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;">

[![](overview.resources/folder-4.png){width="150px"}](../../resources/importing-linking-and-new/importing-linking-and-new-resources.md)

</td>
<td width="100.00%" style="border: 0;">

### 非圖資源

非圖形資源可來自外部應用程式（如 Photoshop 或 Autodesk Maya），而部分資源則 *可在 Designer* 內建立。 主要差異在於它們不是基於節點的圖;大多數都是用於前述圖類型內部或與之同時使用的元素。

存在以下資源類型：

* [位圖](../../resources/bitmap-resource/bitmap-resource.md)
* [向量圖形（SVG）](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md)
* [3D 場景](../../resources/3d-scene-resource/3d-scene-resource.md)
* [字體](../../resources/font-resource/font-resource.md)
* [AxF 檔案](../../resources/axf-appearance-exchange/axf-appearance-exchange-format.md)

</td>
</tr>
</table>
