---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/mask-to-paths.html"
breadcrumb-title: ''
description: 使用 Mask to Paths 節點將遮罩材質轉換成路徑資料，方便程序化路徑生成。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Mask to Paths
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 面具到路徑
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '1113'
ht-degree: 0%

---


# 面具到路徑

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![節點圖示](../../../../../../assets/mask-to-paths-icon.png "節點圖示")

<b>收錄於：</b> 樣條與路徑工具 > 路徑工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

將灰階輸入圖案 <b>遮罩</b> 轉換為編碼在輸出 <b>路徑</b>中的路徑段清單。

可控制生成路徑的起始位置及其在列表中的順序。

產生的路徑可以透過專用節點進一步處理——例如 [路徑二維轉換（Path 2D Transform](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/path-2d-transform/path-2d-transform.md)）、 [路徑扭曲（Paths Warp](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-warp/paths-warp.md) ）——或利用 [路徑到樣條節點（Path to Spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md) ）節點將形狀映射或散佈成樣條線。

</td>
</tr>
</table>

>[!NOTE]
>
> 編碼路徑的方法詳 [見路徑格式規範](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-format-spe/paths-format-specifications.md) 頁面。

## 輸入連接器

<b>面具</b> *灰階*\
輸入模式應該轉換成路徑清單。

## 輸出連接器

<b>預覽</b> *顏色*：一個在遮罩上方合成的預覽，幫助視覺化參數的效果。

<b>路徑</b> *顏色*\
以彩色影像編碼的路徑清單。 每條路徑描述一個編碼區段的清單。\
結果可用其他路徑處理節點處理，或送至 [路徑至樣條線](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md) 節點進一步以樣條處理。

## 參數

<b>光滑面具</b> *浮標*\
對輸入遮罩套用平滑。\
當輸入圖案邊緣非常銳利時，這通常會造成失真，這很有用。

<b>遮罩閾值</b> *浮點*&#x200B;灰階遮罩</b>值<b>，用來分離形狀的外部（遮&lt; Mask Threshold Value) and the inside (values >罩閾值值）。

<b>毀滅之路</b> *浮動式（Float* Implicitly）會隱式控制將產生的區段數量。\
大量減取會使圓形形狀呈現某種多邊形，而若不減算，則會產生幾乎一個像素的區段。\
合理的數量能更好地匹配直線和曲線的形狀，而不會造成太多直線的中間點。

<b>關閉開啟的路徑</b> *布林運算*：在開放路徑的起點與終點頂點之間建立一段線段。\
關閉這個功能可能會修正以意想不到的方式穿越你模式的不良路線，但路徑可能不再關閉。

<b>角落門檻</b> *浮標*\
每個編碼在路徑中的頂點都可以攜帶一個旗標，指示它是硬的（即轉角）還是平滑的。\
這個參數讓你可以根據相鄰線段之間的角度來標記多或少的角。\
*注意：*&#x200B;目前任何現有節點都不支援此「角落」旗標，但可在路徑頂點處理器[&#128279;](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-vertex-processor/paths-vertex-processor.md)節點中使用。你也可以用 [預覽路徑](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md) 節點來視覺化角落。

<b>路徑啟動模式</b> *整數*&#x200B;選擇每個生成路徑起始的頂點的方法。\
這在使用專用節點將產生 <b>的路徑轉換為樣條</b> 時會有重大影響，因為多個樣條線節點會使用樣條的起點與結束點。\
*- 最銳頂點：* 與其前後頂點形成最低角度的頂點\
*- 指定方向的極點：* 在特定方向上的最後一個頂點\
*- 最接近指定位置的頂點
* 距離指定位置最遠的頂點
* 自訂啟動函數：* 使用自訂函式選擇應該作為每條路徑起始的頂點

<b>創業方向</b> *浮點*&#x200B;描述選擇啟動頂點方向的角度。 對於每個路徑，選擇該方向的最後一個頂點。\
這個值是 *旋轉 X 向左向量所需的旋轉* 次數。 這表示 0 設定方向向量為 （-1， 0），而 0.25（90 度）則設定方向向量為 （0， 1）。\
*注意：* 當 <b>路徑啟動模式</b> 設定為「指定方向的極點頂點」時，此參數可用

