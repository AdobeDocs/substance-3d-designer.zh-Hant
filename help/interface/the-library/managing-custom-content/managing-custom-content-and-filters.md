---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/the-library/managing-custom-content-and-filters.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D 設計器庫中管理自訂內容與篩選器，以便有組織地存取資產。
helpx_creative_field: ""
helpx_description: Designer > Interface > The Library > Managing custom content and filters
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 管理自訂內容與過濾器
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '912'
ht-degree: 0%

---


# 管理自訂內容與過濾器

本頁說明如何建立分類與篩選器，以管理圖書館中的自訂內容。 同時也包含專案導向工作流程的建議。

## 概觀

在新增自訂內容到圖書館](../../../interface/preferences-window/project-settings/project-settings.md)後[，你需要讓它&#x200B;*變得可*&#x200B;被發現。

圖書館使用多個 *資料點* 來識別內容，以便篩選並在搜尋中浮現。 這些數據點包括：

* 名稱
* 延伸
* 網址（即 *檔名*）
* 屬性

你可以將 <b>圖書館</b> 組織成包含特定篩選器的類別，並依專案需求調整。\
事實上，自訂分類與篩選器可以針對專案特定，*並儲存在[專案檔案](../../../interface/preferences-window/project-settings/project-settings.md)（\*.sbsprj）。*這些檔案接著可以組合成 [設定檔](../../../interface/preferences-window/project-settings/project-settings.md) （\*.sbscfg），並分發給團隊，讓藝術家都能在任何專案中使用*&#x200B;相同的 <b>函式庫</b> 類別* 。

這表示只要有一個或多個專案檔案，你可以設定應該加入 <b>函式庫</b>的內容資料夾，以及分類和篩選器來排序和整理這些內容。

![圖書館](managing-custom-content-and-filters.resources/managing-custom-content-and-filters-01.png "中的自訂內容 圖書館中的自訂內容")

## 圖屬性

SBS 與 SBSAR 檔案中的圖表[可&#x200B;*透過圖屬性區塊中的資料](../../../compositing-graphs/graph-parameters/graph-parameters.md)集[進行篩選與搜尋*。](../../../getting-started/overview/overview.md) [](../../../getting-started/overview/overview.md)這些屬性中有些也可以設定在其他 [資源類型](../../../resources/resources.md)上。

## 自訂篩選器與資料夾

篩選器是簡單的布林值（真/假）搜尋參數，當選擇該 <b>篩選器</b> 時，該資源會顯示在函式庫內。 資源可以是任何放在包裝裡的東西。 請記住以下幾點：

* 過濾器<b></b>會根據所有監控路徑&#x200B;*與所有資源*&#x200B;進行匹配。
* 一個 <b>過濾器</b> 可以包含多個條件， *所有條件都必須評估為 True* （AND-condition），資源才會顯示在該過濾器下。
* 一個 [資源](../../../resources/resources.md) 可以出現在多個篩選條件下，並不排 *斥* 於任何篩選條件。
* [即使&#x200B;**&#x200B;未被任何篩選</b><b>器，<b>來自監控路徑的資源](../../../resources/resources.md)仍可&#x200B;*透過搜尋</b>功能在<b>函式庫中</b>取得*。

### 如何建立篩選器和資料夾

分類（即資料夾）和篩選器是透過以下按鈕建立與編輯的：

<b>![](managing-custom-content-and-filters.resources/managing-custom-content-and-filters-02.png) 新增資料夾：</b> 在圖書館檢視中建立可擴充的資料夾。 你 *無法* 建立子資料夾。

<b>![](managing-custom-content-and-filters.resources/managing-custom-content-and-filters-03.png) 新增過濾器：</b> 在所選資料夾中新增一個新的過濾器。 你 *無法* 在現有的預設資料夾中新增過濾器。

<b>![](managing-custom-content-and-filters.resources/managing-custom-content-and-filters-04.png) 編輯項目：</b> 編輯目前選取的資料夾或過濾器。 你 *無法* 編輯預設資料夾和過濾器的任何屬性。

要 *移除* 資料夾或過濾器，請 *右鍵點擊* 該資料夾，然後從上下文選單中選擇 <b>「移除</b> 」選項。

### 編輯濾鏡與資料夾

<b>資料夾</b> 與 <b>過濾器</b> 可透過以下資料識別：

* <b>名稱</b> 顯示在圖書館樹狀圖中。
* [專案設定檔（SBSPRJ），](../../../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md) 其中儲存此項目。

>[!WARNING]
>
> 正確設定這些檔案非常重要&#x200B;**，以確保你編輯&#x200B;*的是正確的專案*！

![自訂濾鏡版](managing-custom-content-and-filters.resources/managing-custom-content-and-filters-05.png "自訂濾鏡版")

**過濾器**&#x200B;通常需要設定&#x200B;**&#x200B;條件以達成過濾目的。這些條件依據以下標準進行配置：

* **資源類型**：設定特定的 [資源類型](../../../resources/resources.md)，例如 [圖表](../../../compositing-graphs/substance-compositing-graphs.md)
* ****&#x200B;屬性可套用條件 – 見上文列表
* **條件邏輯**：讓濾波器包含正、負、部分及全匹配結果
* **條件關鍵字：** 用來 **測試屬性** 與 **條件邏輯** 標準的字串。 若留空，則包含符合這兩個條件的任何資源

你可以&#x200B;*使用條件關鍵字最右邊的 &#39;**+**&#39; 和 &#39;**x**&#39; 按鈕新增或移除*&#x200B;條件。

>[!NOTE]
>
> 若未設定&#x200B;****任何條件，則所有圖書館**&#x200B;內容都會被顯示。  

## 最佳實務

### 建議指引

* 預設函式庫的一般規則是<b></b>資料夾列在<b>類別</b>屬性中，而<b>過濾器</b>名稱則由<b>標籤</b>屬性決定
* 除非你 *明確* 想要，否則不要建立與預設函式庫混合的自訂節點。 如果你的節點 *匹配，它們會出現* 在預設篩選器下，所以你必須確保使用 *不同的標籤/命名系統* 以避免這種情況
* 使用&#x200B;*獨特的*&#x200B;專案&#x200B;**&#x200B;識別碼。只要所有專案保持一致&#x200B;**，這些都可以放在你想要的任何地方（例如<b>描述</b>、<b>分類</b>或<b>使用者資料</b>）。這讓依專案&#x200B;*搜尋和篩選內容*&#x200B;變得更簡單
* 使用 <b>作者</b> 屬性來追蹤最初負責內容的人，而不必翻閱版本控制紀錄
* 建立<b>圖示</b>的有效方法是使用<b>圖示](../../../compositing-graphs/graph-parameters/graph-parameters.md)圖屬性中的[生成</b>選項，或建立[圖譜範本](../../../interface/preferences-window/project-settings/project-settings.md)來產生圖示。這樣你才能確保一致性，省下製作工作量。 所有預設的圖書館圖示都是這樣在 Designer 裡建立的！

### 管理不同範圍的內容

* 如果這樣比較合理，你可以把資源加入 *現有的分類* 。 這樣管理和維護濾鏡的工作量會比較少，而且你可以用特殊的圖示樣式來 *區分*&#x200B;它們。
* 你可以在&#x200B;*全域*（工作室層級）[的專案設定檔](../../../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md)中定義資料夾和篩選器，然後只需從連續[*的專案檔案中加入觀看路徑*，即可新增內容](../../../interface/preferences-window/project-settings/project-settings.md)
* 你可以為每個專案&#x200B;*設定特定的資料夾和篩選器*，讓它們保持分隔
* 你可以混合搭配上述三種方法：使用現有篩選器、定義新的全域篩選器，以及建立每個專案獨一無二的篩選器
