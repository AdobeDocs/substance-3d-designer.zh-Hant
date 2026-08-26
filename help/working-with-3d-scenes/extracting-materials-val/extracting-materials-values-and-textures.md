---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/working-with-3d-scenes/extracting-materials-values-and-textures.html"
breadcrumb-title: ''
description: 從 3D 場景中擷取材質屬性，用於 Substance 圖，用於材質製作工作流程。
helpx_creative_field: ""
helpx_description: Designer > Working with 3D scenes > Extracting materials values and textures
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 提取材質值與紋理
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '861'
ht-degree: 0%

---


# 提取材質值與紋理

材料的性質可以被提取出來，用於物質圖。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## 來自貼圖的新圖表

</td>
<td style="border: 0;" valign="top">

### 萃取質地

</td>
<td style="border: 0;" valign="top">

### 萃取值

</td>
</tr>
</table>

## 來自貼圖的新圖表

「從材質輸入建立圖譜」動作會建立一個新的 Substance 圖，包含材質所使用的所有材質材質

使用此動作時會發生幾件事：

* 在選定位置建立一個以材料命名的物質圖。
* 每個材質使用的材質都會建立一個 [點陣資源](../../resources/bitmap-resource/bitmap-resource.md) ，並放置在以材質命名的資料夾中，位於「Resources」資料夾下方。
* 在圖中， [每個點陣資源都會建立點陣](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md) 節點，並自動連接到 [在材質屬性設定後，使用貼圖設定的輸出](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) 節點。
* 若同一紋理的每個通道用於驅動不同的材質屬性（稱為 [通道打包](../../glossary/glossary.md)）， [則會自動加入灰階轉換](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/grayscale-conversion/grayscale-conversion.md) 節點以選擇適當的通道。
* 圖表會自動連接到材質，外觀在你編輯圖表之前不會改變。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![從材質輸入建立圖形 - 在「3D View」視窗](../../assets/createGraphFromTexturesActionViewport.png "中操作 從材質輸入建立圖形 - 在「3D View」視窗中操作"){zoomable="yes"}

*3D 視角中的動作*

</td>
<td style="border: 0;" valign="top">

![從材質輸入建立圖表 - 在「材質」選單](../../assets/createGraphFromTexturesActionMaterials.png "中的動作 從材質輸入建立圖表 - 在「材質」選單中的動作"){zoomable="yes"}

*材料選單中的動作*

</td>
<td style="border: 0;" valign="top">

![從材質輸入建立圖表 - 在「屬性」底座](../../assets/createGraphFromTexturesActionProps.png "中的動作 從材質輸入建立圖表 - 在「屬性」底座中的動作"){zoomable="yes"}

*《物業碼頭》中的行動*

</td>
</tr>
</table>

![從材質材質建立圖的結果 從材質材質](../../assets/createGraphFromTexturesResult.png "材質建立圖的結果"){zoomable="yes"}

*從材質紋理建立圖的結果*

+++示範
![從貼圖輸入建立圖形 - 示範](../../assets/createGraphFromTextures.gif "從貼圖輸入建立圖形 - 示範"){zoomable="yes"}



+++

>[!TIP]
>
> 你可以在 3D 視圖視窗中快速且直接地存取動作，方法是將游標放在物件上，然後按 <b>Shift+LMB</b> 選擇物件。 然後點擊 RMB 進入設置該動作的情境選單。

>[!NOTE]
>
> 對於使用 *內嵌紋理* 的格式（例如：USDZ），紋理需要擷取並複製到磁碟上。 這會產生額外步驟來選擇要擷取貼圖的位置。

## 萃取質地

「將貼圖擷取到圖形」動作會在現有圖中為材質使用的貼圖建立新的點陣節點。

使用此動作時會發生幾件事：

