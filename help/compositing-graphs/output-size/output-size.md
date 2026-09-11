---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/output-size.html"
breadcrumb-title: ''
description: 為 Substance 合成圖設定輸出大小，以控制材質解析度與品質。
helpx_creative_field: ""
helpx_description: Designer > Substance graphs > Output size
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 輸出大小
user-guide-description: ''
user-guide-title: ''
source-git-commit: 46563ec789547cc1add76655dbad02f5099927a6
workflow-type: tm+mt
source-wordcount: '1006'
ht-degree: 5%

---


# 輸出大小

它是圖形<b>基礎參數</b><b>中的第一個，與輸出格式</b>（或位元深度）一起，必須充分理解，因為它對圖形的輸出有重大影響，無論是在 Designer 內，還是作為已發佈的 Substance 3D 資產（SBSAR）[&#128279;](../publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md)檔案，都會影響圖形的輸出。

>[!TIP]
>
> 我們強烈建議 [你深入了解 Substance 圖](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) 中的繼承，作為有效運用輸出大小特性的基礎。

>[!NOTE]
>
> 用 ![](output-size.resources/props-output-size-lock.jpg) 鎖定鍵讓高度值 *和寬度值相符* 。

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

## 2 的冪次方

輸出大小參數決定圖形或節點所輸出紋理&#x200B;*的解析度*。

紋理是一種在圖形運算中受限於圖形處理硬體運算方式所施加的某些限制的物件。 其中一個限制是材質應該代表一張圖片，像素數在 X 和 Y 中是 *2* 的冪次方。

</td>
<td width="33.33%" style="border: 0;" valign="top">

| 2的冪次方 | 像素 |
| --- | --- |
| 7 | 128 |
| 8 | 256 |
| 9 | 512 |
| 10 | 1024 |
| 11 | 2048 |
| 12 | 4096 |
| 13 | 8192 |

</td>
</tr>
</table>

輸出大小特性利用 *對數步進* 來輕鬆映射二的冪次方遞增（例如 256、512、1024 等） 調整為 *線性尺度* （例如 8、9、10 等）。 這表示將 X 或 Y 的輸出大小值增減 1 等同於將當前解析度乘除 2。

當輸出大小值由 [函數](../../function-graphs/function-graphs.md)控制時，這同樣適用，該函數應輸出目標對數值（相對或絕對），而非目標解析度。

>[!IMPORTANT]
>
> 在 X 和 Y 中增加或降低解析度會使像素數 *乘除以 4*，這對圖形 *的效能* 和 *記憶體佔用*&#x200B;有顯著影響。\
> 因此，我們強烈建議使用 *實際達到理想效果所需的最低解析度* 。 控制解析度是我們 [眾多效能優化指引](../../best-practices/performance-optimization/performance-optimization-guidelines.md)之一。

>[!NOTE]
>
> 在函數圖[&#128279;](../../function-graphs/function-graphs.md)中，`$size`與`$sizelog2`[系統變數分別](../../function-graphs/variables/system-variables/system-variables.md)回傳與節點或圖目前解析度相符的 Float2 值，為原始像素數或 2 的冪次方。\
> 例如，對於 1024\*512 的影像，返回 ， `$size` `(1024,512)` 而 `$sizelog2` 返回 `(10,9)`。

## 相對規模

當輸出大小特性使用&#x200B;*相對於...* [&#x200B; 繼承方法](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)時，其值會以相對於繼承的對數值&#x200B;*的修飾符*&#x200B;表示。

相對於繼承解析度的修正值，在對數刻度上範圍從 -12 到 +12，預設值為 0。 這表示每超過或低於一步，解析度就會加倍或減半。 右側表格舉例說明繼承值為 9（即 512 = 2^9）與 11（即 2048 = 2^11）時，一維相對解析度的變化：

注意 8196 以上的大小是 *有*&#x200B;上限的。 這個上限是透過<b>偏好設定[&#128279;](../../interface/preferences-window/preferences-window.md)中「一般</b>」區塊的「烹飪大小限制</b>」設定<b>來控制的。請注意，使用非常高解析度的工作會帶來相應的效能成本與指數級的記憶體佔用。 此外，圖形處理的限制會嚴格限制貼圖的最大尺寸。

| -5 | -4 | -3 | -2 | -1 | 0 | +1 | +2 | +3 | +4 | +5 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 16 | 32 | 64 | 128 | 256 | <b>512</b> | 1024 | 2048 | 4096 | 8196 | 8196 |
| 64 | 128 | 256 | 512 | 1024 | <b>2048</b> | 4096 | 8196 | 8196 | 8196 | 8196 |

>[!NOTE]
>
> 低於 16 **&#x200B; 解析度沒有上限，但不建議降低，因為低於這個門檻不會有效能提升。相反地，效能下降&#x200B;**&#x200B;是因為 Substance 引擎</b>的特定實作<b>。因此，在 Substance 圖中，請使用 16x16 作為一般的最低解析度。

## 變更繼承方法

在大多數情況下，輸出大小屬性的預設 [繼承方式](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) 依項目而定：

* 圖： *相對於母圖*
* Node： *相對於輸入* ——此時使用節點 [主輸入](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) 繼承的值
* [點陣](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md) 節點： *絕對* — 請參考 [點陣圖資源](../../resources/bitmap-resource/bitmap-resource.md) 頁面和 [效能優化指引](../../best-practices/performance-optimization/performance-optimization-guidelines.md) ，了解原因

點擊節點或圖形的屬性，然後在[屬性](../../interface/properties/properties.md)面板的基礎參數</b>區找到<b>輸出大小</b>屬性<b>。點擊繼承方法下拉選單，選擇所需的繼承方式。

![輸出大小繼承法](output-size.resources/change-mode.gif "輸出大小繼承法"){width="512px"}

## 範例問題

如果你是 Adobe Substance 3D Designer[&#128279;](https://www.adobe.com/tw/products/substance3d-designer.html) 的新手，可能會遇到一些常見問題。我們將在下面列出一些範例及解決方案。

+++問題一
**![（錯誤）](output-size.resources/error.svg) 問題**

![範例問題1](output-size.resources/problem2-bad.png "範例問題1")



**父大小**&#x200B;設定顯示&#x200B;*為灰色，*&#x200B;圖形解析度為不想要的 256\*256。

在圖的屬性中，輸出大小屬性的繼承方法被設定為 *絕對*，這會停止繼承，改用任意值。

**![（滴答聲）](output-size.resources/check.svg) 解決方案**

![範例問題1 解](output-size.resources/problem2-good.png "法範例問題1 解法")



將圖的輸出大小設定為 *相對於父*&#x200B;圖的繼承方法。

+++

+++問題二
**![（錯誤）](output-size.resources/error.svg) 問題**

![範例問題2](output-size.resources/problem1-bad.png "範例問題2")



上圖顯示，雖然圖設定為 *相對於母*&#x200B;圖，但解析度（512\*512）與父圖（1024\*1024）不同。

問題出在點陣[&#128279;](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md)節點。[它預設採用&#x200B;*絕對*&#x200B;繼承方法，並根據點陣圖資源](../../resources/bitmap-resource/bitmap-resource.md)選擇了 512\*512 作為解析。連接該節點的節點設定為 *相對於輸入*，因此其輸出大小會繼承自點陣節點。

**![（滴答聲）](output-size.resources/check.svg) 解決方案**

![範例問題2 解](output-size.resources/problem1-good.png "法範例問題2 解法")



將 Bitmap 節點的輸出大小繼承方法設為 *相對於父*&#x200B;節點，這樣就能解決後續鏈的問題。

+++

+++問題三
**![（錯誤）](output-size.resources/error.svg) 問題**

![範例問題3](output-size.resources/problem3-bad.png "範例問題3")



上面你可以看到一個問題，解析度在鏈條中途跳躍得更高，導致輸出解析度遠高於父系統定義的。

問題是因為轉換二維[&#128279;](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md)節點的相對修飾值為 3，使輸出變大了 8 倍。

**![（滴答聲）](output-size.resources/check.svg) 解決方案**

![範例問題3 解](output-size.resources/problem3-good.png "法範例問題3 解法")



將寬度和高度的相對修正值設為 0，這樣就不會有升階。

+++
