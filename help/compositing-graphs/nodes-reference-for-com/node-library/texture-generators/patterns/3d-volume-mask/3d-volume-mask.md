---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/3d-volume-mask.html"
breadcrumb-title: ''
description: 使用 3D 體積遮罩節點，根據 3D 位置建立體積遮罩，以達到進階材質效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > 3D Volume Mask
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D 體積遮罩
user-guide-description: ''
user-guide-title: ''
source-git-commit: db5ad9a6ad1d03fedcc3d760cc8886501d16b87f
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 1%

---


# 3D 體積遮罩

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-volume-mask.resources/3dvolumemask.png){width="256px"}

<b>收錄於：</b> Generator > Pattern

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

**3D Volume Mask** 節點會根據 Position **輸入貼圖產生一個基本形狀&#x200B;***的表示*。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>職位</b> <i>顏色</i> | 描述該原件所表示的三維空間座標&#x200B;*的映射*。<br><br>**X/Y/Z** 座標分別映射到 **R/G/B** 通道。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>形狀</b> <i>整數</i> | 應表示的基本形狀：<br><br>立 *方*<br>&#x200B;體 - *圓柱*<br>&#x200B;體 - *球體* |
| <b>規模</b> <i>浮標</i> | 定義&#x200B;*了原件的全域*&#x200B;尺度，並均勻地應用&#x200B;**&#x200B;於所有軸上。 |
| <b>規模</b> <i>Float3</i> | 定義形狀在每個軸上的大小。 |
| <b>位置輸入</b> <i>整數</i> | 透過 Position 輸入表示空間&#x200B;*的方法：<br><br>-* UV 位置&#x200B;*：使用* UV 貼圖&#x200B;*。**&#x200B;*** X/Y（U/V）座標分別映射到R/G通道。 Z軸假設為 *正交的前向* 向量。<br>- *世界空間位置*：使用 *位置映射* 將原件映射到三維空間中。 X/Y/Z 座標分別映射到 R/G/B 通道。 |
| <b>位置 UV</b> <i>Float2</i> | 圖元在 UV 空間中的位置。<br><br>*注意：此參數僅在 Position Input **參數設為*UV Position *時可用***。 |
| <b>職位</b> <i>Float3</i> | 圖元在世界空間中的位置。<br><br>*注意：此參數僅在 Position Input **參數設為*世界空間位置&#x200B;*時可用***。 |
| <b>旋轉</b> <i>Float3</i> | 定義了圖形在世界空間中的旋轉。 |
| <b>羽寬</b> <i>浮標</i> | 調整從基元表面向內漸變的漸變&#x200B;*寬*&#x200B;度。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-volume-mask.resources/3dvolumemask-variant.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-volume-mask.resources/3dvolumemask-variant2.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-volume-mask.resources/3dvolumemask-variant3.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-volume-mask.resources/3dvolumemask-variant4.jpg" />
        </td>
    </tr>
</table>
