---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/resources/bitmap-resource.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Designer 中匯入、建立及使用點陣圖資源，以製作基於材質的材質。
helpx_creative_field: ""
helpx_description: Designer > Resources > Bitmap resource
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 點陣圖資源
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '648'
ht-degree: 0%

---


# 點陣圖資源

點陣圖資源是物質套件中的一個資源。 它與 [原子點陣節點不同。 原子點陣節點](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md)是該位圖在 Substance 圖](../../compositing-graphs/substance-compositing-graphs.md)中[的特定表示。

點陣圖是 Substance 3D Designer 中最常見的非圖形資源之一，通常其使用範圍屬於以下類別之一：

* 一個烘焙的地圖，可以由 [Designer](../../bakers/bakers.md) 內部烘焙，或由其他外部應用程式烘焙。
* 輔助材質，比如圖案、grunge 地圖或貼紙。
* 一個簡單的灰階遮罩用於混合，可以是透過 [點陣圖節點](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md)內部建立，或是透過外部應用程式製作。

## 點陣圖儲存

點陣圖通常是 Designer 處理的最大資源。 所以你應該了解 Designer 如何處理這兩種主要檔案類型。

### 在Substance 3D檔案（SBS）中

點陣圖在 SBS 中如何儲存取決於你 [是用連結還是匯入，先確定你熟悉這個概念。](../../resources/importing-linking-and-new/importing-linking-and-new-resources.md) 匯入的點陣圖可以用點陣圖繪製工具](../../resources/bitmap-resource/bitmap-painting-tools/bitmap-painting-tools.md)進行[編輯。

與 SVG（向量圖形）資源不同，點陣圖總是儲存在外部，即使是新建立的資源或匯入的。 對於新的 Substance Package，它們會被保存在記憶體中，直到SBS 檔案被儲存到磁碟中。 儲存到磁碟後，點陣圖會儲存在 SBS 檔案旁的 */resources* 資料夾中。

### 在 Substance 3D 資產（SBSAR）中

在 SBSAR 檔案](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md)中[，位圖是嵌入的，這表示它們對最終的 SBSAR 檔案大小有很大影響。你可以在本頁進一步閱讀更多關於檔案大小影響的資訊。 當 SBSAR 檔案發布時，僅嵌入用於計算圖形輸出的位圖。 未使用的點陣圖會被優化並排除於最終的 SBSAR 套件中，且不影響檔案大小。

## 檔案類型、色彩模式與解析度

Substance 3D Designer 可以輕鬆編輯並重新排列點陣圖資料，但最好記住以下幾點：

* 把解析度設成 2 的冪方，也就是跟標準即時材質大小，例如 <b>256、512、1024、2048</b> 等。Designer 會把超出這個範圍的材質縮放到最接近的解析度。 請注意，它們不一定要是正方形比例。
* 支援多種檔案類型，但請選擇最適合你使用情境的一種。 <b>無損壓縮，甚至像 PNG 或 TGA 這類未壓縮</b> 檔案類型，畫質比 JPG 或 DDS 更好。
* 根據你需要色階、灰階還是 alpha 通道，務必正確<b></b>設定你的色彩模式。

## 位圖屬性

套件中的點陣資源有許多屬性可供自訂。 大多數屬性沒有主要用途，主要用於函式庫過濾器，雖然少數屬性會影響檔案大小......

| 屬性名稱 | 目的 |
| --- | --- |
| 識別碼 | 用於參考套件中的位圖資源，必須是唯一的。 |
| 檔案路徑 | 資源參考的點陣圖在磁碟上的路徑。 |
| 說明 | 此說明顯示於 [本資源的探索器](../../interface/the-explorer-window/the-explorer-window.md) 與 [圖書館](../../interface/the-library/the-library.md) 工具提示中。 |
| 類別 | 用於[圖書館的資源](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md)[](../../interface/the-library/the-library.md)整理與整理。 |
| 標籤 | 用於[圖書館的資源](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md)[](../../interface/the-library/the-library.md)整理與整理。 |
| 作者 | 用於[圖書館的資源](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md)[](../../interface/the-library/the-library.md)整理與整理。 |
| 作者網址 | 用於[圖書館的資源](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md)[](../../interface/the-library/the-library.md)整理與整理。 |
| 標記 | 用於[圖書館的資源](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md)[](../../interface/the-library/the-library.md)整理與整理。 |
| 使用者資料 | 可選的額外資料，不用於點陣圖。 |
| 圖書館節目 | 判斷點陣圖是否應該隱藏在 [庫檢視中。](../../interface/the-library/the-library.md) |
| 點陣格式 | 不管是 Raw 還是 Jpeg，對 SBSAR 檔案大小都有很大影響。 請參閱我們的 [檔案大小縮小指南](../../best-practices/filesize-reduction-gui/filesize-reduction-guidelines.md) 以了解更多資訊。 |
| 位圖壓縮品質 | 只有在 Jpeg 壓縮時才會影響，決定品質和檔案大小的平衡。 |

## 檔案大小縮小

請參閱[最佳實務](../../best-practices/best-practices.md)區的檔案大小減少指引](../../best-practices/filesize-reduction-gui/filesize-reduction-guidelines.md)頁面[，了解我們關於縮小嵌入[已發佈 Substance 3D 資產（SBSAR）](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md)中位圖檔案大小的建議。
