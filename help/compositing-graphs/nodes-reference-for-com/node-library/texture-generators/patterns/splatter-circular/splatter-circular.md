---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/splatter-circular.html"
breadcrumb-title: ''
description: 使用濺射圓節點將圓形形狀散布在材質中，創造有機且隨機的圖案。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Splatter Circular
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 濺血圈
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '850'
ht-degree: 7%

---


# 濺血圈

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](splatter-circular.resources/splatter-circular.png){width="128px"}

![](splatter-circular.resources/splatter-circular-color.png){width="128px"}

<b>收錄於：</b> 紋理產生器>圖案

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

Splatter Circular 產生基於環狀的圖案，並具備多種控制。 它可以使用預先定義的形狀或自訂輸入。 它類似[於方塊產生器](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md)，但是圓形擺放而非格子。

這對於想要以各種隨機化選項將形狀呈圓形排列時非常有用。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

兩種輸入都是可選的。

|  |  |
|:---|:---|
| <b>圖案影像輸入 1-6</b> <i>灰階輸入（彩色輸入）</i> | 僅 Splatter Circular ：自訂圖案影像，當「Pattern」參數設為「影像輸入」時使用。 |
| <b>背景</b> <i>灰階輸入（彩色輸入）</i> |  |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>圖案數量</b> <i>1 - 64</i> | 要在戒指上放置的圖案方塊數量。 |
| <b>模式數量隨機</b> <i>0.0 - 1.0</i> | 隨機化放置圖案數量。 最好搭配戒指數量超過1。 |
| <b>模式數量隨機最小值</b> <i>1 - 10</i> | 設定隨機化的最低模式數量。 |
| <b>環數</b> <i>1 - 10</i> | 設定要填滿的環數。 這些環總是放在外層的環內，且空間均勻。 |
| <b>非平方展開</b> <i>錯誤/真實</i> | 能以非平方比率補償擠壓與拉伸。 |
| <b>模式</b> |  |
| <b>模式</b> <i>影像輸入、方形、圓盤、拋物面、鐘形、高斯分布、荊棘、金字塔、磚塊、漸變、波浪、半鐘形、脊狀鐘、新月形、膠囊、錐形</i> | 選擇要使用的圖案形狀。 |
| <b>模式輸入編號</b> <i>1 - 6</i> | 設定可使用的不同影像輸入數量。 僅在上方選擇影像輸入</i>時<i>才可用。 |
| <b>模式輸入分布</b> <i>隨機、按圖案編號、按環號</i> | 設定如何選擇多個模式輸入。 隨機指隨機選出一個，圖案編號指它們只是放在一個循環序列中，而環號則是每個環都有不同的環。 |
| <b>影像輸入過濾</b> <i>雙線性 + 多元映射、雙線性、最近</i> |  |
| <b>圖案專屬</b> <i>0.0 - 1.0</i> | 讓你可以改變所選圖案的形狀。 效果取決於所選的模式。 |
| <b>對稱隨機</b> <i>0.0 - 1.0</i> | 根據以下行為，設定應該隨機翻轉/鏡像的方塊數量。 |
| <b>對稱隨機模式</b> <i>水平 + 垂直，水平，垂直</i> | 決定對稱性、鏡像行為。 |
| <b>職位</b> |  |
| <b>半徑</b> <i>0.0 - 1.0</i> | 設定圖案放置中心的半徑。 |
| <b>隨機半徑</b> <i>0.0 - 1.0</i> | 隨機化每個圖案格塊的半徑。 |
| <b>環形半徑乘數</b> <i>0.0 - 1.0</i> | 影響多環間距。 |
| <b>角度隨機</b> <i>0.0 - 1.0</i> | 隨機化每個圖案的角度。 越多的旋轉量越大。 |
| <b>螺旋因子</b> <i>0.0 - 1.0</i> | 將環形區域變成螺旋形，每塊方塊的半徑都會稍微增加。 |
| <b>擴散</b> <i>0.0 - 2.0</i> | 它設定了環的轉數。 這個數字可以被提升到極限之外。 |
| <b>方向偏移</b> <i>0.0 - 1.0</i> | 將每個圖案從中心沿角度移動。 這個效果很大程度上取決於角度隨機，或者看起來就像是半徑的倍數。 |
| <b>全球抵消</b> <i>0.0 - 1.0</i> | 能翻譯整個形狀。 |
| <b>規模</b> |  |
| <b>連結模式</b> <i>錯誤/真實</i> | 讓圖案方塊的長度取決於半徑，也就是說每個形狀應該會接觸到前一個和下一個形狀。 |
| <b>規模（連通）</b> <i>0.0 - 1.0</i> | 會在全球範圍內改變每個圖案的大小。 連接時，它是相對於總半徑的。 |
| <b>隨機大小</b> <i>0.0 - 1.0</i> | 會隨機化每個圖案的大小。 |
| <b>規模</b> <i>0.0 - 2.0</i> | 均勻地縮放每個圖案。 |
| <b>量表隨機</b> <i>0.0 - 1.0</i> | 隨機化均勻的縮放。 |
| <b>按圖案編號比例</b> <i>0.0 - 1.0</i> | 這樣圖案的比例就會依照環上的位置而定。 |
| <b>反轉模式編號</b> <i>錯誤/真實</i> | 若與前述選項結合，則可將縮放從小變大，反之亦然。 |
| <b>環號比例</b> <i>0.0 - 1.0</i> | 這樣會讓比例依賴環號。 |
| <b>反環數</b> <i>錯誤/真實</i> | 與前一種選項搭配使用時，它可以將縮放從小反轉到大，反之亦然。 |
| <b>旋轉</b> |  |
| <b>模式旋轉</b> <i>0.0 - 1.0</i> | 每個圖案都能均勻旋轉。 |
| <b>模式旋轉隨機</b> <i>0.0 - 1.0</i> | 隨機化圖案輪換。 |
| <b>模式旋轉樞軸</b> <i>中心，最小X，最大X，最小Y，最大Y</i> | 設定每個圖案可單獨旋轉的樞軸點位置。 |
| <b>中心方向</b> <i>錯誤/真實</i> | 會把每個圖案旋轉，使其朝向環的中心。 關閉它會讓它們的方向相同——這可能會產生偏移方向的不良效果。 |
| <b>環旋轉</b> <i>0.0 - 1.0</i> | 可以把整個環繞中心旋轉。 |
| <b>環旋轉隨機</b> <i>0.0 - 1.0</i> | 隨機化每個環的旋轉。 |
| <b>環狀旋轉偏移量</b> <i>0.0 - 1.0</i> | 偏移每個環的旋轉。 |
| <b>顏色</b> |  |
| <b>顏色</b> <i>（灰階）</i> | 顏色會與所選圖案相乘。 |
| <b>亮度隨機</b> <i>0.0 - 1.0</i> | 對每個圖案磚隨機化顏色或亮度。 |
| <b>按比例的亮度</b> <i>0.0 - 1.0</i> | 亮度會依照個別圖案的尺度而定。 |
| <b>依圖案編號的亮度</b> <i>0.0 - 1.0</i> | 讓亮度依賴於圖案序列。 例如可以搭配螺旋圖案使用。 |
| <b>反轉模式編號</b> <i>錯誤/真實</i> | 顛倒了之前的選項。 |
| <b>依環號的亮度</b> <i>0.0 - 1.0</i> | 使亮度依賴於環序列。 |
| <b>反環數</b> <i>錯誤/真實</i> | 顛倒了之前的選項。 |
| <b>隨機面具</b> <i>0.0 - 1.0</i> | 隨機隱藏模式。 |
| <b>背景色</b> <i>（灰階）</i> | 改變純色背景色。 |
| <b>混合模式</b> <i>加、最大、加字幕</i> | 設定如何混合重疊的圖案。 |
| <b>全域不透明度</b> <i>0.0 - 1.0</i> | 設定整個結果的全域不透明度。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="splatter-circular.resources/circularsplatter-ex.png" />
        </td>
    </tr>
</table>
