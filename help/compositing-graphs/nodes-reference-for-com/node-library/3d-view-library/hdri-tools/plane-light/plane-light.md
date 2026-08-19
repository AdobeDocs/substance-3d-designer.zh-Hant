---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/plane-light.html"
breadcrumb-title: ''
description: 使用 Plane Light 節點將平面光源加入 HDRI 環境，以進行方向性光照控制。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Plane Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 飛機燈
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '631'
ht-degree: 0%

---


# 飛機燈

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/panorama-plane-light.png){width="200px"}

## 飛機燈

**收錄於：***3D 視圖/HDRI 工具*

**複合體**

</td>
<td style="border: 0;" valign="top">

## 說明

產生球面投影平面形狀。 平面可利用輸入參數在三維中放置與定向。

它與較 [簡單的 Shape Light](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/hdri-tools/shape-light/shape-light.md) 不同之處在於，除了較簡單的 Distance 投影外，還有更多進階的放置選項，且可套用更多圖案和遮罩，類似 [Line Light](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/hdri-tools/line-light/line-light.md)。

## 輸入

* **背景影像輸入**： *色彩輸入*\
  可選的背景，用來合成產生的光。
* **形狀影像輸入**： *色彩輸入*\
  可選影像映射到線光上。 僅在形狀色彩模式設為影像輸入時使用。
* **圖案影像輸入**： *灰階輸入*\
  自訂圖案影像，當「圖案」參數設為「影像輸入」時使用。

## 參數

* **位置模式**： *地面/天花板、距離原點、世界位置*\
  可從三種不同的放置模式中選擇。 地面/天花板和距離原點支援 2D 視圖中的操作，世界位置只能透過屬性改變，但支持更精確的擺放。
* **顯示地面網格**： *錯誤/真實*\
  輔助功能，用以繪製除錯地面網格。 有助於估算空間中線條的位置。
* **位置座標**
  * **上向量**： *Z 上，Y 上*\
    只有在世界位置模式下，才能確定座標系的方向。
  * **平面紫外線位置**：\
    只有地面/天花板和距離原點。 設定平面在 UV 空間的位置。
  * **平面世界位置**： *-2.0 - 2.0*\
    只有在世界排名模式中才會。 設定平面位置、世界空間。 不支援 2D 視角互動。
  * **飛機絕對高度**： *0.0 - 1.0*\
    只有在地面/天花板位置模式下，設定與天花板的絕對高度。 使用顯示地面網格來更好地估算位置。
  * **距離起點**&#x200B;距離： *0.0 - 1.0*\
    只有在距離原點位置模式時才會這樣。 設定兩個點與全景中心的距離。
* **形狀色彩模式**： *RGB、溫度（開爾文）、影像輸入*\
  選擇用什麼方法來設定形狀顏色。 影像輸入可啟用第二個輸入槽。
* **顏色**： *（顏色值）*\
  只有在 Shape Color Mode 設為 RGB 時才會這樣。 選擇顏色來塑造形狀。
* **溫度**： *800.0 - 20000.0*\
  只有在形狀色彩模式設為溫度時才會這樣。 設定形狀顏色的開爾文值。
* **形狀影像 UV 模式**： *拉伸、僅拉伸中間、重複 + 間距*\
  只有在將形狀色彩模式設為影像輸入時才會這樣。 設定影像如何應用於線條形狀，決定紫外線重複行為。
* **形狀影像重複間距**： *0.0 - 1.0*\
  只有在形狀色彩模式設為影像輸入，UV 模式設為重複+間距時才會這樣。 設定影像沿線重複時的間距。
* **形狀影像伽瑪**： *sRGB，線性*\
  只有在將形狀色彩模式設為影像輸入時才會這樣。 判斷如何解讀形狀影像輸入。
* **曝光（EV）：***0.0 - 10.0*\
  設定產生形狀的曝光值，理想狀況是與背景影像的曝光值相匹配。
* **平面比例**： *0.0 - 1.0*\
  設定平面形狀的均勻縮放。
* **飛機尺寸**： *0.0 - 1.0*\
  設定平面形狀的非均勻大小。
* **平面旋轉**： *0.0 - 1.0*\
  沿著中央軸旋轉平面。
* **圖案**： *平滑方形、銳角方形、錐形、半球形、影像輸入*\
  選擇要使用的圖案形狀。
* **圖案硬度**： *0.0 - 1.0*\
  設定硬度/對比度以符合花紋。
* **圖案UV模式**： *拉伸，拉伸 僅限中間*\
  設定如何使用次要圖案遮罩，套用在 Shape Image 上。
* **啟用接地剪波**： *錯誤/正確*\
  啟用 Plane 是否能被地面平面裁剪，或在下方仍顯示。 使用顯示地面網格來更好地估算這個數字。
* **地面高度**： *-2.0 - 0.0*\
  調整地面高度以防削波。
* **啟用 Backgound 輸入**： *False/True*\
  切換使用可選背景圖片。 合成影像會在背景上產生光。
* **背景色**： *（色彩值）*\
  如果沒有使用背景輸入，請在此設定一個純色背景值。
* **背景伽瑪**： *sRGB，線性*&#x200B;如果使用背景輸入，設定如何解讀背景輸入。

## 範例圖片

![](../../../../../../assets/plane-light-ex.gif)

</td>
</tr>
</table>
