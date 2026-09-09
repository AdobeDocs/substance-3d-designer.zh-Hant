---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/3d-texture-sdf.html"
breadcrumb-title: ''
description: 使用 3D Texture SDF 節點，從 3D 資料產生有符號距離場紋理，以創造平滑的形狀與效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > 3D Texture SDF
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D 貼圖 SDF
user-guide-description: ''
user-guide-title: ''
source-git-commit: 132a27ad47b0272a877b913eaa7957ccf8b549fd
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 2%

---


# 3D 貼圖 SDF

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-texture-sdf.resources/3dtexturesdf.png){width="200px"}

<b>收錄於：</b> 濾波>效應

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

**3D Texture SDF** 節點會&#x200B;*從&#x200B;**輸入**&#x200B;的* 3D 材質&#x200B;*遮罩（代表形狀*&#x200B;體積&#x200B;*的切片）產生形狀的有符號距離場*。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>遮罩輸入</b> <i>灰階</i> | <i>3D 材質</i>遮罩代表形狀<i>體積</i>的切片。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>門檻</b> <i>浮標</i> | 當形狀體積以漸變梯度描述<i>時，會</i>設定形狀表面被<i>偵測到<i></i>的梯度</i>值。 |
| <b>產出</b> <i>整數</i> | 應輸出的距離場類型：<br>- 距離場</i>：輸出描述形狀外</i>距離的距離<i>場。<br>- <i>有符號距離場</i>：輸出描述形狀外</i>（正）與<i>內部</i>（負）距離<i><i>的距離場。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-texture-sdf.resources/3dtexturesdf-variant.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-sdf.resources/3dtexturesdf-variant2.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-sdf.resources/3dtexturesdf-node.png" />
        </td>
    </tr>
</table>
