---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/technical-issues/application-does-not-start.html"
breadcrumb-title: ''
description: 排除阻礙 Substance 3D Designer 啟動的問題，並尋找啟動應用程式的解決方案。
helpx_creative_field: ""
helpx_description: Designer > Technical issues > Application does not start
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 申請不會開始
user-guide-description: ''
user-guide-title: ''
source-git-commit: f320cf6842ff56ac24912ceda264f30c28317c05
workflow-type: tm+mt
source-wordcount: '844'
ht-degree: 0%

---


# 申請不會開始

本頁列出 Substance 3D Designer 無法正確啟動的常見原因，並依作業系統分類提供各項故障排除步驟：

[設計師 15.0 及以上版本](#version-15-0)

[Windows 10/11](#windows-10-11)

[Windows 7/8/8.1](#windows-7-8)

[Linux](#linux)

## 設計師 15.0 及以上版本

<b>![（錯誤）](../../assets/error.svg) 問題</b>

Designer 15.0 及以上版本無法在同時配備整合 GPU（iGPU）與獨立 GPU（dGPU）的系統上啟動。

<b>![（打了](../../assets/check.svg) 推薦步驟</b>

更新 iGPU 的顯示卡驅動程式。 你可以在這裡找到最新的驅動程式： [Intel](https://downloadcenter.intel.com/product/80939/Graphics-Drivers) | [AMD](https://www.amd.com/en/support/download/drivers.html)

## Windows 10/11

**![（錯誤）](../../assets/error.svg)子嗣**

Substance 3D Designer 在使用 Windows 10 或 Windows 11 的系統上無法啟動。

**![（滴答）](../../assets/check.svg)建議步驟**

舊版 Designer 可能因授權驗證過程中使用的過時&#x200B;*`libeay32.dll`函式庫而無法在 Windows 10 或 Windows 11*&#x200B;上啟動。

你可以嘗試用&#x200B;*更新版本*&#x200B;取代函式庫，例如這裡[&#128279;](https://support.networkoptix.com/hc/en-us/articles/115015730007-Nx-Software-crashes-due-to-libeay32-dll-on-Windows)發佈的版本（選擇 32-bit Windows 的檔案），方法是依照以下步驟操作：

1. 在 Designer 的安裝目錄中找到該 `libeay32.dll` 檔案
1. 如果以後需要還原，記得把檔案備份到安全的地方
1. 將檔案替換為更新版本
1. Start Designer

>[!WARNING]
>
> 不支援的配置
> 
> Windows 10 不支援。 你可以在 [系統需求](../../getting-started/system-requirements/system-requirements.md) 頁面了解更多。
> 
> 已過維護期的 Designer 版本不被支援。 若系統有重大變更，例如作業系統升級，這些版本可能無法穩定運行。

## Windows 7/8/8.1

**![（錯誤）](../../assets/error.svg)子嗣**

Substance 3D Designer 在使用 Windows 7、Windows 8 或 Windows 8.1 的系統上無法啟動。

**![（滴答）](../../assets/check.svg)建議步驟**

作為 11.3.0 **版本**&#x200B;更新的一部分，我們升級了多個圖書館、工具和 SDK，導致&#x200B;*與低於 Windows 10 版本的相容*&#x200B;性下降。

我們 *強烈* 建議升級到 Windows 10，因為 Microsoft 本身已不再支援主流使用的舊版本 Windows（詳見 [此處](https://www.microsoft.com/en-us/windows/windows-7-end-of-life-support-information) 與 [此處](https://docs.microsoft.com/en-us/lifecycle/faq/windows#windows-8.1)）。 因此，持續使用這些版本會 *帶來安全問題*。\
如果無法升級到 Windows 10， *請不要將* Designer *安裝更新到* **11.2.2** 之後。

>[!WARNING]
>
> 不支援的配置
> 
> 請注意，Windows 7、Windows 8 和 Windows 8.1 均&#x200B;*未獲得官方支援*。 你可以在[系統需求](../../getting-started/system-requirements/system-requirements.md) 頁面了解更多。

## Linux

<b>![（錯誤）](../../assets/error.svg) 問題</b>

關閉主畫面並顯示主視窗時會當機。

<b>![（打了](../../assets/check.svg) 推薦步驟</b>

Designer 無法載入 Python 元件，因為它載入的是系統的 <b>libffi.so</b> 函式庫，而非系統自身。

為了確保 Designer 能載入自己的函式庫，請在 Designer 的安裝目錄中使用此指令，並用你執行 Designer 的指令替換 `%command%` ：

```
LD_PRELOAD=./plugins/pythonsdk/lib/python3.11/lib-dynload/libffi.so.6 %command%
```


請注意，Python 版本號會依執行的 Designer 版本而異：

* 低於 14.0.0：python3.9
* 低於 12.1.0 版本：python3.7

+++Steam 啟動選項
Linux 用戶若從 Steam 啟動 Designer，可在 Designer 的啟動選項中設定 LD\_PRELOAD 指令，如下所示。

完成後，未來所有遊戲階段都可以正常從 Steam 啟動 Designer。

![Steam 啟動選項](../../assets/steam_linux_launch_option.jpg "Team 啟動選項")



+++

**![（錯誤）](../../assets/error.svg) 子嗣**

Steam 版 Designer 無法啟動，且不會出現錯誤訊息。

**![（滴答）](../../assets/check.svg) 建議步驟**

你可以透過登入 Steam 應用程式來獲取錯誤訊息。

如這裡[&#128279;](https://github.com/ValveSoftware/steam-for-linux/issues/7114#issuecomment-629634260)建議，完全關閉 Steam，然後從終端機執行以下指令（或為此指令建立捷徑）：

```
steam 2>&1 | tee /path/to/logfile
```


<b>![（錯誤）](../../資產/error.svg)Issu</b><b>e</b>

`<b>xcb</b>`外掛無法載入。命令列中顯示以下訊息：

```
qt.qpa.plugin: Could not load the Qt platform plugin "xcb" in "" even though it was found. 

This application failed to start because no Qt platform plugin could be initialized. Reinstalling the application may fix this problem. 

 

Available platform plugins are: minimal, offscreen, xcb. 

 

Aborted (core dumped)
```


**![（滴答）](../../assets/check.svg) 建議步驟**

有些必需的包裹不見了。 從 Designer 的安裝目錄執行以下指令：

```
ldd libQt5XcbQpa.so.5
```


檢查列印清單中是否有被報告為 `not found`的套件，然後對每個遺失的套件執行以下指令：

```
apt-get install <package-name>
```


E.g.

```
apt-get install libxcb-xinput0
```


<b>![（錯誤）](../../assets/error.svg) 問題</b>

啟動 Designer 時會產生這個錯誤：

```
error while loading shared libraries: libcrypt.so.1: cannot open shared object file: No such file or directory
```


由 Designer 載入的系統函式庫與 Designer 自有<b>的 libcrypto.so.1.1</b> 函式庫不相容。

<b>![（打了](../../assets/check.svg) 推薦步驟</b>

將該函式庫從 Designer 的安裝目錄中移除 <b>`libcrypto.so.1.1`</b>，讓系統的函式庫被取代。

>[!NOTE]
>
> 這個解決方法只有在系統有自己的 libcrypto.so.1 函式庫時才有效。 在較新的發行版中，可能需要安裝像 <b>libxcrypt-compat</b> 這類相容套件。

<b>![（錯誤）](../../assets/error.svg) 問題</b>

Substance 3D Designer 在使用 *Arch* 架構的 Linux 發行版系統上無法啟動。

**![（嘀嗒）](../../assets/check.svg) 建議步驟 *（![（警告）](../../assets/warning.svg) 不穩定，僅限 AMD 顯卡！）***

試著安裝 **progl**（AMDGPU-PRO[&#128279;](https://wiki.archlinux.org/title/AMDGPU_PRO) 驅動程式的一部分），然後透過它啟動 Designer。你可以透過應用程式 `progl` 啟動指令中的前綴來完成：

```
progl <designer-application-path>
```


要注意這 `progl` 可能不穩定。 因此，這應該作為 *最後手段*&#x200B;嘗試。

>[!WARNING]
>
> 請注意，Linux 的 Arch 發行版 *不被支援*。 你可以在[系統需求](../../getting-started/system-requirements/system-requirements.md) 頁面了解更多。
