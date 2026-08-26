---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/interface/preferences-window.html"
breadcrumb-title: ''
description: 在 Substance 3D Designer 中進入偏好設定視窗，自訂應用程式設定與行為。
helpx_creative_field: ""
helpx_description: Designer > Interface > Preferences
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 偏好設定
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '1973'
ht-degree: 0%

---


# 偏好設定視窗

![偏好設定視窗](../../assets/image2021-6-22-20-56-1.png "偏好設定視窗")

本頁呈現 <b>偏好設定</b> 視窗及其所有設定。

你可以透過 <b>應用程式主欄頂欄的編輯</b> 選單找到偏好設定視窗。 這個對話框讓你可以調整多種設定。 它以分頁形式組織，涵蓋不同的行為與功能領域。\
我們建議檢視所有這些設定，以更深入了解應用程式的運作方式，以及如何依照你的工作流程調整。

>[!NOTE]
>
> 若想了解更多關於這些偏好設定如何儲存以及如何整合到生產環境的資訊，可以參考 [文件中的使用者偏好設定 - 自動化設定](../../pipeline-and-project-con/user-preferences-aut/user-preferences-automating-setup.md) 頁面。

## 一般

### 近期文件

|  |                                                                                                                                         |
| --- |-----------------------------------------------------------------------------------------------------------------------------------------|
| <b>近期文件列表包含</b>  *預設值：10* | 這讓你能在主選單[&#128279;](../the-main-toolbar/the-main-toolbar.md)的檔案</b>項目中，選擇要列出<b>的「最近包裹</b>」項目<b>中的文件數量。 |

### 歷史記錄

|  |  |
| --- | --- |
| **歷史堆疊大小** *預設值：200* | 這表示主選單[&#128279;](../the-main-toolbar/the-main-toolbar.md)中編輯>復原</b>項目中，任何時候<b>可用的復原操作數量。**注意：** 你需要的復原操作越多，應用程式所需的記憶體就越多。 |

### 語言

|  |  |
| --- | --- |
| **選擇應用程式***語言 預設：系統* | 此設定定義了應用程式介面中使用的語言。 「*系統*」選項會自動偵測系統語言設定中的語言。 可用的語言列於我們的 [系統需求](../../getting-started/system-requirements/system-requirements.md)中。  **注意：**  更改此設定僅在重新啟動應用程式後生效。 |

### 觀點

|  |  |
| --- | --- |
| <b>反向放大檢視</b>  *預設：未勾選* | 如果勾選，縮放控制會在 2D 視圖[&#128279;](../../interface/2d-view/2d-view.md)、3D 視圖[&#128279;](../../interface/3d-view/3d-view.md)和[圖表](../../interface/the-graph-view/the-graph-view.md)中反轉。 |

### 路徑

|  |  |
| --- | --- |
| <b>儲存/匯出路徑</b>  *預設：最後一條路徑* | 判斷建議的儲存/匯出路徑是你最後選擇的路徑，還是 [SBS 套件](../../getting-started/overview/overview.md)的路徑。 最後選中的路徑會被儲存在多個會話之間。 |
| <b>暫存資料夾</b>  *預設：依系統作業系統而定的路徑* | 當圖的影像資料超過分配的記憶體池（見下方 <b>的記憶體>影像快取</b>）時，溢出的資料會寫入磁碟。 這個設定讓你可以定義溢出影像快取資料寫入的位置。   此位置同時也用於存放目前已開啟的 SBS 套件副本，該套件自上次手動存檔以來已進行最新修改。 |

### 記憶

#### 影像快取

應用程式會為當前圖中每個渲染節點保留一張 *全解析度、未壓縮的影像* 。\
實例節點會為其所參考圖中所有節點產生這些影像，並在計算出輸出[&#128279;](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)後刪除這些影像。此時只有輸出會被儲存在記憶體中。

你可以設定系統記憶體中為縮圖和圖片分配的最大快取大小，並查看目前的使用情況。 若快取資料超出其分配的池，多餘的資料會寫入 <b>暫存資料夾</b> （見上文 <b>「路徑>暫存資料夾</b>」）。

|  |  |
| --- | --- |
| <b>記憶體預算</b>  *預設：自動* | 此分配會自動計算至約 75% 的系統記憶體池。 若要手動設定此值，請選擇「*自訂*」選項，並在相鄰的輸入欄位設定一個值。 |

請注意，寫入磁碟 *的速度比寫入系統記憶體慢* 好幾個數量級。 因此，隨著溢出資料需寫入暫存資料夾，圖形渲染時間將 *呈指數* 增加。\
為避免這種情況發生，我們建議參考文件中效能優化指引[&#128279;](../../best-practices/performance-optimization/performance-optimization-guidelines.md)中減少圖表記憶體佔用的建議。

#### 工作排程器

在特定任務中，例如縮圖 [或 2D 視圖](../../interface/2d-view/2d-view.md)的影像轉換，會建立獨立工作並分散到系統處理核心以提升效率。 每個工作都會將資料寫入系統記憶體以執行其操作。\
這個設定讓你可以定義所有同時工作&#x200B;*所*&#x200B;分配的記憶體池。當此池全部使用完畢後，新工作會排隊等待，直到現有工作完成。

|  |  |
| --- | --- |
| <b>記憶體預算</b>  *預設：自動* | 此分配會自動計算至系統記憶體池約 10%。 若要手動設定此值，請選擇「*自訂*」選項，並在相鄰的輸入欄位設定一個值。 |

### 使用者介面

|  |  |
| --- | --- |
| **關閉高 DPI** *預設：未勾選* | <b>高 DPI</b> 模式可獨立於系統顯示與縮放設定，維持文字與使用者介面元素&#x200B;**&#x200B;的一致縮放。關閉（即填入&#x200B;*核取方塊*）會讓介面縮放，這會導致部分顯示器上的文字更大且更易讀，但也可能造成文字大小不一致及其他版面配置問題。**&#x200B;注意：**&#x200B; Designer 會從作業系統&#x200B;*取得特定尺度的使用者介面元素*。因此，任何對使用者介面縮放的調整都應在作業系統的顯示設定中進行。 為了確保在 Designer 中正確套用顯示設定，請 *登出* 作業系統使用者會話，並在更改這些設定後再登入。  &#x200B;** 注意：**  更改此設定僅在重新啟動應用程式後生效。 |

### 自動備份

預設包含自動儲存功能，會在指定時間段建立當前開啟 SBS 套件[&#128279;](https://docs.substance3d.com/display/DRAFTDESIGNER/.Overview+vDraftVersion)狀態的副本。自動存檔會放在 <b>SBS 套件位置的 .autosave</b> 資料夾中。

|  |  |
| --- | --- |
| <b>每 # 分鐘自動備份一次</b>  *預設值：5* | 每次自動存檔之間的時間。 |
| <b>持續關注 # 版本</b>  *預設值：6* | 任何時候最多要保留的自動存檔數量。 |

當版本數達到最大時，較新的備份會刪除最舊的備份。\
請注意，自動存檔應該在移&#x200B;*到原始 SBS 包位置後才開啟*。它們不&#x200B;*應該*&#x200B;在目前的位置開啟。

### 發布與傳送 SBSAR 檔案

|  |  |
| --- | --- |
| <b>發佈到 .sbsar 或傳送到其他應用程式時，請務必儲存 .sbs 檔案</b>  *預設：真* | 控制 SBS 套件在發佈[&#128279;](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md)或傳送至其他應用程式時的自動儲存。 |

### 爐子

|  |                                                                                                                                                                                                                                                                                                 |
| --- |-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>烹飪尺寸限制</b>  *預設值：8192 像素* | 定義了任一 Substance [圖](../../compositing-graphs/substance-compositing-graphs.md)中所有節點允許的最大像素解析度。 由於圖形輸出總是解析度為2的冪方形影像，此處設定的值定義了最大寬度與高度（以像素為單位）。 |

### 引擎

|  |  |
| --- | --- |
| <b>GPU 快取限制</b>  *預設值：2048 MB* | 這個設定讓你可以定義應該保留多少記憶體給快取渲染階段。 通常，Substance Engine 會將每個節點的輸出快取到 Substance 圖中。 |

>[!NOTE]
>
> 我們建議參考文件中效能優化指引[&#128279;](../../best-practices/performance-optimization/performance-optimization-guidelines.md)中減少圖形記憶體佔用的建議。

## 專案

請參閱 [專案設定](../../interface/preferences-window/project-settings/project-settings.md) 頁面。

## 圖

### 常見

|  |  |
| --- | --- |
| <b>Tab 鍵顯示節點選單</b>  *預設：已勾選* | 勾選後，「Tab」鍵會開啟 <b>節點選單</b>，模擬「空格」鍵的功能。 |
| <b>透過點擊拖曳連接器來建立節點</b>  *預設：已勾選* | 如果勾選，點擊任何連接器時，拖曳游鼠元並釋放已建立連結到圖形空白區域，即可顯示 <b>節點選單</b>。   選單也會根據 *被點擊的連接器類型進行* 篩選。 這表示只有與點擊接頭相容的節點才會被顯示。 |
| <b>開啟圖表時，以 3D 視圖查看輸出</b>  *預設：已勾選* | 若勾選，所有圖形輸出會在打開 3D 視圖[&#128279;](../../interface/3d-view/3d-view.md)時自動套用。這也會渲染所有屬於串流 [的節點，這些節點會指向輸出](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) 節點。 |

### 物質合成圖

|  |  |
| --- | --- |
| <b>開啟圖表時自動計算所有節點的縮圖</b>  *預設：已勾選* | 如果勾選，載入圖表時會自動渲染所有節點縮圖。 |
| <b>開啟圖表時以 2D 視圖查看輸出</b>  *預設：已勾選* | 若勾選，打開 2D 檢視[&#128279;](../../interface/2d-view/2d-view.md)時，第一個圖的輸出會自動顯示。這也會渲染所有屬於串流的節點，這些節點會被導向該 [輸出](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) 節點。 |
| <b>自動顯示新建立的合成節點</b>  *預設：已勾選* | 若勾選， [2D 檢視](../../interface/2d-view/2d-view.md) 會自動更新，顯示新建立節點的輸出。 |
| <b>自動插入色彩/灰階轉換節點</b>  *預設：未勾選* | 若勾選，則會自動解決色彩/灰階連線類型不匹配，透過 *放置特定節點* 執行適當的轉換。   當灰 *階* 輸出（灰色連接器）連接到 *彩色* 輸入（黃色連接器）時， [梯度映射](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/gradient-map/gradient-map.md) 節點會自動放置在兩個連接器之間。   當彩色&#x200B;**&#x200B;輸出（黃色連接器）連接到&#x200B;*灰階*&#x200B;輸入（灰色連接器）時，[灰色轉換](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/grayscale-conversion/grayscale-conversion.md)節點會自動放置在兩個連接器之間。 |
| <b>在情境中啟用圖形編輯</b>  *預設：未勾選* | 預設情況下，當右鍵點擊該節點並選擇<b>「開啟參考</b>」來開啟由[實例節點](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)參考的圖時，該圖會被獨立&#x200B;*載入並編輯*。如果勾選，你可以利用當前圖在實例&#x200B;*中傳遞的資訊，編輯實例*&#x200B;所參考的圖。操作方法是右鍵點擊實例節點，選擇 <b>「在上下文</b>中開啟參考」，或使用 Ctrl+E 鍵擊。   這表示實例化的圖可以在其所實例化的圖上下文中進行編輯。 這對於觀察編輯對你正在處理的圖表產生的影響非常有幫助。 請參考下方範例。  **注意：**<b>使用上下文編輯時，圖表屬性[&#128279;](../../compositing-graphs/graph-parameters/graph-parameters.md)中會&#x200B;*關閉*&#x200B;預覽</b>和<b>預設</b>分頁。 |

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![禁用](../../assets/substance3ddesigner_incontext_no.gif "上下文編輯 關閉上下文編輯")

*公開參考*

</td>
<td style="border: 0;" valign="top">

![啟用](../../assets/substance3ddesigner_incontext_yes.gif "上下文編輯 啟用上下文編輯 啟用上下文編輯")

*上下文中的開放參考*

</td>
</tr>
</table>

## 3D 檢視

### 其他

|  |  |
| --- | --- |
| <b>預設隱藏環境</b>  *預設：已勾選* | 決定 [環境](../../interface/3d-view/3d-view.md) 預設的可見性設定。 隱藏時，3D 視角的背景會被 *純色*&#x200B;取代。 |
| <b>視窗縮放</b>  *預設：自動* | 當系統使用顯示縮放時，控制 3D View 渲染解析度的縮放。<ul data-preserve-html="true"> <li data-preserve-html="true"><i>自動</i>：渲染解析度是基於 <i>縮放後</i> 的顯示解析度</li> <li data-preserve-html="true"><i>無：</i>渲染解析度是基於 <i>原生</i> 顯示解析度</li> </ul> |

### OpenGL

|  |  |
| --- | --- |
| <b>樣本計數</b>  *預設值：64* | 會影響 3D View 著色器樣本表的大小。 較高的數值會帶來更高的影像品質，但效能會有所下降。  **注意：**  著色器的取樣表也會受到系統 GPU 和作業系統的影響。 |

## 烘焙師

|  |  |
| --- | --- |
| <b>GPU 光線追蹤</b>  *預設：已勾選* | 如果被檢查，會對相容烘焙器的[&#128279;](https://experienceleague.adobe.com/zh-hant/docs/substance-3d/bakers/features/gpu-raytracing) GPU 執行光線追蹤。以下 GPU 光線追蹤後端將依 NVIDIA GPU 架構而定為預設：<ul data-preserve-html="true"> <li data-preserve-html="true"><i>DXR</i>：圖靈與更新版本</li> <li data-preserve-html="true"><i>Optix</i>：Pascal 與 Maxwell</li> </ul>  **注意：**&#x200B;更多關於 GPU 驅動烘焙器的資訊，請參閱 [Substance Bakers](https://experienceleague.adobe.com/zh-hant/docs/substance-3d/bakers/home) 文件中的 [GPU 光線追蹤](https://experienceleague.adobe.com/zh-hant/docs/substance-3d/bakers/features/gpu-raytracing)部分。**提示：**&#x200B;啟動應用程式時，你可以使用以下&#x200B;*命令列參數*&#x200B;強制&#x200B;**&#x200B;使用不同的 GPU 光線追蹤後端：<ul data-preserve-html="true"> <li data-preserve-html="true"><code>--原力-光學</code> ： 強制在 Nvidia Turing 或更新 GPU 上使用 Optix</li> <li data-preserve-html="true"><code>--強制DXR</code> ： 強制在 Nvidia Pascal GPU 上使用 DXR</li> </ul> |

## 圖書館

|  |  |
| --- | --- |
| <b>重建縮圖</b> | 這個選項會觸發重新計算所有 [函式庫](../../interface/the-library/the-library.md) 縮圖，並自動替換之前的縮圖。 |

## 捷徑

你可以自訂鍵盤快捷鍵來建立圖表中的節點。

所有圖類型的 [節點都可以指派捷徑：Substance 圖](../../compositing-graphs/substance-compositing-graphs.md)、 [Substance 函數圖和](../../function-graphs/function-graphs.md) [FX-Map 圖](../../function-graphs/fxmaps/fxmaps.md)。

任何節點都可以被分配捷徑，甚至是自訂函式庫節點。 同一捷徑可在不同圖型中分配。 預設不會設定捷徑，你可以自由自訂。

若與其他節點捷徑或內建程式捷徑衝突，該條目會被高亮顯示並顯示警告。 在衝突解決前，捷徑不會生效&#x200B;**。

>[!IMPORTANT]
>
> 捷徑被 Python 外掛覆蓋
> 
> 當 Python 外掛定義了指派給節點的鍵盤快捷鍵時，該外掛會覆寫該快捷鍵。 這表示金鑰會觸發插件動作，而不是建立節點。
> 
> 這已經適用於節點對齊工具[&#128279;](../../interface/the-graph-view/node-alignment-tools/node-alignment-tools.md)所使用的 H、S 和 V 鍵。
