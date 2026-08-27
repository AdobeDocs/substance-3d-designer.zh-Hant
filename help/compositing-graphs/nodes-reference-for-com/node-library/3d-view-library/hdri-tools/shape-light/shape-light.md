---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/shape-light.html"
breadcrumb-title: ''
description: 使用 Shape Light 節點為 HDRI 環境新增自訂形狀的光源，以創造創意光效。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Shape Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 形狀光
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 5%

---


# 形狀光

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](shape-light.resources/panorama-shape.png){width="200px"}

<b>收錄於：</b> HDRI 工具> 3D 視圖

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

產生球面投影的長方形圖形。 形狀變換是由變形裝置驅動的。

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
| <b>形狀矩陣</b> |  |
| <b>矩陣</b> <i>（變換矩陣）</i> | 結果的變換控制。 結果可透過直接與畫布互動來修改。 |
| <b>偏移</b> <i>-2.0 - 2.0</i> | 移動或翻譯結果。 結果可透過直接與畫布互動來修改。 |
| <b>形狀</b> <i>矩形，圓盤</i> | 選擇要放置的形狀。 |
| <b>形狀色彩模式</b> <i>RGB、溫度（開爾文）、影像輸入</i> | 選擇用什麼方法來設定形狀顏色。 影像輸入可啟用第二個輸入槽。 |
| <b>顏色</b> <i>（色彩值）</i> | 只有在 Shape Color Mode 設為 RGB 時才會這樣。 選擇顏色來塑造形狀。 |
| <b>形狀溫度</b> <i>800.0 - 20000.0</i> | 只有在形狀色彩模式設為溫度時才會這樣。 設定形狀顏色的開爾文值。 |
| <b>形狀影像輸入伽瑪</b> <i>sRGB，線性</i> | 只有在將形狀色彩模式設為影像輸入時才會這樣。 判斷如何解讀形狀影像輸入。 |
| <b>形狀曝光（EV）</b> <i>0.0 - 10.0</i> | 設定產生形狀的曝光值，理想狀況是與背景影像的曝光值相匹配。 |
| <b>形狀硬度</b> <i>0.0 - 1.0</i> | 設定形狀邊緣的硬度。 |
| <b>熱點暴露（EV）</b> <i>0.0 - 10.0</i> | 設定中央熱點曝光。 請注意，這在 RGB 模式下不太明顯。 |
| <b>熱點大小</b> <i>0.0 - 1.0</i> | 中央熱點的規模。 |
| <b>熱點衰減</b> <i>0.0 - 1.0</i> | 中央熱點的衰落。 |
| <b>熱點位置</b> <i>0.0 - 1.0</i> | 中央熱點的X和Y位置。 |
| <b>啟用 Backgound 輸入</b> <i>錯誤/真實</i> | 切換使用可選背景圖片。 合成影像會在背景上產生光。 |
| <b>背景色</b> <i>（色彩值）</i> | 如果沒有使用背景輸入，請在此設定一個純色背景值。 |
| <b>背景 伽瑪</b> <i>sRGB，線性</i> | 如果使用背景輸入，請設定如何解讀背景輸入。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="shape-light.resources/shape-light-ex.gif" />
        </td>
    </tr>
</table>
