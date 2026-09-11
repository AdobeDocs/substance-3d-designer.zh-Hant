---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape-extrude.html"
breadcrumb-title: ''
description: 使用 Shape Extrude 節點來擠出形狀，並在 Substance 3D Designer 的貼圖中創造類似 3D 的深度效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Shape Extrude
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 形狀擠出
user-guide-description: ''
user-guide-title: ''
source-git-commit: dbfe5b7ce453a6178d8d970698d3a5f8225151b4
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 5%

---


# 形狀擠出

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](shape-extrude.resources/shape-extrude.png){width="128px"}

<b>收錄於：</b> 紋理產生器>圖案

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

一個進階節點，允許將 2D 二元「形狀」輸入渲染成 3D 旋轉高度圖。 這類似於 3D 套件中的擠出，沿著軸線擠出一個形狀，形成體積。 結合輪廓漸層遮罩，也能製作 Revolution/車床型的身體。 對於製作複雜的高程圖人工形狀非常有用。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>擠出形狀輸入</b> <i>灰階輸入</i> | 如果 Extrude Shape 設為自訂，你就在這裡插入你自己的（最好是）二進位形狀遮罩。 |
| <b>剖面梯度</b> <i>灰階輸入</i> | 若 Profile Type 設為垂直梯度，可用來定義軸向形狀的縮放，適用於旋轉物體。 |
| <b>側面面具</b> <i>灰階輸入</i> | 遮罩槽用於隱藏或顯示沿軸線的擠壓形狀。 可用來打破形狀沿軸的連續性。 僅以二進位解讀：灰階賣權值會四捨五入為 0 或 1。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>擠出高度</b> <i>0.0 - 1.0</i> | 從中心向上擠出形狀。 |
| <b>擠出深度</b> <i>0.0 - 1.0</i> | 等於從中心向下擠出形狀。 |
| <b>擠出形狀</b> <i>立方體、圓柱體、自訂輸入</i> | 可以使用內建形狀，或是外部輸入自訂形狀。 |
| <b>擠出形狀尺寸</b> <i>0.0 - 1.0</i> | 僅用於內建立方體與圓柱體，決定基準形狀大小，且可調整非均勻縮放。 |
| <b>規模</b> <i>0.0 - 1.0</i> | 設定效果的全域尺度。 內建形狀時，這是統一的基礎形狀縮放，不影響高度或深度。<br><br>自訂輸入則能統一縮放整個最終結果。 |
| <b>型態類型</b> <i>直線、垂直漸變、遮罩</i> | 主控點用來判斷影響行為，並使用可選的額外輸入映射。<br><br>直線是標準的擠出行為，垂直漸層允許沿整個軸線自訂縮放值，遮罩則允許依遮罩隱藏沿軸的區域。 |
| <b>斜面高度</b> <i>0.0 - 1.0</i> | 設定斜角沿著擠出軸的長度。 |
| <b>斜面強度</b> <i>0.0 - 1.0</i> | 設定斜角從原始形狀回縮的程度。 |
| <b>斜面曲線</b> <i>-1.0 - 1.0</i> | 設定斜面效應的凸或凹曲線。 值為 0 表示直線，沒有曲線。 |
| <b>鏡面斜角</b> <i>錯誤/真實</i> | 切換到形狀的上下都加斜角。 |
| <b>降級多重機</b> <i>0 - 2</i> | 內建簡易降頻控制。 可用來快速加入抗鋸齒;同時也要提升節點解析度。 |
| <b>職位</b> | 旋轉的主要控制會產生三維空間。 在 2D 視圖中與 interavtice Gizmo 對應。 |
| <b>輸出範圍</b> <i>[0, 1], [-1, 1]</i> | 設定輸出最小值和最大值。 若範圍設為 [-1,1]，負值則以黑色呈現。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="shape-extrude.resources/shape-extrude-1.png" />
        </td>
    </tr>
</table>
