---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/extend-shape.html"
breadcrumb-title: ''
description: 使用 Extend Shape 節點將形狀延伸到邊界之外，以建立擴展遮罩和圖案效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Extend Shape
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 延伸形狀
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 0%

---


# 延伸形狀

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](extend-shape.resources/extend-shape-01.png){width="200px"}

</td>
<td style="border: 0;" valign="top">

![](extend-shape.resources/extend-shape-02.png){width="200px"}

</td>
</tr>
</table>

<b>收錄於：</b> 濾鏡>效應

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

<b>延伸形狀</b>節點會將輸入</b>的一段<i></i><b>延伸到固定方向和距離。

<b>Show 助手</b>參數讓你能視覺化延伸段和延伸方向。

</td>
</tr>
</table>

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>模式</b> <i>整數</i> | 定義<i>用於應用延伸的參數</i>：<br><br>- <i>雙向</i>：由延伸位置</b>與<b>伸展角</b>指定的<b>輸入</b>截面<b>向相反方向</i><br>延伸<b>至延伸距離<i></b>。- <i>單向</i>：由<b>延伸位置</b>與<b>延伸角</b>指定的輸入</b>截面在<b></b> <b><i>單向</i><br><i>-起始/結束位置</i>：延伸<i>向量</i>由起始位置</b>與<b>結束位置</b>定義<b>。輸入在起始位置</b>的<b>垂直</i>截面會在此向量</i>上延伸<i>至<b>終點位置<b></b> <i></b> |
| <b>延伸距離</b> <i>浮標</i> | 延伸位置與<b>伸展角</b>所指定的<b></b>截面長度。距離以影像跨度的比例</i>表示<i>。 |
| <b>延伸職位</b> <i>浮標</i> | 在圖中應延伸的截面位置。 該值以 <i>中心偏</i>移表示。 |
| <b>伸展角</b> <i>浮標</i> | 應延伸的截面角度，考慮起點為 <i>垂直截面</i>。 |
| <b>起始位置</b> <i>Float2</i> | 延伸向量</i>的<i>起始位置。 |
| <b>結束位置</b> <i>Float2</i> | 延伸向量</i>的<i>終點位置。 |
| <b>開始亮度偏移</b> <i>浮標</i> | 對影像 <i>中延伸區塊前</i> 的區域施加亮度偏移。 此亮度偏移會 <i>沿該截面</i> 插值至影像後面區域的亮度。<br><br><i>注意</i>：此參數僅在 <b>該節點的灰階</b> 版本中提供。 |
| <b>終點亮度偏移</b> <i>浮標</i> | 在延伸區段後</i>的影像<i>區域套用亮度偏移。此亮度偏移會 <i>沿該區</i> 段插值至影像前方區域的亮度。<br><br><i>注意</i>：此參數僅在 <b>灰階</b> 版本的節點中提供。 |
| <b>Lum。 偏移忽略黑色像素</b> <i>布林值</i> | 當設定為 <i>True（真</i>）時，兩者中指定的 <i>亮度偏移量</i> <b>開始亮度偏移</b> 與 <b>結束亮度偏移</b> 僅套用於 <i>非黑色</i> 像素——即值高於 0 的像素。<br><br><i>注意</i>：此參數僅在 <b>灰階</b> 版本的節點中提供。 |
| <b>過濾模式</b> <i>整數</i> | 定義在像素</i>間插值時如何處理取樣結果<i>：<br><br>- <i>最近</i>：取樣值完全<i>相同</i>（更快）<br>- <i>雙線性</i>：對結果應用雙線性濾波器，使<i>畫面更</i>平滑 |
| <b>節目助手</b> <i>布林值</i> | 將延伸部分想像<i>成一個覆蓋層，並用箭頭標示<i>延伸方向</i>。</i> |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="extend-shape.resources/extend-shape-03.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="extend-shape.resources/extend-shape-04.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="extend-shape.resources/extend-shape-05.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="extend-shape.resources/extend-shape-06.png" />
        </td>
    </tr>
</table>
