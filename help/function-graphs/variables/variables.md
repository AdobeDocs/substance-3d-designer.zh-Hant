---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/variables.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Designer 函數圖中使用變數，以有效儲存和重複使用數值。
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Variables
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 變數
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 0%

---


# 變數

>[!NOTE]
>
> 關於變數節點的建立與使用資訊，請參閱 *[變數節點章節](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/get-nodes/get-nodes.md)*。

## 定義

如果你對程式設計了解不多，可能對變數這個概念很熟悉。

如果沒有，這裡有一個簡單的定義：

>[!NOTE]
>
> 變數，只是帶有特定名稱的「容器」，其中包含一個值。
> 
> 你可以透過呼叫變數名稱來使用變數中包含的值。

## 變數類型

在 Substance 3D Designer 中，你有兩組變數：數值和布林值。

## 數值變數

數值變數基本上就是數字。 但我們明確區分兩種數字：

* 整數 ： 0 |1 |-1 |203568，等等......
* 浮點數：0.23 |1.0 |-0.3546 |等等......

>[!WARNING]
>
> Designer 明確區分整數和浮點數：預設情況下你不能同時操作它們。
> 
> 幸運的是，你可以使用 *To Integer* 或 To Float 節點來執行型別轉換。

### 同一變數中的多個數值

根據你的需求，你可以在同一變數內累積最多4個數值。

同樣地，所有值都必須來自同一類型。

為此，你可以從以下數值中選擇：

![](../../assets/image2015-12-18-14-10-36.png)

## 布林值

布林值是純二進位值，意思是它的值只能是 *真* 或 *假* （你也可以說 0 或 1）。
