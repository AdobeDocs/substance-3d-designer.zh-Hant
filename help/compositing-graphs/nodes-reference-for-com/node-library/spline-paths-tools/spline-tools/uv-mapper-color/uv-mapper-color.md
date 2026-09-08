---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/uv-mapper-color.html"
breadcrumb-title: ''
description: 使用 UV Mapper Color 節點將顏色貼圖沿樣條線映射，方便程序化貼圖生成。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > UV Mapper Color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: UV 映射器色彩
user-guide-description: ''
user-guide-title: ''
source-git-commit: e4c44720897b98db608bc9feabb860d4b1baf332
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 2%

---


# UV 映射器色彩

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![節點圖示](../../../../../../assets/uv-mapper-color-icon.png "節點圖示")

<b>收錄於：</b> 樣條與路徑工具 > 樣條鍵工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

利用 UV 輸入中提供的座標映射輸入的彩色影像。

</td>
</tr>
</table>

>[!NOTE]
>
> 另 [見 UV Mapper 灰階](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/uv-mapper-grayscale/uv-mapper-grayscale.md)。

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>紫外線</b> <i>顏色</i> | 影像座標編碼於彩色影像的紅色（U）與綠色（V）通道中。 |
| <b>輸入</b> <i>顏色</i> | 彩色影像應映射到 UV 輸入所提供的座標。 |

<a name="outputs"></a>

## 輸出

|  |  |
|:---|:---|
| <b>產出</b> <i>顏色</i> | 這是利用輸入 UV 座標將輸入影像映射為彩色影像的結果。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>背景色</b> <i>Float4</i> | 輸出影像的背景色。<br>背景可見於影像中未定義 UV 的區域（例如，值為 （0， 0， 0， 0））。 |

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
      <img src="../../../../../../assets/UVMapper-Variant1-After.jpg" alt="UVMapper-變體1-之後">
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
      <img src="../../../../../../assets/UVMapperColor-Variant2-After.jpg" alt="UVMapperColor-變體2-之後">
      <br><i>之後</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

![圖](../../../../../../assets/UVMapperColor-Graph.jpg "中的節點圖中的節點")
