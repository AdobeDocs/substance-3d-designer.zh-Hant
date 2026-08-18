---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/shape-light.html"
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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---


# 形狀光

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/panorama-shape.png){width="200px"}

## 形狀光

**收錄於：***3D 視圖/HDRI 工具*

**複合體**

</td>
<td style="border: 0;" valign="top">

## 說明

產生球面投影的長方形圖形。 形狀變換是由變形裝置驅動的。

## 輸入

* **背景影像輸入**： *色彩輸入*&#x200B;可選背景，用於合成光源。
* **形狀影像輸入**： *顏色輸入*&#x200B;可選影像映射到球光。 僅在形狀色彩模式設為影像輸入時使用。

## 參數

* **形狀矩陣**
  * **矩陣**： *（轉換矩陣）*\
    結果的變換控制。 結果可透過直接與畫布互動來修改。
  * **偏移**&#x200B;量： *-2.0 - 2.0*\
    移動或翻譯結果。 結果可透過直接與畫布互動來修改。
* **形狀**： *長方形、圓盤*\
  選擇要放置的形狀。
* **形狀色彩模式**： *RGB、溫度（開爾文）、影像輸入*\
  選擇用什麼方法來設定形狀顏色。 影像輸入可啟用第二個輸入槽。
* **顏色**： *（顏色值）*\
  只有在 Shape Color Mode 設為 RGB 時才會這樣。 選擇顏色來塑造形狀。
* **形狀溫度**： *800.0 - 20000.0*\
  只有在形狀色彩模式設為溫度時才會這樣。 設定形狀顏色的開爾文值。
* **形狀影像輸入伽瑪**： *sRGB，線性*\
  只有在將形狀色彩模式設為影像輸入時才會這樣。 判斷如何解讀形狀影像輸入。
* **形狀曝光（EV）：***0.0 - 10.0*\
  設定產生形狀的曝光值，理想狀況是與背景影像的曝光值相匹配。
* **形狀硬度**： *0.0 - 1.0*\
  設定形狀邊緣的硬度。
* **熱點暴露（EV）：***0.0 - 10.0*\
  設定中央熱點曝光。 請注意，這在 RGB 模式下不太明顯。
* **熱點大小**： *0.0 - 1.0*\
  中央熱點的規模。
* **熱點衰減**： *0.0 - 1.0*\
  中央熱點的衰落。
* **熱點位置**： *0.0 - 1.0*\
  中央熱點的X和Y位置。
* **啟用 Backgound 輸入**： *False/True*\
  切換使用可選背景圖片。 合成影像會在背景上產生光。
* **背景色**： *（色彩值）*\
  如果沒有使用背景輸入，請在此設定一個純色背景值。
* **背景伽瑪**： *sRGB，線性*&#x200B;如果使用背景輸入，設定如何解讀背景輸入。

## 範例圖片

![](../../../../../../assets/shape-light-ex.gif)

</td>
</tr>
</table>
