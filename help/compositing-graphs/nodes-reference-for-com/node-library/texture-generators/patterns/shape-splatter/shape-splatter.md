---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape-splatter.html"
breadcrumb-title: ''
description: 使用 Shape Splatter 節點將形狀散布到材質中，創造程序化圖案與細節。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Shape Splatter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 形狀濺射
user-guide-description: ''
user-guide-title: ''
source-git-commit: 79916cdb133abb1a43d11012c9d23c3c6d27b079
workflow-type: tm+mt
source-wordcount: '960'
ht-degree: 7%

---


# 形狀濺射

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/shape-splatter.png){width="128px"}

<b>收錄於：</b> 紋理產生器>圖案

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

這是一個非常複雜的節點，設計用來搭配搭配的節點 [Shape Splatter Blend](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-blend/shape-splatter-blend.md)、 [Shape Splatter to Mask](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-to-mask/shape-splatter-to-mask.md) 以及 [Shape Splatter Data Extract](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-data-ext/shape-splatter-data-extract.md)。 用來以類似 Tile Sampler 或 Generator 的方式[&#128279;](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md)潑灑形狀，但採用動態且非破壞性的過程，透過類似 [Flood Fill 的多層系統控制每一步。](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md) [&#128279;](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md) Flood Fill 是從外部來源取得基礎輸入地圖，而 Shape Splatter 則能在單一步驟內產生地圖及相關資料，作為 Flood Fill[&#128279;](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md) 的進階版本。

它的主要目的是允許將形狀放置在高度圖上並由高度圖驅動，然後從 Splatter Data 生成各種地圖。 例如，在地形上放置石頭、樹枝和樹葉，並由各種地圖來定向和驅動。 不同貼圖可用於高度、法線、底色、粗糙度及其他任何通道，且皆基於相同的共用濺射資料。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>背景高度</b> <i>灰階輸入</i> | 背景高度用來放置磚塊並驅動各種效果。 |
| <b>模式1-8</b> <i>灰階輸入</i> | 可選圖案 |
| <b>模式分布</b> <i>灰階輸入</i> | 灰階映射至 |
| <b>形狀尺度</b> <i>灰階輸入</i> | 用灰階地圖來驅動圖塊縮放。 |
| <b>形狀旋轉</b> <i>灰階輸入</i> | 灰階地圖來驅動地磚旋轉。 |
| <b>身高偏移</b> <i>灰階輸入</i> | 用來作為圖塊高度偏移的灰階貼圖。 |
| <b>身高比例</b> <i>灰階輸入</i> | 用來作為圖塊高度偏移的灰階貼圖。 |
| <b>面具隨機</b> <i>灰階輸入</i> | 遮罩槽用於遮蔽節點的效果。 |
| <b>向量地圖</b> <i>色彩輸入</i> | 色彩向量貼圖來驅動圖塊的位置和旋轉。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>X 金額</b> <i>1 - 64</i> | 該模式重複次數為數。 |
| <b>Y 金額</b> <i>1 - 64</i> | 該模式的Y字重複次數。 |
| <b>模式</b> |  |
| <b>模式輸入編號</b> <i>1 - 8</i> | 設定不同圖案的數量。 解鎖新的圖案輸入欄位。 |
| <b>模式分配模式</b> <i>隨機索引、模式索引、行索引、欄位索引</i> | 設定如何決定要用哪種模式。 隨機或依模式、線條或欄目。 |
| <b>模式分布地圖乘數</b> <i>0.0 - 1.0</i> | 設定可選分布圖的影響來放置圖案。 |
| <b>模式旋轉</b> <i>0, 90, 180, 270</i> | 預設，模式旋轉90度。 |
| <b>模式旋轉隨機</b> <i>0.0 - 1.0</i> | 設定隨機90度步進旋轉的頻率來製作模式。 |
| <b>規模</b> |  |
| <b>規模</b> <i>0.0 - 5.0</i> | 為每塊磚設均勻比例。 |
| <b>量表隨機</b> <i>0.0 - 1.0</i> | 讓每個格子的比例均勻隨機化。 |
| <b>比例無重疊</b> <i>0.0 - 1.0</i> | 隨機比例均勻，但只往下縮，以避免重疊的格子。 不應與前兩個參數同時使用。 |
| <b>比例地圖倍數</b> <i>0.0 - 1.0</i> | 設定比例尺地圖的影響。 |
| <b>規模</b> <i>0.0 - 1.0</i> | 允許非均勻的方塊縮放。 |
| <b>從Bg Slope的尺寸比</b> <i>0.0 - 1.0</i> | 使用背景地圖斜率（計算出法線）來調整非均勻縮放的圖塊。 模擬透視扭曲。 |
| <b>尺寸與X/Y量比</b> <i>0.0 - 1.0</i> | 非均勻縮放以補償 X 與 Y 比例的不同。 |
| <b>職位</b> |  |
| <b>隨機位置</b> <i>0.0 - 2.0</i> | 每個格子隨機偏移操作。 |
| <b>隨機分布</b> <i>高斯分布，均勻</i> | 設定計算值用於前一個參數。 差異不大，數值越高越明顯。 高斯分布通常會讓分布更均勻。 |
| <b>向量映射乘法</b> <i>0.0 - 1.0</i> | 向量輸入映射對偏移量的影響。 |
| <b>水平偏移</b> <i>-2.0 - 2.0</i> | 全域水平偏移。 |
| <b>偏移垂直</b> <i>-2.0 - 2.0</i> | 全域垂直偏移。 |
| <b>界外選項</b> <i>比例形狀，限制位置</i> | 當方塊出現為界外時執行的動作。 |
| <b>旋轉</b> |  |
| <b>旋轉</b> <i>0.0 - 1.0</i> | 全域旋轉所有格子。 |
| <b>旋轉隨機</b> <i>0.0 - 1.0</i> | 每格隨機旋轉。 |
| <b>從Bg斜坡轉動</b> <i>0.0 - 1.0</i> | 使用背景地圖斜率（計算出的法線）來旋轉圖塊。 可以用來讓形狀在斜坡上朝上或朝下。 |
| <b>旋轉映射乘數</b> <i>0.0 - 1.0</i> | 混合旋轉對每個圖塊旋轉的效果。 |
| <b>向量映射乘法</b> <i>0.0 - 1.0</i> | 混合旋轉對每個圖塊旋轉的效果。 |
| <b>高度</b> |  |
| <b>高度刻度自動調整</b> <i>錯誤/真實</i> | 自動調整相對於背景的高度範圍，而不是定義一個絕對範圍。 可以讓控制權多或少。 |
| <b>身高偏移</b> <i>-1.0 - 1.0</i> | 修改器可以均勻地偏移/移動所有瓦片，沿著高度範圍移動。 |
| <b>高度偏移隨機</b> <i>0.0 - 1.0</i> | 隨機根據每格改變高度偏移。 |
| <b>高度偏移地圖多重機</b> <i>0.0 - 1.0</i> | 修改器用來設定偏移貼圖的影響。 |
| <b>身高比例</b> <i>0.0 - 1.0</i> | 修改器可以均勻地在高度範圍內縮放/展開所有格子。 相對於偏移，這會讓數值更遠，就像對比度一樣。 |
| <b>身高隨機</b> <i>0.0 - 1.0</i> | 高度比例會隨機根據每格改變。 |
| <b>高度比例地圖乘數</b> <i>0.0 - 1.0</i> | 修改器用來設定比例地圖的影響。 |
| <b>符合背景</b> <i>0.0 - 1.0</i> | 影響磚塊與背景的混合。 不符合的意思是高度圖保持剛性，並且跟著背景形狀相符。 例如葉子和樹枝的對立。 |
| <b>平滑的貼合背景</b> <i>0.0 - 2.0</i> | 對先前效果進行平滑值，以避免錯誤或極端的變化。 |
| <b>斜坡斜坡</b> <i>0.0 - 1.0</i> | 調整/傾斜圖塊高度，由背景斜度（計算出的法線）驅動。 |
| <b>背景斜坡平滑度</b> <i>0.0 - 2.0</i> | 對先前效果進行平滑值，以避免錯誤或極端的變化。 |
| <b>剪裁黑像素</b> <i>錯誤/真實</i> | 切換以忽略磚塊底形中全黑（0）像素。 |
| <b>扁平圖案底座</b> <i>錯誤/真實</i> | 調整圖塊與背景的混合行為：圖塊會在較低位置時與背景相交（False），或在較低時覆蓋背景。 |
| <b>遮蔽</b> |  |
| <b>面具隨機</b> <i>0.0 - 1.0</i> | 隨機隱藏地磚。 這個數值越高，消失的地塊就越多。 |
| <b>遮罩隨機映射乘法</b> <i>0.0 - 1.0</i> | Treshold 用來判斷什麼時候開始隱藏格子。 |
| <b>Bg Slope 的面具</b> <i>-1.0 - 1.0</i> | 使用背景地圖斜度（計算出的法線）來隱藏圖塊。 |
