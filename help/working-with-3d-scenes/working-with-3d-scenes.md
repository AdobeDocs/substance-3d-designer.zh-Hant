---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/working-with-3d-scenes.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Designer 中匯入、編輯及操作 3D 場景，以預覽並測試你的材質。
helpx_creative_field: ""
helpx_description: Designer > Working with 3D scenes
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 與3D場景合作
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '872'
ht-degree: 0%

---


# 與3D場景合作

![3D場景工作 3D場景](../assets/workingWith3DScenes.png "工作"){zoomable="yes"}

Designer 允許你載入 [3D 場景](../glossary/glossary.md) ，在上下文中處理材質。 你可以在這裡找到支援的 3D 場景檔案格式清單，包括每種格式所支援的功能清單。 <b>&lt;link needed></b>

在情境中工作是指 [覆](../working-with-3d-scenes/overriding-scene-mat/overriding-scene-materials.md) 寫場景中的 [一個素材](../glossary/glossary.md) ，以替換成 Designer 中撰寫的素材。\
你可以從頭開始，使用 Designer 中可用的任何 Substance 圖形範本，或 [從 3D 場景的材質中提取數值和材質](../working-with-3d-scenes/extracting-materials-val/extracting-materials-values-and-textures.md) 作為起點。

完成 3D 場景後，你可以 [匯出](../working-with-3d-scenes/exporting-scenes/exporting-scenes.md) 成新檔案，讓它匯入其他應用程式。

匯出為 USD 格式時，此工作流程可完全 <b>非破壞</b>性，僅匯出編輯與新增內容。

首先，你需要載入一個 3D 場景來處理，並且能在 Designer 中跨次工作階段保留其狀態。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## 3D 場景內容

</td>
<td style="border: 0;" valign="top">

### 載入場景

</td>
<td style="border: 0;" valign="top">

### 場景狀態檔案

</td>
</tr>
</table>

## 3D 場景內容

載入 3D 場景時，Designer 會建立自己的場景來承載它。

你可以與場景中的以下內容互動：

* <b>材質：</b> 場景中使用的所有材質都可以用 [Designer 建立的複製品覆蓋](../working-with-3d-scenes/overriding-scene-mat/overriding-scene-materials.md) 。 你可以編輯 [該複製品的材質屬性](../interface/3d-view/material-properties/material-properties.md) ，並使用Substance圖中的原始值或貼圖。
* <b>網格：</b> 幾何體可以直接在視窗中選擇，或從 [場景瀏覽器](../interface/3d-view/scene-browser/scene-browser.md)中選取，以存取其材質動作（[覆寫](../working-with-3d-scenes/overriding-scene-mat/overriding-scene-materials.md)、 [重置](../working-with-3d-scenes/overriding-scene-mat/overriding-scene-materials.md)、 [提取至實體圖](../working-with-3d-scenes/extracting-materials-val/extracting-materials-values-and-textures.md)）
* <b>燈光：</b>場景瀏覽器中所有燈光都可以被關閉[&#128279;](../interface/3d-view/scene-browser/scene-browser.md)。
* <b>攝影機：</b> 場景中偵測到的任何攝影機，都會作為預設加入到由 Designer 新增的攝影機上。

![3D 場景](../assets/loaded3DScene.png "內容 3D 場景內容"){zoomable="yes"}

Designer 對其 3D 場景使用了 USD 描述。 其版面配置可在場景瀏覽器中瀏覽，每種 [USD prim](https://openusd.org/release/glossary.html#usdglossary-prim) 類型都有自己的圖示（幾何體、材質、著色器、攝影機、變換等）。

[場景瀏覽器](../interface/3d-view/scene-browser/scene-browser.md)可用來選擇、啟用及停用場景內容。因此，我們建議您在處理自訂 3D 場景時保持顯示。

## 載入場景

在 3D 視圖中載入 3D 場景有幾種路徑：

1. 雙擊或拖曳 [3D 場景資源](../resources/3d-scene-resource/3d-scene-resource.md) 從 [套件](../glossary/glossary.md) 中進入 3D 檢視
1. 將 3D 場景項目從 [函式庫](../interface/the-library/the-library.md) 拖曳到 3D 視圖（前提是你已 [將自己的內容加入函式庫](../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md)）
1. 將系統檔案瀏覽器中的 3D 場景檔案拖入 3D 檢視
1. 載入一個 3D 場景狀態檔案（SBSSCN）及其參考的網格

請注意，只有方法1和4能讓你完全重新載入場景，因為場景的狀態會寫入3D場景資源和場景狀態檔，並儲存在套件中。 方法2和3則是像載入其他場景一樣載入。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![載入 3D 場景 - 從 3D 場景資源](../assets/load3DScene-3DSceneResource.gif "讀取 - 載入 3D 場景 - 從 3D 場景資源"){zoomable="yes"}

載入 3D 場景資源

</td>
<td style="border: 0;" valign="top">

![載入 3D 場景 - 從函式庫](../assets/load3DScene-Library.gif "載入 3D 場景 - 從函式庫"){zoomable="yes"}

從函式庫載入 3D 場景

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![從 3D 場景檔案載入 3D 場景 - 從 3D 場景檔案](../assets/load3DScene-3DSceneFile.gif "載入"){zoomable="yes"}

載入 3D 場景檔案

</td>
<td style="border: 0;" valign="top">

![從場景狀態檔案載入 3D 場景 - 從場景狀態檔案](../assets/load3DScene-sceneStateFile.gif "讀取"){zoomable="yes"}

載入場景狀態檔案

</td>
</tr>
</table>

>[!NOTE]
>
> 在 3D View 中導航與視覺化場景的說明已在 3D View 文件[&#128279;](../interface/3d-view/3d-view.md)中有說明。

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

設計師總是建立自己的環境（以美元為單位的 DomeLight）和攝影機，除了場景中可能存在的場景外。

Designer 建立的任何物品會在場景瀏覽器中以 <b>粗體標籤</b> 列出。

>[!NOTE]
>
> 當載入的場景至少有一個環境（DomeLight）時，Designer 建立的環境預設會 *被停用* ，以免干擾場景的環境光照。

</td>
<td width="33.33%" style="border: 0;" valign="top">

![場景瀏覽器 - 由設計師](../assets/sceneBrowser-createdByDesigner.png "建立的元素 場景瀏覽器 - 由設計師建立的元素"){zoomable="yes"}

</td>
</tr>
</table>

## 場景狀態檔案

在 3D View 中設定好材質、攝影機、燈光等後，該狀態可以儲存到場景狀態檔案（.sbsscn），之後可載入以恢復該狀態。 例如，你可能想設置幾個場景來預覽不同材質，或是特定的光照環境。

![載入場景狀態檔案](../assets/loadSceneStateFile.gif "載入場景狀態檔案"){zoomable="yes"}

儲存的場景狀態也可以作為 3D View 的預設狀態，因此每當新建 3D View 時，該狀態都會被使用。 如果你想在 Sphere 2-Tiles 網格上預設預覽材質，且平鋪值為 2，並搭配特定環境貼圖，這很有用。

與場景狀態檔案相關的動作位於 3D View 的場景選單中，並在此處有[&#128279;](../interface/3d-view/3d-view.md)詳細說明。

場景狀態檔案使用 XML 格式，並且如果專案設定中有別[&#128279;](../interface/preferences-window/project-settings/project-settings.md)名，也會使用[別名](../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md)。

>[!NOTE]
>
> 渲染器不會儲存到場景狀態檔案。
