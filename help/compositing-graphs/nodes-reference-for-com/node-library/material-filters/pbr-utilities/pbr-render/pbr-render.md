---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/pbr-render.html"
breadcrumb-title: ''
description: 使用 PBR 渲染節點來渲染基於物理的材質，並搭配逼真的光照來預覽材質外觀。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > PBR Utilities > PBR Render
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: PBR 渲染
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '1365'
ht-degree: 1%

---


# PBR 渲染

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/pbr-render.png){width="250px"}

**收錄於：***材料過濾器/PBR工具*

**複合體**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## 說明

利用基於影像的光照（IBL）將 PBR 材質渲染到球體、平面或圓柱體上。這是位於節點內的渲染引擎，對於產生縮圖、預覽或 2D 資產非常有用。 它不是像 3D 視圖那樣的渲染，而是實際在你的圖表中產生的貼圖。

此節點至少需插入完整的 PBR 材料。 理想狀況是利用連結建立模式（Link Creation Modes）將材質連接到 PBR Render。 此外，渲染計算光照時，還需要一個球形展開的 HDRI 環境。 測試材料可在 PBR 材料中找到，環境地圖則可在圖書館的 3D View 中找到 [。](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/3d-view-library.md)

</td>
</tr>
</table>

>[!WARNING]
>
> **CPU（SSE2）引擎**
> 
> PBR 渲染節點非常笨重，且與 SSE2 CPU 引擎相容性不佳。 如果節點表現極差，按 F9 切換到另一個引擎。

## 輸入

* **物料通道****輸入**\
  在幾何體上渲染材質時，會使用多種材質輸入：
  * 基本顏色
  * 正常
  * 發射體
  * 粗糙度
  * 金屬
  * 反射層級
  * 高度
  * 環境遮擋
  * 不透明度遮罩
  * 異向性層級
  * 異向性角度
  * 半透明
  * 散射距離尺度
* **鏡頭髒污地圖**： *灰階輸入*&#x200B;自訂的鏡頭髒污地圖，當鏡頭光暈可見時會出現。
* **鏡頭光圈貼圖**： *灰階輸入*&#x200B;可用來覆蓋散景、失焦形狀。 對比越強烈，它就越明顯。 請注意，貼圖中只有一個圓形會被取樣，所以任何形狀都必須符合圓形。
* **背景輸入**： *色彩輸入*\
  當 **背景模式** 參數設為 *Backgroud 輸入時，自訂地圖可用作背景*
* **環境地圖**： *用於計算光照的色彩輸入*&#x200B;環境地圖。 必須是球形映射且以 HDR 格式呈現。

輸出

* **美**\
  最終渲染圖
* **原始輻照**\
  最終渲染的輻射度資料\
  *Alpha：* 不透明度地圖
* **原始鏡面**\
  最終渲染的鏡面資料\
  *Alpha：* 鏡面陰影貼圖
* **正常世界空間**\
  世界空間的法線資料是最終渲染的\
  *Alpha：* 世界空間高度圖
* **正規切空間**\
  切線空間法線資料是最終渲染的\
  *Alpha：* 切線空間高度圖
* **紫外線**\
  最終渲染的 UV 資料\
  *Alpha：* 不透明度地圖

## 參數

* **形狀**： *球體、平面、圓柱體*\
  設定用於渲染的形狀。 無法自訂形狀。
* **位移強度**： *0.0 - 0.5*&#x200B;設定高度位移強度。
* **環境旋轉**： *0.0 - 1.0*\
  旋轉光影環境。 比起移動相機，這是預旋轉的。
* **背景模式**： *色彩、環境、環境、背景輸入*\
  設定背景中顯示的內容。 顏色是純色，環境是你插入並可選模糊的地圖。 環境音是一個非常模糊的環境版本。
* **背景色**： *（色彩值）*\
  只有在背景模式設為彩色時才可用。
* **環境背景模糊**： *0.0 - 1.0*\
  只有在背景模式設為環境時才可用。
