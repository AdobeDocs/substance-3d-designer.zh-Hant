---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/working-with-3d-scenes/exporting-scenes.html"
breadcrumb-title: ''
description: 在 Designer 裡用 3D View 場景選單中的「匯出場景」動作，匯出所有編輯的 3D 場景。
helpx_creative_field: ""
helpx_description: Designer > Working with 3D scenes > Exporting scenes
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 匯出場景
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 1%

---


# 匯出場景

當你需要匯出包含所有在 Designer 中完成的編輯的場景時，請使用 3D View](../../interface/3d-view/3d-view.md) 的「場景」選單中的「匯出場景...」操作[。

匯出為 USD 格式時，場景內容會與場景瀏覽器](../../interface/3d-view/scene-browser/scene-browser.md)中顯示[的樹相符。

對於其他格式，場景內容及其內部結構會依據所選檔案格式所支援的功能而定。

>[!NOTE]
>
> Designer 新增到場景的所有項目都會包含在匯出的場景中：預設相機、預設環境，所有材質都會複製任何額外的燈光。

![場景匯出動作](../../assets/exportActions.png "場景匯出動作"){zoomable="yes"}

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## 匯出場景

</td>
<td style="border: 0;" valign="top">

### 將場景匯出為圖層

</td>
<td style="border: 0;" valign="top">

### 材質

</td>
</tr>
</table>

## 匯出場景

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

「匯出場景......」在「場景」選單中的動作會將經過編輯的 3D 場景輸出得很嚴重：場景被 *壓* 扁，且任何對原始的參考資料都消失了。

這表示對原始場景的編輯完全不會影響匯出後的場景。

</td>
<td style="border: 0;" valign="top">

![匯出場景檔案 - 扁平](../../assets/exportFlattened.png "化 匯出場景檔案 - 扁平化"){zoomable="yes"}

</td>
</tr>
</table>

## 將場景匯出為圖層

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

「將場景匯出為圖層......」動作會匯出成 <b>USD</b> 格式（.usd、.usda、.usdc、.usdz），且是 *非破壞*&#x200B;性的：主匯出檔案會引導一條 *參考* 鏈，將新場景的所有編輯部分儲存在獨立的 USD 檔案中。

這表示對原始場景的編輯會帶到匯出後的場景中。

</td>
<td style="border: 0;" valign="top">

![匯出場景檔案 - 分層](../../assets/exportLayered.png "匯出場景檔案 - 分層"){zoomable="yes"}

</td>
</tr>
</table>

匯出檔案的結構如下：

* <b>主檔案</b>
  * <b>.layers</b>：參考下方的子圖層並宣告材質覆蓋，將幾何體綁定到 Designer 建立的材質副本。
    * <b>.assembly</b>：參考 .scene# 檔案並宣告幾何覆蓋，這些覆蓋會帶來設計師重新計算的受覆寫材質影響的幾何體資料。
      * <b>.scene#</b>：參考原始場景。
    * <b>.camera</b>：宣告設計師新增的攝影機到場景中。
    * <b>.light</b>：宣告設計師在場景中新增的燈光。
    * <b>.material</b>：宣告 Designer 新增到場景中的材質副本，這些材質使用匯出的材質。

## 材質

材質會匯出到匯出檔案旁的目錄，並以檔案命名，並加上「<b>\_textures</b>」後綴。

它們使用 <b>PNG</b> 格式，除了 HDR 材質（浮點）則使用 <b>EXR</b> 格式。
