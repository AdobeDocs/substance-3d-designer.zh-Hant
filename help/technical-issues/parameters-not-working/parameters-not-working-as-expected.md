---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/technical-issues/parameters-not-working-as-expected.html"
breadcrumb-title: ''
description: 排除 Substance 圖參數不正常的問題並尋找解決方案。
helpx_creative_field: ""
helpx_description: Designer > Technical issues > Parameters not working as expected
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 參數未如預期運作
user-guide-description: ''
user-guide-title: ''
source-git-commit: 21af965a075e8c119d16922f15b867da99c21397
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 0%

---


# 參數未如預期運作

本頁列出 Substance 3D Designer 參數無法正常運作的常見原因，並提供每個參數的故障排除步驟。

## 參數在預覽模式中無法運作，且已發佈的 Substance 3D 資產（SBSAR）

<b>![（錯誤）](parameters-not-working-as-expected.resources/error.svg) 子嗣</b>

在使用 [Designer 的預覽模式](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)時，或該圖發佈[&#128279;](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md)的 Substance 3D 資產（SBSAR）參數清單中，部分已暴露的圖形參數未&#x200B;*被列出*。

<b>![（滴答）](parameters-not-working-as-expected.resources/check.svg)建議步驟</b>

缺少的參數很可能[是靜態參數](../../glossary/glossary.md)，*圖在處理*&#x200B;完成後無法即時編輯&#x200B;**，以快速且有效率地執行演算法。每次圖表被 *編輯* 或 *發佈*&#x200B;時，Designer 都會進行煮食。 受此類限制影響的參數列於[本文件「暴露參數](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)」頁面的[限制](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)部分。

因此，靜態參數在 Designer 中可見且可編輯，但在已發佈的 Substance 3D 資產中則隱藏&#x200B;**。你可以使用 [預覽模式](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md) 查看這些限制的生效，然後再發佈到 Substance 3D 資產。

以下是靜態參數列表：

| 節點 | 參數 |
| --- | --- |
| 所有節點 | 平鋪模式像素比率 |
| [制服顏色](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/uniform-color/uniform-color.md) | 彩色模式 |
| [像素處理器](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md) | 彩色模式 |
| [混合](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md) | 混合模式 Alpha 混合 裁切區域 |
| [效果圖](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md) | 混合模式 |
| [象限](../../function-graphs/fxmaps/the-quadrant-node/the-quadrant-node.md) | 圖案輸入影像 alpha 輸入影像過濾 |

## 對參數應用的實質函數圖結果錯誤

<b>![（錯誤）](parameters-not-working-as-expected.resources/error.svg) 子嗣</b>

應用於節點參數的 Substance 函數圖，當使用負整數時，不會輸出預期值。

<b>![（滴答）](parameters-not-working-as-expected.resources/check.svg) 建議步驟</b>

負整數目前尚未得到適當支援。 作為一個變通方法，可以用 Integer2[&#128279;](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/constant-nodes/constant-nodes.md) 值中的負整數值，再用 [Swizzle 整](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/vector-and-swizzle-nodes/vector-and-swizzle-nodes.md)數節點提取它。
