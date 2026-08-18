---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/multi-clone-patch.html"
breadcrumb-title: ''
description: 使用 Multi Clone Patch 節點來克隆並修補多個材質通道，以修復掃描的材質瑕疵。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Multi Clone Patch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 多重複製人補丁
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 0%

---


# 多重複製人補丁

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/clone-patch-multi.png){width="128px"}

![](../../../../../../assets/clone-patch-multi-grayscale.png){width="128px"}

## 多重複製補丁（灰階）

**收錄於：***材料濾鏡/掃描處理*

**複合體**

</td>
<td style="border: 0;" valign="top">

## 說明

此節點是 Clone Patch[&#128279;](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md) 的多輸入版本。它連接最多八個輸入，並對所有輸入執行完全相同的複製補丁操作。 它主要用於多角度照片，然後 [再與多角度轉反照](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md) 率或 [多角度轉正常](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-normal/multi-angle-to-normal.md)合成。

>[!NOTE]
>
> 更多資訊請參見 [複製補丁](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md) ，材質版本請參見 [材料複製補丁](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/material-clone-patch/material-clone-patch.md) 。

## 參數

### 參數

* **輸入數量**： *1 - 8*&#x200B;設定將接收相同 Patch 操作的輸入數量。
* **是 Normal（僅限 Color）：**&#x200B;**False/True** Sets 判斷輸入是否為法線貼圖，以及混合是否應被視為法線映射。
* **形狀**： **方形，郵票組圓盤**&#x200B;形狀。 只當作基礎使用。
* **Edge**
  * **閾值**： *0.0 - 1.0*&#x200B;設定混合區域應該達到的距離。 它沿著目標區域的形狀呈階梯狀生長;對於均勻背景來說，效果非常有限*。
  * **模糊**： *0.0 - 2.0*&#x200B;模糊印章區域邊緣，方便需要較柔和的過渡。
  * **平滑度**： *0.0 - 2.0*&#x200B;郵票形狀邊緣會圓滑，使輪廓更流暢。
  * **格點解析度**： *1 - 11*&#x200B;設定混合分析的高品質解析度。 較高的數值代表融合更準確。
* **變換**
  * **來源矩陣**：*（轉換矩陣）*轉換來源（縮放與旋轉）。 無法在 Canvas 上進行，只能透過這些參數來改變。
  * **來源偏移**： *-0.5 - 0.5*&#x200B;轉換來源位置。 無法在 Canvas 上進行，只能透過這些參數來改變。 *這個參數大概是你最想改變的！*
  * **目標矩陣**：*（轉換矩陣）*轉換目標位置（縮放與旋轉）。 也可以用 Gizmo 在畫布上來完成。
  * **目標偏移**： *-0.5 - 0.5*&#x200B;轉換目標位置。 也可以用 Gizmo 在畫布上來完成。

## 範例圖片

|  |
| --- |
| 本頁無附帶圖片。 |

</td>
</tr>
</table>
