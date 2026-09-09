---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/cross-section.html"
breadcrumb-title: ''
description: 使用 Cross Section 節點根據高度貼圖建立橫截面遮罩，用於切割和切割效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Cross Section
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 橫斷面
user-guide-description: ''
user-guide-title: ''
source-git-commit: 07f136ebd89fbe737b6c042f1275bd348b2be514
workflow-type: tm+mt
source-wordcount: '494'
ht-degree: 0%

---


# 橫斷面

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![「橫切面」節點圖示](cross-section.resources/cross-section-2.png "「橫截面」節點圖示"){width="200px"}

<b>收錄於：</b> 濾鏡>效應

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

繪製輸入的橫斷面剖面圖。 可以調整垂直或水平切片，並具備繪圖風格、圖形偏移與縮放控制。

</td>
</tr>
</table>

此節點特別適合除錯和分析高度圖。 讓你擁有像素級的側面視角，無需複雜節點或冗長且不精確的 3D 視圖設定。

或者，它也可以用來創造難以達成的二維形狀和輪廓。 結合 [曲線節點](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/curve/curve.md)，可以直接視覺化套用到線性梯度上的曲線剖面。

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>橫截面座標</b> *浮標* | 設定在取樣切片的座標。 座標可以是X或Y，視截面軸而定。 |
| <b>截面軸</b> *整數* | 設定切片是垂直還是水平。 |
| <b>節目助手</b> *布林值* | 啟用疊加圖，顯示該區段在輸入影像上的位置。 |
| <b>輔助設定</b> |  |
| <b>輔助量表</b> *浮標* | 疊加圖的大小以倍數表示，其中 1.0 是整個影像。 |
| <b>助手職位</b> *Float2* | 輸出影像中疊加層的（X， Y）位置，其中（0.0， 0.0）為左上角，（1.0， 1.0）為右下角。 |
| <b>身高比例</b> *浮標* | 會縮小整個圖表的比例。 對 HDR 觀看很有用。 |
| <b>高度偏移</b> *浮標* | 整個圖表上下移動。 對 HDR 觀看很有用。 |
| <b>繪畫風格</b> *整數* | 在實心填充和線條繪製之間切換。 |
| <b>反轉梯度</b> *布林值* | 如果繪圖風格設定為 *漸層* 或 *漸層鏡像*，可以反轉該漸層而不影響背景。<br><br>*注意：* 僅在「繪圖風格」設為「漸層」或「漸層鏡像」時使用。 |
| <b>光滑/多邊形</b> *布林值* | 形狀可切換於完美平滑輪廓或鋸齒狀多邊形間。<br><br>*注意：* 僅在「繪圖風格」設為「實心」、「漸層」或「漸變鏡像」時使用。 |
| <b>分段金額</b> *整數* | 設定在多邊形風格或線條風格下繪製所需的線段數量。<br><br>*注意：* 僅在「平滑/多邊形」設為「多邊形」或「繪圖風格」設為「線條」時可用。 |
| <b>線條粗細</b> *浮標* | 設定線條的粗細。<br><br>*注意：* 只有當「繪圖風格」設為「線條」時才可用。 |
| <b>線條風格</b> *整數* | 讓你可以選擇線條的顏色和衰減。<br><br>*注意：* 只有當「繪圖風格」設為「線條」時才可用。 |
| <b>線條平滑度</b> *浮標* | 設定線條的漸變衰減。<br><br>*注意：* 只有當「繪圖風格」設為「線條」時才可用。 |
| <b>顏色</b> *浮標* | 線條或形狀的灰階色彩。<br><br>*注意：* 僅在「繪圖樣式」設為「實線」或「線條」且「線條樣式」設為「平滑」或「實線」時使用。 |
| <b>背景色</b> *浮標* | 背景的灰階色彩。<br><br>*注意：* 當「繪圖樣式」設為「線條」且「線條樣式」設為「線段 ID」或「沿線漸層」時，無法使用。 |

## 範例

![截面：範例1](cross-section.resources/cross-section-example-01.gif "截面：範例1")

![截面：範例2](cross-section.resources/cross-section-example-02.gif "截面：範例2")

![截面：範例3](cross-section.resources/cross-section-example-03.png "截面：範例3")

![截面：範例4](cross-section.resources/cross-section-example-04.png "截面：範例4")
