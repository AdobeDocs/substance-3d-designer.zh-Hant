---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/pipeline-and-project-configuration/configuration-list-sbscfg.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Designer 中使用 SBSCFG 配置清單來管理專案設定和預設。
helpx_creative_field: ""
helpx_description: Designer > Pipeline and Project Configuration > Configuration List - SBSCFG
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 配置清單 - SBSCFG
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 0%

---


# 配置清單 - SBSCFG

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

設定檔比 [專案組態檔案](../../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md)簡單得多，因為它只包含專案清單，以及引擎相容模式。 它們作為比單一專案檔案更高層次的專案/環境配置清單。

你可以針對不同環境設定多種設定，這些檔案可以和 SBSPRJ 檔案一起在版本控制下保存。

</td>
<td width="25.00%" style="border: 0;" valign="top">

![SBSCFG 檔案圖示](../../assets/sbscfg.png "SBSCFG 檔案圖示")

</td>
</tr>
</table>

## 修改設定檔

這些檔案雖然簡單，但仍可像 SBSPRJ 檔案一樣以兩種不同方式修改。

### 在專案設定中

高亮區塊是與設定檔相關的部分，你只要將更多專案加入清單，這些專案就儲存在上述定義的 SBSCFG 檔案中。

![專案設定](../../assets/config-ui.png "專案設定")

### 外部編輯為 XML

Windows 用 <b>Notepad++</b> 是個不錯的免費選擇，macOS <b>則用 Sublime Text</b> 作為替代方案。 不過，任何有適當縮排、章節摺疊功能和某種語法標示的編輯器，都會讓你的工作輕鬆許多。

一旦你在編輯器中打開 SBSCFG 檔案，你會看到一個相當直接的結構化版面，並有對應介面的區塊。

```
<?xml version="1.0" encoding="UTF-8"?> 

<root> 

 <projects> 

  <projectfiles> 

   <size>1</size> 

   <_1 prefix="_"> 

    <path>custom_project.sbsprj</path> 

   </_1> 

  </projectfiles> 

 </projects> 

 <preferences> 

  <configuration> 

   <compatibilitymode>sbs_engine_v6</compatibilitymode> 

  </configuration> 

 </preferences> 

</root>
```


請注意，預設專案與使用者專案未明確列出，且其他專案則定義在這些之後。

上述範例也使用 [了相對路徑](../../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md)。 請注意，CFG 與 PRJ 檔案的相對路徑邏輯略有不同：如上所述， **CFG 檔案不應在路徑**&#x200B;前輸入「file：/」。 路徑僅附加在定義其 CFG 檔案的位置上。

## 移除預設函式庫

目前預設函式庫無法移除。 其實這樣做可能也不是好主意，因為你會失去很多 Designer 的功能。
