---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/pipeline-and-project-configuration/retrieving-the-installation-path.html"
breadcrumb-title: ''
description: 學習如何取得 Substance 3D Designer 安裝路徑，用於腳本和自動化用途。
helpx_creative_field: ""
helpx_description: Designer > Pipeline and Project Configuration > Retrieving the installation path
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 取回安裝路徑
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 1%

---


# 取回安裝路徑

本頁彙整了根據版本與平台，如何取得 Substance 3D Designer](https://www.adobe.com/products/substance3d-designer.html) 安裝路徑[的資訊。

## 窗戶

### 創意雲端桌面

1. 開啟 <b>Windows 登錄檔編輯器</b> （regedit）
1. 請前往登錄檔鍵<b>：HKEY\_LOCAL\_MACHINE\Software\Microsoft\Windows\CurrentVersion\App Paths\
1. 打開名為 <b>Adobe Substance 3D 的子鍵Designer.exe</b>
1. 該金鑰的值包含應用程式執行檔安裝地點的路徑

>[!NOTE]
>
> 此登錄檔金鑰僅自版本 11.2 開始提供。\
> 對於較舊版本，安裝路徑可從 HKEY\_CURRENT\_USER\Software\Microsoft\Windows\CurrentVersion\ Explorer\FileExts 的檔案關聯中取得

### Substance 版本（獨立版）

1. 開啟 <b>Windows 登錄檔編輯器</b> （regedit）
1. 請前往登錄檔鍵<b>：HKEY\_LOCAL\_MACHINE\ SOFTWARE\Microsoft\Windows\CurrentVersion\Uninstall</b>
1. 找出與你應用程式版本 AppID</b> 相符<b>的子金鑰（見下表）
1. 該密鑰的值包含通往應用程式安裝位置的路徑

| 版本 | AppID |
| --- | --- |
| **版本 5.x** | {25E7D16D-1FBA-49EA-BF36-E2D6B20A9206} |
| **版本 6.x** | {09a302b1-8da8-4f62-b0cb-a208faa210f9} |
| **版本 7.x（2017.x）至 11.1** | {e9e3d6d9-3023-41c7-b223-11d8fdd691b9} |
| **版本 11.2（或更新版本）** | {662bb79f-5616-44e6-a84d-b3d6abebe002} |

### Steam 版

該應用程式安裝在 Steam 安裝資料夾的 steamapps/common/ 子資料夾中。

## macOS

在 Mac 上，該應用程式安裝於以下格式：

| 版本 | 路徑 |
| --- | --- |
| **11.2 或更新版本** | **/應用程式/Adobe Substance 3D Designer.app** |
| **遺產** | **/應用/物質 Designer.app** |

## Linux

在 Linux 上，rpm 套件的安裝路徑如下：

| 版本 | 路徑 |
| --- | --- |
| **11.2 或更新版本** | **/opt/Adobe/Adobe\_Substance\_3D\_Designer** |
| **遺產** | **/opt/寓言/實質\_Designer** |
