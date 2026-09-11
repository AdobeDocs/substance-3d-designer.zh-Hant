---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/variables/create-a-variable.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Designer 函數圖中建立可重複使用的數值與參數的自訂變數。
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Variables > Create a variable
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 建立一個變數
user-guide-description: ''
user-guide-title: ''
source-git-commit: 81c39001686736d41614fd59247d53e6d8438def
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 0%

---


# 建立一個變數

在 Substance 3D Designer 中建立變數有多種方式：

* 使用輸入參數
* 使用 Set 節點。

## 使用輸入參數

當你建立輸入參數時，會建立一個變數並與之關聯。 你可以在圖的任何函數中重複使用這個變數。

因此，一個暴露的參數可能影響圖的多個部分。

## 使用 Set 節點

集合節點是指僅在函數圖中可用的節點：

它允許使用者建立自訂變數：

* 名稱會在參數中宣告。
* 這個值是由輸入定義的。

### 如何使用 *Set* 節點

Set 節點的使用有點特殊：

當你宣告它時，它只會在圖中顯示，這在預設情況下其實沒什麼用（畢竟你已經可以用連結輸出它的值了）。

因此，你必須宣告這個新變數，放在圖之外。

要做到這點，你必須使用序列節點並執行以下步驟：

* 將實際輸出節點連結到序列節點的「最後」輸入
* 將 Set 節點連結到序列節點的「In」輸入。
* 將序列設為輸出節點

完成後，該變數就會出現在同一節點的另一個函式圖中。

>[!WARNING]
>
> 當節點被物質引擎處理時，其參數（以及可控制它們的函式）會從上到下被讀取。 因此，集合節點只能由位於節點參數堆疊下方的參數存取。

>[!NOTE]
>
> 如果你有多個變數要建立，只要重複 *Set* 和 *Sequence* 節點的建立操作，並將最後一個序列節點設為輸出節點：
> 
> ![](create-a-variable.resources/image2015-12-18-18-43-8.png)
