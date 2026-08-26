---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/resources/importing-linking-and-new-resources.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Designer 中匯入、連結並建立新資源，用於你的材料專案。
helpx_creative_field: ""
helpx_description: Designer > Resources > Importing, linking and new resources
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 匯入、連結與新資源
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '711'
ht-degree: 0%

---


# 匯入、連結與新資源

[Substance 3D Designer](https://www.adobe.com/tw/products/substance3d-designer.html) 支援三種模式，讓你能引入或創建新資源，用於你的圖表。 這些資源類型多樣，包括但不限於 [點陣](../../resources/bitmap-resource/bitmap-resource.md)圖、 [向量圖形](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md)、 [3D 場景](../3d-scene-resource/3d-scene-resource.md) 和 [字型](../../resources/font-resource/font-resource.md)。 本頁說明了不同的方法以及每種方法的最佳使用時機。

所有方法皆可透過在檔案總管中點擊套件上的右鍵鍵存取。

下表簡要概述了兩種方法在功能上的差異。

|                                                                                                                                                                         | 新增 | 匯入 | 連結 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| 圖（[實體圖](../../compositing-graphs/substance-compositing-graphs.md)、 [物質函數圖](../../function-graphs/function-graphs.md) | <div><img alt="（滴答聲）" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="（錯誤）" data-preserve-html="true" src="../../assets/error.svg"/></div> | <div><img alt="（錯誤）&quot; data-preserve-html=&quot;true" src="../../assets/error.svg"/></div> |
| [點陣圖](../../resources/bitmap-resource/bitmap-resource.md)、[向量圖形（SVG）](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md) | <div><img alt="（滴答聲）" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="（滴答聲）" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="（滴答聲）&quot; data-preserve-html=&quot;true" src="../../assets/check.svg"/></div> |
| 3D 場景、 [字型](../../resources/font-resource/font-resource.md) | <div><img alt="（錯誤）" data-preserve-html="true" src="../../assets/error.svg"/></div> | <div><img alt="（錯誤）" data-preserve-html="true" src="../../assets/error.svg"/></div> | <div><img alt="（滴答聲）&quot; data-preserve-html=&quot;true" src="../../assets/check.svg"/></div> |
| 建立在 SBS 檔案旁邊 | <div><img alt="（滴答聲）" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="（滴答聲）" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="（錯誤）&quot; data-preserve-html=&quot;true" src="../../assets/error.svg"/></div> |
| 可在 Designer 中編輯 | <div><img alt="（滴答聲）" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="（滴答聲）" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="（錯誤）&quot; data-preserve-html=&quot;true" src="../../assets/error.svg"/></div> |
| 外部剪輯會自動同步 | <div><img alt="（錯誤）" data-preserve-html="true" src="../../assets/error.svg"/></div> | <div><img alt="（錯誤）" data-preserve-html="true" src="../../assets/error.svg"/></div> | <div><img alt="（滴答聲）&quot; data-preserve-html=&quot;true" src="../../assets/check.svg"/></div> |
| 嵌入已發表的SBSAR中 | <div><img alt="（滴答聲）" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="（滴答聲）" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="（滴答聲）&quot; data-preserve-html=&quot;true" src="../../assets/check.svg"/></div> |

## 新資源

建立新資源意味著你的套件中的資源將從零開始建立。 所有僅由設計者開發的資源，例如實體圖和實體函數圖，只能以此方式建立。

一個特殊情況是當你建立新的 [點陣圖](../../resources/bitmap-resource/bitmap-resource.md)或 [SVG](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md) 時：這些檔案會顯示在你的檔案總管中，並像匯入的資源一樣運作，但不需要外部檔案。 它們可以在 Designer 中進行修改。 如果你不需要依賴外部編輯器，這種方式產生新的點陣圖和 SVG 很適合，例如你只想要快速簡單的向量圖形，或是簡單的繪製 2D 點陣遮罩。

## 進口資源

匯入資源意味著資源檔案會在你的 SBS 檔案旁（ *Graphname.resources* 資料夾）建立一個重複的資源檔案， [SVG 檔案](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md)除外。 有時也被稱為「嵌入」資源。

匯入資源後，可在 Designer [中使用點陣繪製工具](../../resources/bitmap-resource/bitmap-painting-tools/bitmap-painting-tools.md)或 [2D 視圖](../../interface/2d-view/2d-view.md)中的向量編輯[&#128279;](../../resources/vector-graphics-svg-res/vector-editing-tools/vector-editing-tools.md)工具，並置入圖表中。匯入的資源不再連結到其原始來源檔案：也就是說，如果你更改、移除或更新原本匯入的檔案，這對 Designer 中的資源沒有影響。

對於 [AxF 檔案](../../resources/axf-appearance-exchange/axf-appearance-exchange-format.md) ，流程會稍微複雜一些;Substance 圖和點陣圖資源是從 AxF 套件中建立的。 不過這些都仍可在各自的編輯器中編輯：圖表檢視或 2D 檢視。

>[!WARNING]
>
> 對於新套件，匯入和新資源在儲存套件之前不會儲存到磁碟。

## 連結資源

連結資源意味著 Designer 會從原始位置參考原始檔案，但在檔案總管中仍會以套件的一部分呈現。 你無法直接在 Designer 裡編輯實際的資源，只能把它當作圖表的元件或作為烘焙地圖的來源使用。

如果你知道需要在同時使用 Designer 工作時使用外部編輯器更新資源，連結是理想的選擇。 烘焙貼圖就是一個很好的例子：你可以讓 Designer 參考點陣圖組成外部烘焙應用程式，當這些檔案被更改時，它會自動重新載入並更新你的圖表。 同樣地，3D 場景只能連結，所以每次從 3D 應用程式匯出新的 FBX 檔案時，Designer 會自動更新 3D 視圖中使用的網格。 如果你是從這個網格烘焙地圖，就必須手動重新開始烘焙過程，理想狀況是點 RMB 並選擇「重新整理所有烘焙地圖」。

## 刪除資源

從套件刪除資源時， <b>會顯示確認項目移除</b> 對話框。 若移除過程中的任何項目被其他資源&#x200B;*（如 [Substance 圖](../../compositing-graphs/substance-compositing-graphs.md)中使用[的圖形實例](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)與[點陣資源](../../resources/bitmap-resource/bitmap-resource.md)）所參考，對話框將包含*&#x200B;警告及這些項目清單&#x200B;*。*

>[!NOTE]
>
> 我們建議對這些項目保持謹慎，並採取必要措施，預期 *刪除套件中項目可能導致的依賴性* 失效。\
> 這些行動可能包括 *在刪除前移除所有這些資源的使用* 。

![「資源被刪除」警告](../../assets/confirm-item-removal.png "「資源被刪除」警告"){width="512px"}
