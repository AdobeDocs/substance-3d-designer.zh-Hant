---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/function-graphs/the-function-graph.html"
breadcrumb-title: ''
description: 學習 Designer 中的 Substance 函數圖，用於建立自訂函數和可重複使用的節點網路。
helpx_creative_field: ""
helpx_description: Designer > Substance function graphs > The Substance function graph
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 物質函數圖
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 0%

---


# 與物質圖的相似之處

乍看之下，Substance 函數圖和 Substance 圖非常相似，工作流程也幾乎相同。

![實體函數圖](../../assets/image2015-12-18-11-29-28.png "實質函數圖")

## 導航方式類似

在 Substance 函式圖中，你可以像在 Substance 圖中一樣建立和組織節點。

你也可以用同樣方式存取這些節點：

* 來自圖書館
* 按空白鍵或 Tab 鍵
* 透過右鍵點擊並使用新增節點選單

### 工作流程也類似

就像 Substance 圖一樣，你會透過串聯一串節點來建立你的函式，每個節點都使用前一個節點產生的結果來建立。

輸出會定義參數的值或像素處理器節點的輸出。

## 與物質圖的差異

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

### 節點

Substance 函數圖中可用的節點與你在 Substance 圖中遇到的完全不同。

</td>
<td width="25.00%" style="border: 0;" valign="top">

![Substance 函數圖節點列表](../../assets/image2015-12-18-13-46-55.png "Substance 函數圖節點列表")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### 產出

與 Substance 圖相反，函數只能有一個輸出。

另一點是，沒有特定的輸出節點是用來插入最終結果的。 相反地，你可以直接將產生你期望結果的節點標記為輸出：

</td>
<td style="border: 0;" valign="top">

![物質函數圖的輸出節點](../../assets/image2015-12-18-13-49-43.png "實質函數圖的輸出節點")

</td>
</tr>
</table>

#### 如何定義輸出節點？

要定義輸出，只需右鍵點擊產生預期輸出的節點，然後點選 *「設定為輸出」節點：*

![定義輸出節點](../../assets/setoutputnode.gif "定義輸出節點")

>[!WARNING]
>
> <b>請再次確認產生的結果類型</b>
> 
> 如果你注意到 *「Set as Output Node* 」是灰色的，代表節點產生的值與參數或像素處理器預期的值不同。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

至於 Substance 圖，你可以匯入其他圖中產生的函數。 你可以右鍵點擊參考圖，並選擇「開啟參考」來開啟它：

</td>
<td style="border: 0;" valign="top">

![開放參照的實質函數圖](../../assets/image2017-6-27-10-44-55.png "開放參照的實質函數圖")

</td>
</tr>
</table>

如果你有一個包含多個函式的 SBS，你可以直接拖放到 Substance 函數圖中，選擇你想匯入的函式列表：

![從套件](../../assets/sbsdrag.gif "中移除物質函數圖 從套件中移除物質函數圖")
