---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/technical-issues/cannot-create-load-a-project.html"
breadcrumb-title: ''
description: 在 Substance 3D Designer 中排解建立或載入專案時的問題，並尋找解決方案。
helpx_creative_field: ""
helpx_description: Designer > Technical issues > Cannot createload a project
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 無法 createload 專案
user-guide-description: ''
user-guide-title: ''
source-git-commit: f72773d86b681ce0e815c5595067b1593cdd1f0a
workflow-type: tm+mt
source-wordcount: '1101'
ht-degree: 0%

---


# 無法建立或載入專案

本頁列出無法在 Substance 3D Designer 中建立或載入專案的常見原因，並提供各項故障排除步驟。

## 應用程式太舊，無法開啟 URL

**![（錯誤）](cannot-create-load-a-project.resources/error.svg) 子嗣**

**Substance 3D 檔案（SBS）**&#x200B;是由不支援其格式&#x200B;*的 Substance 3D Designer*&#x200B;版本載入。Substance 3D 檔案很可能 *是儲存在較新版本的軟體中，該版本* 使用更新格式來處理這些檔案。

**![（滴答）](cannot-create-load-a-project.resources/check.svg) 建議步驟**

隨著 Substance 3D Designer 的演進，Substance 3D 檔案格式（SBS）也在演進。 通常，新版本的軟體需要 *更新你的檔案* ，才能支援最新功能。

當你&#x200B;*第一次*&#x200B;在新版本載入檔案時，會&#x200B;*被*&#x200B;提示執行此更新。

