---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/manage-parameters/exposing-a-parameter.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Designer 合成圖中暴露參數，使材質可自訂且可重複使用。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Exposing a parameter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 暴露參數
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '2267'
ht-degree: 0%

---


# 暴露參數

參數曝光是最強大的工具之一，也是將圖表開放給其他應用程式的關鍵，例如 Substance 3D Painter、Substance 3D Sampler 以及 Maya 和 3DS Max 的 Substance Integrations。

本頁說明所有開始學習所需的概念。 建議 [你先了解什麼是圖實例](../../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)，再繼續閱讀本頁。 了解發佈和匯出的差異，以及相關的檔案類型也很有幫助[。](../../../getting-started/overview/overview.md)

![參數曝光簡化](exposing-a-parameter.resources/exposing-a-parameter-01.png "參數曝光簡化")

*上方的透明線條是連接的抽象表示\
從公開參數到圖參數。*

## 了解參數與曝光

+++什麼是參數？
*參數是一個簡單的值，帶有 UI 元素，用來控制圖的行為。* 你在所有 Substance 軟體中都會不斷使用它們：改變顏色、設定混合模式、選擇不透明度值等等......沒有參數的話，Substance 軟體根本不允許任何自訂。

參數可以有許多不同的形式：滑桿、旋鈕、輸入框、下拉選單等等......它們所代表的值可以有許多不同類型：十進位值、整數值、布林值（真/假值），甚至是文字片段。

+++

+++什麼是「揭露」？
***暴露是讓參數在你目前的圖視圖之外可用。***  在建立圖時，通常會選擇節點來更改其屬性中的參數;當暴露時，你可以 *從外部控制面板*&#x200B;啟用這個參數。 這個「外部控制面板」會根據上下文有不同含義：當它作為 Designer 內的圖實例時，它只是另一個節點。 當使用 Substance 3D Painter、Substance 3D Sampler 或整合時，這些暴露的參數將是 *你對圖表唯一的控制* 。

+++

+++為什麼揭露有用？
***Exposing Parameters讓Substance 3D Designer超越了簡單的貼圖編輯器，讓你能創造可自訂、動態的貼圖生成工具***  **。** 如果不曝光，Substance Material 和靜態材質差不多：你無法修改它們的輸出。

+++

+++為什麼不一直自動暴露所有參數？
<b> [物質圖表](../../../compositing-graphs/substance-compositing-graphs.md)可能非常複雜，且可能同時包含數百個參數。 不應該總是向使用者展示所有參數，尤其是當你建立一個簡單目標、不需要太多參數的圖形時。</b> 在揭露參數時，你是 UI 或 UX 設計師：你會思考哪些控制項合理、哪些數值需要，以及如何讓它對自己、線上其他使用者或同事都容易使用。

+++

