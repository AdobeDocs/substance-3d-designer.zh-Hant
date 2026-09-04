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
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '517'
ht-degree: 11%

---


# 點陣圖轉為 Material Light

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](bitmap-to-material-light.resources/bitmap-to-material-light-01.png)

<b>收錄於：</b> 材料過濾器>一鍵

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

此節點將單一的 Diffuse/Base color 輸入轉換成完整材質。 作為 Allegorithmic 完整版 Bitmap2Material 的簡單「輕量」版本 [，可以單獨](https://www.allegorithmic.com/products/bitmap2material)購買，讓你稍微體驗完整版。 這方法對較簡單的案件也很有效。

雖然不保證能得到完美且符合 PBR 正確的材質，但如果你只有一張圖片，想要完整素材，這是個不錯且快速的入門方法。

</td>
</tr>
</table>

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>頻道</b> | 在這個群組中切換材質通道，例如使用高光/光澤貼圖而非金屬/粗糙度時。 |
| <b>全球</b> |  |
| <b>深度平衡</b> <i>-1.0 - 1.0</i> | 為高度圖設定偏壓/偏移。 |
| <b>彌漫</b> |  |
| <b>磨利</b> <i>0.0 - 1.0</i> | 為擴散效果增添銳利感。 |
| <b>色相</b> <i>0.0 - 1.0</i> | 色調會透過使用者選擇的色調變化來擴散。 |
| <b>飽和度</b> <i>0.0 - 1.0</i> | 修改擴散結果的飽和度。 |
| <b>亮度</b> <i>0.0 - 1.0</i> | 調整擴散結果亮度。 |
| <b>對比</b> <i>-1.0 - 1.0</i> | 調整結果的對比度。 |
| <b>地形</b> | 救援組控制正常與高度輸出。 |
| <b>輸出標準格式</b> <i>DirectX、OpenGL</i> | 可在普通格式間切換（翻綠色）。 |
| <b>倒置產生的救濟</b> <i>錯誤/真實</i> | 顛覆了身高的解釋。 |
| <b>正常力量</b> <i>0.0 - 20.0</i> | 生成的法線貼圖強度。 |
| <b>緩解均衡器</b> <i>0.0 - 1.0</i> | 設定不同細節刻度的轉換天平。 |
| <b>捏合強度</b> <i>0.0 - 1.0</i> | 讓普通難度的過渡更明顯。 在轉為正常前，實際上會先加一個銳化濾鏡，讓邊緣更明顯。 |
| <b>普通銳利</b> <i>0.0 - 1.0</i> | 轉換後會銳化 Normalmap，讓細節更清晰。 |
| <b>正常軟化</b> <i>0.0 - 1.0</i> | 轉換後會軟化法線貼圖，隱藏細節。 |
| <b>鏡面鏡面</b> |  |
| <b>鏡面擴散影響</b> <i>0.0 - 1.0</i> | Set的擴散對Specular的影響。 同時也會影響光澤度和粗糙度的輸出。 |
| <b>鏡面飽和</b> <i>0.0 - 1.0</i> | 改變鏡面輸出的飽和度。 |
| <b>鏡面銳化</b> <i>0.0 - 1.0</i> | 讓鏡面輸出更銳利。 |
| <b>鏡面關卡</b> <i>0.0 - 1.0</i> | 設定輸入等級以進行鏡面詮釋。 |
| <b>鏡面水平</b> <i>0.0 - 1.0</i> | 修改 Specular 的輸出電平。 |
| <b>金屬鏡面影響</b> <i>0.0 - 1.0</i> | 決定可選金屬輸入對鏡面貼圖的影響。 |
| <b>光澤</b> |  |
| <b>光澤度等級</b> <i>0.0 - 1.0</i> | 設定光澤度解讀的輸入層級。 |
| <b>光澤趨於穩定</b> <i>0.0 - 1.0</i> | 調整光澤輸出水平。 |
| <b>金屬光澤影響</b> <i>0.0 - 1.0</i> | 決定可選金屬輸入對光澤度地圖的影響。 |
| <b>粗糙度</b> |  |
| <b>粗糙度等級</b> <i>0.0 - 1.0</i> | 設定輸入等級以進行粗糙度的詮釋。 |
| <b>粗糙度趨於穩定</b> <i>0.0 - 1.0</i> | 修改粗糙度輸出等級。 |
| <b>金屬粗糙度影響</b> <i>0.0 - 1.0</i> | 決定可選金屬輸入對光澤度地圖的影響。 |
| <b>環境遮蔽</b> |  |
| <b>擴散中的環境遮蔽</b> <i>0.0 - 1.0</i> | 將生成的 AO 混合成 Diffuse 輸出。 |
| <b>環境遮蔽擴散</b> <i>0.0 - 1.0</i> | 設定產生的AO擴散範圍。 |
| <b>環境遮蔽光距離</b> <i>0.0 - 1.0</i> | 設定 AO「深度」詮釋。 當擴散很大時，影響力會比較小。 |
| <b>環境遮蔽光角度</b> <i>0.0 - 1.0</i> | 設置假光照 AO 投射角度。 若設定角度相反，可用來補償擴散器中已存在的任何方向性 AO。 |
| <b>環境遮蔽等級</b> <i>0.0 - 1.0</i> | 修改AO輸出電平。 |
