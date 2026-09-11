---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/pipeline-and-project-configuration/project-configuration-files-sbsprj.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Designer 中使用 SBSPRJ 專案設定檔來管理專案設定。
helpx_creative_field: ""
helpx_description: Designer > Pipeline and Project Configuration > Project Configuration Files - SBSPRJ
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 專案設定檔 - SBSPRJ
user-guide-description: ''
user-guide-title: ''
source-git-commit: ea2e2d76d225a0e17c84c3312934f62aa5ef3915
workflow-type: tm+mt
source-wordcount: '1001'
ht-degree: 0%

---


# 概觀

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

<b>專案設定檔</b> 是用來配置 Substance 3D Designer 最複雜且最廣泛的檔案。

它們的特殊之處在於你可以使用多個專案設定檔，每個下一個「子專案」都會擴展或覆蓋前一個「父專案」。 除非明確需要，設定不應被修改或加入專案檔案，讓 Designer 可以退回到其父設定，甚至預設設定。

</td>
<td width="25.00%" style="border: 0;" valign="top">

![SBSPRJ 檔案圖示](project-configuration-files-sbsprj.resources/sbsprj.png "SBSPRJ 檔案圖示")

</td>
</tr>
</table>

預設情況下，Designer 有兩種活躍的專案配置：

<b>預設專案： </b>包含所有預設設定，且全新安裝時會附帶函式庫 Designer。*唯讀，無法修改或刪除。*

<b>使用者專案： </b>由於預設值為唯讀 *，使用者* 所做的任何變更都會預設進入此專案。 *無法移除。*

這種基本設定確保預設函式庫及其他設定不會被破壞或修改，同時仍讓單身業餘使用者能自行添加修改，無需繁瑣的設定。

## 擴展或覆寫

連續專案中的大多數設定會 <b>覆蓋</b> 前一個專案的設定。 例如，自訂專案檔案中的另一個 Tangent Space 插件會覆蓋預設專案或使用者專案中定義的任何 TS 插件。 這表示除非明確需要，否則建議不要在子專案中覆寫或更改設定。

不過有些設定會 <b>擴展</b> 父設定，而不是覆蓋它們。 最明顯的是這些設定是圖書館路徑和篩選器，所以你總是會新增更多內容到圖書館，而不是覆蓋它。 此外，還有別名（路徑關鍵字，代表相對檔案路徑）會擴展，若定義重複則會覆蓋。 這讓內容的檔案路徑和參考資料能有很好的控制。

## 專案檔案內容

專案檔案可包含以下設定：

<b>3D 視角： </b>預設著色器、HDR 及場景狀態定義。

<b>別名： </b>相對路徑的關鍵字別名。

<b>烘焙： </b>烘焙命名規則的設定。

<b>一般： </b>圖形範本、切線空間插件、法線和影像格式預設。

<b>圖書館： </b>觀察路徑以展示在圖書館中。

<b>腳本： </b>回調腳本與直譯器。

<b>版本控制： </b>將版本控制整合到 Designer 中的設定。

## 修改專案檔案

專案配置與其他類型一樣，會以結構化 XML 檔案（使用 <b>.sbsprj</b> 副檔名）儲存，並可透過設計器介面或外部文字編輯器進行修改。

## Inside Substance 3D 設計師

請參閱 [專案設定](../../interface/preferences-window/project-settings/project-settings.md) 頁面，了解如何管理專案檔案及更改專案設定。

