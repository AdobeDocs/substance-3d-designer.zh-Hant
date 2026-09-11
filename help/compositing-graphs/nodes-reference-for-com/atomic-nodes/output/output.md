---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/output.html"
breadcrumb-title: ''
description: ''
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Output
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 輸出
user-guide-description: ''
user-guide-title: ''
source-git-commit: 31d4d930c789d693362ef3a16c72016bd030a89b
workflow-type: tm+mt
source-wordcount: '788'
ht-degree: 0%

---


# 輸出

<table>
<tr style="border: 0;">
<td style="border: 0; width: 30%; vertical-align: top">

![原子節點：輸出](output.resources/comp_output_1.png "原子節點：輸出"){width="200px"}

</td>
<td style="border: 0; vertical-align: top">

輸出節點指定 <b>物質圖的結果</b> ，或若存在多個輸出節點則指定其結果之一。

連接到圖的輸出節點的影像或值，由任何代表該圖的實例節點輸出[，並可[匯出為圖輸出](../../../../compositing-graphs/exporting-bitmaps/exporting-bitmaps.md)。](../../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)

</td>
</tr>
</table>

同樣地，當已發佈的 [SBSAR 檔案](../../../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md) 包含此圖時，該檔案可輸出該影像，並用於任何使用該檔案的整合或外掛。

它有一個單一輸入槽，且不拘型別，意即在與其連接的資料型別之後自動輸入。

它沒有參數，而是有屬性，對於正確標示輸出並使其用於預期用途非常重要。

每個 Substance 圖必須至少有一個&#x200B;**&#x200B;輸出節點。若無輸出，圖無法回傳實際結果，並 [會觸發警告](../../../../technical-issues/warnings-and-errors/warnings-and-errors.md) 。

## 屬性

|                             |                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>識別碼</b> *弦* | 輸出的唯一識別碼。 此屬性不能留空，且不得包含特殊字元或空格。   識別碼是因為節點的標籤是空白的，「Label」屬性會留空。 它也可以用來命名 [匯出的材質](../../../../compositing-graphs/exporting-bitmaps/exporting-bitmaps.md)。 |
| <b>描述</b> *弦* | 輸出工具提示的可選描述是 Substance 圖表。 |
| <b>唱片公司</b> *弦* | 此標記用於輸出節點，並在代表此圖的實例節點](../../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)中作為對應連接器[。標籤可能包含空格和特殊字元。 |
| <b>使用者資料</b> *弦* | 可選的元資料可用於特定過濾操作。 [Substance 3D Painter](https://www.adobe.com/products/substance3d/apps/painter.html) 利用這些資料來 [推動部分功能](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/content/creating-custom-effects/user-data)...... |
| <b>團體</b> *弦* | 屬性用於將輸出群組在一起，用於 Designer [的連結建立模式](../../../../interface/the-graph-view/link-creation-modes/link-creation-modes.md)。   具有相同「群組」屬性的輸出會在「Compact Material」連結建立模式下以單一連線呈現。 |

## 整合屬性

這些屬性是供整合或外掛使用，使用已發佈的 SBSAR 檔案](../../../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md)中的[圖表。

因此，它們對點陣圖匯出](../../../../compositing-graphs/exporting-bitmaps/exporting-bitmaps.md)的格式[沒有影響。此外，Designer 中僅 <b>使用使用</b> 屬性，詳情請見下文。

+++ 使用情況

|                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>組成部分</b> *弦* | 用來將一些貼圖通道映射到 AxF 工作流程中適當的 SVBRDF 著色器輸入。 |
| <b>使用情況</b> *弦* | 定義輸出節點的型別與使用方式。 這個房產很重要，因為它能驅動：<ul data-preserve-html="true"> <li data-preserve-html="true">在使用某些[連結建立模式](../../../../interface/the-graph-view/link-creation-modes/link-creation-modes.md)時，Substance 圖中節點的連結 </li> <li data-preserve-html="true">將貼圖與 3D View 中的著色器連結（見下文：「[關於 3D View](#about-the-role-of-usages-in-the-3d-view) 中使用的角色」）</li> <li data-preserve-html="true">在整合/插件中將貼圖與材質連結</li> </ul> |
| <b>色彩空間</b> *弦* | 設定該輸出應解讀的色彩空間。 在其他應用程式中被部分整合使用，且在 Designer 中沒有影響。 |

+++

### 關於 3D 視圖中使用的角色

由於圖形輸出通常是特定紋理通道的最終結果，輸出可以自動傳送到3D View所用著色器的適當取樣器。

事實上，若 <b>輸出 Usage</b> 屬性 *與 3D View 中的取樣器使用* 量相符，會連接到該取樣器。 例如，一個有 `basecolor` 使用情況的輸出會連接到 `basecolor` 3D View 著色器的取樣器。 （了解更多： [ 以3D視圖](../../../../interface/3d-view/3d-view.md#view-data-in-3d-view)查看資料）

在圖形檢視中[點選空白區域的 RMB，並在情境選單中選擇<b>「3D 檢視</b>中的輸出」選項，將所有輸出連接到 3D 檢視取樣器，並有&#x200B;*相同的使用情況*。](../../../../interface/the-graph-view/the-graph-view.md)

>[!IMPORTANT]
>
> 如果有多個使用順序，例如將使用分配給包裝材質中的頻道，只有 *列表中的第一個使用* 會連接到 3D 檢視。 這是已知的限制。

## 預設輸出

當一個圖有多個輸出時，可以設定其中一個作為該圖的預設輸出。 此規定應用於以下情況的輸出：

* 任何代表該圖的實例節點的縮圖
* 在 2D 視圖中檢視這些實例節點
* 該圖的縮圖在圖書館中（點此](../../../../interface/preferences-window/project-settings/project-settings.md)了解如何新增資源[）

此功能允許您將圖形輸出以任意順序排列，獨立於圖形作為節點的視覺化方式。

要將輸出節點設為圖的預設輸出：

* 右鍵點選輸出節點，並在情境選單中選擇「設定為預設輸出」動作。
* 在輸出節點的屬性中，使用「屬性」區塊標頭中的「設定為預設」按鈕。

以下是一個設定預設輸出前後的實例節點範例：

<table>
  <tr style="border: 0">
    <td style="border: 0">
      <img src="output.resources/defaultouput2.png" alt="defaultouput2">
      <br><i>之前</i>
    </td>
    <td style="border: 0">
      <img src="output.resources/defaultouput1.png" alt="預設1">
      <br><i>之後</i>
    </td>
  </tr>
</table>
