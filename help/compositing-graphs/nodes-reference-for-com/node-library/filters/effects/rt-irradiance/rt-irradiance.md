---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/rt-irradiance.html"
breadcrumb-title: ''
description: 使用 RT 輻照度節點從幾何體中即時計算光照度資訊，以實現逼真的光照計算。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > RT Irradiance
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: RT 輻射
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---


# RT 輻射

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/rt-irradiance.png){width="128px"}

**收錄於：***濾鏡/效果*

**複合體**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## 說明

在由環境圖與發射映射生成的高度圖輸入上產生光線追蹤輻照度。 可以用來「烘焙」光照到圖表中的貼圖中。 用於假全域光暈與發光效果。由於計算時間，此節點不應與 CPU（SSE）引擎搭配使用。 回傳兩張地圖：一張是將輻照度應用於材料輸入的 Irradiance 輸出，另一張僅包含計算出的輻照度值的原始 irradiance map。

</td>
</tr>
</table>

## 參數

### 輸入

* **高度：***灰階輸入*&#x200B;高度是材質槽唯一需要的輸入。沒有它，節點將無法良好運作。
* **發光：***顏色輸入*&#x200B;的發光應該是純黑色不發光的格式，其他顏色值會發光。Alpha 被忽視了。 需要連接到這個插槽或環境插槽才能看到任何結果。
* **環境**： *色彩輸入*\
  利用 HDR 照明環境計算輻射度。 需要連接到此插槽或發射插槽才能看到任何結果。

### 參數

* **身高評分**： *0.0 - 1.0*\
  用比例來解釋高度。 影響整個場景的視覺效果。
* **品質**： *32 射線、64 射線、128 射線*\
  決定結果品質，也會影響效能。 光線越少，噪音越多。
* **計算反彈：***假/真*\
  切換彈跳計算。 會影響品質和速度。
* **環境旋轉**： *0.0 - 1.0*\
  讓環境旋轉。
* **環境暴露（EV）：***-4.0 - 4.0*\
  曝光值對環境的使用影響效果的總亮度。
* **發射強度**： *0.0 - 20.0*\
  發射輸入的乘數會影響發射輻射的照射強度。
* **發射色空間**： *sRGB，線性*\
  色彩空間曾用來解讀 Enissive 輸入。
* **IBL Raw Irradiance Alpha** 陰影： *錯誤/真實*\
  切換是否要加入陰影到
* **發射 LOD 偏壓**： *-1.0 - 1.0*&#x200B;發射輻射的調諧品質。 值越低，噪音越多。

## 範例圖片

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/rt-irr-03-1.jpg" width="300px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c1_image" src="../../../../../../assets/rt-irr-01-1.jpg" width="300px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c2_image" src="../../../../../../assets/rt-irr-02-1.jpg" width="300px"/></div> |
| --- | --- | --- |
|  |  |  |
