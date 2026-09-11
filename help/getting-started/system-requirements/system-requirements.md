---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/getting-started/system-requirements.html"
breadcrumb-title: ''
description: 請檢視 Substance 3D Designer 的系統需求，確保您的電腦符合必要規格。
helpx_creative_field: ""
helpx_description: Designer > Getting started > System requirements
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 系統需求
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '830'
ht-degree: 0%

---


# 支援系統

以下是該應用程式所支援的硬體與系統清單：

## 窗戶

|  | 最低限度 | 推薦 | 最佳 |
| --- | --- | --- | --- |
| <b>作業系統</b> | Windows 11 64 位元版本 23H2 | Windows 11 64 位元版本 24H1 | Windows 11 64 位元版本 24H2 |
| <b>中央處理器</b> | Intel Core i5 AMD Ryzen 5 | Intel Core i7 AMD Ryzen 7 | Intel Core i9 AMD Ryzen 9 |
| <b>GPU</b> | NVIDIA GeForce RTX 2060 超級 NVIDIA Quadro RTX 4000 AMD Radeon RX 5700 XT AMD Radeon Pro W5700 | NVIDIA GeForce RTX 3080、NVIDIA Quadro RTX A4000、AMD Radeon RX 6800 XT、AMD Radeon Pro W7700 | NVIDIA GeForce RTX 4090、NVIDIA Quadro RTX 5000、Ada 世代 AMD Radeon RX 7900、XTX AMD Radeon Pro W7800 |
| <b>VRAM</b> | 8 GB | 16 GB | 24 GB |
| <b>記憶體</b> | 16 GB | 32 GB | 64 GB |
| <b>儲存</b> | SSD 有 30 GB 可用空間 | SSD 有 50 GB 可用空間 | SSD 有 70 GB 可用空間 |

### MACOS

|  | 最低限度 | 推薦 | 最佳 |
| --- | --- | --- | --- |
| <b>作業系統</b> | macOS 14 Sonoma | macOS 26 Tahoe | macOS 26 Tahoe |
| <b>中央處理器</b> | 蘋果 M1 | 蘋果 M2 Pro | Apple M4 Pro |
| <b>GPU</b> | 蘋果 M1 | 蘋果 M2 Pro | Apple M4 Pro |
| <b>記憶體</b> | 16 GB | 32 GB | 64 GB |
| <b>儲存</b> | SSD 有 30 GB 可用空間 | SSD 有 50 GB 可用空間 | SSD 有 70 GB 可用空間 |

### Linux

| 企業號 | 蒸汽 |
| --- | --- |
| RHEL 8 </br>RHEL 9 | Ubuntu 22.04 |

## 一般建議

* 若在舒適環境下工作，我們建議使用解析度大於 1 百萬像素且寬度超過 1280 像素的螢幕。
* 許多 Substance 應用程式依賴 OpenSSL 1.1.1 來相容 RHEL8/9。 對於使用較新版本 OpenSSL 的系統，你需要手動提供。
* *只有* 2019.x</b> 及以上版本<b>經過公證，才能在 <b>MacOS 10.15</b>（Catalina）上運行。
* <b>若有 OpenGL 3.3 上下文，遠端桌面</b> 連線是可能的。 它在 Nvidia Quadro 上可用<b>，但在 *Nvidia GeForce 上不*&#x200B;行，因為它只提供 OpenGL 1.4 的</b>上下文。如果這是個問題，我們建議使用像 VNC/Teamviewer</b> 這類替代解決方案<b>。<b></b>
* <b>Steam</b> 版本用戶應 *關閉* <b>Steam 設計者覆蓋</b> 層，因為啟用時可能會造成效能問題。

## 支援的 GPU

以下是與該應用程式相容的 GPU 列表：

* NVIDIA GeForce GTX 1060 及以上版本
* NVIDIA Quadro P2200 及以上機型
* AMD Radeon RX 580 及以上版本
* AMD Radeon Pro 5300 M

>[!TIP]
>
> **TDR（僅限 Windows）**
> 
> 為了在執行大量 GPU 運算時保持最佳穩定性——例如渲染複雜圖形、在 3D 視圖中渲染、從 3D 視圖匯出場景等——強烈建議確保<b>逾時偵測與恢復（TDR）</b>值符合本頁[&#128279;](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/technical-support/technical-issues/gpu-issues/gpu-drivers-crash-with-long-computations-tdr-crash)文件中的建議。

## 不支援的配置

<b>窗戶</b>

* 不支援虛擬機。
* Windows Server 不支援。

<b>macOS</b>

* 不支援基於 Intel 的 macOS 系統。
* 僅支援官方蘋果配置。
* 目前不支援 eGPU，且可能存在穩定性問題。

<b>Linux</b>

* Linux 上的 Mesa 驅動程式不被支援。

<b>任何平台</b>

* 整合式 GPU 不支援 x86-64（Intel、AMD）CPU 的配置。
* 不支援將 Designer 與攔截 Designer 呼叫至圖形驅動程式的第三方軟體結合使用。 此類軟體包括：
  * 後製注入器，例如可套用色彩分級、攝影機效果等的重著色器......
  * 螢幕上的疊加層，例如自訂準星、GPU 效能指標、影片串流的皮膚......

## 最低 GPU 驅動程式版本

以下是應用程式正常運行所需的最低 GPU 驅動版本清單。 隨著新版本發布，此列表可能會有所變動。

要下載新驅動程式請參考： [GPU 驅動程式過](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/technical-support/technical-issues/gpu-issues/gpu-has-outdated-drivers)時。

| 作業系統 | NVIDIA | AMD | 英特爾 |
| --- | --- | --- | --- |
| <b>窗戶</b> | GeForce 451.48 Quadro 451.48 | Radeon 19.7.1 Radeon Pro / FirePro 18.Q4 | 15.33 |
| <b>Linux</b> | 535.129.03 | Radeon 23.20 Pro 23.Q3 | 無支撐 |

>[!NOTE]
>
> 在 Mac OS **上**，GPU 驅動程式是由作業系統本身提供。更新到作業系統最新版本以存取最新的驅動程式。

## GPU 光線追蹤用於烘焙

若要透過 Optix 或 DXR 啟用 GPU 光線追蹤，必須安裝上述推薦的驅動程式。

<b>DXR</b> 要求以下最低配置：

* <b>Windows 10</b> 版本 1809，請參閱 [此頁面](https://experienceleague.adobe.com/en/docs/substance-3d/bakers/features/gpu-raytracing) 以獲取更多資訊
* <b>採用 Pascal 架構</b> 的 GPU（Nvidia GeForce 10XX）

>[!TIP]
>
> GPU 光線追蹤在專用光線追蹤硬體上運行最佳，例如 NVIDIA GeForce RTX 或 NVIDIA Quadro RTX GPU。

## 使用平板

Windows 平板用戶<b></b>應依以下頁面所述設定，以獲得最可靠的體驗：[設定筆與平板](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/technical-support/configuring-pens-and-tablets)。

## 語言

軟體介面提供以下語言：

* 德意志（Deutschland）
* 英語（美國）
* 西班牙語（España）
* 法國
* 義大利人（Italia）
* 葡萄牙（巴西）
* 日本語（日本）
* 한국어(한국)
* 简体中文（中国)
