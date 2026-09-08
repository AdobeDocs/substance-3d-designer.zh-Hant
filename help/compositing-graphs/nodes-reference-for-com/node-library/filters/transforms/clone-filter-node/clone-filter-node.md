---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/clone-filter-node.html"
breadcrumb-title: ''
description: 使用 Clone 濾鏡節點來複製和偏移貼圖區域，創造無縫的圖案和平鋪效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Clone (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 克隆（濾波節點）
user-guide-description: ''
user-guide-title: ''
source-git-commit: 03373417b3d82a278c159aa83baf282b67c9cbe3
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 3%

---


# 克隆（濾波節點）

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/clone-4.png)

<b>收錄於：</b> 《濾波器>轉換》

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

複製一次影像到指定位置。 可以作為粗糙的「複製印章」工具使用。

需要謹慎才能達到預期效果：

* 理想狀況下，輸入影像會有 alpha 通道（像是貼紙），因為混合就是直接複製。
* 遮罩預設是黑色，所以要看到結果，至少需要輸入一個均勻的白色灰階值。
* 偏移量很容易從畫面外穿插，所以用小數值。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>資料來源</b> <i>色彩輸入</i> | 映像到複製人。 重要提示：理想狀況下，圖片應該有 alpha 通道！ |
| <b>面具</b> <i>灰階輸入</i> | 遮罩槽用於遮蔽節點的效果。 預設是黑色！ |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>偏移</b> <i>-</i> | 移動或翻譯結果。 正是左和上，負是右和下。 用小數值，1.0 以上的數字會移到畫面外！ |
| <b>模糊面具</b> <i>0.0 - 10.0</i> | 用模糊濾鏡遮罩，柔化邊緣。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/clone-example.png" />
        </td>
    </tr>
</table>
