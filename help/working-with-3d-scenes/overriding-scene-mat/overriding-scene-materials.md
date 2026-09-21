---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/working-with-3d-scenes/overriding-scene-materials.html"
breadcrumb-title: ""
description: 在 3D 場景中覆寫現有材質，並用你自己的 Substance 材質來測試和預覽。
helpx_creative_field: ""
helpx_description: Designer > Working with 3D scenes > Overriding scene materials
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 覆蓋場景素材
user-guide-description: ""
user-guide-title: ""
source-git-commit: b1404a9f03e3156f5fba0e499bbe41dbc79b7308
workflow-type: tm+mt
source-wordcount: '889'
ht-degree: 0%
---

# 覆蓋場景素材

在使用現有材質處理 3D 場景時，必須覆寫這些材質，才能用自己的材質取代。

你的材質可以從零開始建立，也可以是經過調整的場景材質，再 [提取成物質圖](../../working-with-3d-scenes/extracting-materials-val/extracting-materials-values-and-textures.md)。

![覆寫場景材質、微調並將其重置到場景狀態](overriding-scene-materials.resources/tweakOverriddenMaterial.gif "覆寫場景材質、微調並將其重置為場景狀態"){zoomable="yes"}

## 覆蓋場景素材

場景中使用的任何素材都可以被你自己的版本覆蓋，也就是新素材或現有素材的編輯版本。

「覆寫材料」動作可在兩個地方找到：

* 打開「材料」選單，進入所需材料的子選單
* 按場景物件上的 Shift+Lb 選擇該物件，然後點擊 RMB 開啟其上下文選單

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![覆寫材質 - 「3D 視圖」視窗](overriding-scene-materials.resources/overrideMaterialActionViewport.png "中的動作 覆蓋材質 - 「3D 視圖」視窗中的動作"){zoomable="yes"}

*3D 視角中的動作*

</td>
<td style="border: 0;" valign="top">

![覆蓋材料 - 「材料」選單中的動作 覆寫材料 - 「材料」選單](overriding-scene-materials.resources/overrideMaterialActionMaterials.png "中的動作"){zoomable="yes"}

*材料選單中的動作*

</td>
</tr>
</table>

在 Designer 的語境中，其內部場景描述使用 USD，覆寫是指 *建立一份盡可能與原始材質相符的材質複製* 品，並將 *場景網格的材質綁定* 從原始變更為複製品。

>[!NOTE]
>
> 副本會在場景中建立在根目錄下的「<b>material</b>」資料夾（以美元為「Scope」），並使用與原始相同的識別碼加上數字後綴（例如：「rustedMetal\_0&#39;）

這代表兩個重要的事情：

1. 原始內容從未有任何改變。
1. 在 Designer 中完成的任何工作都會套用到文案上。

你可以在同一個「覆蓋素材」操作中隨時開關任何覆蓋，無論是還原原始場景的素材，或是進行快速的前後檢查

考慮到複製品是為了與原始資料相符而建立，在大多數情況下覆寫材料的外觀不會改變（見下方註解），除非你將物質圖連結到該材料或編輯其屬性。

>[!NOTE]
>
> 當套用覆寫時，Designer 會計算受影響網格的切線和雙法線，這可能需要一些時間並改變這些網格的側向，尤其是當這些網格沒有定義的法線縮放和偏壓，或使用不同的法線時。

>[!IMPORTANT]
>
> <b>AdobeStandardMaterial</b> 著色模型在 Substance 3D 生態系統中均支援，但並非業界標準，因此&#x200B;*第三方應用程式如 Blender 可能不支援*。
> 
> 為了在 Substance 3D 應用之外達到最佳互通性，目前建議使用 <b>UsdPreviewSurface 著色模型，即使該模型支援的材質屬性與效果遠低於 UsdPreviewSurface</b> 。

## 重置到場景狀態

如果你需要回到材質的初始狀態，同時保持覆蓋狀態並仍能編輯，任何材質複製都可以重置回初始值。

若材質屬性值被修改，或套用圖中的紋理，屬性會回復到原始值或紋理。

材料可以完全重置，或依屬性重置。

請使用材質子選單或網格的情境選單中的「將材質重置為場景狀態」動作，將材質完全重置。

該動作可在三個地點找到：

* 打開「材料」選單，進入所需材料的子選單
* 按場景物件上的 Shift+Lb 選擇該物件，然後點擊 RMB 開啟其上下文選單
* 漢堡菜單在該材料特性的頂端

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![將材質重置為場景狀態 - 在「3D VIew」視窗](overriding-scene-materials.resources/resetMaterialToSceneStateActionViewport.png "中執行動作 將材質重置為場景狀態 - 在「3D VIew」視窗中操作"){zoomable="yes"}

*3D 視角中的動作*

</td>
<td style="border: 0;" valign="top">

![將材質重置為場景狀態 - 在「材質」選單](overriding-scene-materials.resources/resetMaterialToSceneStateActionMaterials.png "中的動作 將材質重置為場景狀態 - 在「材質」選單中操作"){zoomable="yes"}

*材料選單中的動作*

</td>
<td style="border: 0;" valign="top">

![將材質重置為場景狀態 - 在「屬性」底座](overriding-scene-materials.resources/resetMaterialToSceneStateActionProps.png "中的動作 將材質重置為場景狀態 - 在「屬性」底座中執行動作"){zoomable="yes"}

*材料性質的作用*

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

這個動作也可以在材料屬性中依屬性&#x200B;*設定，*&#x200B;如果你只想重置材料的部分面向。

打開材質屬性的漢堡選單，找到「重置為預設場景狀態」的動作。

</td>
<td style="border: 0;" valign="top">

![重置到場景狀態 - 材質屬性](overriding-scene-materials.resources/resetPropertyToSceneStateAction.png "中的動作 重置場景狀態 - 材質屬性中的動作"){zoomable="yes"}

</td>
</tr>
</table>

## 連通材料

再說一次：Designer 不會直接修改場景的材質，而是在場景中建立一個複製品，並將網格綁定到該複製品上，而不是原始的。

另一方面，Designer 在「材質」選單中有 *自己的* 獨立材質清單，預設與場景材質清單相符。 您可以隨時在該清單中新增教材。

這是 *一組不同的* 資料，僅在 Designer 中撰寫和管理。 這些材質接著 *與複製品連結，複製品* 會覆蓋場景的原始素材。

![覆蓋材料 - 資料示意圖](overriding-scene-materials.resources/overridingMaterialsSchematic.png "覆蓋材料 - 資料示意圖"){zoomable="yes"}

你可以將「材質」選單中列出的任何材質連接到場景中由 Designer 建立的複製品：在場景瀏覽器點擊 RMB 複製品，然後進入「連接材質」子選單。

子選單列出場景中的所有材質，以及你可能從「材質」選單手動製作的材質。

![連結材料](overriding-scene-materials.resources/connectMaterials.gif "連結材料 連結"){zoomable="yes"}
