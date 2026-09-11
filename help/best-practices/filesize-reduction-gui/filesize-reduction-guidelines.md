---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/best-practices/filesize-reduction-guidelines.html"
breadcrumb-title: ''
description: 學習減少 Substance 圖檔案大小的指引，以優化效能與儲存需求。
helpx_creative_field: ""
helpx_description: Designer > Best Practices > Filesize Reduction Guidelines
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 檔案大小減少指引
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '822'
ht-degree: 0%

---


# 概觀

在某些情況下，Substance 3D 資產（SBSAR）[&#128279;](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md)的總檔案大小可能是一個重要因素。本頁涵蓋幾個關鍵領域與設定，建議在嘗試縮小檔案大小時留意。

檔案大小主要由 [嵌入的點陣圖決定。](../../resources/bitmap-resource/bitmap-resource.md) 這些檔案會連結、嵌入或烘焙，並作為資源加入  [Substance 3D Designer](https://www.adobe.com/products/substance3d-designer.html) 檔案（SBS）。 只有用於圖形中的位圖，也就是直接或透過節點鏈連接到輸出的位圖，才會被發佈在 Substance 3D 資產中。 在 Substance 3D 檔案中，點陣圖對檔案大小沒有影響，因為所有點陣資源仍儲存在檔案外部。

>[!IMPORTANT]
>
> 確保所有位圖[&#128279;](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md)節點的輸出大小[&#128279;](../../compositing-graphs/output-size/output-size.md)屬性都設定為&#x200B;*絕對[*&#x200B;繼承方法](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)。若非如此，其參考 [點陣圖資源](../../resources/bitmap-resource/bitmap-resource.md) 將以預設的 256\*256 解析度儲存在已發佈的 Substance 3D 資產檔案中，這會影響*&#x200B;一個或多個輸出的品質* 。

## 檔案大小因素

影響SBSAR總檔案大小有幾個不同的因素。 以下列出這些問題，並附有簡短說明。

+++解決方法
顯然影響很大。 盡量用最小解析度，記得你可能也希望 Substance 檔案能支援高解析度。 你可以用標準的解析度遮罩技巧，讓較小的位圖看起來更大。

*可在：外部軟體中找到，或在 Designer 中匯入/重新匯出點陣圖。*

+++

+++檔案色彩模式
在匯出前，在影像編輯器中設定好顏色模式，使用原始點陣圖格式時也會影響檔案大小。 僅灰階的點陣圖比 RGB（A） 影像小。

*可在外部軟體中找到，或在 Designer 中正確設定 [輸出節點](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) 時匯入/重新匯出點陣圖。*

+++

+++檔案格式
你的影像檔案格式會影響，雖然在某些情況下可以忽略。 像 Photoshop 這類軟體能稍微控制 JPG 壓縮，有時也能提供不錯的折衷方案。

*可在：外部軟體中找到，或在 Designer 中匯入/重新匯出點陣圖。*

+++

+++圖中的應用
你設定點陣圖節點的模式也會影響 Designer 如何壓縮檔案，使用灰階模式檔案作為圖形中的彩色點陣圖，檔案會變大。 務必正確設定這些！

*可於：[Bitmap Node properties 找到。](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md)*

+++

+++點陣圖格式封裝
在資源屬性中，你可以選擇「原始」或「JPEG」壓縮。 這對最終結果會有相當大的影響。

*可於：點陣資源屬性，透過總管視窗找到。*

+++

+++點陣圖壓縮品質套件
使用「Jpeg」點陣圖格式時，下方的滑桿會影響畫質和檔案大小。 這個滑桿的行為不太可預測，但 1 通常對應最高品質的 JPG 壓縮，0.5 則是最小的壓縮。

*可於：點陣資源屬性，透過總管視窗找到。*

+++

+++發佈時的壓縮模式
發佈到 SBSAR 時，你可以選擇「自動」、「最佳」或「無」來壓縮，如果你使用「原始」點陣圖格式，這些選項會有相當大的差異。 這對出口速度也有很大影響。 一般不建議使用「無」，因為它不會提升品質。

*在：SBSAR 套件的最終出版設定中。*

+++

## 檔案大小比較

下表顯示所有設定彼此之間的影響。 所使用的點陣圖為一張 4096x4096 的產生雜訊影像，從 Photoshop 匯出為 24 位元 TGA 或 JPG，品質為 8。 TGA 也曾以灰階和 RGBA 模式匯出。

圖只是將一個位圖節點連接到單一輸出。 點陣模式依據原始檔案模式設定。

雖然右側表格尚未完全決定性，但從比較視覺結果與檔案大小時可得以下資訊：

* 原始位圖+壓縮最佳能提供最佳畫質且檔案大小合理。
* 預壓縮的原始碼檔案在大多數情況下可提供較小的檔案大小，但品質成本較高。
* 檔案大小最小，但品質最差的是 JPG 套件格式，品質為 0.5。
* 灰階檔案大小不一定比較小，但在相似設定下，畫質會比彩色高。

>[!NOTE]
>
> **JPEG 點陣格式**
> 
> 值得注意的是，需要高精度的特殊貼圖，如法線貼圖、向量貼圖等，可能不應該設成 Jpeg 壓縮，因為這會導致更多明顯的瑕疵！

| 原始圖片 | 彩色TGA | 彩色 JPG | 灰階TGA | 灰階JPG |
| --- | --- | --- | --- | --- |
| <b>原始點陣圖格式</b> 壓縮模式： *無* | 48 MB | 48 MB | 16 MB | 16 MB |
| <b>原始點陣圖格式</b> 壓縮模式： *最佳* | 9.11 MB | 3.37 MB | 5.06 MB | 4.75 MB |
| <b>JPEG 點陣圖格式</b> 壓縮品質： *1* | 5.09 MB | 1.94 MB | 6.30 MB | 2.49 MB |
| <b>JPEG 點陣圖格式</b> 壓縮品質： *0.5* | 231 KB | 230 KB | 626 KB | 569 KB |
| <b>JPEG 點陣圖格式</b> 壓縮品質： *0* | 407 KB | 433 KB | 990 KB | 808 KB |
