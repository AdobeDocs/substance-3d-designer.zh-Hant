---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/technical-issues/python-issues.html"
breadcrumb-title: ''
description: 排除 Substance 3D Designer 中 Python 腳本問題，包括外掛和 API 問題。
helpx_creative_field: ""
helpx_description: Designer > Technical issues > Python issues
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Python 問題
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 0%

---


# Python 問題

本頁列出與 Substance 3D Designer [Python API](../../scripting/scripting.md) 相關的技術問題，以及以 Python 實作的功能，並提供各項的故障排除步驟。

Python 實作的功能包括[檔案總管](../../interface/the-explorer-window/the-explorer-window.md)工具列中的[發佈](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md)/[發送操作](../../interface/the-explorer-window/send-to-interoperability/send-to-interoperability.md)，以及移除圖表中未使用的節點的工具。

## &#39;QtForPython&#39; 模組無法載入

<b>![（錯誤）](../../assets/error.svg) 問題</b>

Python 模組「QtForPython」無法載入，導致 Python 中實作的功能缺失，例如[檔案總管](../../interface/the-explorer-window/the-explorer-window.md)工具列中的[發佈](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md)/[發送動作](../../interface/the-explorer-window/send-to-interoperability/send-to-interoperability.md)，以及移除圖表中未使用的節點的工具。

此外，許多 [Python 插件](../../scripting/plugin-basics/plugin-basics.md) 會無法載入，或無法如預期運作。

<b>![（打了](../../assets/check.svg) 推薦步驟</b>

Designer 安裝的 QtForPython 及其相依套件，與系統上現有的安裝之間很可能存在衝突。

移除所有其他系統安裝的 QtForPython[&#128279;](https://doc.qt.io/qtforpython-5/index.html)（[PySide2](https://pypi.org/project/PySide2/)）和 [Shiboken2](https://pypi.org/project/shiboken2/)。

或者，你可以考慮使用像 rez **[&#128279;](https://github.com/AcademySoftwareFoundation/rez)*這樣的套件管理器*，取代系統層級的 QtForPython 安裝。
