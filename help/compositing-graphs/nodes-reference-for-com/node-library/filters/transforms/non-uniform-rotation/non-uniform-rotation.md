---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/non-uniform-rotation.html"
breadcrumb-title: ''
description: 使用非均勻旋轉節點來套用非均勻旋轉轉換，以創造螺旋和漩渦效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Non-Uniform Rotation
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 非均勻旋轉
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 1%

---


# 非均勻旋轉

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](non-uniform-rotation.resources/non-uniform-rotation-01.png){width="200px"}

</td>
<td style="border: 0;" valign="top">

![](non-uniform-rotation.resources/non-uniform-rotation-02.png){width="200px"}

</td>
</tr>
</table>

<b>收錄於：</b> 《濾波器>轉換》

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

**非均勻旋轉**&#x200B;節點會利用&#x200B;**旋轉映射**&#x200B;輸入來旋轉&#x200B;****&#x200B;輸入。

影像的數值代表&#x200B;**&#x200B;數圈。旋轉是圍繞樞 **軸位置** 值或 **樞軸位置地圖** 輸入所指定的位置進行。\
旋轉映射輸入中的&#x200B;**正值會產生&#x200B;*順*時針**&#x200B;旋轉。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>輸入</b> <i>灰階/彩色</i> | 輸入的灰階影像應該被旋轉。 |
| <b>旋轉地圖</b> <i>灰階</i> | 地圖用來控制旋轉的次數，也就是 *回合數*。 取樣值會與旋轉角度乘&#x200B;**數相乘**。負值則會逆 *時針* 旋轉。 |
| <b>旋轉樞軸位置圖</b> <i>顏色</i> | 用來指定旋轉 *樞軸*&#x200B;位置的影像。 **X/Y** 位置映射到&#x200B;**影像的 R/G** 通道。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>旋轉角度乘數</b> <i>浮標</i> | 調整旋轉地圖&#x200B;**輸入的**&#x200B;強度。 |
| <b>旋轉角偏移</b> <i>浮標</i> | 施加指定的額外旋轉量。 |
| <b>使用樞軸位置圖</b> <i>布林值</i> | 使用 *點陣圖輸入* 來指定旋轉樞軸的位置。 **X/Y** 位置映射到&#x200B;**位置映射**&#x200B;輸入的 **R/G** 通道。 |
| <b>PIvot 職位</b> <i>Float2</i> | 影像旋轉的樞軸位置。 |
| <b>背景色</b> <i>浮動/漂浮4</i> | 背景色顯示 *在影像範圍之外* ，以防鋪磚未設為 **H 和 V 平鋪**。 |
| <b>過濾模式</b> <i>整數</i> | 定義在像素&#x200B;*間插值時如何處理取樣結果*：<br><br>- *最近*：取樣值完全&#x200B;*相同*（更快）<br>- *雙線性*：對結果應用雙線性濾波器，使&#x200B;*畫面更*&#x200B;平滑 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="non-uniform-rotation.resources/non-uniform-rotation-03.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="non-uniform-rotation.resources/non-uniform-rotation-04.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="non-uniform-rotation.resources/non-uniform-rotation-05.png" />
        </td>
    </tr>
</table>
