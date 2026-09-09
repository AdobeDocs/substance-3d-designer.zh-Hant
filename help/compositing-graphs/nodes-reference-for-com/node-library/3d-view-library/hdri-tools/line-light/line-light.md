---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/line-light.html"
breadcrumb-title: ''
description: 利用線光節點在HDRI環境中建立線性光源，以模擬螢光與條帶照明。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Line Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 線路燈
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9aaf135d4c336ea0cff865524ad1ccd5dcc225bd
workflow-type: tm+mt
source-wordcount: '707'
ht-degree: 3%

---


# 線路燈

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](line-light.resources/panorama-line-light.png){width="200px"}

<b>收錄於：</b> HDRI 工具> 3D 視圖

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

根據空間中兩點的座標生成球面投影的線形。 與 Shape Light[&#128279;](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/hdri-tools/shape-light/shape-light.md) 相比，它有更多選項來調整形狀方向和套用重複圖案。

此節點的定位模式比其他 HDRI 光節點稍複雜。 建議嘗試幾種不同的尺寸模式，找出最適合你情況的。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>背景影像輸入</b> <i>色彩輸入</i> | 可選的背景，用來合成產生的光。 |
| <b>形狀影像輸入</b> <i>色彩輸入</i> | 可選影像映射到線光上。 僅在形狀色彩模式設為影像輸入時使用。 |
| <b>圖案影像輸入</b> <i>灰階輸入</i> | 自訂圖案影像，當「圖案」參數設為「影像輸入」時使用。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>位置模式</b> <i>地面/天花板、起點距離、世界位置</i> | 可從三種不同的放置模式中選擇。 地面/天花板和距離原點支援 2D 視圖中的操作，世界位置只能透過屬性改變，但支持更精確的擺放。 |
| <b>展覽場地格</b> <i>錯誤/真實</i> | 輔助功能，用以繪製除錯地面網格。 有助於估算空間中線條的位置。 |
| <b>位置座標</b> |  |
| <b>向上向量</b> <i>Z Up， Y Up</i> | 只有在世界位置模式下，才能確定座標系的方向。 |
| <b>點 1 紫外線位置</b> | 只有地面/天花板和距離原點。 設定 UV 空間中的第一點位置。 |
| <b>點2 紫外線位置</b> | 只有地面/天花板和距離原點。 設定 UV 空間中的第二個點位置。 |
| <b>點一 世界排名</b> <i>-2.0 - 2.0</i> | 只有在世界排名模式中才會。 設定世界空間的第一點。 不支援 2D 視角互動。 |
| <b>第二點 世界位置</b> <i>-2.0 - 2.0</i> | 只有在世界排名模式中才會。 設定世界空間的第二點。 不支援 2D 視角互動。 |
| <b>線路絕對高度</b> <i>0.0 - 1.0</i> | 只有在地面/天花板位置模式下，設定與天花板的絕對高度。 使用顯示地面網格來更好地估算位置。 |
| <b>距離起源地</b> <i>0.0 - 1.0</i> | 只有在距離原點位置模式時才會這樣。 設定兩個點與全景中心的距離。 |
| <b>形狀色彩模式</b> <i>RGB、溫度（開爾文）、影像輸入</i> | 選擇用什麼方法來設定形狀顏色。 影像輸入可啟用第二個輸入槽。 |
| <b>顏色</b> <i>（色彩值）</i> | 只有在 Shape Color Mode 設為 RGB 時才會這樣。 選擇顏色來塑造形狀。 |
| <b>溫度</b> <i>800.0 - 20000.0</i> | 只有在形狀色彩模式設為溫度時才會這樣。 設定形狀顏色的開爾文值。 |
| <b>形狀影像 UV 模式</b> <i>拉伸，只拉伸中間，重複+間距</i> | 只有在將形狀色彩模式設為影像輸入時才會這樣。 設定影像如何應用於線條形狀，決定紫外線重複行為。 |
| <b>形狀影像重複間距</b> <i>0.0 - 1.0</i> | 只有在形狀色彩模式設為影像輸入，UV 模式設為重複+間距時才會這樣。 設定影像沿線重複時的間距。 |
| <b>形狀影像伽瑪</b> <i>sRGB，線性</i> | 只有在將形狀色彩模式設為影像輸入時才會這樣。 判斷如何解讀形狀影像輸入。 |
| <b>曝光（EV）</b> <i>0.0 - 10.0</i> | 設定產生形狀的曝光值，理想狀況是與背景影像的曝光值相匹配。 |
| <b>線路旋轉</b> <i>0.0 - 1.0</i> | 沿著長度軸旋轉線。 旋轉時，線條被視為平面卡。 |
| <b>線條粗細</b> <i>0.0 - 1.0</i> | 設定線路卡的厚度。 |
| <b>模式</b> <i>平滑方形、銳角方形、錐形、半球、影像輸入</i> | 選擇要使用的圖案形狀。 |
| <b>模式硬度</b> <i>0.0 - 1.0</i> | 設定硬度/圖案對比度。 |
| <b>圖案UV模式</b> <i>拉伸，只拉伸中間，重複+間距</i> | 設定如何使用次要圖案遮罩，套用在 Shape Image 上。 |
| <b>圖案重複間距</b> <i>0.0 - 1.0</i> | 只有當 Pattern UV 模式設為重複 + 間距時才會這樣。 設定重複模式間的間隔。 |
| <b>啟用接地剪裁</b> <i>錯誤/真實</i> | 啟用線條繪製的裁剪。 使用地面/天花板放置模式時，效果是看不出來的。 |
| <b>地面高度</b> <i>-2.0 - 0.0</i> | 設定圓平面的相對高度，用於裁剪。 影響繪製的地面網格。 |
| <b>啟用 Backgound 輸入</b> <i>錯誤/真實</i> | 切換使用可選背景圖片。 合成影像會在背景上產生光。 |
| <b>背景色</b> <i>（色彩值）</i> | 如果沒有使用背景輸入，請在此設定一個純色背景值。 |
| <b>背景 伽瑪</b> <i>sRGB，線性</i> | 如果使用背景輸入，請設定如何解讀背景輸入。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="line-light.resources/line-light-ex.gif" />
        </td>
    </tr>
</table>
