---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/uv-mapper-grayscale.html"
breadcrumb-title: ''
description: 使用 UV Mapper 灰階節點將灰階貼圖沿樣條線映射，方便程序化貼圖生成。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > UV Mapper Grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: UV 映射器灰階
user-guide-description: ''
user-guide-title: ''
source-git-commit: e4c44720897b98db608bc9feabb860d4b1baf332
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 2%

---


# UV 映射器灰階

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![節點圖示](../../../../../../assets/uv-mapper-grayscale-icon.png "節點圖示")

<b>收錄於：</b> 樣條與路徑工具 > 樣條鍵工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

利用 UV 輸入提供的座標映射輸入的灰階影像。

</td>
</tr>
</table>

>[!NOTE]
>
> 另 [見 UV 映射器色彩](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/uv-mapper-color/uv-mapper-color.md)。

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>紫外線</b> <i>顏色</i> | 影像座標編碼於彩色影像的紅色（U）與綠色（V）通道中。 |
| <b>輸入</b> <i>顏色</i> | 灰階影像應該映射到 UV 輸入中提供的座標。 |

<a name="outputs"></a>

## 輸出

|  |  |
|:---|:---|
| <b>產出</b> <i>顏色</i> | 這是將輸入影像利用輸入 UV 座標映射成灰階影像的結果。 |

## 範例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/UVMapper-Variant1-Before.jpg" alt="UVMapper-變體1-之前">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../../../assets/UVMapperGrayscale-Variant1-After.jpg" alt="UVMapperGrayscale-變體1-之後">
      <br><i>之後</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/UVMapper-Variant2-Before.jpg" alt="UVMapper-變體2-之前">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../../../assets/UVMapper-Variant2-After.jpg" alt="UVMapper-變體2-之後">
      <br><i>之後</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

![節點範例 1](../../../../../../assets/UVMapper-Graph.jpg "節點範例 1")
