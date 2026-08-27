---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/auto-crop.html"
breadcrumb-title: ''
description: 使用自動裁切節點自動裁切材質，移除空白邊框並優化材質尺寸。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Auto Crop
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 自動裁切
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 1%

---


# 自動裁切

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](auto-crop.resources/autocropgrayscale.png){width="200px"}

</td>
<td style="border: 0;" valign="top">

![](auto-crop.resources/autocropcolor.png){width="200px"}

</td>
</tr>
</table>

<b>收錄於：</b> 《濾波器>轉換》

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

**自動裁切**&#x200B;節點會&#x200B;**調整輸入**，使其內容要麼放在&#x200B;*圖片中央*&#x200B;且不調整大小，要麼&#x200B;*調整大小至影像的長度*。

影像內容由一個框定義，該框貼合在 X 和 Y 的首尾像素上，該值&#x200B;*大*&#x200B;於 0 *（即非黑色）。**&#x200B;**&#x200B;**&#x200B;**&#x200B;***彩色**&#x200B;版本允許你從 RGB 和 Alpha 通道中選擇來定義該框。

</td>
</tr>
</table>

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>模式</b> <i>整數</i> | 設定應適用的裁切方法：<br><br>- <i>裁切方格</i>：將影像裁切成<i>形狀位於最小正方形影像中心，且該正方</i>形能完整包含該<br>方形- <i>自動裁切</i>：將影像裁切至<i>形狀位於最小正方形或非正方形</i>影像中心，且該影像能完整包含該<br>方形- <i>貼合（保持比例）：</i> 影像會被調整至<i>影像的整個展度</i>，同時保持<i>其比例</i>（即寬度與長度的比例）<br>- <i>填充（拉伸）：</i>將影像調整至<i>整個影像的展度</i> |
| <b>使用 alpha</b> <i>布林值</i> | 利用輸入的 <b>alpha 通道來判斷影像內容<i>的裁切範圍</i>。</b>當設定為 <i>False</i> 時，則會使用黑色像素。<br><br><i>注意：</i> 此參數僅在 <b>節點的 Color</b> 版本中可用。 |
| <b>過濾模式</b> <i>整數</i> | 定義在像素間插值</i>時如何處理取樣結果<i>：<br><br>- <i>最近</i>：取樣值完全<i>相同</i>（更快）<br>- <i>雙線性：</i>對結果套用雙線性濾波器，使<i>畫面<br>更</i>平滑- <i>自動</i>：根據裁切所選<b></b>模式，使用上述兩種模式中最合適的 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="auto-crop.resources/autocrop-demo-01-resized.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="auto-crop.resources/autocrop-variant2.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="auto-crop.resources/autocrop-variant.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="auto-crop.resources/autocrop-variant4.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="auto-crop.resources/autocrop-variant3.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="auto-crop.resources/autocrop-node.png" />
        </td>
    </tr>
</table>
