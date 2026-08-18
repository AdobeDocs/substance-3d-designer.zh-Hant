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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 0%

---


# 球光

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/panorama-sphere-light.png){width="200px"}

## 球光

**收錄於：***3D 視圖/HDRI 工具*

**複合體**

</td>
<td style="border: 0;" valign="top">

## 說明

產生球面投影的球體形狀。 球體變換是由變形裝置驅動的。

球光相當多功能，不僅能產生簡單的圓形光，還能生成行星或其他天體。 如果你不需要更進階的光照和旋轉選項，可以 [考慮 Shape Light](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/hdri-tools/shape-light/shape-light.md) 。

## 輸入

* **背景影像輸入**： *色彩輸入*&#x200B;可選背景，用於合成光源。
* **形狀影像輸入**： *顏色輸入*&#x200B;可選影像映射到球光。 僅在形狀色彩模式設為影像輸入時使用。

### 參數

* **位置模式**： *距離原點、世界位置*\
  請在兩種放置模式中選擇。 距離原點的距離類似極座標，球體相對於全景中心設定，世界位置則像標準三維座標一樣運作。
* **位置座標**
  * **上向量**： *Z 上，Y 上*\
    只有在世界位置模式下，才能確定座標系的方向。
  * **球體世界排名**： *-2.0 - 2.0*\
    只有在世界位置模式中，才能設定球面在世界空間中的位置。
  * **職位**：\
    只有在距離原點模式時才會這樣。 設定相對於中心的位置。 可以在 2D 視圖中操作。
  * **距離原點**： *0.0 - 20.0*&#x200B;僅限於距離原點模式。 設定原點距離，影響球體的可見大小。
* **形狀色彩模式**： *RGB、溫度（開爾文）、影像輸入*\
  選擇用什麼方法來設定形狀顏色。 影像輸入可啟用第二個輸入槽。
* **顏色**： *（顏色值）*\
  只有在 Shape Color Mode 設為 RGB 時才會這樣。 選擇顏色來塑造形狀。
* **形狀溫度**： *800.0 - 20000.0*\
  只有在形狀色彩模式設為溫度時才會這樣。 設定形狀顏色的開爾文值。
* **球體影像輸入伽瑪**： *sRGB，線性*\
  只有在將形狀色彩模式設為影像輸入時才會這樣。 判斷如何解讀形狀影像輸入。
* **球面旋轉**： *0.0 - 1.0*\
  只有在將形狀色彩模式設為影像輸入時才會這樣。 會繞著中心旋轉球體來定位映射影像。
* **曝光（EV）：***0.0 - 10.0*\
  設定產生形狀的曝光值，理想狀況是與背景影像的曝光值相匹配。
* **球體半徑**： *0.0 - 1.0*\
  設定球體的半徑/大小。
* **球體硬度**： *0.0 - 1.0*\
  用來設定球體的硬度/衰減。
* **陰影**： *無，肢體變暗，光線漸暗*\
  設定是否需要對球體施加任何陰影。 讓球體不會看起來像實心、未點亮的物體。 邊緣變暗表示邊緣會出現輕微變暗，陰影光則是球體被可選的陰影光照亮。
* **陰影之光世界排名**： *-1.0 - 1.0*\
  如果著色設定為著色光，這裡會控制光線在球體上的位置。
* **Penombra 透明度**： *0.0 - 1.0*\
  如果 Shading 設為 Shading Light，則控制陰影的衰減。
* **啟用 Backgound 輸入**： *False/True*\
  切換使用可選背景圖片。 合成影像會在背景上產生光。
* **背景色**： *（色彩值）*\
  如果沒有使用背景輸入，請在此設定一個純色背景值。
* **背景伽瑪**： *sRGB，線性*&#x200B;如果使用背景輸入，設定如何解讀背景輸入。

## 範例圖片

![](../../../../../../assets/sphere-light-ex.gif)

![](../../../../../../assets/spherelight-ex1.png)

</td>
</tr>
</table>
