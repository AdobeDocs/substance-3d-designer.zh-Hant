---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/resources/font-resource.html"
breadcrumb-title: ''
description: 在 Substance 3D Designer 中匯入並使用字型資源，為材質添加文字與排版。
helpx_creative_field: ""
helpx_description: Designer > Resources > Font resource
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 字型資源
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 0%

---


# 字型資源

字型資源是設計用來與 [原子文字節點](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md)一起使用的。 它們允許你使用系統中未安裝的字型，只要參考磁碟上任意的字型檔案即可。

>[!NOTE]
>
> **SBSAR 中的字型**
> 
> 字型總是嵌入在 SBSAR 中，無論是來自連結的資源，或是使用系統安裝的字型。 這種方法的優點是不需要安裝，且匯出有相依的 SBS 檔案時，字型檔案會隨附而來。

## 使用自訂字型資源

* 右鍵點擊套件，選擇 <b>「連結>字型」</b>
* 選擇.otf或.ttf檔案。
* 在你的圖表中放置一個[文字節點](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md)。](../../compositing-graphs/substance-compositing-graphs.md)[
* 在字型</b>屬性下<b>，任何字體資源都會在列表頂端找到。

請注意，字型列表在屬性開啟時不會自動重新整理。 你必須切換到另一個屬性視窗，再回到文字節點，才能看到新連結的字型。
