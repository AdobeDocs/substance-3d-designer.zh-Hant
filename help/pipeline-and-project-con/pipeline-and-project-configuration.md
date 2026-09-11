---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/pipeline-and-project-configuration.html"
breadcrumb-title: ''
description: 在 Substance 3D Designer 中設定管線和專案設定，以優化你的工作流程與產出。
helpx_creative_field: ""
helpx_description: Designer > Pipeline and Project Configuration
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 管線與專案配置
user-guide-description: ''
user-guide-title: ''
source-git-commit: ea2e2d76d225a0e17c84c3312934f62aa5ef3915
workflow-type: tm+mt
source-wordcount: '596'
ht-degree: 0%

---


# 管線與專案配置

Substance 3D Designer 擁有強大的系統，可配置應用程式以符合管線使用需求。 透過進階的階層式「**專案**」檔案系統，應用程式可立即配置至 Studio 或專案標準，所有設定與函式庫內容皆受版本控制。 系統的主要目標是集中所有與管線相關的設定，同時允許多種配置相互覆寫與擴展。

>[!WARNING]
>
> 此系統並非為需求較簡單的單一使用者設計，而是針對 *大型專案與團隊* 且組織需求較高的工作室設計。 要充分利用此系統，建議有相當程度的規劃與準備，並具備一定程度的自動化設定！

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## 組態檔案階層

Designer 有三個層級或組態檔，每個層級都有不同的用途。 在 Windows 上，所有檔案都位於 *~User\AppData\Local\Adobe\Adobe Substance 3D Designer。*

圖片說明了 Designer 預設設定中不同檔案在全新安裝後的關係。

</td>
<td style="border: 0;" valign="top">

![設定檔案階層](pipeline-and-project-configuration.resources/filestructureoverview.png "設定檔案階層")

</td>
</tr>
</table>

* <b>[使用者\_Preferences.XML](../pipeline-and-project-con/user-preferences-aut/user-preferences-automating-setup.md)</b> 包含一般程式設定，其中除一項外皆與專案管線無關。 這個檔案是唯一的，無法替換，Designer 是硬編碼來使用這個檔案的。\
  它只包含一個對設定檔的參考。
* <b>[預設_Configuration.SBSCFG](../pipeline-and-project-con/configuration-list-sbscfg/configuration-list-sbscfg.md)</b> 可以替換成其他名稱不同的 SBSCFG 檔案，但同時只能使用一個 SBSCFG 檔案。\
  它包含多個專案檔案的參考。 *請注意，預設設定中這些檔案並未明確定義，而是硬編碼的！*
* <b>[Project.SBSPRJ](../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md)</b> 檔案包含與專案/管線相關的設定。 多個專案可以在階層結構中定義，覆蓋或擴展先前定義的專案。

## 設計管線設定

每種檔案類型在本頁子頁面都有更詳細的說明，但理想上如何定義 Designer 自訂設定的簡短概述如下：

1. <b>辨識並分組要加入專案檔案的設定。</b> 每間工作室都不一樣，需要一定的規劃！\
   幾乎每種情況下，至少應該定義兩個專案：一個是全域、整個工作室的預設值（例如標準範本、著色器檔案、烘焙設定），另一個則是更具體的內容，例如庫內容。 如果你同時有多個專案在執行，建議為每個專案建立多個專案配置（總共三個以上）。
1. <b>建立相關的 [SBSPRJ 檔案]（../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md），並將其及其內容置於版本控制之下。</b> 強烈建議將 Designer 的管線和函式庫內容與你的專案內容及資源（3D 模型、材質、程式碼）分開，建立 *一個獨立的倉庫* 來管理。
1. <b>建立一個[ SBSCFG 配置]（../pipeline-and-project-con/configuration-list-sbscfg/configuration-list-sbscfg.md）檔案，列出所有專案檔案，並將其置於版本控制</b>之下。 如果你有多個專案，可以為每個專案建立一個設定檔。
1. <b>設定每位使用者的 [User\_Preferences.xml]（../pipeline-and-project-con/user-preferences-aut/user-preferences-automating-setup.md）來參考他們相關的設定檔。</b>\
   你可以讓每個使用者手動執行，或者透過注入線條到他們的 XML 檔案來寫腳本。 [更多資訊請見相關頁面](../pipeline-and-project-con/user-preferences-aut/user-preferences-automating-setup.md)。
