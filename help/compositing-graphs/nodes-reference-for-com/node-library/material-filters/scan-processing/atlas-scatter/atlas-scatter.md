---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/atlas-scatter.html"
breadcrumb-title: ''
description: 使用Atlas散佈節點將紋理散佈到圖集上，從掃描的材質中創造出拼貼圖案。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Atlas Scatter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 阿特拉斯散布
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2c331b568074714ea71231410f997f965e2bcdaa
workflow-type: tm+mt
source-wordcount: '1223'
ht-degree: 7%

---


# 阿特拉斯散布

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](atlas-scatter.resources/atlas-scatter.png){width="200px"}

<b>收錄於：</b> 《材料濾>掃描處理》

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

從地圖集中提取元素，散布在背景上。 Atlas 輸入是完整的材質，由各個元素排列並包裝在單一材質圖表上組成。 這個節點會利用內部 [的 Atlas Splitter](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/atlas-splitter/atlas-splitter.md) 流程將它們分割並散布，類似 [Shape Splatter](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter/shape-splatter.md)。 Atlas Scatter 至少需要輸入不透明度地圖，以及 Atlas 的高度地圖輸入，才能運作。

</td>
</tr>
</table>

>[!NOTE]
>
> 數百個 [圖集](https://source.substance3d.com/allassets?assetType=substanceAtlas)已準備好用於阿特拉斯散佈節點，現已在 [Substance Source](https://source.substance3d.com/)上取得。

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>圖集輸入解析</b> <i>決議，1至12</i> | 手動設定完整輸入圖集的解析度，以確保良好的效能與品質比。 |
| <b>X 金額</b> <i>1 - 64</i> | 該模式重複次數為數。 |
| <b>Y 金額</b> <i>1 - 64</i> | 該模式的Y字重複次數。 |
| <b>模式</b> |  |
| <b>圖案範圍</b> <i>0 - 10</i> | 定義了要散佈的圖案範圍。 若設為 0，則所有模式都會被使用。 |
| <b>模式分配模式</b> <i>隨機索引、模式索引、行索引、欄位索引</i> | 定義圖集元素的使用順序。 |
| <b>模式分布地圖乘數</b> <i>0.0 - 1.0</i> | 根據輸入影像的灰階值選擇形狀圖案。 |
| <b>模式旋轉</b> <i>0, 90, 180, 270</i> | 對每個圖譜元素施加固定旋轉，依選定度數調整。 |
| <b>模式旋轉隨機</b> <i>0.0 - 1.0</i> | 對設定的圖集元素部分施加隨機旋轉。 |
| <b>Atlas 形狀偵測精確度</b> <i>簡單或小形狀，複雜或大形狀，無故障模式</i> | 設定形狀偵測的精確度。 準確度越高，對效能的影響就越大。 |
| <b>縮小圖集不透明度（更快的偵測）</b> <i>-4 - 0</i> | 讓你可以控制輸入圖集不透明度貼圖的下縮比例，這張圖用於形狀偵測。 較低的解析度會提升效能，但犧牲準確度。 |
| <b>忽略小於</b> <i>0.0 - 1.0</i> | 設定一個形狀必須被偵測到的最小尺寸，表示為整體影像的比值 |
| <b>規模</b> |  |
| <b>規模</b> <i>0.0 - 5.0</i> | 設定散佈形狀的相對比例。 |
| <b>量表隨機</b> <i>0.0 - 1.0</i> | 定義了對每個散落形狀施加隨機縮放的乘數。 |
| <b>比例無重疊</b> <i>0.0 - 1.0</i> | 縮小形狀比例，避免重疊。 |
| <b>比例地圖倍數</b> <i>0.0 - 1.0</i> | 將形狀縮放乘以輸入影像灰階值。 |
| <b>規模</b> <i>0.0 - 1.0</i> | 以長度（X）和寬度（Y）來設定散落形狀的相對比例尺。 |
| <b>從Bg Slope的尺寸比</b> <i>0.0 - 1.0</i> | 根據背景高度斜率調整形狀大小比。 |
| <b>保留長寬比</b> <i>0.0 - 1.0</i> | 決定應保留散落形狀原始比例的多少，而非使用其網格單元比例，即 X Amount 與 Y M 值的比例。 |
| <b>職位</b> |  |
| <b>隨機位置</b> <i>0.0 - 2.0</i> | 一個乘數，用於將每個形狀從網格起點隨機方向移動。 |
| <b>隨機分布</b> <i>高斯分布，均勻</i> | 隨機位置從高斯分布切換為均勻分布。 高斯分布會產生比均勻分布更有機的結果。 |
| <b>向量映射乘法</b> <i>0.0 - 1.0</i> | 控制向量地圖輸入的影響，使形狀朝地圖紅色（X）和綠色（Y）通道指定的向量方向移動。 |
| <b>水平偏移</b> <i>-2.0 - 2.0</i> | X 軸位置偏移的乘數。 |
| <b>偏移垂直</b> <i>-2.0 - 2.0</i> | 一個位置偏移的乘數，沿著Y軸。 |
| <b>界外選項</b> <i>比例形狀，限制位置</i> | 由於濺射的技術特性，形狀只能畫出比原本位置超過2格大小的距離。 如果形狀變得太大或移動太遠，你有兩個選擇：- 縮放形狀會在遇到界限時縮小形狀大小 - 限制位置會將形狀移回原本位置 |
| <b>旋轉</b> |  |
| <b>旋轉</b> <i>0.0 - 1.0</i> | 讓你可以控制所有形狀的局部旋轉。 |
| <b>旋轉隨機</b> <i>0.0 - 1.0</i> | 每個形狀隨機施加旋轉量的乘數。 |
| <b>從Bg斜坡轉動</b> <i>0.0 - 1.0</i> | 根據背景高度斜率的函數修改形狀旋轉。 通常與「來自Bg斜率的尺寸比」參數結合使用。 |
| <b>旋轉映射乘數</b> <i>0.0 - 1.0</i> | 將形狀旋轉與輸入影像灰階值相乘。 |
| <b>向量映射乘法</b> <i>0.0 - 1.0</i> | 根據向量影像輸入設定形狀旋轉。 |
| <b>高度</b> |  |
| <b>高度刻度自動調整</b> <i>錯誤/真實</i> | 根據圖案比例自動調整高度，使形狀高度與背景高度成比例。 |
| <b>混合模式</b> <i>身高混合，Alpha測試</i> | 設定了重疊形狀的求解方法。 |
| <b>身高偏移</b> <i>-1.0 - 1.0</i> | 對形狀高度套用全域偏移 |
| <b>高度偏移隨機</b> <i>0.0 - 1.0</i> | 每個形狀隨機施加高度偏移的乘數 |
| <b>高度偏移地圖多重機</b> <i>0.0 - 1.0</i> | 將形狀高度偏移乘以輸入影像灰階值。 |
| <b>身高比例</b> <i>0.0 - 1.0</i> | 讓你能控制散落形狀的全局高度比例 |
| <b>身高隨機</b> <i>0.0 - 1.0</i> | 每個形狀隨機施加高度刻度的乘數 |
| <b>高度比例地圖乘數</b> <i>0.0 - 1.0</i> | 以輸入影像灰階值乘以形狀高度尺度。 |
| <b>符合背景</b> <i>0.0 - 1.0</i> | 在 0 時，形狀高度保持不變;在 1 時，形狀高度會被底層高度背景所改變。 |
| <b>平滑的貼合背景</b> <i>0.0 - 2.0</i> | 讓你可以控制形狀在與背景形成對其高度變形時施加的平滑量。 |
| <b>斜坡斜坡</b> <i>0.0 - 1.0</i> | 根據局部背景高度斜率變形形狀高度：在形狀高度上加入對應背景斜率的線性梯度。 |
| <b>背景斜坡平滑度</b> <i>0.0 - 2.0</i> | 控制當形狀因斜率而傾斜時，對背景斜率施加的平滑量。 |
| <b>剪裁黑像素</b> <i>錯誤/真實</i> | 忽略圖案輸入的黑色值。 |
| <b>扁平圖案底座</b> <i>錯誤/真實</i> | 讓你能將背景高度壓平，使其起始高度與形狀相符。 |
| <b>遮蔽</b> |  |
| <b>面具隨機</b> <i>0.0 - 1.0</i> | 遮罩隨機數量的形狀，表示為總數的比值。 |
| <b>遮罩隨機映射乘法</b> <i>0.0 - 1.0</i> | 將隨機形狀遮罩設定為灰階影像輸入的函數。 |
| <b>Bg Slope 的面具</b> <i>-1.0 - 1.0</i> | 根據背景斜率控制形狀的遮罩。 |
| <b>顏色</b> |  |
| <b>色彩調整</b> <i>-1.0 - 1.0</i> | 讓你可以全局調整散布元素的顏色。 |
| <b>顏色隨機</b> <i>0.0 - 1.0</i> | 一個乘數，用來隨機偏移每個形狀的顏色值。 |
| <b>背景色彩</b> <i>0.0 - 1.0</i> | 將形狀顏色轉換成其位置背景的顏色。 |
| <b>正常</b> |  |
| <b>斜坡斜坡</b> <i>0.0 - 1.0</i> | 根據背景法線調整形狀的法線。 |
| <b>普通隨機</b> <i>0.0 - 1.0</i> | 一個乘數，將形狀的法線偏斜，隨機偏向每個形狀。 |
| <b>一般格式</b> <i>DirectX、OpenGL</i> | 切換不同的法線貼圖格式（反轉綠色通道） |
| <b>粗糙度</b> |  |
| <b>粗糙度調整</b> <i>-1.0 - 1.0</i> | 這樣可以讓你偏移全域形狀的粗糙度。 |
| <b>來自背景的粗糙感</b> <i>0.0 - 1.0</i> | 將形狀的粗糙度轉換到它們所在位置的背景粗糙度。 |
| <b>粗糙隨機</b> <i>0.0 - 1.0</i> | 一個乘數，用來將粗糙度以隨機的比例抵消每個形狀。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="atlas-scatter.resources/atlas-scatter-11.png" />
        </td>
    </tr>
</table>