>[!WARNING]
>
> 如果檔案是在更新後&#x200B;*才被儲存*，格式版本也會隨之改變。此時，它 *已無法在先前版本* 的 Substance 3D Designer 中載入。
> 
> 此限制同樣適用於 [物質玩家](https://helpx.adobe.com/substance-3d-player/home.html)。

首先，確認你使用的是最新版本的 Substance 3D Designer，這是你目前授權的授權。 以下是各版本更新的存取點：

* <b>Adobe Substance 3D 訂閱：</b>請前往 Adobe Creative Cloud 桌面[&#128279;](https://creativecloud.adobe.com/en/apps/download/creative-cloud)應用程式應用程式中應用程式標籤的更新區塊
* <b>[Substance3d.com](http://Substance3d.com) 訂閱：</b>在 Substance 3D Designer 中按需更新，或在 [Substance3d.com](http://substance3d.com) 網站的「我的授權[&#128279;](https://store.substance3d.com/user)」區下載最新安裝程式
* <b>Steam：</b> 應用程式會預設自動更新。 你可以手動啟動 Substance 3D Designer，或進入下載頁面來觸發更新

>[!WARNING]
>
> 在儲存&#x200B;*已更新的檔案前，請確定你不需要在 Substance 3D Designer*&#x200B;的舊版本中載入檔案。
> 
> 或者，你也可以&#x200B;*先複製**檔案，再用*&#x200B;新版本的 Substance 3D Designer 載入，這樣如果需要使用舊版本軟體，隨時有檔案可以回頭查看。

## 建立或載入專案時會當機

<b>![（錯誤）](cannot-create-load-a-project.resources/error.svg) 子嗣</b>

建立或載入專案時的當機，通常是因為 3D 視圖[&#128279;](../../interface/3d-view/3d-view.md)初始化時出現錯誤，而這個錯誤發生在工作區設定過程中。

如果系統是筆記型電腦，第三方應用程式可能會強制執行 *電源管理計畫* ，阻止 3D View 使用系統的 GPU。 如果沒有其他 GPU 裝置能替代執行此任務，可能會導致當機。

當 *顯示設定或縮放* 在不同工作階段間改變，導致 3D View 渲染幀在無效座標時也可能發生當機。

<b>![（滴答）](cannot-create-load-a-project.resources/check.svg) 建議步驟</b>

考量到這次當機可能的原因有多重，我們建議依序進行以下故障排除步驟：

更新顯示卡驅動程式

首先，確保顯示卡驅動程式是最新的。 你可以在這裡（NVIDIA）、[這裡](https://www.amd.com/en/support)（AMD）或[這裡](https://downloadcenter.intel.com/product/80939/Graphics-Drivers)（Intel）找到你GPU的[&#128279;](https://www.nvidia.com/Download/index.aspx?lang=en-us)最新版本。

力的最佳效能

找任何能管理系統 *電源方案* 的軟體（例如 ASUS Armoury Crate），尤其是系統是筆電時。

部分電源管理應用程式可能會限制其他應用程式存取系統 GPU 的權限，或影響 GPU 效能，可能導致當機。 如果有電源管理應用程式且正在啟用，請切換到能提供最佳效能的方案。

強制使用獨立 GPU

如果你的系統有 *可切換顯示卡*，可以考慮強制使用獨立 GPU（dGPU）來執行 Substance 3D 應用。

大多數情況下，這會在專門控制 GPU 設定的應用程式中實現。 例如，NVIDIA GPU 可以在「NVIDIA 控制面板」應用程式中做到這點。

重設儲存在登錄檔中的使用者介面

如果當機是因為顯示設定或縮放的改變，你可以嘗試刪除 Designer 現有的登錄檔，完全重置使用者介面及其他設定。

以下說明了每個作業系統執行此重置的程序：

+++窗戶
* Close Designer

Close Designer

* 開啟 <b>命令提示字元</b> 應用程式

開啟 <b>命令提示字元</b> 應用程式

* 輸入以下指令並按下 <b>Enter</b>：

  <b>創意雲端桌面</b>

  ```
  reg delete "HKEY_CURRENT_USER\Software\Adobe\Adobe Substance 3D Designer" /f
  ```


  <b>Steam/Substance 版本</b>

  ```
  reg delete "HKEY_CURRENT_USER\Software\Allegorithmic\Substance Designer" /f
  ```


輸入以下指令並按下 <b>Enter</b>：

<b>創意雲端桌面</b>

<b>Steam/Substance 版本</b>

* 請把第二台螢幕從系統中斷開，再重新連接（如果你 *沒有* 安裝多個顯示器，請忽略這個步驟）。

請把第二台螢幕從系統中斷開，再重新連接（如果你 *沒有* 安裝多個顯示器，請忽略這個步驟）。

* 啟動 Designer，但不要&#x200B;**&#x200B;建立或開啟任何專案

啟動 Designer，但不要&#x200B;**&#x200B;建立或開啟任何專案

* 在頂欄，打開 <b>Windows</b> 選單，選擇 <b>「新 3D 檢視</b> 」選項

在頂欄，打開 <b>Windows</b> 選單，選擇 <b>「新 3D 檢視</b> 」選項

* 檢查 3D 視圖</b>是否<b>正確初始化，並在面板頂部列的場景</b>選單中嘗試不同的預覽網格<b>

檢查 3D 視圖</b>是否<b>正確初始化，並在面板頂部列的場景</b>選單中嘗試不同的預覽網格<b>

* 創建或開啟素材

創建或開啟素材

+++

+++macOS
* Close Designer

Close Designer

* 開啟 <b>終端</b> 機應用程式

開啟 <b>終端</b> 機應用程式

* 輸入以下指令並按下 <b>Enter</b>：

  <b>創意雲端桌面</b>

  ```
  rm ~/Library/Preferences/com.adobe.Adobe\ Substance\ 3D\ Designer.plist
  ```


  <b>Steam/Substance 版本</b>

  ```
  rm ~/Library/Preferences/com.allegorithmic.Substance\ Designer.plist
  ```


輸入以下指令並按下 <b>Enter</b>：

<b>創意雲端桌面</b>

<b>Steam/Substance 版本</b>

* 請把第二台螢幕從系統中斷開，再重新連接（如果你 *沒有* 安裝多個顯示器，請忽略這個步驟）。

請把第二台螢幕從系統中斷開，再重新連接（如果你 *沒有* 安裝多個顯示器，請忽略這個步驟）。

* 啟動 Designer，但不要&#x200B;**&#x200B;建立或開啟任何專案

啟動 Designer，但不要&#x200B;**&#x200B;建立或開啟任何專案

* 在頂欄，打開 <b>Windows</b> 選單，選擇 <b>「新 3D 檢視</b> 」選項

在頂欄，打開 <b>Windows</b> 選單，選擇 <b>「新 3D 檢視</b> 」選項

* 檢查 3D 視圖</b>是否<b>正確初始化，並在面板頂部列的場景</b>選單中嘗試不同的預覽網格<b>

檢查 3D 視圖</b>是否<b>正確初始化，並在面板頂部列的場景</b>選單中嘗試不同的預覽網格<b>

* 創建或開啟素材

創建或開啟素材

+++
