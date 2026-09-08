---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/transformation-2d.html"
breadcrumb-title: ''
description: 使用 Transformation 2D 節點對貼圖套用 2D 轉換，包括平移、旋轉和縮放。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Transformation 2D
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 轉換二維
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 0%

---


# 轉換二維

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![原子節點：轉換二維](../../../../assets/comp_transformation_1.png "原子節點：轉換二維"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

對影像應用二維轉換矩陣：平移、旋轉、縮放、對稱與剪切。

這與 Photoshop 中的 Transforming（Ctrl-T）或 Substance 3D Painter 中的 2D 映射操作器相當相似。

</td>
</tr>
</table>

這是一個非常有用且廣泛應用的節點，允許增加平鋪、移除平鋪、將影像置於特定位置、拉伸或壓縮輸入等。

然而，它在某些應用上可能無法完全匹配，因此以下節點可能值得關注： [安全轉換](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/safe-transform/safe-transform.md)、 [非平方轉換](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/non-square-transform/non-square-transform.md)、 [四邊轉換](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/quad-transform/quad-transform.md) 及 [梯形轉換](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/trapezoid-transform/trapezoid-transform.md)。

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">



</td>
<td width="83.33%" style="border: 0;" valign="top">



</td>
<td width="100.00%" style="border: 0;" valign="top">



</td>
</tr>
</table>

>[!TIP]
>
> 停用平鋪
> 
> 將「平鋪模式」[基底參數](../../../../glossary/glossary.md)的繼承方法](../../../../glossary/glossary.md)設[為「絕對」，這樣你就可以將參數值設為「無平鋪」：
> 
> ![](../../../../assets/tilingmode.png)

>[!NOTE]
>
> 節點屬性中的縮放與旋轉值是 *相對於當前變換*&#x200B;的，直到你點擊「套用」按鈕後才會套用到 2D 視圖。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## 輸出連接器

</td>
<td style="border: 0;" valign="top">

### 範例

</td>
</tr>
</table>

## 參數

|  |  |
| --- | --- |
| <b>轉換矩陣</b> *Float4* | 打開底層的轉換矩陣進行直接編輯。 允許你改變旋轉和縮放。 也可以透過 2D 視角中的裝置調整。   警告：這些調整與視圖不直接相關，且是可分階段進行的相對調整。 |
| <b>偏移</b> *Float2* | 定義影像的二維位移。 允許你改變位置或偏移，也可以透過 2D 視角的裝置調整。   這直接關聯到 2D 視圖輸出。 |
| <b>Mipmap 模式</b> *整數* | 允許你切換到手動 [mipmap](../../../../glossary/glossary.md) 等級，透過貼圖過濾減少影像中的雜訊。 |
| <b>Mipmap 層級</b> *整數* | 設定 [要使用的 mipmap](../../../../glossary/glossary.md) 電平。     *當「Mipmap 模式」設為「手動」時可用* |
| <b>霧面色</b> *Float4* | 當轉換平鋪時所用的背景顏色是被禁用的。 也就是說，設定當轉換後的輸入未覆蓋輸出區域時所使用的顏色。   如果用RGBA顏色工作，可以做成透明。 |
| <b>過濾</b> *整數* | 設定所使用的降取樣方法。 降低 Mipmap Level 時效果不太好。 |

## 輸入連接器

|  |  |
| --- | --- |
| <b>輸入</b> *灰階/彩色* 原色 | 那個形象要被改造。 |

## 輸出連接器

|  |  |
| --- | --- |
| <b>產出</b> *灰階/彩色* |  |

## 範例

*即將推出。*