+++我需要懂數學才能曝光嗎？ 我應該理解物質函數圖嗎？
***不必具備數學知識即可良好運用 Exposing Parameters，函數的使用也不需要。***  作為初學者，你幾乎可以完全避免在函數圖[&#128279;](../../../function-graphs/function-graphs.md)中做數學運算。唯一強烈建議的是對不同資料類型有 [不錯的基礎知識，例如整數、浮點數和布林。](../../../function-graphs/nodes-reference-for-fun/function-nodes-overview/function-nodes-overview.md)

+++

## 如何揭露

目前有兩種主要方法來揭露參數。 一種方法較適合快速暴露單一參數，後者則較適合一次掃描多個參數。

![單曝光方法攻略](exposing-a-parameter.resources/exposing-a-parameter-02.gif "單張曝光法攻略"){width="512px"}

### 單曝光法

1. 在屬性[&#128279;](../../../interface/properties/properties.md)面板的「特定參數」標籤下找到你想暴露的參數
1. 點選下 ![](exposing-a-parameter.resources/exposing-a-parameter-03.png) 拉選項按鈕
1. 從下拉選單中選擇![](exposing-a-parameter.resources/exposing-a-parameter-04.png)<b>「暴露」作為新圖形輸入</b>，這是第一個選項。
1. <b>會出現 Expose 參數</b>對話框，請依照你的需求設定任何參數屬性。

   建議至少更改 <b>識別碼</b> 與 <b>標籤</b>
1. 請按 <b>確定</b> 鍵以確認
1. 參數名稱變 *為藍色*，且 ![](exposing-a-parameter.resources/exposing-a-parameter-05.png)\
   <b> 在下拉選單旁邊會出現「編輯參數功能</b> 」按鈕，確認參數是否公開

>[!NOTE]
>
> 大多數數值領域都支援 *基本的數學公式* 作為輸入——例如， `17+3.5`， `7/3`， `(4+2)*3`， ， 按下 *Enter* 鍵驗證公式，結果會被輸入欄位。 若公式無效，欄位會回復到先前的值。\
> 應用程式其他部分的部分數值欄位，例如 [屬性](../../../interface/properties/properties.md) 底座，也支援此功能。

![批次暴露方法攻略](exposing-a-parameter.resources/exposing-a-parameter-06.gif "批次暴露方法攻略"){width="512px"}

### 批次曝光法

當暴露一個參數時，此方法會比前一種稍慢。 當暴露多個參數時，速度會快得多。

1. 不要只找單一參數，而是在「特定參數</b>」標籤右上角<b>的![](exposing-a-parameter.resources/exposing-a-parameter-07.png)<b>多重曝光</b>按鈕
1. 從下拉選單選擇<b>批次曝光參數</b>
1. <b>會出現「批次曝光</b>」對話框，讓你自訂節點所有<b>特定參數的曝光方式</b>
1. 使用 <b>全部</b>、 <b>無</b> 或特定核取方塊來決定要暴露哪些參數
1. 點擊列表中圖輸入識別碼</b>欄下的<b>參數名稱即可更改其名稱。
1. 點擊<b>列表中圖輸入群組</b>欄下的<b>群組名稱</b>，即可為特定參數新增一個（子）群組
1. 使用 <b>底部的 Graph 輸入識別碼</b> 與 <b>Graph 輸入群組</b> 打字框，一次為所有暴露參數新增前綴、後綴與輸入群組。 所有這些數值都套用在每個參數設定之上。
1. 點擊 <b>確定</b> 以確認並顯示所有選取的參數。 參數名稱現在會顯示&#x200B;*藍色*，以確認參數已被揭露，並且有![](exposing-a-parameter.resources/exposing-a-parameter-05.png)<b>編輯功能</b>按鈕。

## 限制

暴露參數存在一些限制，詳見下表。

| 參數類型 | 原因 |
| --- | --- |
| [漸層斜坡](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/gradient-map/gradient-map.md)、 [曲線編輯器](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/curve/curve.md)、 [字型](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md)、 [關卡直方圖](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/levels/levels.md) | 要求無法提供使用者自訂參數的小工具。 |

另一個重大限制與靜態參數[&#128279;](../../../glossary/glossary.md)有關[。這些在已發佈的Substance 3D資產（SBSAR）](../../publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md)中無法更改。

靜態參數——與動態參數不同——*在圖*&#x200B;被煮熟&#x200B;*後無法即時編輯，也就是說，為了快速且有效率地執行演算法，無法即時編輯*。每次圖表被 *編輯* 或 *發佈*&#x200B;時，Designer 都會進行煮食。

因此，靜態參數在 Designer 中可見且可編輯，但在已發佈的 Substance 3D 資產中則隱藏&#x200B;**。你可以使用預覽模式查看這些限制，然後再發佈到 Substance 3D 資產：詳見下方「預預覽參數」。

作為一個變通方法，你可以使用 [開關](../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blending/switch/switch.md) 或 [多重開關](../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blending/multi-switch/multi-switch.md) 節點，並搭配多組邏輯在這些參數的不同值/狀態間切換。

| 節點 | 參數 |
| --- | --- |
| 所有節點 | 平鋪模式像素比率 |
| [制服顏色](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/uniform-color/uniform-color.md) | 彩色模式 |
| [像素處理器](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md) | 彩色模式 |
| [混合](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md) | 混合模式 Alpha 混合 裁切區域 |
| [效果圖](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md) | 混合模式 |
| [象限](../../../function-graphs/fxmaps/the-quadrant-node/the-quadrant-node.md) | 圖案輸入影像 alpha 輸入影像過濾 |

## 修改外洩參數

一旦暴露，就無法像以前那樣存取參數。 更改其值、重新命名、在介面中排列，甚至移除參數，這些都在圖屬性層級完成。 本節詳細說明如何做到。

要更改外露參數的選項，請：

1. 點擊已曝光參數旁的下拉選項按鈕![](exposing-a-parameter.resources/exposing-a-parameter-03.png)
1. 選擇 ![](exposing-a-parameter.resources/exposing-a-parameter-04.png)<b> 編輯暴露的圖形輸入</b>。 這會直接帶你到圖屬性中相關的項目
1. 在圖的空白區域雙擊進入圖屬性，然後在輸入參數清單 <b>中找到該參數</b>
1. 在檔案總管</b>中單擊你的圖表<b>，然後在輸入參數列表中<b>找到該參數</b>

![輸入參數](exposing-a-parameter.resources/exposing-a-parameter-08.png "輸入參數"){width="512px"}

### 輸入參數

所有暴露的參數都列在輸入參數標籤下。 以下屬性適用於大多數常見情況，例如帶有預設編輯器類型的浮點數與整數。

1. <b>識別碼</b>：此參數的唯一識別碼。 不能包含空格或特殊字元。
1. <b>標籤</b>：僅 UI 標籤。 若未定義標籤，識別碼會在使用者介面中顯示。 可以包含空格和特殊字元
1. <b>群組</b>：將參數群組成可摺疊區塊，保持長串參數清晰且易於管理。 如果參數擁有 *完全相同的* 群組名稱，則會被歸為一組。 利用字 `/` 元來建立 *子群組* ——例如： `My Group/My Sub-group`
1. <b>說明：描述欄位</b>，作為提示。
1. <b>類型 / 編輯器</b>：設定資料型別以及 UI 編輯器類型。 某些編輯器僅適用於特定資料類型（例如整數的下拉選單）。 *更改編輯器在很多情況下會清除預設值，請小心。*
1. <b>預設</b>值：參數起始的預設值。 這也是你預覽節點時圖表中使用的數值。 試著用一個簡單且實用的數值，避免極端情況。
1. <b>最低</b>值：失業保險的最低價值
1. <b>最大</b>值：UI 的最大價值
1. <b>夾具</b>：設定最小值和最大值是軟性或硬性限制（允許使用者超過限制）。
1. <b>逐步調整</b>:Set 價值的精確度或細緻度。
1. <b>使用者資料： </b>自訂使用者資料，可用於任何用途。
1. <b>可見 If</b>：特殊的表達系統，可根據外部條件顯示或隱藏參數。 參見 [可見 if：控制輸入、輸出與參數的可見性](../../../compositing-graphs/visible-control-vis/visible-if-control-visibility-of-inputs-outputs-and-parameters.md)

![整數參數](exposing-a-parameter.resources/exposing-a-parameter-09.gif "下拉清單編輯器整數參數下拉清單編輯器"){width="512px"}

#### 下拉選單

一個特殊情況是整數型別的 <b>下拉選單</b> 。 沒有預設值、最小值或最大值，只有一個值設定，讓你可以定義一串項目。

* 每個項目對應下拉選單中的一個項目。
* Item 的第一個值是圖實際使用的內部整數。 例如，請確保你為多 [開關](../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blending/multi-switch/multi-switch.md) 正確設定這些（它們是從 1 開始，不是 0）。
* 第二個值是顯示給使用者的 UI 標籤。
* 第三個勾選框允許你標記一個物品為預設選取的項目。
* X 是刪除一個項目，+ 是新增一個項目

![重新排序輸入參數](exposing-a-parameter.resources/exposing-a-parameter-10.gif "重新排序輸入參數"){width="512px"}

#### 重新訂購

參數的重新排序可以輕鬆地透過拖放輸入參數名稱左側的深色條紋握柄來完成。 要注意，分組參數會影響順序。

![預視輸入參數](exposing-a-parameter.resources/exposing-a-parameter-11.gif "預視輸入參數"){width="512px"}

### 預覽參數

由於設定參數時無法看到最終結果 <b>，可以啟用預覽模式</b> ，檢查參數介面在外部的外觀與行為。 點擊 <b>輸入參數下落區中上方的預覽</b> 標籤。

通常，預覽<b>模式</b>中所做的任何變更都會被&#x200B;**&#x200B;捨棄。不過你可以用眼睛圖示旁的<b>「套用」按鈕</b>，將預覽模式</b>目前的數值<b>設為&#x200B;*新的預設值*。

[預覽模式也允許你建立嵌入式預設。](../../../compositing-graphs/manage-parameters/parameter-presets/parameter-presets.md)

>[!IMPORTANT]
>
> 使用 [上下文編輯](../../../interface/preferences-window/preferences-window.md)時，預覽模式會被關閉。

>[!WARNING]
>
> 預覽模式旨在盡可能準確地呈現已發佈的 Substance 3D 資產（SBSAR[&#128279;](../../publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md)）的體驗。因此，本頁列出的限制在此模式下也會適用，例如 *列表中缺少*&#x200B;靜態參數。

![複製並貼上輸入參數](exposing-a-parameter.resources/exposing-a-parameter-12.gif "複製並貼上輸入參數"){width="512px"}

### 複製貼上參數

參數可以在圖之間複製貼上。

可透過複製按鈕 ![](exposing-a-parameter.resources/exposing-a-parameter-13.png)複製單一參數。 多個參數可透過參數選單 ![](exposing-a-parameter.resources/exposing-a-parameter-07.png)複製。 選擇複製輸入以複製所有輸入。

在參數選單![](exposing-a-parameter.resources/exposing-a-parameter-07.png)中選擇「貼入輸入」![](exposing-a-parameter.resources/exposing-a-parameter-14.png)來貼上一個或多個參數。

如果你想轉移數值，而不是實際暴露的參數本身，可以 [閱讀關於參數預設（Parameter Presets）的相關資料。](../../../compositing-graphs/manage-parameters/parameter-presets/parameter-presets.md)

## 移除與清潔暴露參數

由於參數的特性，例如輸入參數可能控制多個節點，或輸入參數存在但不控制節點，可能會出現缺少或未使用的參數問題。 以下將說明常見問題及其解決方案。

![節點參數](exposing-a-parameter.resources/exposing-a-parameter-15.gif "錯誤節點參數錯誤"){width="512px"}

### 追蹤節點上破損的參數

你可以透過節點搜尋工具追蹤哪個節點使用的參數，該工具 ![](exposing-a-parameter.resources/exposing-a-parameter-16.png)位於圖圖檢視的頂欄。 點擊它，你可以用特定參數找到節點。

如果節點真的有問題，會在左上角顯示警告徽章 ![](exposing-a-parameter.resources/exposing-a-parameter-17.png) 。 將滑鼠移到徽章上會顯示一個提示，裡面有更多資訊。

要重設並移除問題，針對你想修正或重設的參數，請點擊編輯功能按鈕旁的下拉選![](exposing-a-parameter.resources/exposing-a-parameter-03.png)單，選擇![](exposing-a-parameter.resources/exposing-a-parameter-18.png)<b>重設。</b>這會將參數回復到先前未曝光的狀態，藍色名稱會再次變為灰色以反映此情況。

![清理未使用的輸入參數](exposing-a-parameter.resources/exposing-a-parameter-19.gif "清理未使用的輸入參數"){width="512px"}

### 清理未使用的輸入參數

如果你已經失去輸入參數的蹤跡，不知道哪些參數被使用，可以用一個小工具清理。 點擊輸入參數選單按鈕 ![](exposing-a-parameter.resources/exposing-a-parameter-07.png) ，選擇 <b>乾淨輸入。</b>

會跳出一個新對話框，列出所有未使用的參數。 勾選或取消你想移除或保留的參數，然後點選確定。 如果沒有對話框，表示目前沒有未使用的參數需要清理。

![移除參數](exposing-a-parameter.resources/exposing-a-parameter-20.gif "移除參數"){width="512px"}

### 移除參數

要實際移除正在使用的參數，需要兩個不同的步驟。

1. 在有暴露參數的節點上，點擊「函式暴露」按鈕右側藍色的下拉箭頭： ![](exposing-a-parameter.resources/exposing-a-parameter-21.png)。 然後選擇「重置為預設值」。 這樣就不用再用這個節點的參數。 對使用相同參數的其他節點重複此法。 「Reset to Default value」也會將參數小工具的範圍重置為軟 *範圍*。
1. 在圖的輸入參數清單中，點擊參數最右邊的 X。 這樣會完全刪除該參數。 若有節點嘗試使用此參數，將會出現警告徽章（見上文）。
