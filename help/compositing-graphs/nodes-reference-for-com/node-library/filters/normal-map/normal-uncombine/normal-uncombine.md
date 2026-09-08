---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-uncombine.html"
breadcrumb-title: ''
description: 使用法線解合節點將合併的法線貼圖資料分離成獨立的 X、Y 和 Z 元件。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal map > Normal uncombine
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 普通未合併
user-guide-description: ''
user-guide-title: ''
source-git-commit: 03373417b3d82a278c159aa83baf282b67c9cbe3
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 1%

---


# 普通未合併

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![正常解合圖示](../../../../../../assets/NormalUncombine.png "正常解合圖示"){width="200px"}

<b>收錄於：</b> 法線貼圖>濾波器

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

從法線貼圖中移除高度貼圖所描述的表面細節。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>綜合標準</b> <i>色彩 原色</i> | 應該移除細節的法線貼圖。 |
| <b>高度</b> <i>灰階</i> | 代表表面細節的高度圖，應該從合併法線貼圖中移除。 |

<a name="outputs"></a>

## 輸出

|  |  |
|:---|:---|
| <b>未合併的正常</b> <i>顏色</i> | 法線貼圖中輸入高度圖描述的表面細節被移除。 |
| <b>推測強度</b> <i>浮標</i> | 一個強度估計值，應該設定在 [連接到輸入高度貼圖的法線](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md) 節點上，以匹配輸入法線貼圖的強度。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>標準格式</b> *整數* | 輸入法線貼圖的格式。 這有效地將綠色通道反轉。<ul data-preserve-html="true"> <li data-preserve-html="true"><b>DirectX：</b> Y 軸指向上方</li> <li data-preserve-html="true"><b>OpenGL：</b> Y 軸指向下方</li> </ul> |

## 範例

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/normal_uncombine_example_3_before.jpg" alt="normal_uncombine_example_3_before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../../../assets/normal_uncombine_example_3_after.jpg" alt="normal_uncombine_example_3_after">
      <br><i>之後</i>
    </td>
  </tr>
</table>

![普通解合：範例2](../../../../../../assets/normal_uncombine_example_4.png "普通解合：範例2"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/normal_uncombine_example_1_before.jpg" alt="normal_uncombine_example_1_before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../../../assets/normal_uncombine_example_1_after.jpg" alt="normal_uncombine_example_1_after">
      <br><i>之後</i>
    </td>
  </tr>
</table>

![普通解合：範例4](../../../../../../assets/normal_uncombine_example_6.png "正常未合併：範例4"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/normal_uncombine_example_2_before.jpg" alt="normal_uncombine_example_2_before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../../../assets/normal_uncombine_example_2_after.jpg" alt="normal_uncombine_example_2_after">
      <br><i>之後</i>
    </td>
  </tr>
</table>

![普通解體：範例6](../../../../../../assets/normal_uncombine_example_5.png "正常解體：範例6"){zoomable="yes"}
