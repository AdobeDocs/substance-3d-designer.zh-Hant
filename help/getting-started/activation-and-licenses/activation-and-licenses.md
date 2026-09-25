---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/getting-started/activation-and-licenses.html"
breadcrumb-title: ""
description: 學習如何啟用 Substance 3D Designer 並管理所有功能與能力的授權。
helpx_creative_field: ""
helpx_description: Designer > Getting started > Activation and licenses
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 啟動與執照
user-guide-description: ""
user-guide-title: ""
source-git-commit: 21ee545724852c876444dcf3ed4a82af8d1e3715
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 0%
---

# 依應用程式類型的啟動流程

啟動流程取決於你在哪裡購買或能使用 Designer：

| 版本 | 啟動過程 |
|:-----------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 創意雲端桌面（CCD） | 從 CCD 應用程式安裝產品，然後啟動。 如果你遇到授權問題，請參考這些頁面： [應用程式因訂閱錯誤](https://helpx.adobe.com/creative-cloud/apps/troubleshoot/launch-issues/apps-wont-launch-due-to-subscription-error.html) 無法啟動 / [帳號、方案與帳單協助](https://helpx.adobe.com/account/individual.html) |
| 蒸汽 | 直接從你的 Steam 遊戲庫啟動產品。 |
| 實質（獨立作品） | 請參考下方說明的啟動流程。 |

## 啟動步驟（Substance 版）

### 使用啟動精靈

當你第一次啟動 Designer 時，啟動精靈會打開並引導你完成啟動流程。

有三種選擇：

* <b>評估此產品</b>：舊有試驗已不再提供。 你可以在這裡或使用 Creative Cloud Desktop 開始為每個 Substance 3D 應用程式[](https://www.adobe.com/creativecloud/3d-augmented-reality.html)開啟 30 天試用。每個試驗都獨立於其他Substance 3D應用程式，所以你可以一次嘗試一個或全部。
* <b>使用授權檔案</b>啟用：請於 2022 年 9 月 30 日前，使用 Substance 3D 網站](https://store.substance3d.com/user)帳號頁面[下載的授權檔案（<b>\*.key</b>）啟用產品。
* <b>使用您的帳戶</b>啟用：舊有物質帳戶已無法再用於啟用。

>[!IMPORTANT]
>
> 要用啟用精靈安裝授權檔案，請確保以管理員身份執行 Designer，並暫時停用防毒軟體。

![啟動精靈](activation-and-licenses.resources/activation-wizard.png "啟動精靈")

### 手動啟動

你可以手動啟用 Designer，方法是將 license.key 檔案放入以下資料夾：

<table data-preserve-html="true" style="table-layout:auto">
    <tbody>
        <tr>
            <th style="text-align: left;">平台</th>
            <th style="text-align: left;">版本</th>
            <th colspan="2" style="text-align: left;">路徑</th>
        </tr>
        <tr>
            <td rowspan="4" style="text-align: left;"><b>窗戶</b></td>
            <td rowspan="2" style="text-align: left;"><b>11.2</b> 或更高</td>
            <td style="text-align: left;"><code>AppData&#92;Local</code></td>
            <td style="text-align: left;"><code>C:&#92;Users&#92;&#91;username&#93;&#92;AppData&#92;Local&#92;Adobe&#92;Adobe Substance 3D Designer</code></td>
        </tr>
        <tr>
            <td style="text-align: left;"><code>AppData&#92;Roaming</code></td>
            <td style="text-align: left;"><code>C:&#92;Users&#92;&#91;username&#93;&#92;AppData&#92;Roaming&#92;Adobe&#92;Adobe Substance 3D Designer</code></td>
        </tr>
        <tr>
            <td rowspan="2" style="text-align: left;"><b>11.1</b> 或更低</td>
            <td style="text-align: left;"><code>AppData&#92;Local</code></td>
            <td style="text-align: left;"><code>C:&#92;Users&#92;&#91;username&#93;&#92;AppData&#92;Local&#92;Allegorithmic&#92;Substance Designer</code></td>
        </tr>
        <tr>
            <td style="text-align: left;"><code>AppData&#92;Roaming</code></td>
            <td style="text-align: left;"><code>C:&#92;Users&#92;&#91;username&#93;&#92;AppData&#92;Roaming&#92;Allegorithmic&#92;Substance Designer</code></td>
        </tr>
        <tr>
            <td rowspan="2" style="text-align: left;"><b>macOS</b></td>
            <td style="text-align: left;"><b>11.2</b> 或更高<br/></td>
            <td colspan="2" style="text-align: left;"><code>/Users/&#91;username&#93;/Library/Application Support/Adobe/Adobe Substance 3D Designer</code></td>
        </tr>
        <tr>
            <td style="text-align: left;"><b>11.1</b> 或更低<br/></td>
            <td colspan="2" style="text-align: left;"><code>/Users/&#91;username&#93;/Library/Application Support/Allegorithmic/Substance Designer</code></td>
        </tr>
        <tr>
            <td rowspan="2" style="text-align: left;"><b>Linux</b></td>
            <td style="text-align: left;"><b>11.2</b> 或更高</td>
            <td colspan="2" style="text-align: left;"><code>/home/&#91;username&#93;/.local/share/Adobe/Adobe Substance 3D Designer</code></td>
        </tr>
        <tr>
            <td style="text-align: left;"><b>11.1</b> 或更低<br/></td>
            <td colspan="2" style="text-align: left;"><code>/home/&#91;username&#93;/.local/share/Allegorithmic/Substance Designer</code></td>
        </tr>
    </tbody>
</table>

>[!NOTE]
>
> 上述路徑中的部分目錄可能預設是隱藏的。 在檔案總管手動輸入路徑，或顯示隱藏檔案以查看。

>[!IMPORTANT]
>
> 請確保該檔案被呼叫 `license.key` ，否則應用程式找不到。

### 環境變數

你可以用[環境變數](../../pipeline-and-project-con/environment-variables/environment-variables.md)覆蓋設計者檢查`license.key`檔案的位置。
