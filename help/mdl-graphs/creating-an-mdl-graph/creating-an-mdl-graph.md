---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/mdl-graphs/creating-an-mdl-graph.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Designer 中建立材料定義語言圖表，以進行自訂材料製作。
helpx_creative_field: ""
helpx_description: Designer > MDL graphs > Creating an MDL graph
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 建立 MDL 圖
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '588'
ht-degree: 0%

---


# 建立 MDL 圖

本頁說明如何在 Substance 3D Designer 中建立 MDL 圖以撰寫 MDL 材料的過程。

![MDL 圖建立路徑](../../assets/mdl-new-graph-hl.png "MDL 圖建立路徑")

*在 Designer 介面中建立新 MDL 圖形的路徑*

## 建立 MDL 圖的方法

您可以使用以下任一方法建立 MDL 圖：

* 在主選單欄選擇新> MDL 圖表&#x200B;**選項&#x200B;*>**&#x200B;檔案*
* 點擊![](../../assets/mdl-new-graph-icon.png)**主工具列中的&#x200B;*「新增 MDL 圖表**」按鈕*
* 在檔案總管面板中右鍵點擊&#x200B;*現有套件&#x200B;***，選擇**&#x200B;新> MDL 圖表&#x200B;**選項**

您將看到 **新的 MDL 圖表** 對話框，詳見下方。

![新 MDL 圖對話框](../../assets/mdl-templates.png "新 MDL 圖對話")

*新的 MDL 圖形對話框*

## 新的 MDL 圖形對話框

無論用哪種方法建立新的 MDL 圖，你都會 <b>看到「新 MDL 圖</b> 」對話框，讓你可以設定新的圖。

### 範本

模板<b></b>區塊允許你選擇圖模板，包含預先設定的節點，幫助你更快開始製作圖。預先設定的節點包括輸出節點、簡單節點，用來傳遞這些輸出值——例如，統一顏色，以及依範本而定的輸入節點。

要從完全 *空白* 的圖形開始，選擇 <b>Empty</b> 範本。

專案<b></b>選項可以依專案檔案篩選範本清單。這讓你很容易在專案設定的一般</b>區塊中找到自訂<b>範本。

>[!WARNING]
>
> 如果你選擇錯誤的範本， *建立圖表後就無法* 切換到其他範本。\
> 要將現有的圖表移植到另一個範本，你可以使用相應的範本建立一個新的圖表，然後複製貼上你的圖表到新的模板。 視情況重新連接節點，包括 [根](../../mdl-graphs/main-mdl-graph-concepts/main-mdl-graph-concepts.md) 節點。

範本清單可透過&#x200B;*專案&#x200B;**組合框旁**&#x200B;的按鈕*&#x200B;以不同模式顯示：

* **![](../../assets/mdl-template-recent-icon.png)顯示最近使用的**：篩選清單，依照最近到最近的&#x200B;*順序顯示最後使用的*&#x200B;範本，頂端為最新的項目
* **![](../../assets/mdl-template-graphs-icon.png)顯示圖表**：範本僅&#x200B;*依標籤*&#x200B;顯示，依模板目錄中 Substance 3D[&#128279;](https://www.adobe.com/products/substance3d/3d-augmented-reality.html) 檔案的順序排列
* **![](../../assets/mdl-template-packages-icon.png)顯示 Substance 3D 檔案**：範本依其標籤顯示，作為 *其所屬* Substance 3D 檔案的子檔，依範本目錄中檔案的順序排列
* **![](../../assets/mdl-template-directory-icon.png)顯示目錄**：範本依照其所屬&#x200B;*目錄的子目錄*&#x200B;標籤顯示，順序依照範本目錄中檔案的順序排列

### 屬性

<b>圖屬性</b>區塊允許你設定新圖的基本資訊。這些都可以隨時更改，但一開始就要注意並根據你的使用情境適當設定是合理的。

* <b>圖名</b>：圖的識別碼。 它必須對特定套件唯一，且不能包含空格和某些特殊字元。
* <b>在套件</b>中建立圖表：你可以使用此組合框為新圖形建立 *新*&#x200B;套件，或將新圖形加入已載入檔案總管面板中的任何 *現有* 套件。\
  注意：若建立過程是使用方法<b>4</b>（見上文）啟動，該參數會預設&#x200B;**&#x200B;為程序啟動的現有套件。
* <b>範本詳情</b>：本節提供簡短文字說明範本的特性與目的
