---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators.html"
breadcrumb-title: ''
description: 在 Substance 3D Designer 中存取遮罩產生節點，根據網格幾何與屬性建立遮罩。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 遮罩產生器
user-guide-description: ''
user-guide-title: ''
source-git-commit: c002fea6f396f09ccb3218bd290db812d8367dc4
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 0%

---


# 遮罩產生器

此類別包含一系列黑白遮罩產生節點。 根據烘焙的貼圖資訊，他們會產生遮罩，然後用來混合材質和其他效果。 這些節點類似 [於 Substance Painter 中的智慧面具](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/features/smart-materials-and-masks) 與 [生成器](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/content/creating-custom-effects/generators) 。

這些節點都需要 [烘焙地圖，](../../../../../bakers/bakers.md) 因為沒有 [烘焙地圖](../../../../../bakers/bakers.md) ，效果會很有限。

主要用途是將這些遮罩產生器與 [多通道材料](../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/material-filters.md)一起使用。 一旦產生遮罩，它就會被用作材質混合[&#128279;](../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/material-blend/material-blend.md)的遮罩。

此類別中一些有趣的節點包括：

* [滴落的鏽蝕](../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/dripping-rust/dripping-rust.md)
* [邊緣損害](../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/edge-damages/edge-damages.md)
* [從底部到頂部](../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/bottom-to-top/bottom-to-top.md)
* [面具製作者](../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/mask-builder/mask-builder.md)
