---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/id-to-mask.html"
breadcrumb-title: ''
description: 使用 ID To Mask Grayscale 節點，將 ID 映射值轉換成灰階遮罩以便選擇材質。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > ID To Mask Grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ID 以掩蓋灰階
user-guide-description: ''
user-guide-title: ''
source-git-commit: 7f15827b198bfbc133601581dc54ed894e98d89d
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 1%

---


# ID 以掩蓋灰階

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![ID 以遮罩灰階圖示](id-to-mask.resources/IDToMask.png "ID 以遮罩灰階圖示 ID 以遮罩灰階圖示"){width="200px"}

<b>收錄於：</b> 篩選>調整

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

它會從一個 ID 映射中產生遮罩，選取像素值的像素為白色。

ID 映射是一種影像，其中屬於整體（例如形狀）的像素都擁有相同的唯一識別值。 此時，值為整數。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>身分證</b> <i>灰階</i> 初級 | 應從中擷取遮罩的輸入 ID 映射。 |

<a name="outputs"></a>

## 輸出

|  |  |
|:---|:---|
| <b>產出</b> <i>灰階</i> | 從輸入 ID 映射中提取的二元遮罩。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>選擇模式</b> *整數* | 選擇遮罩中應為白色的 ID 映射像素值的方法：<ul data-preserve-html="true"> <li data-preserve-html="true"><b>單人：</b> 選擇單一像素值</li> <li data-preserve-html="true"><b>範圍：</b> 選擇一個像素值範圍</li> </ul> |
| <b>ID 整數</b> *當「選擇模式」設為「單人」時，整數*   *可用* | ID 映射中的像素值，在輸出遮罩中應該是白色的。 |
| <b>識別區間</b> *當「選擇模式」設為「範圍」時，整數*    *2 可用* | ID 映射中從開始到結束的像素值範圍，在輸出遮罩中應該是白色的。 |

## 範例

<table>
  <tr>
    <td>
      <img src="id-to-mask.resources/id_to_mask_grayscale_example_1_before.jpg" alt="id_to_mask_grayscale_example_1_before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="id-to-mask.resources/id_to_mask_grayscale_example_1_after.jpg" alt="id_to_mask_grayscale_example_1_after">
      <br><i>之後</i>
    </td>
  </tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![ID 對掩碼：範例 2](id-to-mask.resources/id_to_mask_example_2.gif "ID 對掩碼：範例 2"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![ID 對遮罩：範例 3](id-to-mask.resources/id_to_mask_example_3.png "ID 對遮罩：範例 3"){zoomable="yes"}

</td>
</tr>
</table>
