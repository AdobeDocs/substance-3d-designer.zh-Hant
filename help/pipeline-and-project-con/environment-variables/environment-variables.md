---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/pipeline-and-project-configuration/environment-variables.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Designer 中使用環境變數來設定路徑和系統設定。
helpx_creative_field: ""
helpx_description: Designer > Pipeline and Project Configuration > Environment variables
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 環境變數
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---


# 環境變數

本頁列出可用來覆寫應用程式預設行為的環境變數。

| 變數 | 說明 |
| --- | --- |
| **SBS\_DESIGNER\_PYTHON\_PATH** | Designer 會從中載入 [Python 外掛](../../scripting/plugin-basics/plugin-basics.md)的路徑。 |
| **內容\_DESIGNER\_LICENSE** | 授權檔案&#x200B;*（license.key*）的位置，應該由 Designer 使用。 會覆蓋設計師 [啟動精靈](../../getting-started/activation-and-licenses/activation-and-licenses.md)設定的路徑。  **注意：**  舊版本可能需要使用替代變數名稱：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>SUBSTANCE_DESIGNER_6_LICENSE</strong></li><li data-preserve-html="true"><strong>SUBSTANCE_DESIGNER_5_LICENSE</strong></li></ul> |
| <b>OCIO</b> | 使用OpenColorIO [色彩管理](../../color-management/color-management.md)時應使用的OCIO設定檔路徑。 覆蓋 Designer 在專案設定[&#128279;](../../interface/preferences-window/project-settings/project-settings.md)中色彩管理設定中的路徑設定。 |
| **阿勒_LICENSE\_IDLE\_DELAY** | 多用戶設定時，釋出授權席位的延遲為 7200 秒（2 小時）。 |
