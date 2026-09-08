---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/sphere-light.html"
breadcrumb-title: ''
description: 使用 Sphere Light 節點為 HDRI 環境新增球形光源，以提升光照控制效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Sphere Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 球光
user-guide-description: ''
user-guide-title: ''
source-git-commit: 43dd5433948c89f68426040a2a2d76282072c75d
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 4%

---


# 球光

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/panorama-sphere-light.png){width="200px"}

<b>收錄於：</b> HDRI 工具> 3D 視圖

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

產生球面投影的球體形狀。 球體變換是由變形裝置驅動的。

球光相當多功能，不僅能產生簡單的圓形光，還能生成行星或其他天體。 如果你不需要更進階的光照和旋轉選項，可以 [考慮 Shape Light](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/hdri-tools/shape-light/shape-light.md) 。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>背景影像輸入</b> <i>色彩輸入</i> | 可選的背景，用來合成產生的光。 |
| <b>形狀影像輸入</b> <i>色彩輸入</i> | 可選的影像可映射到 Sphere 燈光上。 僅在形狀色彩模式設為影像輸入時使用。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>位置模式</b> <i>距離起點距離、世界位置</i> | 請在兩種放置模式中選擇。 距離原點的距離類似極座標，球體相對於全景中心設定，世界位置則像標準三維座標一樣運作。 |
| <b>位置座標</b> |  |
| <b>向上向量</b> <i>Z Up， Y Up</i> | 只有在世界位置模式下，才能確定座標系的方向。 |
| <b>球體世界位置</b> <i>-2.0 - 2.0</i> | 只有在世界位置模式中，才能設定球面在世界空間中的位置。 |
| <b>職位</b> | 只有在距離原點模式時才會這樣。 設定相對於中心的位置。 可以在 2D 視圖中操作。 |
| <b>距離起源地</b> <i>0.0 - 20.0</i> | 只有在距離原點模式時才會這樣。 設定原點距離，影響球體的可見大小。 |
| <b>形狀色彩模式</b> <i>RGB、溫度（開爾文）、影像輸入</i> | 選擇用什麼方法來設定形狀顏色。 影像輸入可啟用第二個輸入槽。 |
| <b>顏色</b> <i>（色彩值）</i> | 只有在 Shape Color Mode 設為 RGB 時才會這樣。 選擇顏色來塑造形狀。 |
| <b>形狀溫度</b> <i>800.0 - 20000.0</i> | 只有在形狀色彩模式設為溫度時才會這樣。 設定形狀顏色的開爾文值。 |
| <b>球面影像輸入伽瑪</b> <i>sRGB，線性</i> | 只有在將形狀色彩模式設為影像輸入時才會這樣。 判斷如何解讀形狀影像輸入。 |
| <b>球面旋轉</b> <i>0.0 - 1.0</i> | 只有在將形狀色彩模式設為影像輸入時才會這樣。 會繞著中心旋轉球體來定位映射影像。 |
| <b>曝光（EV）</b> <i>0.0 - 10.0</i> | 設定產生形狀的曝光值，理想狀況是與背景影像的曝光值相匹配。 |
| <b>球半徑</b> <i>0.0 - 1.0</i> | 設定球體的半徑/大小。 |
| <b>球面硬度</b> <i>0.0 - 1.0</i> | 用來設定球體的硬度/衰減。 |
| <b>陰影</b> <i>無，肢體漸暗，光明漸暗</i> | 設定是否需要對球體施加任何陰影。 讓球體不會看起來像實心、未點亮的物體。 邊緣變暗表示邊緣會出現輕微變暗，陰影光則是球體被可選的陰影光照亮。 |
| <b>著影光世界排名</b> <i>-1.0 - 1.0</i> | 如果著色設定為著色光，這裡會控制光線在球體上的位置。 |
| <b>Penombra 透明度</b> <i>0.0 - 1.0</i> | 如果 Shading 設為 Shading Light，則控制陰影的衰減。 |
| <b>啟用 Backgound 輸入</b> <i>錯誤/真實</i> | 切換使用可選背景圖片。 合成影像會在背景上產生光。 |
| <b>背景色</b> <i>（色彩值）</i> | 如果沒有使用背景輸入，請在此設定一個純色背景值。 |
| <b>背景 伽瑪</b> <i>sRGB，線性</i> | 如果使用背景輸入，請設定如何解讀背景輸入。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/sphere-light-ex.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/spherelight-ex1.png" />
        </td>
    </tr>
</table>
