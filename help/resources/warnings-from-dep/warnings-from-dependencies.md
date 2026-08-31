---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/resources/warnings-from-dependencies.html"
breadcrumb-title: ''
description: 了解 Substance 3D Designer 中資源依賴的警告，以及如何解決它們。
helpx_creative_field: ""
helpx_description: Designer > Resources > Warnings from dependencies
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 依賴性警告
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '1158'
ht-degree: 0%

---


# 依賴性警告

本頁列出可能因 Substance 3D Designer 相依性觸發的警告與錯誤訊息，並提供每種常見的故障排除步驟。

相依關係是 *Substance 3D 檔案（SBS）所參考的其他檔案* 。 它們包含[&#128279;](../../resources/resources.md)資源及其他由[圖形實例](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)節點參考的 Substance 3D 檔案。

## ![（錯誤）](warnings-from-dependencies.resources/error.svg) 無效的依賴套件

相依套件無法載入，因為它缺少、損壞或與所使用的 Designer 版本不相容。

<b>![（勾選）]（warnings-from-dependencies.resources/check.svg）解決方案</b>

解決此問題主要有兩種方法：

1. <b>成功讓相依載入成功</b>

   檢查相依套件是否存在於警告訊息中指定的位置。 如果沒有，就找到該檔案放回原位，或重新建立。 如果檔案存在，試 *著在 Designer 載入，* 並留意是否有與該套件相關的警告或錯誤。 參考針對這些特定問題的故障排除步驟，並相應地修正。

   接著，在檔案總管[&#128279;](../../interface/the-explorer-window/the-explorer-window.md)面板點擊 RMB 鍵，並在情境選單中選擇 <b>Reload</b> 選項，重新載入主機套件。

   ![「無效相依套件」解決方案 1](warnings-from-dependencies.resources/warnings-from-dependencies-01.gif "&#39;無效相依套件」解決方案 1")
1. <b>重新定位套件中的相依</b>

   你可以用 [依賴管理器](../../interface/dependency-manager/dependency-manager.md) 重新定位相依。 在檔案總管[&#128279;](../../interface/the-explorer-window/the-explorer-window.md)面板中點選主機套件的 RMB，然後在情境選單中選擇<b>相依性管理器</b>選項。

   在 Dependendy Manager 的清單中找到缺少的依賴，點選 RMB 並選擇 <b>「重新定位...</b> 」選項。 使用檔案瀏覽器對話框找到相依套件並點選 <b>「開啟</b>」。

   接著，在檔案總管[&#128279;](../../interface/the-explorer-window/the-explorer-window.md)面板點擊 RMB 鍵，並在情境選單中選擇 <b>Reload</b> 選項，重新載入主機套件。

   ![「無效相依套件」解決方案 2](warnings-from-dependencies.resources/warnings-from-dependencies-02.gif "&#39; 無效相依套件」解決方案 2")

## ![（錯誤）](warnings-from-dependencies.resources/error.svg)請檢查你的專案中定義了別名&#x200B;*「X」*

套件的一個相依或資源正從一個在 Substance 3D 檔案（SBS）資料中被 [別](../../interface/preferences-window/project-settings/project-settings.md) 名化的地點載入，該別名在警告中報告的別名下，儘管該別名並未在目前 [專案檔案](../../interface/preferences-window/project-settings/project-settings.md)中定義。

<b>![（勾選）]（warnings-from-dependencies.resources/check.svg）解決方案</b>

至少有一個 [專案檔案](../../interface/preferences-window/project-settings/project-settings.md) 應該定義警告中報告的別名。

![「檢查別名已定義」解](warnings-from-dependencies.resources/warnings-from-dependencies-03.gif "答「檢查別名已定義」解法")

## ![（錯誤）](warnings-from-dependencies.resources/error.svg) 找不到與此資源相符的檔案

無法找到與 UDIM 範本&#x200B;*相符*&#x200B;的[點陣圖資源](../../resources/bitmap-resource/bitmap-resource.md)檔案。

<b>![（勾選）]（warnings-from-dependencies.resources/check.svg）解決方案</b>

當 [一個點陣圖資源](../../resources/bitmap-resource/bitmap-resource.md) 被連結，且 Designer 偵測到其檔名中有 *UDIM 命名分類法* 時——例如 `0x1` 在 `my_texture_0x1.png`中，它會提供將其連結為 *UDIM 範本*，讓 [點陣](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md) 圖節點能 *在使用 Designer 的 UDIM 工作流程時，自動切換* 到使用該分類法的 UDIM 點陣圖集合中其他位圖。 在這種情況下，Designer 會以不同方式&#x200B;*連結點陣資源*，並考慮 UDIM 編號範本。

解決此問題主要有兩種方法：

1. <b>還原檔案</b>

   前往資源 <b>檔案路徑</b> 屬性指定的位置，檢查範本後的檔案是否存在。 如果沒有，就還原或重新製作。

   ![「沒有檔案匹配資源」解決方案1](warnings-from-dependencies.resources/warnings-from-dependencies-04.gif "「沒有檔案匹配資源」解決方案1")
1. <b>重新定位檔案</b>

   若檔案被移動或重新命名，請在檔案總管[&#128279;](../../interface/the-explorer-window/the-explorer-window.md)面板中點擊資源項目的 RMB 鍵，選擇<b>「重新定位</b>」選項，將該資源連結到&#x200B;*同一類型 UDIM 映像檔*&#x200B;中的第一個檔案。

   ![「沒有符合資源的檔案」解決方案2](warnings-from-dependencies.resources/warnings-from-dependencies-05.gif "「沒有符合資源的檔案」解決方案2")

## ![（錯誤）](warnings-from-dependencies.resources/error.svg) 找不到連結檔案

連結資源所參考的檔案不存在於其 <b>檔案路徑</b> 屬性所指定的位置。

<b>![（勾選）]（warnings-from-dependencies.resources/check.svg）解決方案</b>

解決此問題主要有兩種方法：

1. <b>還原檔案</b>

   前往資源 <b>檔案路徑</b> 屬性指定的位置，檢查該檔案是否存在。 如果沒有，就還原或重建它。

   ![「找不到連結檔案」解決方案 1](warnings-from-dependencies.resources/warnings-from-dependencies-06.gif "&#39;找不到連結檔案」解決方案 1")
1. <b>重新定位檔案</b>

   如果檔案被移動或重新命名，請在檔案總管[&#128279;](../../interface/the-explorer-window/the-explorer-window.md)面板中點擊資源項目的 RMB，並選擇<b>重新定位</b>選項，將該資源連結到同類型的另一個檔案。

   ![「找不到連結檔案」解決方案 2](warnings-from-dependencies.resources/warnings-from-dependencies-07.gif "&#39;找不到連結檔案」解決方案 2")

## ![（錯誤）](warnings-from-dependencies.resources/error.svg) 找不到色彩空間

[點陣圖資源](../../resources/bitmap-resource/bitmap-resource.md)參考的色彩空間在目前[的色彩管理](../../color-management/color-management.md)環境中無法找到。這可能是 ICC 設定檔，或是 OCIO 配置中的色彩空間。

<b>![（勾選）]（warnings-from-dependencies.resources/check.svg）解決方案</b>

色彩空間屬性的選項列表會自動填入可用的有效色彩空間。 將該資源的色彩空間值改為列表中的其他項目。

或者，將該色彩空間加入目前的 [色彩管理](../../color-management/color-management.md) 環境，然後重新啟動 Designer。 這可能是 ICC 設定檔，或是 OCIO 配置中的色彩空間。

>[!NOTE]
>
> 此警告僅在使用除 **Legacy** 以外的色彩管理模式時觸發（類似於關閉色彩管理）。 你可以在&#x200B;**專案設定[&#128279;](../../interface/preferences-window/project-settings/project-settings.md)的色彩管理**&#x200B;區段啟用色彩管理。

![「找不到色彩空間」的解](warnings-from-dependencies.resources/warnings-from-dependencies-08.gif "法「找不到色彩空間」的解法")

## ![（錯誤）](warnings-from-dependencies.resources/error.svg) 找不到參考資源

分配給 3D 場景資源[&#128279;](../3d-scene-resource/3d-scene-resource.md) UV 圖塊的圖形，無法在警告中報告的位置找到。

<b>![（勾選）]（warnings-from-dependencies.resources/check.svg）解決方案</b>

解決此問題主要有兩種方法：

1. <b>還原該圖</b>

   請在 Explorer[&#128279;](../../interface/the-explorer-window/the-explorer-window.md) 面板中檢查 UV Tiles</b> 列表中指定的<b>圖表。如果不存在，就還原或重建它。

   ![「找不到參考資源」解決方案 1](warnings-from-dependencies.resources/warnings-from-dependencies-09.gif "&#39;找不到參考資源」解決方案 1")
1. <b>選擇另一張圖</b>

   在套件中再指派一個圖給 UV 圖塊。

   ![「找不到參考資源」解決方案 1](warnings-from-dependencies.resources/warnings-from-dependencies-10.gif "&#39;找不到參考資源」解決方案 2")

## ![（錯誤）](warnings-from-dependencies.resources/error.svg) UV 圖塊會被多次指定

3D 場景資源[&#128279;](../3d-scene-resource/3d-scene-resource.md)的 UV 圖塊會被多次指派到 [Substance 圖](../../compositing-graphs/substance-compositing-graphs.md)。

<b>![（勾選）]（warnings-from-dependencies.resources/check.svg）解決方案</b>

對於每個 3D 網格資源的 UV 集合，請確保 UV 圖塊</b>列表中沒有重複<b>*出現的 UDIM 索引*。

![「UV圖塊被多次指派」解](warnings-from-dependencies.resources/warnings-from-dependencies-11.gif "法「UV圖塊被多次指派」解法")

## ![（錯誤）](warnings-from-dependencies.resources/error.svg) 無效的 UV 圖塊

列出的  [3D 場景資源](../3d-scene-resource/3d-scene-resource.md) UV 磚塊在網格中未定義或損壞。

<b>![（勾選）]（warnings-from-dependencies.resources/check.svg）解決方案</b>

對於 3D 網格資源的每個 UV 集合，請確保 UV 磚</b>塊清單中<b>的所有項目都指向連結資源中存在&#x200B;*的 UDIM*&#x200B;元素。

>[!NOTE]
>
> 此警告無法透過使用者介面觸發，因為它 *只* 列出連結資源中偵測到的 UDIMS。 只有直接&#x200B;*修改 Substance 3D 檔案（SBS*）中的資料才會觸發此警告。

![「無效 UV 圖塊」解決方案](warnings-from-dependencies.resources/warnings-from-dependencies-12.gif "「無效 UV 圖塊」解決方案")