<b>新創目標職位</b> *Float2*&#x200B;是影像中用來選擇啟動頂點的位置。\
對於每條路徑，根據所選 <b>的路徑啟動模式</b>，會選擇最接近或最遠於此位置的頂點。\
*注意：* 當 <b>路徑啟動模式</b> 設定為「最接近指定位置的頂點」或「最遠離指定位置的頂點」時，此參數可用

<b>啟動功能</b> *浮點*&#x200B;用來選擇啟動頂點的函式。 它會回傳一個浮動值。\
對每個頂點執行函數，並選擇函數回傳 *最高結果* 的頂點。\
可用變數：\
*-* 頂點.角度（Float）：**&#x200B;頂點作為角點候選的分數\
*-* vertex.pos（Float2）：**&#x200B;影像空間中的頂點位置\
*注意：* 當路徑啟動模式設定為「最接近指定位置的頂點」或「自訂啟動函數」時，此參數可用

<b>秩序模式</b> *整數*&#x200B;排序產生路徑的方法。\
路徑的邊界框&#x200B;*（Bbox）位置或大小*&#x200B;可作為排序路徑的標準。\
這在使用專用節點將生成 <b>路徑轉換為樣條</b> 時會有重大影響，因為多個樣條節點會使用樣條的順序。\
*- Legacy（快速）：* 此節點前版本所採用的方法，提供顯著更好的效能\
*- 依 Bbox 中心位置沿方向排列：* 路徑依其 Bbox 中心的位置排序，從頭到尾沿指定方向排列\
*- 依 Bbox Bbox 左上角位置排列：* 路徑依其 Bbox 左上角的位置排序，從頭到尾沿指定方向排列\
*- 依 Bbox 大小 - 由最大到最小：* 路徑依其 Bbox 大小排序，從最大到最小\
*- 依 Bbox 大小 - 從小到大：* 路徑依其 Bbox 大小排序，從最小到最大\
*- 自訂排序功能：* 使用自訂函式來排序路徑

<b>排序方向</b> *浮點*&#x200B;描述路徑從頭到尾排列的方向角度。\
這個數值是 *旋轉 X 向左方向向量所使用的旋轉* 次數。 這表示 0 設定方向向量為 （-1， 0），而 0.25（90 度）則設定方向向量為 （0， 1）。

<b>排序函數</b> *浮點*&#x200B;數 用來排序路徑的函數。 它會回傳一個浮動值。\
路徑依 *據函數值依序遞增* 排列。 換句話說，每個路徑的函數結果就是 *用來排序路徑的排序鍵* 。\
可用變數：
* bbox.center （Float2）：路徑 Bbox 中心的位置
* bbox.topleft（Float2）：路徑 Bbox 左上角的位置
* bbox.size （Float2）：路徑 Bbox 的大小（X：寬度，Y：高度）

## 範例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/MaskToPaths-Variant2-Before.jpg" alt="MaskToPaths-Variant2-Before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../../../assets/MaskToPaths-Variant2-After.jpg" alt="MaskToPaths-變體2-After">
      <br><i>之後</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/MaskToPaths-Variant1-Before.jpg" alt="MaskToPaths-變體1-之前">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../../../assets/MaskToPaths-Variant1-After.jpg" alt="MaskToPaths-變體1-之後">
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

![節點範例 2](../../../../../../assets/MaskToPaths-Demo2.gif "節點範例 2"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![節點範例 1](../../../../../../assets/MaskToPaths-Demo1.gif "節點範例 1"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![節點範例 3：啟動模式](../../../../../../assets/MaskToPaths-Demo3.gif "節點範例 3：啟動模式"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![節點範例 3：排序模式](../../../../../../assets/MaskToPaths-Demo4.gif "節點範例 3：排序模式"){zoomable="yes"}

</td>
</tr>
</table>
