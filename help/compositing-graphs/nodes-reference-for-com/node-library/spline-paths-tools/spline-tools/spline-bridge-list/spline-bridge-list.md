---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-bridge-list.html"
breadcrumb-title: ''
description: 使用 Spline Bridge List 節點來橋接列表中多個樣條紋的紋理，以處理複雜圖案。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Bridge (List)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 花鍵橋（列表）
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '1001'
ht-degree: 0%

---


# 花鍵橋（列表）

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![節點圖示](spline-bridge-list.resources/spline-bridge-list-01.png "節點圖示")

<b>收錄於：</b> 樣條與路徑工具 > 樣條鍵工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

產生樣條曲線，遍歷輸入列表中所有樣條曲線，沿著這些樣條曲線。

產生的樣條可以是線性（直線）或二次貝茲曲線（曲面）。

</td>
</tr>
</table>

>[!TIP]
>
> 產生的樣條從列表中第一個樣條線到最後一個樣條線，並嚴格依照列表中這些樣條線的順序遍歷中間樣條線。
> 
> 因此，你應該事先注意樣條的附加順序。

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>預覽</b> <i>灰階</i> | 輸入樣條線預覽為灰階影像。 |
| <b>樣條座標</b> <i>顏色</i> | 彩色影像RGBA通道中編碼的輸入樣條點座標：<br><b>R</b> - X 位置<br><b>G</b> - Y 位置<br><b>B</b> - 高度<br><b>A</b> - 填充資料：<br>符號：樣條線為閉合（負）或開（正）;<br>- 絕對值：厚度 + 1。 |
| <b>樣條資料</b> <i>顏色</i> | 彩色影像的 RGBA 通道中編碼的輸入樣條線額外資料。<br><b>R</b> - 切線 x<br><b>G</b> - 切線 y<br><b>B</b> - 未使用<br><b>A</b> - 未使用 |
| <b>樣條量</b> <i>整數</i> | 輸入樣條的數量。 |

<a name="outputs"></a>

## 輸出

