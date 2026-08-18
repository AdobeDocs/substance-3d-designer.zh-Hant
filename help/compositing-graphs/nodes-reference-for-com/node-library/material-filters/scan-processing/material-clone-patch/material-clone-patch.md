---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/material-clone-patch.html"
breadcrumb-title: ''
description: 使用 Material Clone Patch 節點來克隆並修補掃描材質中修復瑕疵的貼圖區域。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Material Clone Patch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 物質複製補丁
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 0%

---


# 物質複製補丁

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/clone-patch-material.png){width="128px"}

## 物質複製補丁

**收錄於：***材料濾鏡/掃描處理*

**複合體**

</td>
<td style="border: 0;" valign="top">

## 說明

這是多頻道完整素材版本的 [《Clone Patch](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md)》。 它會對材料的任何通道執行克隆補丁。 [更多資訊請參閱原版！](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md)

如果你想從材質的所有通道中移除細節，這非常有用。 輸出會針對多個聲道進行除錯影像，精確查看智慧音色區域的樣貌。

## 參數

### 輸入

* **遮罩**： *灰階輸入*\
  遮罩槽用於遮蔽節點的效果。 可以用「遮罩」參數切換。

### 參數

* **頻道**
  * 在這個群組中切換材質通道，例如使用鏡面/光澤貼圖而非金屬/粗糙度時。
* **形狀**： *方形，郵票組圓盤*&#x200B;形狀。 只當作基礎使用。
* **Edge**
  * **閾值（多聲道）：***0.0 - 1.0*&#x200B;設定混合區域應該覆蓋的距離。這個層級會沿著目標區域的形狀逐步增加，所以在均勻背景下幾乎沒有影響*。*要小心不要在不同頻道間調整太多，否則可能會導致視覺上的差異！
  * **模糊**： *0.0 - 2.0*&#x200B;模糊印章區域邊緣，方便需要較柔和的過渡。
  * **平滑度**： *0.0 - 2.0*&#x200B;郵票形狀邊緣會圓滑，使輪廓更流暢。
  * **格點解析度**： *1 - 11*&#x200B;設定混合分析的品質解析度。 較高的數值代表融合更準確。
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
