---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/working-with-path-and-spline-tools.html"
breadcrumb-title: ''
description: 學習如何運用路徑與樣條工具，在圖表中創造程序式圖案和有機形狀。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Working with Path  Spline tools
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 使用路徑樣條工具
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '1544'
ht-degree: 0%

---


# 使用路徑與樣條鍵工具

路徑與樣條工具組是一組節點，讓你可以撰寫和編輯與解析度無關的形狀與曲線，這些圖形用於繪製、映射及散射影像。

## 概觀

### 什麼是路徑和樣條？

<b>路徑是一連串點連接</b> 成直線。

<b>樣條</b> 曲線是由控制點及其切線所塑造的平滑曲線。\
每個點也控制樣條的高度與厚度屬性，這些屬性用於驅動影像的映射、變形與散射。

每個都能建造封閉或開放形狀。

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

### 節點輸出

節點輸出的 <b>影像包含編碼資料</b> ，代表路徑與樣條曲線。

例如，右側的圖片代表 Paths 多邊形[&#128279;](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-polygon/paths-polygon.md)節點的影像輸出。

</td>
<td width="33.33%" style="border: 0;" valign="top">

![路徑多邊形輸出](../../../../../assets/PathsPolygon_Data.jpg "路徑多邊形輸出")

</td>
</tr>
</table>

因此，它們產生的影像無法直接作為圖形元素使用。 它們需要由工具集中的其他節點處理，這些節點能將它們轉換成圖形結果，然後再與其他可用於 Substance 圖表的其他節點一起使用。

當你處理路徑和樣條曲線時，可以使用專用 [的預覽路徑](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md) 節點預覽這些映射在影像中的物件，並用專用 <b>的預覽</b> 輸出來預覽樣條曲線。

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

### 2D 視圖互動

工具集中有相當多節點可直接使用控制裝置在 [2D 視圖](../../../../../interface/2d-view/2d-view.md) 中進行編輯。 這些裝置包括位置裝置與轉換矩陣。

例如，樣條產生節點 [如樣條（三次曲線）](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-cubic/spline-cubic.md) 或 [樣條曲線（多元二次曲線）允許](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-poly-quadratic/spline-poly-quadratic.md) 你移動樣條曲線的控制點。 對於路徑 [，選取路徑上的四邊變換](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/quad-transform-on-path/quad-transform-on-path.md) 也有類似的控制。

</td>
<td width="33.33%" style="border: 0;" valign="top">

![二維視圖](../../../../../assets/SplineCubic-Demo.gif "中的樣條三次曲線 二維視圖中的樣條三次曲線")

</td>
</tr>
</table>

### 性能

路徑與樣條工具需要大量計算，因此你應該注意幾個設定，以確保使用工具組時能達到最佳效能與反應性：

1. 工具組大量運用 <b>Substance Engine</b> 功能，在 GPU 上運行速度大幅提升。 因此，請使用系統的 GPU 版本引擎： <b>Direct3D</b> （Windows）或 <b>OpenGL</b> （macOS）。\
   你可以按 F9</b> 鍵切換引擎<b>，或是進入<b>主選單列的 Tools > Switch 引擎</b>。
1. 接著，我們強烈建議<b>在偏好設定[&#128279;](../../../../../interface/preferences-window/preferences-window.md)的圖表</b>區關閉上下文編輯</b><b>（前往<b>主選單列的>編輯偏好設定......</b>可進入此視窗）。\
   上下文編輯允許你在主機圖的上下文中開啟實例節點，這確實非常方便，但副作用是工具組影像快取所需的計算量呈指數成長。

只要將這兩個設定改成建議狀態，你應該會注意到顯著的效能提升。

![圖書館](../../../../../assets/PathsTools.jpg "中的路徑工具圖書館中的路徑工具")

## 路徑工具

### 產生路徑

[路徑多邊形](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-polygon/paths-polygon.md)會產生一條形狀為指定半徑與邊數的多邊形路徑。

另外，也可以透過「遮罩到路徑[&#128279;](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md)」節點從灰階影像中擷取路徑。\
目前這是產生複雜形狀的唯一方法，並且讓你能利用整個 Substance 圖形節點[&#128279;](../../../../../compositing-graphs/nodes-reference-for-com/nodes-reference-for-substance-compositing-graphs.md)庫，產生最終會轉換成路徑的形狀。

![路徑產生節點路徑](../../../../../assets/Paths_Generation.jpg "產生節點"){width="600px"}

### 編輯路徑

[Path 2D 變換](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/path-2d-transform/path-2d-transform.md)、 [Paths Warp](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-warp/paths-warp.md) 和 [Quad Transform 在 Path](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/quad-transform-on-path/quad-transform-on-path.md) 上可以編輯路徑的形狀。

你也可以透過「 [路徑選擇](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-select/paths-select.md) 」節點，依索引或長度選擇路徑來移除不需要的路徑。

在路徑頂點處理器[&#128279;](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-vertex-processor/paths-vertex-processor.md)節點的協助下，可以對路徑的每一點進行更複雜的處理。[有更簡單的版本](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-vertex-processor-1/paths-vertex-processor-simple.md)用於較輕的調整。

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

### 預覽路徑節點

預視路徑節點的結果則使用專用 [的預覽路徑](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md) 節點來完成。\
此節點沒有輸出。 雙擊節點上的 LMB 即可在 2D 視圖[&#128279;](../../../../../interface/2d-view/2d-view.md)中顯示預覽畫面。

獨立路徑在預覽中會有獨特的顏色，方便區分每條路徑。

</td>
<td width="33.33%" style="border: 0;" valign="top">

![預覽路徑節點](../../../../../assets/PreviewPaths_Node.jpg "預覽路徑節點")

</td>
</tr>
</table>

### 通往樣條的路徑

你可以利用所有專門針對帶有路徑的樣條曲線工具組，透過 Paths to Spline[&#128279;](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md) 節點將路徑轉換成樣條曲線。

請記住樣條曲線是曲線，因此無法保留路徑的銳利度。 在將路徑轉換成樣條曲線時，可以預期形狀會有些平滑。

利用樣條工具組穿越路徑的一個非常有用組合如下：

<b>遮罩 > 遮罩轉為路徑 > 路徑轉為樣條</b>

![路徑到樣條](../../../../../assets/Spline_PathToSpline.jpg "曲線路徑 路徑到 樣條曲線")

### 路徑格式規範

預覽路徑節點是必要的，因為路徑節點會輸出以彩色影像編碼的路徑資料。\
此編碼遵循路徑格式規範[&#128279;](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-format-spe/paths-format-specifications.md)頁面所述的規範。

你可以利用這個規格來製作屬於自己的節點，並充分利用 [Paths 頂點處理器](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-vertex-processor/paths-vertex-processor.md) 節點。

![函式庫中的樣條鍵工具函](../../../../../assets/SplineTools.jpg "式庫中的樣條鍵工具")

## 花鍵工具

### 樣條曲線的產生

樣條可透過樣條圓[&#128279;](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-circle/spline-circle.md)、[樣條（三次曲線）](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-cubic/spline-cubic.md)或[樣條曲線（多二次曲線）](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-poly-quadratic/spline-poly-quadratic.md)等節點生成。這些節點讓你能根據節點的不同控制方式，繪製任意軌跡的樣條曲線。

或者，也 [可以透過 Paths to Spline](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md) 節點從路徑中擷取樣條曲線。\
請記住樣條曲線是曲線，因此無法保留路徑的銳利度。 在將路徑轉換成樣條曲線時，可以預期形狀會有些平滑。

利用樣條工具組穿越路徑的一個非常有用組合如下：

<b>遮罩 > 遮罩轉為路徑 > 路徑轉為樣條</b>

樣條也能幫助你產生更多樣條曲線。 例如， [樣條橋（2個樣條）](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-bridge-2-splines/spline-bridge-2-splines.md) 和 [樣條橋（列表）會](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-bridge-list/spline-bridge-list.md) 依序遍歷一串樣條曲線。

### 編輯樣條曲線

[樣條 2D 變形](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-2d-transform/spline-2d-transform.md) 和 [樣條曲線扭曲](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-warp/spline-warp.md) 讓你可以編輯樣條曲線的形狀。

你也可以透過 [依索引選擇路徑及修剪樣條，使用樣條選擇](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-select/spline-select.md) 節點來移除不需要的樣條線。

除了軌跡外，樣條的高度與厚度特性還可透過 [樣條樣本高度](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-sample-height/spline-sample-height.md) 與 [樣條厚度](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-sample-thickness/spline-sample-thickness.md)後續調整。

最後，透過 [樣條合併清單](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-merge-list/spline-merge-list.md) 節點，可以將獨立樣條線合併成單一樣條線。

### 附加樣條

當你撰寫和編輯樣條曲線時，可能需要將多個樣條線合併，以便調整或同時使用。

重要的是要記住樣條線是以有序清單</b>的形式儲存和處理<b>的。

組合樣條線是透過 [Spline Append](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-append/spline-append.md) 節點完成的。 附加是指在有序實體的末尾添加某個東西。 事實上，節點會將兩個樣條線列表結合，方法是在第一組的末尾加入第二個樣條線集合。

因此，考慮你將樣條線相連的順序非常重要。

這會影響需要將樣條線合併的節點，例如[&#128279;](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-bridge-mapper-gra/spline-bridge-mapper-grayscale.md)樣條橋（列表）、[&#128279;](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-bridge-list/spline-bridge-list.md)樣條橋映射器和[樣條合併清單](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-merge-list/spline-merge-list.md)。

![附加帶有連結建立模式](../../../../../assets/LinkCreationMode_Splines.gif "的樣條 附帶連結建立模式的樣條")

### 樣鍵輸入與輸出

樣條線透過一組連接器從一個節點傳遞到另一個節點：

* <b>樣條座標&#x200B;</b>*顏色*&#x200B;輸入樣條點的座標編碼在彩色影像的 RGBA 通道中。
* <b>樣條線資料&#x200B;</b>*顏色*&#x200B;在彩色影像的 RGBA 通道中編碼的輸入樣條的額外資料。
* <b>樣條量整&#x200B;</b>*數*&#x200B;輸入樣條的數量。

來源節點的每個輸出連接器都應連接到目標節點中名稱相符的輸入連接器。

為了讓這些連接更快，你可以使用 <b>Material</b> 或 <b>Compact Material。</b> [連結建立模式](../../../../../interface/the-graph-view/link-creation-modes/link-creation-modes.md)。 這樣可以讓你一次連接三個花鍵連接器。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### 預覽輸出

大多數節點都會提供 <b>預覽</b> 輸出，讓你能在影像中渲染樣條，讓你了解它們的軌跡和屬性。

這個預覽可以在節點參數中調整，使用預覽</b>群組中的<b>參數。

</td>
<td style="border: 0;" valign="top">

![樣條線節點](../../../../../assets/Spline_PreviewOutput.jpg "上的預覽輸出樣條線節點上的預覽輸出")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

### 以段形式渲染

樣條曲線本身沒有固有解析度，意味著它們可以無限放大或縮小，唯一準確表示的限制是儲存資料的精度。

要將樣條曲線繪製為像素，工具組會將其簡化為沿著樣條軌跡繪製的線條或段。

</td>
<td width="33.33%" style="border: 0;" valign="top">

![樣條以段](../../../../../assets/Spline_Segments.jpg "形式渲染 樣條曲線以段形式渲染")

</td>
</tr>
</table>

這表示你可能需要注意畫樣條曲線所需的片段數，因為這個數量可能太低無法畫出平滑曲線，或是太高而浪費於目標解析度。

在影像中繪製樣條的節點有一個 <b>Segments Amount</b> 參數，可以讓你控制該段數量。 較高的數值會讓曲線更平滑，但性能會因此下降。

### 從樣條曲線建立影像

當你完成撰寫和編輯樣條曲線後，可以用來產生能利用其他 Substance 圖形節點的影像。

使用樣條曲線生成圖形主要有三種方式：

* 使用樣條[&#128279;](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-render/spline-render.md) [渲染或樣](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-fill/spline-fill.md)條填充節點，利用形狀與屬性渲染樣條曲線;
* 沿樣條曲線繪圖影像，搭配像樣條映射[&#128279;](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-mapper-grayscale/spline-mapper-grayscale.md)器、[樣條橋映射器](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-bridge-mapper-gra/spline-bridge-mapper-grayscale.md)及[樣條流映射器](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-flow-mapper/spline-flow-mapper.md)等映射節點;
* 沿著樣條線進行散佈圖案，使用 [散佈在樣條](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/scatter-spline-grayscale/scatter-on-spline-grayscale.md) 線上的散佈節點。
