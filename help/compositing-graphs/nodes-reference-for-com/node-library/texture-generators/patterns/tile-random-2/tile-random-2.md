---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/tile-random-2.html"
breadcrumb-title: ''
description: 使用 Tile Random 2 節點，在 Substance 3D Designer 中建立帶有進階變化控制的隨機圖塊圖案。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Tile Random 2
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 隨機方塊2
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '1308'
ht-degree: 0%

---


# 隨機方塊2

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](tile-random-2.resources/tilerandom2.jpg){width="200px"}

<b>收錄於：</b> 紋理產生器>圖案

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

**Tile Random 2** 節點會產生相鄰的圖塊，尺寸和高寬比都隨機。

網格可以透過隨機 *傾斜* 形狀的側邊來打散角度來調整。

形狀可透過縮放、斜角&#x200B;**、圓角&#x200B;*及*&#x200B;分列旋轉&#x200B;*等選項*&#x200B;進行調整。 &#x200B;**

這些調整可由 *輸入映射*&#x200B;控制。

專用輸出可以讓你將形狀的 **UV** 輸入到 **Flood Fill（...）** 節點用於施加額外變化。

</td>
</tr>
</table>

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>隨機大小地圖</b> <i>灰階</i> | 灰階輸入影像控制形狀的隨機比例。<br><br>其影響由 <b>隨機大小輸入映射乘</b> 數參數控制。 |
| <b>隨機斜面圖</b> <i>灰階</i> | 灰階輸入影像控制形狀的隨機傾斜。<br><br>其影響由 <b>隨機斜入映射乘</b> 數參數控制。 |
| <b>圓角半徑地圖</b> <i>灰階</i> | 灰階輸入影像，控制形狀圓角的半徑。<br><br>其撞擊由圓角半徑輸入地圖多數控制 <b>。</b> 參數。 |
| <b>斜角距離圖</b> <i>灰階</i> | 灰階輸入影像控制形狀的斜角。<br><br>其撞擊由斜面距離輸入映射多重控制 <b>。</b> 參數。 |
| <b>面具地圖</b> <i>灰階</i> | 灰階輸入影像，控制形狀的遮罩。<br><br>其影響由遮罩映射輸入開始與<b>遮罩映射輸入結束</b>參數控制<b>。</b> |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>金額 X</b> <i>整數</i> | X 軸上的<b></b>格子數量。 |
| <b>金額 Y</b> <i>整數</i> | Y軸上的<b></b>格子數量。 |
| <b>規模</b> |  |
| <b>隨機尺寸乘數</b> <i>浮標</i> | 對隨機縮放強度進行 <i>全域</i> 調整。 |
| <b>隨機大小輸入映射乘法</b> <i>浮標</i> | 利用從隨機尺寸映射</b>輸入中取<b></i>樣的值<i>調整隨機縮放強度。 |
| <b>隨機大小 X</b> <i>浮標</i> | 僅</i>調整 X</b> 軸<i>隨機縮放<b>的強度。 |
| <b>隨機大小 Y</b> <i>浮標</i> | 只能</i>調整 Y</b> 軸<i>隨機縮放<b>的強度。 |
| <b>隨機大小分布</b> <i>整數</i> | 控制隨機尺度值分配的方法：- 均勻：隨機尺度以相同方式</i>套用<i>於所有格<br>子- <i>藍噪聲</i>：利用藍噪聲模式調整</i>隨機尺度<i></i><i><br><br> |
| <b>形狀面向 - 變形</b> |  |
| <b>間隙厚度</b> <i>浮標</i> | 調整形狀間隙的厚度。 它對所有</i>形狀都是<i>平等的。 |
| <b>隨機位置乘法</b> <i>浮標</i> | 對形狀施加一個隨機位置偏移，直到 <i>它與格子的邊界</i>相接。 |
| <b>圓角半徑</b> <i>浮標</i> | 調整 <i>形狀圓角的半徑</i> 。 值為 <b>0</b> 表示未套用四捨五入。<br><br><i>注意</i>：當 <b>Enable per Axis Bevel 控制</b> 參數設 <i>為 True</i>，此效果無法套用。 |
| <b>圓角 半徑輸入 地圖 多。</b> <i>浮標</i> | 調整 <b>圓角半徑地圖</b> 輸入映射對圓角半徑的影響強度。<br><br>該映射作為<i>圓角半徑</b>參數的每像素</i>乘<b>數。<br><br><i>注意</i>：當<b>「每軸斜角啟用</b>」參數設<i>為 True</i>，此效果無法套用。 |
| <b>規模倍增器</b> <i>浮標</i> | 調整每個形狀的大小，依其單元</i>面積的比例<i>調整。 |
| <b>量表隨機</b> <i>浮標</i> | 調整每個形狀所施加<i></i>隨機刻度的強度。 |
| <b>旋轉</b> <i>浮標</i> | 透過將每個<i>角落移動到<i>格子邊界上的相鄰</i>角</i>來旋轉形狀。<br><br>此方法會在旋轉時對形狀施加一定程度 <i>的變形</i> 與 <i>縮放</i> 。 |
| <b>旋轉隨機</b> <i>浮標</i> | 調整每個形狀所施加隨機旋轉強度的強度。<br><br>旋轉方法描述於 <b>旋轉</b> 參數中。 |
| <b>角位隨機</b> <i>浮標</i> | 透過對其<i>格子邊界的每個角落</i>施加隨機偏<i>移</i>來扭曲形狀。 |
| <b>斜坡</b> |  |
| <b>隨機斜率乘數</b> <i>浮標</i> | 對隨機傾斜強度進行 <i>全域</i> 調整。 |
| <b>隨機斜面輸入映射乘法</b> <i>浮標</i> | 利用從隨機斜面圖</b>輸入取<b></i>樣的數值<i>調整隨機傾斜強度。 |
| <b>隨機斜面X</b> <i>浮標</i> | 僅</i>調整 X</b> 軸<i>上隨機傾斜<b>的強度。 |
| <b>隨機斜面 Y</b> <i>浮標</i> | 只</i>調整Y</b>軸<i>隨機傾斜<b>的強度。 |
| <b>隨機斜面分布</b> <i>整數</i> | 控制隨機斜率值分配的方法：- 均勻：隨機斜面以相同方式</i>應用<i>於所有格<br>子- <i>藍噪點</i>：利用藍噪點模式調整</i>隨機斜面<i></i><i><br><br> |
| <b>斜面</b> |  |
| <b>斜面距離模式</b> <i>整數</i> | 設定形狀斜角的取得<i></i>方法：<br><br>相<i>對於格線大小</i>：形狀依其格線大小</i><br>的指定<i>比例斜角 - <i>相對於形狀大小</i>：形狀依其尺寸</i><br>的指定<i>比例斜角 - <i>相對於影像大小</i>：形狀依指定<i>比例斜角</i> |
| <b>斜面距離乘數</b> <i>浮標</i> | 對斜角的距離進行 <i>全域</i> 調整。 |
| <b>斜角距離輸入映射 多重</b> <i>浮標</i> | 利用 <b>斜面距離圖</b> 輸入映射作為 <i>每像素</i> 乘數來調整斜角距離。 |
| <b>斜角圓弧</b> <i>浮標</i> | 調整斜角所施加的圓角強度，使其更具 <i>凸性</i>。 |
| <b>啟用每軸斜角控制</b> <i>布林值</i> | 當 True 時<i>，可以分別</i><b>在 X</b> 軸和 <b>Y</b> 軸上套用和調整<i>斜角。<br><br><i>注意</i>：這會<i>抵</i><b>消圓角</b></i>效應。 |
| <b>斜角距離 X</b> <i>浮標</i> | 只能</i>調整 X</b> 軸<i>斜面<b>的距離。此距離取決於斜面距離模式</b>參數的值<b>。<br><br><i>注意</i>：此參數僅在「<b>每軸斜面</b>啟用」參數設<i>為 True</i> 時可用。 |
| <b>斜面距離 Y</b> <i>浮標</i> | 僅</i>調整 Y</b> 軸<i>斜角<b>的距離。此距離取決於斜面距離模式</b>參數的值<b>。<br><br><i>注意</i>：此參數僅在「<b>每軸斜面</b>啟用」參數設<i>為 True</i> 時可用。 |
| <b>面具</b> |  |
| <b>遮罩隨機反演</b> <i>布林值</i> | 顛倒形狀的隨機遮罩。 |
| <b>掩蔽隨機起跑</b> <i>浮標</i> | 對於給定 <b>的隨機種子</b>，偽隨機遮罩會依 <i>照從起始形狀到終點形狀的特定順序</i> 進行。 這個參數可以讓你<i>偏移起始</i>形狀的<i>索引</i>。<br><br><i>注意</i>：這決定了遮罩值範圍</i>的一個限制<i>。因此 <i>，該值可能大</i> 於 <b>遮罩隨機端</b> 值。 |
| <b>面具隨機結局</b> <i>浮標</i> | 對於給定 <b>的隨機種子</b>，偽隨機遮罩會依 <i>照從起始形狀到終點形狀的特定順序</i> 進行。 這個參數可以讓你<i>偏移終端</i>形狀的<i>索引</i>。<br><br><i>注意</i>：這決定了遮罩值範圍</i>的一個限制<i>。因此 <i>，該值可能大</i> 於 <b>遮罩隨機起始</b> 值。 |
| <b>以細胞面積遮罩反演</b> <i>布林值</i> | 將形狀的遮蔽被其細胞面積反轉。 |
| <b>按細胞區域開始的遮罩</b> <i>浮標</i> | 調整<i>遮罩形狀的最小</i>格子面積閾值。<br><br><i>注意</i>：此舉決定遮蔽值範圍</i>的<i>一個限制。因此 <i>，該值可能大</i> 於 <b>遮罩單元面積的終點</b> 值。 |
| <b>依單元區域遮罩 結束</b> <i>浮標</i> | 調整<i></i>遮罩形狀的最大格子面積閾值。<br><br><i>注意</i>：此舉決定遮蔽值範圍</i>的一個限制<i>。因此 <i>，該值可能低於</i> <b>Mask by Cell Area 起始</b> 值。 |
| <b>遮罩貼圖輸入反轉</b> <i>布林值</i> | 透過遮罩貼圖</b>輸入映射反轉形狀<b>的遮罩。 |
| <b>遮罩映射輸入開始</b> <i>浮標</i> | 調整遮罩</b>圖輸入映射中<b>遮罩形狀的最小灰階值</i>閾值。<br><br><i>注意</i>：此決定遮罩值範圍</i>的一個上限<i>。<i>因此 <i>，該值可能大</i> 於 <b>遮罩映射輸入端</b> 值。 |
| <b>遮罩映射輸入結束</b> <i>浮標</i> | 調整<i>遮罩圖</b>中遮罩形狀最大灰階值</i>閾<b>值。<br><br><i>注意</i>：此決定遮罩值範圍</i>的一個上限<i>。因此<i>，該值可能低於</i><b>遮罩映射輸入起始</b>值。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="tile-random-2.resources/tilerandom2-variant.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="tile-random-2.resources/tilerandom2-variant2.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="tile-random-2.resources/tilerandom2-variant3.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="tile-random-2.resources/tilerandom2-inputs.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="tile-random-2.resources/tilerandom2-demo.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="tile-random-2.resources/tilerandom2-demo2.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="tile-random-2.resources/tilerandom2-node.png" />
        </td>
    </tr>
</table>
