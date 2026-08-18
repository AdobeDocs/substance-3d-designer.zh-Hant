---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/1-click/bitmap-to-material-light.html"
breadcrumb-title: ''
description: 使用 Bitmap to Material Light 節點快速將點陣圖影像轉換成材質，並優化光照以快速工作流程。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > 1-Click > Bitmap to Material Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 點陣圖轉為 Material Light
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 0%

---


# 點陣圖轉為 Material Light

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/b2m-light.png)

## 點陣圖轉為 Material Light

**收錄於：***材質過濾器/一鍵*

**中級**

</td>
<td style="border: 0;" valign="top">

## 說明

此節點將單一的 Diffuse/Base color 輸入轉換成完整材質。 作為 Allegorithmic 完整版 Bitmap2Material 的簡單「輕量」版本 [，可以單獨](https://www.allegorithmic.com/products/bitmap2material)購買，讓你稍微體驗完整版。 這方法對較簡單的案件也很有效。

雖然不保證能得到完美且符合 PBR 正確的材質，但如果你只有一張圖片，想要完整素材，這是個不錯且快速的入門方法。

## 參數

* **頻道**
  * 在這個群組中切換材質通道，例如使用高光/光澤貼圖而非金屬/粗糙度時。
* **全球**
  * **深度平衡**： *-1.0 - 1.0*&#x200B;為高度圖設定偏移/偏移。
* **彌漫**
  * **銳化**： *0.0 - 1.0*&#x200B;為擴散效果增加銳化效果。
  * **色調**： *0.0 - 1.0*&#x200B;透過使用者選擇的色調偏移來擴散。
  * **飽和度**： *0.0 - 1.0*&#x200B;修正擴散結果的飽和度。
  * **亮度**： *0.0 - 1.0*&#x200B;調整漫射結果亮度。
  * **對比度**： *-1.0 - 1.0*\
    調整結果的對比度。
* **地形**\
  救援組控制正常與高度輸出。
  * **輸出為一般格式**： *DirectX，OpenGL*&#x200B;在正常格式間切換（綠色翻轉）。
  * **反轉產生的浮雕**： *錯誤/真*&#x200B;反轉對高度的詮釋。
  * **法線強度**： *0.0 - 20.0*&#x200B;生成法線貼圖的強度。
  * **Relief Equalizer**： *0.0 - 1.0*&#x200B;為不同細節刻度設定轉換平衡。
  * **捏合強度**： *0.0 - 1.0*&#x200B;讓普通轉場更銳利。 在轉為正常前，實際上會先加一個銳化濾鏡，讓邊緣更明顯。
  * **法線銳化**： *0.0 - 1.0*&#x200B;轉換後銳化法線貼圖，顯示細節。
  * **Normal Soften**： *0.0 - 1.0*&#x200B;轉換後會軟化法線貼圖，隱藏細節。
* **鏡面鏡面**
  * **鏡面擴散影響**： *0.0 - 1.0*&#x200B;擴散對鏡面的影響。 同時也會影響光澤度和粗糙度的輸出。
  * **鏡面飽和度**： *0.0 - 1.0*&#x200B;改變鏡面輸出的飽和度。
  * **鏡面銳化**： *0.0 - 1.0*&#x200B;銳化鏡面輸出。
  * **鏡面音量（0.0***- 1.0*）設定高光解讀的輸入電平。
  * **鏡面音量輸出**： *0.0 - 1.0*&#x200B;調整鏡面輸出等級。
  * **金屬鏡面影響**： *0.0 - 1.0*&#x200B;決定可選金屬輸入對鏡面映射的影響。
* **光澤**
  * **光澤度等級：***0.0 - 1.0*&#x200B;設定光澤度解讀的輸入等級。
  * **光澤度水平：0.0***- 1.0*&#x200B;調整光澤輸出水平。
  * **金屬光澤影響**： *0.0 - 1.0*&#x200B;決定可選金屬輸入對光澤地圖的影響。
* **粗糙度**
  * **粗糙度等級：***0.0 - 1.0*&#x200B;設定輸入強度以解釋粗糙度。
  * **粗糙度水平：***0.0 - 1.0*&#x200B;調整粗糙度輸出水平。
  * **金屬粗糙度影響**： *0.0 - 1.0*&#x200B;決定可選金屬輸入對光澤度貼圖的影響。
* **環境遮蔽**
  * **漫反射**&#x200B;環境遮蔽： *0.0 - 1.0*&#x200B;生成的 AO 混合成漫反射輸出。
  * **環境遮蔽擴散**： *0.0 - 1.0*&#x200B;設定產生的光域擴散範圍。
  * **環境遮蔽光距離**： *0.0 - 1.0*&#x200B;設定 AO「深度」解讀。 當擴散很大時，影響力會比較小。
  * **環境遮蔽光角度**： *0.0 - 1.0*&#x200B;設定假光照 AO 投射角度。 若設定角度相反，可用來補償擴散器中已存在的任何方向性 AO。
  * **環境遮蔽等級**： *0.0 - 1.0*&#x200B;調整 AO 輸出音量。

## 範例圖片

|  |
| --- |
| 本頁無附帶圖片。 |

</td>
</tr>
</table>