* [為材質所用的材質建立一個點陣資源](../../resources/bitmap-resource/bitmap-resource.md)，並放置在以材質命名的資料夾中，位於「Resources」資料夾下方。
* 在所選的圖中，會為該點陣資源建立一個 [點陣](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md) 節點，並自動連接到 [一個在材質屬性後設定的輸出](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) 節點，使用該材質的紋理。

如果圖中已有&#x200B;*為材質屬性*&#x200B;配置的輸出，則&#x200B;*不會建立*&#x200B;節點，僅執行點陣圖資源建立。

例如：將「基色」屬性的貼圖擷取到已設定為「基色」的輸出節點的圖中，圖中不會新增任何節點。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![從 Properties Dock 中擷取貼圖 - 在 Properties Dock](../../assets/extractTextureAction.png "中執行動作 將 擷取到圖表 - 在 Properties Dock 中執行"){zoomable="yes"}

物業碼頭中關於物質財產的訴訟

</td>
<td style="border: 0;" valign="top">

![將貼圖擷取到圖表 - 「選擇目的地圖表」對話框](../../assets/extractTextureSelectGraph.png "將貼圖擷取到圖表 - 「選擇目的地圖表」對話框"){zoomable="yes"}

「選擇目的地圖」對話框

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

![紋理萃取](../../assets/extractTextureResult.png "的結果 紋理萃取的結果"){zoomable="yes"}

紋理提取的結果

+++示範
![從貼圖擷取貼圖 - 示範](../../assets/extractTextureToGraph.gif "擷取貼圖至圖 - 示範"){zoomable="yes"}



+++

「將材質擷取為資源」動作只會為材質所用材質建立一個點陣圖資源，並將其放入以材質命名的資料夾中，位於「資源」資料夾下方。

>[!NOTE]
>
> 對於使用 *嵌入紋理* 的格式（例如：USDZ），紋理需要先解壓並複製到磁碟上。 這會產生一個額外的步驟來選擇貼圖應該被提取到的位置。

## 萃取值

「將值抽取到圖譜」動作會在現有圖中為某物質屬性值建立新的 [值處理](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/value-processor/value-processor.md) 節點。

使用此動作時會發生幾件事：

* 在所選圖中， [會為該屬性值建立一個價值處理器](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/value-processor/value-processor.md) 節點，並自動連接到 [該材料屬性後設定的輸出](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) 節點。
* 在 Value 處理器節點的 [Substance 函數圖](../../function-graphs/function-graphs.md)中， [會建立一個與值類型相符的常數節點](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/constant-nodes/constant-nodes.md) ，並設定為擷取後的值作為圖的輸出。

如果圖中已有&#x200B;*為材料屬性*&#x200B;配置的輸出，則&#x200B;*不會建立*&#x200B;節點。

例如：對已設定為「各向異性層級」的輸出節點的圖提取「各向異性層級」屬性的值，該圖中將不會產生任何節點。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![擷取到圖的值 - 在屬性掛鉤](../../assets/extractValueAction.png "中的動作 從圖中提取到圖的值 - 在屬性停靠中的動作"){zoomable="yes"}

物業碼頭中關於物質財產的訴訟

</td>
<td style="border: 0;" valign="top">

![將值抽取到圖 - 「選擇目標圖」對話框](../../assets/extractValueSelectGraph.png "擷取到圖的值 - 「選擇目標圖」對話框"){zoomable="yes"}

「選擇目的地圖」對話框

</td>
<td style="border: 0;" valign="top">

![擷取圖中的值 - 值處理器節點函式](../../assets/extractValueResult2.png "中的常數節點 擷取圖中的值 - 值處理器節點函式中的常數節點"){zoomable="yes"}

Value 處理器節點函式中的常數節點

</td>
</tr>
</table>

![價值萃取](../../assets/extractValueResult.png "的結果 價值萃取的結果"){zoomable="yes"}

價值提取的結果

+++示範
![擷取圖的值 - 示範](../../assets/extractValueToGraph.gif "擷取圖的值 - 示範"){zoomable="yes"}



+++
