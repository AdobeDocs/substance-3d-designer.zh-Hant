---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/base-material.html"
breadcrumb-title: ''
description: 使用基礎材質節點來建立基礎材質屬性，從零開始製作物理基礎材質。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > PBR Utilities > Base Material
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 基礎材料
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 0%

---


# 基礎材料

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/pbr-base-material.png){width="128px"}

## 基礎材料

**收錄於：***材料過濾器/PBR工具*

**中級**

</td>
<td style="border: 0;" valign="top">

## 說明

在 Adobe Substance 3D Designer](https://www.adobe.com/products/substance3d-designer.html) 中製作多通道素材[最快速、最簡單的方法。此節點回傳一個基於簡單、純色設定與數值的全材質。 此資料可用作佔位符或精煉成複雜材料。

節點在貼圖完整道具和混合多種材質時非常有用。 事實上，你可以從這個節點開始製作每一個材料，完全不需要複雜的材料基底。

## 參數

### 輸入

* 每個通道都有可透過「使用者定義輸入」開關切換的可選輸入。

### 參數

* **PBR 工作流程**： *金屬 - 粗糙度，鏡面 - 光澤度* PBR 模型的設定。
* **材料預設**： *自訂、介電、黃金、銀、鋁、鐵、銅、鈦、鎳、鈷、鉑*&#x200B;金，快速製作特定金屬。 關閉無關選項。
* **基色**：*（顏色值）*用於基色的純色。
* **金屬色**：*（灰階值）*金屬色的實心數值。
* **漫射色**：*（色彩值）*用於漫射的純色。
* **鏡面**：*（色值）*用於鏡面的純色。
* **鏡面預設**： *塑膠、木頭、石頭、磚塊、沙子、混凝土、布料、生鏽金屬、水、冰、玻璃*&#x200B;可選快速預設以設定符合 PBR 的鏡面值。
* **鏡面範圍**： *0.0 - 1.0*&#x200B;調整鏡面範圍。
* **粗糙度-光澤度**
  * **粗糙度值**：*（灰階值）*設定全局基準粗糙度值，若通道已啟動。
  * **光澤值**：*（灰階值）*用於光澤的純色，若通道啟動。
  * **Grunge Mount**： *0.0 - 1.0*&#x200B;可選的 Grunge 地圖輸入與 Gloss 或 Roughness 融合的程度。
  * **Grunge 平鋪**： *1 - 16*&#x200B;可選的 Grunge 地圖鋪片範圍。
  * **自訂 Grunge 輸入**： *False/True*&#x200B;啟用或停用可選的自訂 Grunge 地圖。
* **正常**
  * **從高度法線 強度**： *0.0 - 16.0*&#x200B;可選擇性地將自訂高度貼圖轉換為法線，並回傳為材質法線貼圖。
* **高度**
  * **高度位置**： *0.0 - 1.0*&#x200B;實心值用於高度輸出。
  * **高度範圍**： *0.0 - 1.0*&#x200B;設定使用者自訂高度圖的影響（若啟用）。
* **使用者自訂地圖**
  * 切換開啟或關閉所有使用者自訂的地圖，回傳這些地圖而非實體值。

## 範例圖片

|  |
| --- |
| 本頁無附帶圖片。 |

</td>
</tr>
</table>
