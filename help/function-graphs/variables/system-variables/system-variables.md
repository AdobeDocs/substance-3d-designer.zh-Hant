---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/function-graphs/variables/system-variables.html"
breadcrumb-title: ''
description: 了解Substance 3D Designer功能圖中內建的系統變數，方便進階工作流程使用。
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Variables > Built-in variables
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 內建變數
user-guide-description: ''
user-guide-title: ''
source-git-commit: c002fea6f396f09ccb3218bd290db812d8367dc4
workflow-type: tm+mt
source-wordcount: '549'
ht-degree: 1%

---


# 內建變數

你可以在 Substance 函數圖[&#128279;](../../../function-graphs/function-graphs.md)中使用內建變數來存取特定值。它們總是以 `$` （美元）符號開頭。

有些變數只在特定情境中可用。

<b>所有節點</b>

系統變數

| 名稱 | 類型 | 目的 |
| --- | --- | --- |
| $size | Float2 | 回傳目前節點的像素大小。 若在輸出大小參數中使用[&#128279;](../../../compositing-graphs/output-size/output-size.md)，設定為 *Relative to...* [&#x200B; 繼承方法](../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)，則會回傳&#x200B;*繼承的值*。 |
| $sizelog 2 | Float2 | 如上所述，但回傳大小為2的冪次方值（例如：對於2048\*2048影像，回 `$sizelog2` 傳11）。 若在輸出大小參數中使用[&#128279;](../../../compositing-graphs/output-size/output-size.md)，設定為 *Relative to...* [&#x200B; 繼承方法](../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)，則會回傳&#x200B;*繼承的值*。 |
| $pixelratio | 整數 | 回傳一個整數值，對應於目前節點像素比（繼承或絕對）：0：拉伸 1：正方形 |
| $tiling | 整數 | 回傳一個整數值，對應目前節點鋪磚模式（繼承或絕對）：0：無鋪磚 1：水平鋪砌 2：垂直鋪砌 3：H 與 V 鋪砌 |
| $physicalsize | Float3 | 回傳[圖的](../../../compositing-graphs/graph-parameters/graph-parameters.md)<b>物理尺寸</b>屬性值。 |
| $uvtile | 整數2 | 使用 UDIM 工作流程時，這個變數會回傳 u 和 V 中目前 UDIM 的索引。 例如，（2， 0） 對應第1003塊，（7， 11） 對第1118塊，... |

<b>效果圖</b>

系統變數

| 名稱 | 類型 | 目的 |
| --- | --- | --- |
| $pos | Float2 | 回傳圖案的出生位置。 原點（0， 0）位於影像的左上角。 |
| $depth | 浮標 | 回傳 FX-Map[&#128279;](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md) 節點的八度（電平）數。這允許節點根據它所代表的四叉樹層級來調整行為。 |
| $depthpow 2 | 浮標 | 如上所述，但 會回傳 2 的乘法反元，升為八度（音量）的冪次方——即 1/（2^八度）。 這是一個輔助值，對某些常見計算非常有用。 |
| $number | 浮標 | 回傳抽圖的編號。 這可透過動態 [函數圖控制迭代](../../../function-graphs/fxmaps/using-functions-in-fxmaps/iterate-and-number-var/iterate-and-number-variable.md) 節點，在每個迭代步驟中修改其行為來存取。 注意，是 `$number` 從 0 開始計數，而不是從 1 開始。 使用一串迭代節點時，變 `$number` 數會回傳在使用函數參數之前最後一個迭代節點的次數。 如果你想從多個迭代節點取得迭代次數，應該透過 Set[&#128279;](../../../function-graphs/fxmaps/using-functions-in-fxmaps/using-the-set-sequence/using-the-set-sequence-nodes.md) 節點使用「自訂變數」。 |

<b>像素處理器</b>

系統變數

| 名稱 | 類型 | 目的 |
| --- | --- | --- |
| $pos | Float2 | 回傳被評估像素的位置。 |

<b>全球</b>

系統變數

| 名稱 | 類型 | 目的 |
| --- | --- | --- |
| $time | 浮標 | 此變數回傳自物質引擎啟動以來的時間（秒數）。 它可用於結果應隨時間變化的圖表中。  **注意：**  雖然目前無法在 Designer 中更改此數值，但整合 Substance Engine 的應用程式可利用此功能，例如 [Substance Player](https://helpx.adobe.com/substance-3d-player/home.html) 用於動畫或 [Substance 3D Painter](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/home) 用於 [動態筆觸](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/painting/dynamic-strokes/creating-custom-dynamic-strokes)。 |
| $normalformat | 整數 | 這是目前環境中使用的標準格式（例如 DirectX 或 OpenGL）。  **注意：**  此變數在 Designer 中無效，其他整合 Substance Engine 的應用程式可能會使用。 |
