---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/scripting/plugin-search-paths.html"
breadcrumb-title: ''
description: 在 Substance 3D Designer 中設定插件搜尋路徑，指定 Python 插件的位置。
helpx_creative_field: ""
helpx_description: Designer > Scripting > Plugin search paths
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 插件搜尋路徑
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 0%

---


# 插件搜尋路徑

Designer 會在特定目錄（例如搜尋路徑）中尋找外掛。 本頁說明如何配置這些路徑。

使用者可在 *軟體偏好設定中手動新增自訂目錄* ，或使用環境變數指定。

## 手動新增外掛搜尋路徑

1. 前往 <b>編輯>偏好設定...</b>
1. 選擇 <b>專案</b>類別
1. 選擇<b>你想編輯的專案檔案</b>
1. 在 <b>Python</b> 標籤中，點擊 *<b>+</b>*按鈕以新增包含外掛的目錄
1. 點擊<b>確定</b>以驗證

![設定 up Python 插件 搜尋路徑 專案設定](../../assets/image-70.png "Up Python 插件搜尋路徑 專案設定")

## 使用環境變數

應用程式會在所有路徑中尋找外掛，這些路徑使用 <b>SBS\_DESIGNER\_PYTHON\_PATH </b>環境變數。
