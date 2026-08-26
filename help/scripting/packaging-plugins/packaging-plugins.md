---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/scripting/packaging-plugins.html"
breadcrumb-title: ''
description: 學習如何將 Python 外掛打包到 Substance 3D Designer 的發行與安裝。
helpx_creative_field: ""
helpx_description: Designer > Scripting > Packaging plugins
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 封裝插件
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 2%

---


# 封裝插件

## 插件套件內容

套件是一個單一檔案，內部為壓縮壓縮檔，內含 **包含外掛的 pluginInfo.json** 檔案，內含關於該外掛的元資料，

外掛程式碼，以及外掛運作所需的其他檔案或資源。

**PluginInfo.json條目：**

| 參賽 | 說明 | 預設值 | 註釋 |
| --- | --- | --- | --- |
| 元資料\_format\_version | 元資料檔案的格式。 | 1 | 必須。目前必須設定為 1。 |
| 名稱 | 插件名稱。 |  | Required.必須與包含外掛程式碼的 Python 模組名稱相符 |
| 版本 | 外掛版本。 |  | 選填。 |
| 作家 | 外掛作者。 |  | 選填。 |
| 電子郵件 | 外掛作者的電子郵件。 |  | 選填。 |
| Min\_designer\_version | 外掛所需的最低版本應用程式。 | 2019.2 | 選填。 |
| 平台 | 外掛運行的平台。 | 任何 | 可選。對於包含編譯程式碼的外掛，此條目可用於在非支援平台上停用該外掛。可能的數值：win、linux、osx、任意。 |

## 建立新的插件套件專案

我們提供 [一個 Cookiecutter](https://cookiecutter.readthedocs.io/en/latest/) 範本專案，以簡化外掛套件專案的建立。

你可以直接使用它，或是根據自己的需求修改它。

範本可在應用程式目錄中，於 <b>plugins/tools/pkgplugintemplate</b> 下找到。

1. <b>如果你系統裡還沒安裝 Python，請安裝它</b>

   Cookiecutter 相容於 Python 2 與 Python 3
1. <b>如果你還沒有 Cookiecutter，建議安裝</b>

   通常可以透過使用pip來完成：

   ```
   pip install cookiecutter
   ```


   想用其他方式安裝 Cookiecutter，或想了解更多關於 Cookiecutter 的資訊，可以參考相關文件。 <https://cookiecutter.readthedocs.io/en/latest/installation.html>
1. <b>建立一個新的外掛套件專案</b>

   在終端機視窗執行中：

   ```
   cookiecutter path/to/pkgplugintemplate -o path/to/new/project
   ```


   填寫所需資訊。 新專案會在指定的目錄中建立。
1. <b>開發完成後再打包你的外掛</b>

   在終端機視窗執行中：

   ```
   python makepackage.py
   ```

1. 插件套件會在建置目錄中產生