|  |  |
|:---|:---|
| <b>預覽</b> <i>灰階</i> | 輸出時條線預覽為灰階影像。 |
| <b>樣條座標</b> <i>顏色</i> | 輸出樣條點的座標編碼在彩色影像的 RGBA 通道中。<br><b>R</b> - X 位置<br><b>G</b> - Y 位置<br><b>B</b> - 高度<br><b>A</b> - 打包資料：<br>符號：樣條線為閉合（負）或開（正）;<br>- 絕對值：厚度 + 1。 |
| <b>樣條資料</b> <i>顏色</i> | 彩色影像RGBA通道中編碼的輸出樣條額外資料。<br><b>R</b> - 切線 x<br><b>G</b> - 切線 y<br><b>B</b> - 未使用的<br><b>A</b> - 未使用的 |
| <b>樣條量</b> <i>整數</i> | 輸出花鍵的數量。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>橋式樣條量</b> <i>整數</i> | 輸入樣條上產生的樣條數。 |
| <b>橋式樣鍵類型</b> <i>整數</i> | 所產生的樣條類型：<br><br>- 線性樣條：連接從起點到結束的直軌軌跡的中間樣條的銳利樣條;<br>- 二次貝茲曲線：一種曲線樣條，連接從開始到結束<br><br>的中間樣條，軌跡平滑。注意：計算二次貝塞爾樣條至少需三個輸入樣條。 |
| <b>輸入樣條為封閉式</b> <i>布林值</i> | 控制輸入樣條曲線的第一點與最後兩點是否應作為單一點處理。 這樣可以避免重複第一個和最後一個穿越樣條。 |
| <b>翻轉方向</b> <i>布林值</i> | 會反轉花鍵的方向。 |
| <b>閉橋樣鍵</b> <i>布林值</i> | 將遍歷樣條線延伸回輸入列表中的第一個樣條線。 |
| <b>第一橋式樣鍵偏移量</b> <i>Float2</i> | 在所有穿越的樣條起始處套用偏移量。 該值為輸入樣條的正規化長度。<br>產生的樣條與遍歷樣條的起點或終點相交的樣條會留在那裡。 |
| <b>最後橋式樣條偏移量</b> <i>Float2</i> | 在所有穿越樣條的末端套用偏移量。 該值為輸入樣條的正規化長度。<br>產生的樣條與遍歷樣條的起點或終點相交的樣條會留在那裡。 |
| <b>隨機偏移範圍</b> <i>整數</i> | 隨機偏移量施加於樣條曲線的最大距離。<br><br>- <i>父樣條</i> ：使用母樣條的全長。 可能導致重疊。<br>- <i>間隔：</i> 使用橋式樣鍵之間的間隔。 這樣可以減少重疊。 隨著橋樑樣鍵數量增加，這個距離會逐漸減少。 |
| <b>開始隨機偏移</b> <i>浮標</i> | 一個乘數，用於施加在橋式樣條起始位置的隨機偏移，最大距離由 <b>隨機偏移範圍</b> 參數決定。 |
| <b>結束隨機偏移</b> <i>浮標</i> | 一個隨機偏移的乘數，適用於橋式樣條的末端位置，最大距離由 <b>隨機偏移範圍</b> 參數決定。 |
| <b>全域隨機偏移量</b> <i>浮標</i> | 乘數是對&#x200B;*橋式樣條起始與終點位置施加**相同隨機*&#x200B;偏移量的倍數，最大距離由<b>隨機偏移範圍</b>參數決定。 |
| <b>均勻分布</b> <i>布林值</i> | 當為真時，產生的樣條曲線點從開始到結束均勻分布。 |
| <b>厚度</b> |  |
| <b>厚度模式</b> <i>整數</i> | 取得橋式樣條厚度值的方法。<br><br>- <i>繼承自父樣條：</i>使用<br>橋式樣條起始與結束位置的父樣條厚度- <i>覆寫：</i>使用您在厚度</b>參數中<b>指定的任意值 |
| <b>厚度</b> <i>浮標</i> | 絕對厚度值應用於橋式樣鍵。 |
| <b>厚度隨機</b> <i>浮標</i> | 橋式樣條厚度的隨機乘法，該乘數的初始厚度由厚度</b>模式參數指定<b>。 |
| <b>高度</b> |  |
| <b>高度模式</b> <i>整數</i> | 取得橋式樣條高度值的方法。<br><br>- <i>繼承自父樣條：</i>使用<br>橋式樣條起始與結束位置的父樣條高度- <i>覆寫：</i>使用您在高度</b>參數中<b>指定的任意值 |
| <b>身高偏移</b> <i>浮標</i> | 在從父樣條線繼承到該高度之前，對橋接樣條線施加的偏移量。 |
| <b>高度</b> <i>浮標</i> | 絕對高度值應用於橋式樣鍵。 |
| <b>高度隨機</b> <i>浮標</i> | 對橋式樣條線高度的隨機調整，調整取決於所選 <b>的高度模式</b> 參數：<br><br>- <i>繼承父樣條曲線：</i> 該值為繼承高度的乘數。<br>- <i>覆寫：</i> 此值是高度的偏移量。 |
| <b>非平方修正</b> <i>布林值</i> | 調整點的位置與厚度，以在非正方形解析度下保留樣條形狀。 這也影響均勻分布。 |
| <b>預覽</b> |  |
| <b>節目指導助理</b> <i>布林值</i> | 在預覽輸出中，樣條曲線起始顯示一個點，末尾顯示箭頭。 |
| <b>顯示厚度包絡</b> <i>布林值</i> | 在樣鍵厚度邊緣顯示額外線條。 |
| <b>分段數量</b> <i>整數</i> | 調整預覽輸出中繪製樣條視覺化所需的段數。 數值越高，線條越平滑。 |
| <b>厚度（px）</b> <i>浮標</i> | 調整預覽輸出中樣條曲線的厚度（像素數）。 |
| <b>背景預覽強度</b> <i>浮標</i> | 預覽視覺化的強度。 |

## 範例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-bridge-list.resources/spline-bridge-list-02.jpg" alt="花鍵橋List_Variant1_Before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="spline-bridge-list.resources/spline-bridge-list-03.jpg" alt="樣條橋-List_Variant1_After">
      <br><i>之後</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![節點範例 2](spline-bridge-list.resources/spline-bridge-list-04.gif "節點範例 2")

</td>
</tr>
</table>

![圖](spline-bridge-list.resources/spline-bridge-list-05.jpg "中的節點圖中的節點")