專案檔案也包含圖書館的自訂<b>分類</b>與<b>篩選</b>[&#128279;](../../interface/the-library/the-library.md) [器，您可以在「管理自訂內容與篩選器](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md)」頁面了解更多。

## 外部編輯 XML

在 Windows 上， [Notepad++](https://notepad-plus-plus.org) 是個不錯的免費選擇。 在 macOS 上， [Sublime Text](https://www.sublimetext.com/) 是個替代方案。 不過，任何有適當縮排、章節摺疊和某種語法標示的編輯器，都會讓你輕鬆許多。

一旦你在編輯器中打開 SBSPRJ 檔案，你會看到一個相當直接的結構化版面，區塊對應 UI 中的分頁。 這裡不會記錄所有設定，因為內容相當容易理解。

![XML 編輯](project-configuration-files-sbsprj.resources/project-xml.png "XML 編輯")

## 相對路徑與別名

結合別名的相對路徑是專案配置中較為複雜但最重要的部分之一，本節將為其說明。 為特定專案檔案新增自訂別名，則可在專案設定[&#128279;](../../interface/preferences-window/project-settings/project-settings.md)中完成。

在多個使用者電腦上，檔案互相引用系統中其他檔案的主要問題之一，就是絕對檔案路徑無法運作。 使用者可以在完全不同的位置定義他們的 SVN 儲存庫（例如： C：/John/Gamedev/SubstanceLibrary 或 D：/Dev/SubstanceLibrary）。 別名與相對路徑共同作用以解決此問題。 否則，你可能會打開別人的檔案，它會嘗試尋找該使用者在本地位置使用的自訂節點，而你可能沒有完全相同的定義。

<b>別名</b>是一個關鍵字，用來替換（部分）路徑。這有點像 Windows 環境變數，例如 %TEMP%，一個字會取代一個常用的路徑，然後由中央定義。 優點是路徑在各處都簡化，且當你決定重新定位這條路徑時，可以一次修改所有參考資料。

>[!NOTE]
>
> **別名範例**
> 
> | 別名 | 實際路徑值 |
> | --- | --- |
> | <b>SBS</b> | *C：\Program Files\Adobe\Adobe Substance 3D Designer\resources\packages* |
> | <b>習俗</b> | *D：\Dev\CustomProject\Substance* |
> 
> 預設函式庫預設位於 *C：\Program Files\Adobe\Adobe Substance 3D Designer\resources\packages*，所有使用預設內容的圖表都會參考此目錄。 它不再參考完整路徑，而是定義了「SBS</b>」（無引號）的別名<b>。以預設函式庫為例，SBS 路徑的精確值會在安裝到使用者選擇的 Designer 目錄時設定。
> 
> 在內部，當參考包含帶有別名的路徑時，會以以下方式修改：
> 
> **C：\Program Files\Adobe\Adobe Substance 3D Designer\resources\packages\blur\_hq.sbs => sbs:// <b></b>blur\_hq.sbs**

<b>相對路徑</b> 總是相對於所定義的檔案。 這表示設定檔目前的位置決定了大部分路徑，而別名路徑也會基於它，主要是透過新增一個子資料夾來決定。 <b>這表示強烈建議將 sbsprj 檔案放在你想看的資料夾旁邊！</b>

舉例來說，請以 C：/Versioncontrol/Substance/ 的一個儲存庫&#x200B;*為例，裡面有* CustomProject.sbsprj *，然後有*&#x200B;兩個資料夾 /Base *和*/Tools，裡面&#x200B;*有節點。*

要為 Base 和 Tools 定義兩個相對別名，可以在 SBSPRJ 檔案中進行如下操作：

### C：/Versioncontrol/Substance/CustomProject.sbsprj

```
   <urlaliases> 

    <size>2</size> 

    <_2 prefix="_"> 

     <path>file:Base</path> 

     <name>BaseAlias</name> 

    </_2> 

    <_1 prefix="_"> 

     <path>file:Tools</path> 

     <name>ToolsAlias</name> 

    </_1> 

   </urlaliases>
```


此設定檔的結果如下：

**BaseAlias://** 會是 *C：/Versioncontrol/Substance/Base/*，ToolsAlias://**&#x200B;**&#x200B;會是 *C：/Versioncontrol/Substance/Tools/。*

如果你只想定義  *C：/Versioncontrol/Substance/*，路徑會標示為 **「file：.」**，點代表檔案本身的位置。
