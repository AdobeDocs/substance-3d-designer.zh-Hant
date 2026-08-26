---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/interface/the-main-toolbar.html"
breadcrumb-title: ''
description: 了解 Substance 3D Designer 的主工具列，以存取你工作流程中常見的工具與指令。
helpx_creative_field: ""
helpx_description: Designer > Interface > Main toolbar
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 主工具列
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '929'
ht-degree: 0%

---


# 主要工具列

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

本頁介紹 Substance 3D Designer[&#128279;](https://www.adobe.com/tw/products/substance3d-designer.html) 的主工具列與選單，位於主視窗左上角。它由兩部分組成：下拉選單主選單和快速存取按鈕。 所有快速存取按鈕功能也可透過 <b>檔案</b> 與 <b>編輯</b> 選單存取。

</td>
<td width="41.67%" style="border: 0;" valign="top">

![主工具列](../../assets/mainmenu.png "主工具列")

</td>
</tr>
</table>

## 快速存取按鈕

![](../../assets/newsubstance.png)  <b>New Substance 圖...：</b> （Ctrl+N） 會 [顯示新圖](../../compositing-graphs/creating-compositing-gra/creating-a-substance-compositing-graph.md) 視窗，然後建立一個包含 [Substance 圖](../../compositing-graphs/substance-compositing-graphs.md)的新套件。

![](../../assets/open.png)  <b>開啟...：</b> （Ctrl+O） 開啟現有[的物質套件（.SBS， .SBSAR， .SBSASM）。](../../getting-started/overview/overview.md)

![](../../assets/saveall.png)  <b>全部儲存：</b>（Ctrl+⇧+S）儲存檔案總管[&#128279;](../../interface/the-explorer-window/the-explorer-window.md)中列出的所有套件。

![](../../assets/undo.png)  <b>復原：</b> （Ctrl+Z）還原上一次操作。

![](../../assets/redo.png)  <b>重做：</b> （Ctrl+Y）重做上次未完成的操作。

## 檔案

<b>新增：</b> 開啟子選單以建立圖表或套件：

* <b>新實體圖...：</b>（Ctrl+N） 呈現[新圖形](../../compositing-graphs/creating-compositing-gra/creating-a-substance-compositing-graph.md)視窗，讓你能建立新的[實體圖;](../../compositing-graphs/substance-compositing-graphs.md)
* <b>新 Substance 函數圖：</b> 建立一個包含 [Substance 函數圖](../../function-graphs/function-graphs.md)的新套件;
* <b>Empty：</b> 產生一個空的套件。

<b>開啟...：</b> （Ctrl+O） 開啟現有[的物質套件（.SBS， .SBSAR， .SBSASM）。](../../getting-started/overview/overview.md)

<b>最近包裹：</b> 顯示最近開啟的包裹清單。 點擊一條條目即可開啟。

<b>開啟上次會話套件（#）</b>：開啟上次會話關閉或結束時所有開啟的套件。

<b>全部儲存：</b> （Ctrl+⇧+S） 儲存所有未開啟的套件，包括背景載入的套件。

<b>關閉所有</b> ：關閉所有未結包裹。

<b>重新載入資源：</b> 強制 Designer 重新載入 [所有資源，包括點陣圖和 SVG 資料](../../resources/importing-linking-and-new/importing-linking-and-new-resources.md)。

<b>退出：</b> （Ctrl+Q）- 關閉 Substance 3D 設計師。

## 編輯

<b>復原：</b> （Ctrl+Z）還原上一次操作。

<b>重做：</b> （Ctrl+Y） 重做上次未完成的操作。

<b>偏好設定...：</b> 開啟偏好設定視窗。

>[!NOTE]
>
> 此對話框可從 macOS 工作列中的 Substance 3D Designer 選單存取。

## 工具

<b>取消渲染：</b> （Esc） 停止物質引擎的當前運作。 可以用來中止不想要的重手術。

<b>暫停引擎：</b> （⇧+Esc） 暫停渲染引擎。 這能加快複雜 [物質圖表](../../compositing-graphs/substance-compositing-graphs.md)的編輯速度。

<b>Switch 引擎...： </b>（F9） 提供多種渲染引擎選擇，包括 GPU 引擎（Windows 為 DirectX，macOS 為 OpenGL）及 CPU 引擎（Apple Silicon 為 &#39;NEON&#39;，其他為 SSE）。

<b>Substance Player：</b> 管理 Designer 與 Substance Player 的整合：

* <b>尋找玩家...：</b> 讓設計師知道玩家安裝在哪裡;
* <b>下載播放器...：</b> 開啟物質玩家文件 [的登陸頁面](https://helpx.adobe.com/substance-3d-player/home.html)，玩家可在此下載。

<b>插件管理器...</b>：會打開插件管理器視窗，你可以安裝、載入及卸 [載 Substance 3D Designer 的 Python 插件。](../../scripting/scripting.md)

## 窗戶

<b>新探險家：</b> 開啟一個新的探險者碼頭。 你可以同時開啟多個 Explorer 底座。

<b>新 3D 視角：</b> 開啟一個新的 3D 視角底座。 你可以同時開啟多個 3D View 底座。

<b>新圖書館視圖：</b> 開啟新的圖書館碼頭。 你可以同時開啟多個圖書館底座。

<b>Python 編輯器：</b> 開啟用於[評估與建立腳本](../../scripting/scripting.md)的 Python 編輯器。

<b>重設版面配置：</b> 將工作區重置為預設版面配置。 所有窗戶都會重新排列，有些窗戶可能會再次被隱藏。 在程式排版出現問題時使用。

<b>視窗未最大化：</b>當任何面板被&#x200B;*最大化*&#x200B;時，此選項會將其恢復最大化，並恢復視窗最大化前&#x200B;*的*&#x200B;版面配置

<b>探險者：</b> 顯示/隱藏探 [險者](../the-explorer-window/the-explorer-window.md)。

<b>圖表：</b> 顯示/隱藏 [圖表視窗](../../interface/the-graph-view/the-graph-view.md)。

<b>參數：</b>顯示/隱藏屬性[&#128279;](../properties/properties.md)。

<b>控制台：</b> 顯示/隱藏控制台視窗。

<b>3D 視圖：</b> 顯示/隱藏 [3D 視圖](../../interface/3d-view/3d-view.md)。

<b>依賴管理工具：</b> 顯示/隱藏 [依賴管理工具](../../interface/dependency-manager/dependency-manager.md)。

<b>2D 視圖：</b> 顯示/隱藏 [2D 視圖](../2d-view/2d-view.md)。

<b>圖書館：</b> 顯示/隱藏 [圖書館視窗。](../../interface/the-library/the-library.md)

<b>主工具列：</b> 顯示/隱藏主工具列（僅限快速存取按鈕）。

>[!NOTE]
>
> 想了解更多關於 Designer 面板管理、自訂功能及提升工作流程的功能，請前往 [本文件中的「自訂你的工作區](../../interface/customizing-your-wor/customizing-your-workspace.md)」頁面。

## 說明

<b>教學：</b> 開啟 [Substance 3D 教學](https://substance3d.adobe.com/tutorials/) 網站（前身為 Substance Academy）。<b>\
</b>

<b>發行說明：</b> 會開啟一個視窗，顯示最新版本的變更日誌。

<b>技術需求：</b> 顯示執行應用程式所需的技術需求。

<b>文件：</b>在此文件[&#128279;](https://www.adobe.com/go/Substance-3D-doc-Designer)中開啟預設瀏覽器。

<b>腳本文件：</b> 開啟瀏覽器，查看本地的 Python API 文件。

<b>論壇...：</b> 開啟您的網頁瀏覽器，進入我們的 [支援社群](https://forum.substance3d.com/) 論壇，與社群聯繫並提出問題。

<b>回報錯誤......：</b> 開啟錯誤回報視窗。

<b>匯出日誌...：</b> 將當前日誌檔案匯出為壓縮（.zip）檔案，以提供技術支援。

<b>給予回饋......：</b> 在 Adobe [支援社群](https://www.adobe.com/go/Substance-3D-feedback-Designer) 首頁開啟你的瀏覽器。

<b>Substance 3D 資產：</b> 瀏覽 [訂閱者的高級 3D 內容](https://substance3d.adobe.com/assets) （前稱 Substance Source）。

<b>Substance 3D 社群資產：</b> 讓你瀏覽 [免費社群資產](https://substance3d.adobe.com/community-assets/) （前稱 Substance Share）。

<b>管理我的帳號\*：</b> 開啟你的 Adobe 帳號網頁。

<b>登入/登出...\*：</b> 讓你登入/登出你的 Adobe 帳號。

<b>主畫面...：</b>顯示主畫面[&#128279;](../../interface/home-screen/home-screen.md)對話框。

<b>新功能...：</b> 顯示一個螢幕，顯示 Designer 最新版本新增的功能

<b>歡迎畫面......\*：</b> 顯示一個引導新用戶了解 Designer 的目的及其在 Substance 3D 生態系統中 [定位的畫面](https://helpx.adobe.com/tw/substance-3d.html)

<b>合作夥伴：</b> 讓您在 Designer 中存取合作夥伴對第三方整合的免責聲明與通知。

<b>關於 Substance 3D Designer...：</b> 顯示應用程式及其元件的資訊，例如版本號。

\*：這些選項僅在透過 Adobe Creative Cloud Desktop[&#128279;](https://creativecloud.adobe.com/en/apps/download/creative-cloud) 安裝的 Designer 版本中提供，該版本需要訂閱 [Substance 3D](https://www.adobe.com/creativecloud/plans.html?amp%3Bplan=individual#filter=3dar)。
