---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-render.html"
breadcrumb-title: ''
description: 使用 Spline Render 節點將樣條線渲染成材質，並可自訂寬度、顏色和混合模式。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Render
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 樣條渲染
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '810'
ht-degree: 0%

---


# 樣條渲染

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![節點圖示](spline-render.resources/spline-render-01.png "節點圖示")

<b>收錄於：</b> 樣條與路徑工具 > 樣條鍵工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

沿著輸入 <b>樣條</b> 線在輸入 <b>背景</b>上繪製線段串。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>背景</b> <i>灰階</i> | 灰階影像，應該繪製在上面的樣條曲線。 |
| <b>樣條座標</b> <i>顏色</i> | 彩色影像RGBA通道中編碼的輸入樣條點座標：<br><b>R</b> - X 位置<br><b>G</b> - Y 位置<br><b>B</b> - 高度<br><b>A</b> - 打包資料：<br>- 符號：樣條線為閉合（負）或開（正）;<br>- 絕對值：厚度 + 1。 |
| <b>樣條資料</b> <i>顏色</i> | 彩色影像的 RGBA 通道中編碼的輸入樣條線額外資料。<br><b>R</b> - 切線 x<br><b>G</b> - 切線 y<br><b>B</b> - 未使用<br><b>A</b> - 未使用 |
| <b>樣條量</b> <i>整數</i> | 輸入樣條的數量。 |

<a name="outputs"></a>

## 輸出

|  |  |
|:---|:---|
| <b>產出</b> <i>灰階</i> | 這是將輸入樣條線繪製在背景上方的結果影像。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>模式</b> <i>整數</i> | 選擇繪製樣條的方法：<br>- <i>繪製樣條條列表</i>：繪製輸入列表中<br>的所有樣條;- <i>繪製單樣條：</i>只從輸入列表中繪製指定的樣條;<br>- <i>繪製樣條範圍</i>：從輸入列表中繪製指定範圍內的樣條。 |
| <b>繪製樣條指數</b> <i>整數</i> | （當「模式」設為「繪製單樣條鍵」時可用）應繪製的樣條曲線索引。 |
| <b>拉取樣條範圍</b> <i>整數2</i> | （當「模式」設為「繪製樣條範圍」時可用）應繪製樣條曲線的索引範圍。 |
| <b>節目指導助理</b> <i>布林值</i> | 對每個樣條曲線，在樣條曲線的起始處畫一個點，在末端畫一個箭頭。 |
| <b>分段數量</b> <i>整數</i> | 調整沿著樣條曲線繪製的線段數。<br>值越高，線條越平滑。 |
| <b>包絡樣條量</b> <i>整數</i> | 每個樣條線厚度上應繪製的重複段數。 |
| <b>開始</b> <i>浮標</i> | 偏移應該繪製樣條曲線起始部分的起點。<br>該值代表樣條的正規化長度。 |
| <b>結束</b> <i>浮標</i> | 偏移應該繪製樣條曲線部分的末端。<br>該值代表樣條的正規化長度。 |
| <b>厚度尺寸模式</b> <i>整數</i> | 計算繪製區段厚度的方法：<br>- <i>影像</i>：數值在貼圖空間中正規化，1 為影像的全寬度。 厚度是相對於貼圖解析度的<br>;- <i>Pixel</i>：值為貼圖中絕對的像素數，其中 1 代表完整像素。 厚度和貼圖解析度是分開的。 |
| <b>厚度（圖片）</b> <i>浮標</i> | （當「厚度大小模式」設為影像時可用）繪製區段的厚度在貼圖空間中正規化，其中 1 為影像的全寬。 |
| <b>厚度（px）</b> <i>浮標</i> | （當「厚度大小模式」設為像素時可用）繪製區塊的厚度以貼圖中像素的絕對數表示，其中 1 是完整像素。 |
| <b>啟用接頭</b> <i>布林值</i> | 利用圓盤填補沿樣條線繪製的各段間隙。 |
| <b>非平方修正</b> <i>布林值</i> | 調整點的位置與厚度，以在非正方形解析度下保留樣條形狀。<br>這也影響均勻分布。 |
| <b>顏色</b> |  |
| <b>背景強度</b> <i>浮標</i> | 該值與背景輸入影像相乘。 |
| <b>花鍵風格</b> <i>整數</i> | 樣條曲線的著色方法：<br>- 實心</i>：段段以均勻灰階值繪製;<br>- <i>漸層</i>：從黑到白的漸層從每串段開始到結束<br>;- <i>高度</i>：樣條的高度作為繪製段的<i>灰階值。 |
| <b>樣條色彩</b> <i>浮標</i> | 用於繪製這些段落的均勻灰階值。<br>當選擇非「實心」樣條時，該顏色會與已樣式色彩相乘。 |
| <b>隨機亮度</b> <i>浮標</i> | 對於樣條線中每一串未切割的段，對繪製該字串所用的灰階值施加指定範圍內的隨機偏移。 |
| <b>混合模式</b> <i>整數</i> | 混合背景顏色與重疊段沿樣條線繪製的方法：<br>- <i>最大</i>值：使用最亮值;<br>- <i>加</i>法：將數值相加。 |
| <b>隨機片段</b> |  |
| <b>隨機片段開始</b> <i>浮標</i> | 調整靠近樣條起點的線段被切割的機率。 |
| <b>隨機片段結束</b> <i>浮標</i> | 調整靠近樣條末端的線段被切割的機率。 |
| <b>隨機偏移</b> <i>浮標</i> | 設定每個切割段沿法線施加的最大位移量。<br>當 Start 和 End 都設為 0 時，這個參數沒有影響。 |
| <b>隨機偏移中心</b> <i>浮標</i> | 偏移隨機位移中心，該位移作用於每個切割段沿法線的法線。 |

## 範例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-render.resources/spline-render-02.jpg" alt="樣條渲染變體2之前">
      <br><i>之前</i>
    </td>
    <td>
      <img src="spline-render.resources/spline-render-03.jpg" alt="樣條渲染變體2-After">
      <br><i>之後</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-render.resources/spline-render-04.jpg" alt="樣條渲染變體1之前">
      <br><i>之前</i>
    </td>
    <td>
      <img src="spline-render.resources/spline-render-05.jpg" alt="樣條渲染變體1-After">
      <br><i>之後</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-render.resources/spline-render-04.jpg" alt="樣條渲染變體1之前">
      <br><i>之前</i>
    </td>
    <td>
      <img src="spline-render.resources/spline-render-06.jpg" alt="樣條渲染變體3">
      <br><i>之後</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![節點範例 1](spline-render.resources/spline-render-07.gif "節點範例 1")

</td>
</tr>
</table>
