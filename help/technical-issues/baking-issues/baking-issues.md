---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/technical-issues/baking-issues.html"
breadcrumb-title: ''
description: 尋找與 Substance 3D Designer 中烘焙貼圖相關技術問題的故障排除步驟。
helpx_creative_field: ""
helpx_description: Designer > Technical issues > Baking issues
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 烘焙問題
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 0%

---


# 烘焙問題

本頁列出了與 [Substance 3D Designer 中烘焙貼圖](../../bakers/bakers.md) 相關的技術問題，並提供每個問題的故障排除步驟。

## 在本頁

「以姓名配對」無法使用

## 「以姓名配對」無法使用

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<b>![（錯誤）](../../assets/error.svg) 問題</b>

當「匹配」選項設為「依網格名稱」時，匹配似乎沒有套用，或在所有場景物件間不一致。

<b>![（打了](../../assets/check.svg) 推薦步驟</b>

在 Designer 14.1 及以下版本中，低多邊形與高多邊形物件會以其父物件的名稱&#x200B;**&#x200B;來匹配——大多數情況下，是父物件的變換。

自 Designer 15.0 起， *幾何* 物件名稱直接使用。

</td>
<td style="border: 0;" valign="top">

![場景樹](../../assets/sceneTree_objectsName.png "中的幾何物件及其父節點幾何物件及其場景樹中的父節點"){zoomable="yes"}

</td>
</tr>
</table>

你可以走兩條路來達到預期的 macthing：

* 調整幾何物件名稱以套用相符的名稱。
* 可透過專案設定中的「名稱過濾模式」[&#128279;](../../interface/preferences-window/project-settings/project-settings.md)選項，回復到行為或先前的 Designer 版本：
  1. 前往編輯>偏好設定>專案
  1. 選擇列表中最後一個專案檔案
  1. 在專案檔案清單下方，選擇「Bakers」標籤
  1. 將「名稱過濾模式」設為「父名稱（舊有）」
