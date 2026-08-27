---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/interface/2d-view/color-sampler.html"
breadcrumb-title: ''
description: 在 2D 視圖中使用色彩取樣工具，從材質中取樣顏色以進行精確的色彩匹配。
helpx_creative_field: ""
helpx_description: Designer > Interface > 2D view > Color sampler tool
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 色彩取樣工具
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '406'
ht-degree: 0%

---


# 色彩取樣工具

![色彩取樣工具](color-sampler.resources/color-sampler-demo.png "色彩取樣工具"){zoomable="yes"}

色彩取樣器工具讓你在<b>調整參數或切換節點時，追蹤 2D 視圖[&#128279;](../../../interface/2d-view/2d-view.md)中特定像素</b>的值。

它會在視窗中放置一個針腳，並取樣該位置像素的顏色與位置。

## 使用工具

請依照以下步驟存取並使用此工具：

1. 點擊 ![](color-sampler.resources/color-sampler-information-button.png) <b>2D 檢視工具列中的資訊</b> 按鈕，即可開啟資訊底座與工具列
1. 點擊![](color-sampler.resources/color-sampler-tool-icon.png)<b>資訊工具列中的色彩取樣工具</b>按鈕
1. 在視窗中，點擊你想要取樣的特定像素來放置![](color-sampler.resources/color-sampler-pin-icon.png)<b>針腳</b>
1. 請在資訊碼頭專用區查看取樣的數值
1. 工具使用完成後，點擊![](color-sampler.resources/color-sampler-remove-pin.png)<b>刪除</b>按鈕，將該針從視窗中移除。\
   你也可以點擊 RMB 鍵，然後在情境選單中選擇「刪除」動作來移除該 PIN 針。

以下是工具實際操作的示範：

![色彩取樣器：使用 工具](color-sampler.resources/color-sampler-demo.gif "色彩取樣器：使用 工具"){zoomable="yes"}

*點擊放大*

+++複製取樣的RGBA值
你可以點擊針腳上的 RMB，然後在情境選單中選擇「複製 RGBA 值」操作來複製取樣值。

複製的數值可以用 <b>顏色縮圖</b>貼上參數。

資訊面板中的彩色縮圖也可以直接拖放到這些參數的彩色縮圖上。

![色彩取樣器：複製 RGBA 值](color-sampler.resources/color-sampler-demo-copy-rgba-values.gif "色彩取樣器：複製 RGBA 值"){zoomable="yes"}



*點擊放大*

+++

## 取樣資訊

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

資訊分為三種類型和兩種格式。

* <b>儲存在影像各 RGBA 通道中的取樣值</b> ：\
  變數\* / 浮點
* <b>HSV 表示中的取樣顏色</b> ：\
  8位元整數 / 浮點
* <b>像素在</b> 像素數與正規化影像空間中的位置：\
  整數 / 浮點數

</td>
<td width="33.33%" style="border: 0;" valign="top">

![取樣資訊](color-sampler.resources/color-sampler-information.png "取樣資訊"){zoomable="yes"}

</td>
</tr>
</table>

這個值取決於影像所使用的位元深度。 在 Substance 圖中，位元深度由 <b>輸出格式控制</b> [基礎參數](../../../compositing-graphs/graph-parameters/graph-parameters.md)。

可用的位元深度如下：

* <b>8位元整數：</b> 256個整數值，範圍從0到255。
* <b>16 位元整數：</b> 從 0 到 65,535 個整數值 65,536。
* <b>HDR 低精度（16 位元）：</b>以 16 位元編碼的浮點數值。
* <b>HDR 高精度（32位元）：</b>以 32 位元編碼的浮點數值。 這是 Designer 中可用的最高精度。
