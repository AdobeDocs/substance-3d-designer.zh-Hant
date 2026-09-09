---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/non-square-transform.html"
breadcrumb-title: ''
description: 使用 Non-Square Transform 節點，對具有獨立 X 和 Y 縮放的非正方形材質套用變換。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Non-Square Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 非平方轉換
user-guide-description: ''
user-guide-title: ''
source-git-commit: caf740432682ed82eb55ad2f84bc9dd6ed15ad14
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 4%

---


# 非平方轉換

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](non-square-transform.resources/safe-transform.png)

![](non-square-transform.resources/safe-transform-grayscale.png)

<b>收錄於：</b> 《濾波器>轉換》

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

非方形安全的 Transform 2D](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md) 版本[。自動偵測非正方形比例，並能將正方形輸入影像轉換到非正方形畫布上。

務必完全了解 [圖參數](../../../../../../compositing-graphs/graph-parameters/graph-parameters.md)，才能充分利用這個節點，因為你需要正確設定幾個參數：

* 你的 **圖** 大小應該是非方形的，否則不需要這個節點。
* 將非正方形轉換 **節點的** 輸出大小設為「*相對於父節點*」。
* 如果你只想將輸入轉換到單一位置，請將節點的&#x200B;**平鋪模式設**&#x200B;為「*無平鋪*」。

</td>
</tr>
</table>

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>瓦片模式</b> <i>自動、手動</i> | 啟用自動非平方補償是否啟用。 |
| <b>瓷磚</b> <i>1 - 16</i> | 只有在瓦片模式設為手動時才能進入。 讓你能以安全的平鋪方式改變比例。 |
| <b>偏移</b> <i>0.0 - 1.0</i> | 移動或翻譯結果。 雙擊滑桿以輸入負值。 |
| <b>旋轉</b> <i>0.0 - 1.0</i> | 旋轉輸入影像。 |
| <b>安全旋轉（僅限方形）</b> <i>錯誤/真實</i> | 吸附到安全值以維持像素銳利度。 |
| <b>背景色</b> <i>（色彩值）</i> | 背景色可以用來填滿圖片。 只有當 [基礎參數的平鋪模式設為「*無平鋪*」](../../../../../../compositing-graphs/graph-parameters/graph-parameters.md)時才會顯示。 |

## 範例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="non-square-transform.resources/nonsquare-ex.png" />
        </td>
    </tr>
</table>