* **形狀**
  * **等級**： *0.0 - 2.0*\
    設定球體的比例。
  * **飛機尺寸**： *0.0 - 1.0*\
    設定飛機的比例。
  * **汽缸半徑**： *0.0 - 1.0*\
    設定圓柱體的半徑。
  * **汽缸長度**： *0.0 - 1.0*\
    設定圓筒長度。
  * **旋轉**： *0.0 - 1.0*\
    可以旋轉形狀，但不會旋轉燈光。
  * **旋轉方向**： *0.0 - 1.0*\
    設定旋轉軸為二維。
  * **旋轉方向**： *0.0 - 1.0*\
    自旋在旋轉軸上成形。
  * **形狀位置**： *-1.0 - 1.0*\
    移動形狀。
  * **UV 平鋪**： *1.0 - 6.0*\
    設定 UV 平鋪的量。
  * **球體紫外線等級**： *0.0 - 4.0*\
    它設定了球體上的紫外線尺度。
  * **平面紫外線等級**： *1.0 - 4.0*\
    設定平面上的紫外線比例。
  * **圓柱紫外線等級**： *1.0 - 6.0*\
    設定圓柱體上的紫外線強度尺度。
  * **紫外線偏移**&#x200B;量： *0.0 - 1.0*\
    偏移 UV
  * **傾斜紫外線**： *錯誤/真實*\
    球體的紫外線會傾斜 45 度。
* **相機**
  * **曝光**&#x200B;度： *-4.0 - 4.0*\
    設定相機曝光。
  * **音調映射器**： *Linear、ACES、Filmic Hejl*\
    設定最終影像要使用的色調映射解決方案。
  * **相機模式**： *透視、正交*\
    在兩種投影模式間切換攝影機。
  * **視野**： *0.01 - 100.0*\
    設定攝影機視野角度。
  * **距離**： *0.0 - 4.0*\
    設定相機距離物體中心的距離。
  * **短片強度**： *0.0 - 1.0*\
    設定短片效果的強度。
  * **Vignette 半徑**： *0.0 - 1.0*\
    設定短片效果的半徑。
  * **螢幕位置**：\
    移動攝影機繞著物件移動，也可以用 2D 視角中的裝置來改變。
* **景深**
  * **光圈半徑** ： *0.0 - 0.1*&#x200B;設定光圈半徑。 數值越高，模糊區域會變得模糊（散景）。
  * **光圈刀片**： *3 - 9*\
    設定散景模糊的形狀。
  * **光圈環**： *0.0 - 1.0*\
    為散景形狀增加內部漸層。
  * **光圈分數**： *0.0 - 2.0*\
    為散景增添色差。
  * **旋轉散景**： *0.0 - 1.0*\
    為模糊的散景區域加入漩渦或旋轉效果。
  * **對焦模式：*自動、點點***\
    設定焦點是預先設定或使用者設定的。 點對焦可以讓你在2D視角中移動一個點來決定對焦距離。
  * **重點**：\
    如果焦點設為 Point，這可以讓你移動那個點。 有一個 2D 視角裝置。
  * **對焦偏移**： *-0.5 - 0.5*\
    如果設定為自動，可以來回切換對焦。
  * **使用自訂光圈地圖**： *False/True（真）*\
    覆蓋上述光圈設定，並使用光圈貼圖輸入來決定散景形狀。 需要輸入。
* **後續影響**
  * **啟用後效**： *錯誤/真實*\
    在最終渲染中切換 *所有* 後期效果。
  * **光暈強度** ： *0.0 - 2.0*&#x200B;設定光花效果的強度。
  * **布隆門檻** ： *0.0 - 2.0*&#x200B;設定布魯姆出現的低門檻。
  * **綻放色度偏移** ： *0.0 - 1.0*
  * **鏡頭光暈強度** ： *0.0 - 1.0*&#x200B;設定鏡頭光暈效果的強度。
  * **鏡頭光暈** 強度： *0.0 - 1.0*&#x200B;設定鏡頭光暈的強度。 確保環境背景的光線在視野內，才能清楚看到這個效果。
  * **鏡頭髒污強度** ： *0.0 - 1.0*&#x200B;將鏡頭髒污貼圖對鏡頭光暈產生影響。
