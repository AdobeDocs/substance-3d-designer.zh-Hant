---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/function-graphs/fxmaps/the-iterate-node.html"
breadcrumb-title: ''
description: 利用 FXMaps 中的 Iterate 節點，在材質中創造重複圖案和程序變化。
helpx_creative_field: ""
helpx_description: Designer > Function graphs > FXMaps > The Iterate Node
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 迭代節點
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 0%

---


# 迭代節點

迭代節點讓你可以乘以象限節點的影像，基本上是一個「重複」節點。 一個象限節點深度為 1，通常會輸出 4 個象限。 迭代節點允許你無限次重複其輸出影像，每組重複會分別處理。

迭代節點除了「你想要多少重複？」這個參數外，沒有其他屬性。 結果是新影像預設會直接疊加並混合於象限節點產生的影像上。

迭代節點會重複接收到的輸入影像。 重複次數由其迭代性質定義：

使用迭代節點的關鍵在於，任何附加在每個重複影像上的動態函數也會被處理。 這表示每次重複都可以有自己獨特的調整。 你可以利用迭代節點的隨機種子屬性來修改這個功能。 你也可以在動態函式中存取 *$number* 系統變數，判斷目前正在渲染哪個重複，並相應地修改函式的結果。

舉例來說：如果你對象限節點的每個影像施加隨機旋轉，然後將該象限節點的輸出輸入輸入給迭代節點的主動輸入，每個重複的影像也會有自己的隨機旋轉。

象限節點所能提供的所有動態特徵同樣適用於迭代節點產生的重複影像。 就像節點在同一層級重複了象限節點，而不是新增另一個深度層級。

## 直通連接器

每個迭代節點底部有兩個連接器。 左側連接器為通通連接器。 接收到的影像會直接傳送到節點的輸出連接器，與重複的影像混合：

請注意，無論迭代參數的設定如何，直通影像都會保持不動。

![](the-iterate-node.resources/iterate.jpg)
