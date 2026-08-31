---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/function-graphs/fxmaps/the-quadrant-node.html"
breadcrumb-title: ''
description: 使用 FXMaps 中的象限節點，將材質分成四個區塊，以創造拼貼圖案和變化。
helpx_creative_field: ""
helpx_description: Designer > Function graphs > FXMaps > The Quadrant Node
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 象限交點
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '778'
ht-degree: 1%

---


# 象限交點

許多 FX-Maps 完全由象限節點鏈組成。 象限節點是 FX-Map 群組中最強大且靈活的節點，因此了解這個節點的運作方式非常值得。

象限節點最重要的一點是，它們是唯一能增加 FX-Map 圖深度或 *八度*&#x200B;的節點。 每個象限節點都會加到底層的四叉樹圖;其他節點則不會加總。

象限節點包含多個參數：

## 色彩 / 亮度

當節點將影像加入 FX-Map 時，這些設定定義了通道如何與鏈中其他影像混合。 *色彩/亮度參數會*&#x200B;套用到這個特定節點渲染的任何影像。

### 分支偏移量

改變節點的影像。 偏移量會套用到圖中後續節點渲染的所有其他影像。 分支偏移量將平移應用於當前象限節點及其下方所有節點，該節點位於圖的同一分支中。

此參數可用動態函數控制。

### 圖樣

定義此節點要加入FX-Map的影像（如有）。

象限節點支援一長串模式，稍後將在此主題中詳細說明。

>[!WARNING]
>
> 這個參數無法由 sbsar 檔案中的動態函式控制。

### 圖案偏移

會使節點的影像偏移指定數量，但不影響後續節點。 此參數可用動態函數控制。

### 圖樣大小

定義要加入FX-Map的影像大小（如適用）。 此參數可用動態函數控制。

### 圖樣旋轉

定義影像的旋轉（如適用）需加入 FX-Map。 此參數可用動態函數控制。

### 圖樣變量

有些圖案有變體。 這個設定讓你可以選擇要用哪個變體。 此參數可用動態函數控制。

### 混合模式

指定將此節點影像（如適用）與 FX-Map 影像混合時所採用的混合流程。 此參數可用動態函數控制。

### 隨機種子

隨機數產生器的種子。

生成器以這個種子作為起點，產生一串看似隨機的數字序列。 這種方法的優點在於，與現實世界不同，你可以確保每次產生的隨機數字序列完全相同，產生可預測、可重複但看起來隨機的結果。

此參數可用動態函數控制。

### 繼承隨機

若設為「是」，則隨機數產生器的種子會繼承自圖中前一個節點（即四叉樹中該節點上方的節點）。 如果這是第一個節點，則會從包含的 [Substance 圖](../../../compositing-graphs/substance-compositing-graphs.md)中隨機取種子。

## 模式

每個象限節點可選擇性地將影像加入最終效果圖。

預設情況下，選擇無圖案，因此不會渲染任何影像。 象限節點僅將 FX-Map 影像細分，將其分成四個，供鏈中下一個節點使用。

下一個選項輸入 *影像*，是使用FX-Map節點提供的影像。 FX-Map 節點接受彩色或灰階影像，作為背景或取代內建圖案。 請注意，象限節點只能在灰階 FX-Map 中渲染灰階輸入影像，反之，它只能在彩色 FX-Map 中渲染彩色輸入影像。 如果你想混合顏色類型，你需要先在圖表中轉換輸入。

最後，你可以從內建圖案中選擇：方形、圓盤、拋物面、鐘形、高斯分布、荊棘、金字塔、磚塊、漸變、波浪、半鐘形、有脊形鈴、新月形和膠囊。

補充說明：你可以在這個參數中建立動態函數，但只能在 Substance 3D Designer 中運作。 要透過動態函數存取影像輸入，你必須使用從 256（影像條目 1）到更高值（影像條目 2 為 257 等）的值。

### 模式類型。

圖案都是灰階的。 有些可以用圖案變化&#x200B;*參數稍微修改*。

許多內建圖案都有某種形式的放射狀漸層填充或類似功能。 這使得它們在多種噪音和模式中非常有用。 其他圖案，如磚、圓盤和方形，則是簡單且平面的形狀。

模式變化參數用來調整模式的一個定義特徵。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](the-quadrant-node.resources/the-quadrant-node-01.png){width="80px"}

</td>
<td style="border: 0;" valign="top">

![](the-quadrant-node.resources/the-quadrant-node-02.jpg)

</td>
</tr>
</table>