* **渲染設定**
  * **擴散品質**： *16個樣本、32個樣本、64個樣本、128個樣本*\
    在擴散地圖的品質間切換。
  * **漫射發射多重器**： *0.0 - 1.0*\
    控制發射部分對輻照的貢獻程度。
  * **漫反射陰影強度**： *0.0 - 1.0*\
    控制擴散陰影的強度。
  * **鏡面抖動**： *0.0 - 1.0*\
    設定鏡面鏡面的抖動量。
  * **鏡面陰影倍率**： *0.0 - 1.0*\
    控制鏡面反射中陰影的強度。
  * **不透明度模式***抖動 Alpha 測試，簡單 Alpha 混合*\
    控制透明度的應用方式。 *簡單 Alpha 混合*&#x200B;模式在均勻背景上最為明顯。
  * **環境遮蔽強度**： *0.0 - 1.0*\
    設定環境遮蔽陰影的強度。
* **材料調整**
  * **重新計算法態：***假/真*\
    法線會根據位移強度從高度圖重新計算。
  * **一般格式**： *DirectX、OpenGL*\
    切換不同的法線貼圖格式（反轉綠色通道）
  * **介電F0輸入**： *恆定值，鏡面電平輸入*\
    設定驅動 F0 值的因素。 鏡面級輸入代表它會由輸入映射驅動。
  * **介電 F0**： *0.0 - 0.08*\
    如果介電 F0 輸入選擇 Constant Value，這個滑桿可以設定全域值。
* **透明外套**
  * **啟用透明塗層**： *錯誤/真實*\
    讓輸入材料上能再塗一層簡單的透明塗層。
  * **透明毛皮重量**： *0.0 - 1.0*\
    設定透明層的強度或強度。
  * **透明外套鏡面等級**： *0.0 - 1.0*\
    設定透明塗層的粗糙度。
  * **從底層**&#x200B;繼承法線： *如果透明塗層忽略或使用基底材質的法線，則為假/真*&#x200B;集合。
* **發射體**
  * **啟用發射光真***/假*&#x200B;切換發射光的漫射貢獻。
  * **發射強度**： *0.0 - 10.0*\
    為發射映射設定全域乘數。
* **次表面散射**
  * **啟用次表面散射***真/假*\
    切換最終渲染中的次表面散射。\
    *注意：* 次表面散射需要 **半透明** 輸入值高於 *0.0*
  * **散射距離** *0.0 - 1.0*\
    調整散射效應的最大距離。\
    *注意：*&#x200B;此值與每個色道&#x200B;*的散射距離刻度&#x200B;**輸入值*相乘**。
  * **紅移** *0.0 - 1.0*\
    調整紅移效應在散射中的強度。
  * **雷利** *0.0 - 1.0*\
    調整散射中瑞利效應的強度。

## 範例圖片

所有影像皆直接在 Designer 的 2D 視圖窗中產生，使用來自 [Substance 3D 資產](https://helpx.adobe.com/substance-3d/unlisted/assets.html) 庫的材質。

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/pbr-render-v2.jpg" width="300px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c1_image" src="../../../../../../assets/sphere-thermal-insulation-panel.jpg" width="300px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c2_image" src="../../../../../../assets/sphere-ominous-obsidian.jpg" width="300px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c3_image" src="../../../../../../assets/sphere-forest-gravel-1.jpg" width="300px"/></div> |
| --- | --- | --- | --- |
|  |  |  |  |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r2-column-c0_image" src="../../../../../../assets/sphere-chesterfield-1.jpg" width="300px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r2-column-c1_image" src="../../../../../../assets/sphere-carbon-fiber.jpg" width="300px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r2-column-c2_image" src="../../../../../../assets/plane-inclined-lumber-tiles.jpg" width="300px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r2-column-c3_image" src="../../../../../../assets/cylinder-medieval-leaded-glass-window.jpg" width="300px"/></div> |
|  |  |  |  |
