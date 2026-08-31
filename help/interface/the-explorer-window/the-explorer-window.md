---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/the-explorer-window.html"
breadcrumb-title: ''
description: 使用 Substance 3D Designer 的 Explorer 視窗瀏覽、整理和管理你的專案檔案與資源。
helpx_creative_field: ""
helpx_description: Designer > Interface > Explorer
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 總管
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '1104'
ht-degree: 0%

---


# 總管

本頁介紹了Substance 3D Designer](https://www.adobe.com/products/substance3d-designer.html)中的[Explorer停靠座。這個 dock 讓你可以管理包裹及其資源。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## 概觀

Explorer 底座是你管理目前在 Substance 3D Designer 中開啟的檔案和資源的地方。 它會顯示目前所有已開啟的套件清單，每個套件以階層形式展開，顯示 [裡面的資源](../../resources/resources.md)。

Explorer 是你專案的起點和結束點，因為它讓你能創建、儲存和匯出任何類型的資源。

</td>
<td style="border: 0;" valign="top">

![探險者碼頭](the-explorer-window.resources/the-explorer-window-01.jpg "探險者碼頭")

</td>
</tr>
</table>

你可以透過 Explorer 底座執行幾個重要操作：

* 建立新的套件與圖表
* 載入現有套件
* 儲存並關閉已載入的包裹
* [匯入與連結資源](../../resources/importing-linking-and-new/importing-linking-and-new-resources.md)
* [將圖形結果匯出成貼圖](../../compositing-graphs/exporting-bitmaps/exporting-bitmaps.md)
* [將套件發佈到 Substance 3D 資產（SBSAR）](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md)
* [傳送套件至其他 Substance 3D 應用程式](send-to-interoperability/send-to-interoperability.md)
* [從網格烘焙貼圖](../../bakers/bakers.md)

## 頂端工具列

這個工具列讓你能快速執行與整體工作流程相關的功能。 所有按鈕都是 *情境感知*&#x200B;的，也就是說它們會根據你在檔案總管中當前選擇來啟動和改變行為。

![](the-explorer-window.resources/the-explorer-window-02.png)  <b>儲存</b> 所選套件。

![](the-explorer-window.resources/the-explorer-window-03.jpg)  <b>發佈或 [發送](../../interface/the-explorer-window/send-to-interoperability/send-to-interoperability.md)</b> 選定元素：

* [將任一選定的套件發佈至Substance 3D資產（SBSAR）;](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md)
* 將所選套件寄送至 [Substance 3D Sampler](https://www.adobe.com/products/substance3d-sampler.html)、 [Substance 3D Painter](https://www.adobe.com/products/substance3d-painter.html) 或 [Substance 3D Stager](https://www.adobe.com/products/substance3d-stager.html)。

![](the-explorer-window.resources/the-explorer-window-04.png)  <b>發佈或傳送如前版本：</b> 以相同設定發佈或傳送選取的元素。 此選項僅適用於本場至少已發佈&#x200B;*過一次***&#x200B;的套件。

![](the-explorer-window.resources/the-explorer-window-05.jpg)  <b>移除選取圖中未使用的節點</b> 。 該工具遵循以下規則：

* 此工具僅在所選項目為 *相同類型*&#x200B;時可用：僅限圖表、資料夾或套件;
* 當選取包含資料夾或套件時，工具會遞迴&#x200B;*地清理其中*&#x200B;的所有圖表;
* 如果其中一個目標圖是 [Substance 圖](../../compositing-graphs/substance-compositing-graphs.md)，則有第二個選項，可以清理該圖中節點上的所有參數函數。

想了解更多關於此工具的資訊，請參閱圖視圖](../../interface/the-graph-view/the-graph-view.md)頁面的[「移除未使用節點」區塊。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![發佈/傳送下拉選單](the-explorer-window.resources/the-explorer-window-06.jpg "發佈/發送下拉選單")

*發佈/傳送*

</td>
<td style="border: 0;" valign="top">

![移除未使用的節點下拉選單](the-explorer-window.resources/the-explorer-window-07.jpg "移除未使用的節點下拉選單")

*移除未使用的節點*

</td>
</tr>
</table>

## 情境選單

你與 Explorer 的大部分互動都是透過情境選單進行，透過在 Explorer 的樹狀圖中點擊 RMB 項目來顯示。

可用的選項會根據所選及點擊的項目而有所不同：

+++空曠空間

空位僅提供目前開放的套件下方。 點擊現有項目旁邊不算是空白。

<b>新套件</b>：建立一個新的空套件;

<b>開啟套件</b>：開啟檔案對話框以開啟 SBS 檔案。

+++

+++包裝

<b>新版</b>可以讓你建立新的圖表（[Substance 圖](../../compositing-graphs/substance-compositing-graphs.md)、[點陣](../../resources/bitmap-resource/bitmap-resource.md)圖和[向量圖形](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md)資源，以及&#x200B;*用於排序內容的資料夾*

<b>匯入</b>和<b>連結</b>可以讓你帶資源進來[](../../resources/importing-linking-and-new/importing-linking-and-new-resources.md)

<b>重新載入</b>、 <b>儲存、另存新檔</b> 和<b> 另存副本</b> ，讓你可以儲存到磁碟，或從磁碟中調出之前儲存的套件版本。

<b>Publishing .sbsar 檔案</b> 與<b> Republish .sbsar 檔案</b> 讓您能 [將未編譯、未優化的 Substance 圖表發佈](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md) 成高效且可攜的 SBSAR 檔案，供我們在其他 Substance 應用程式與整合中使用使用。 「以先前發佈」會重複先前的發佈動作，並使用相同的選項，跳過選項對話框以加快迭代速度。 工具列中包含具有相同功能的按鈕。

<b>帶依賴</b> 的匯出和儲存和發佈是不同的。 它會收集你的 SBS 檔案，收集所有參考的資源和相依，並建立一個自成一體的套件。 對話框讓你選擇要收集哪些函式庫，以及檔案是否應該是壓縮壓縮檔（7-zip）。 這是個不錯的選擇，可以與他人分享 SBS 檔案，不用擔心遺漏相依。

<b>發送至...</b> 會開啟一個子選單，讓你直接 [將包裹傳送](send-to-interoperability/send-to-interoperability.md) 到 [Substance 3D取樣器](https://www.adobe.com/products/substance3d-sampler.html)、 [Substance 3D Painter](https://www.adobe.com/products/substance3d-painter.html)、 [Substance 3D Stager](https://www.adobe.com/products/substance3d-stager.html) 或 [Substance Player](https://helpx.adobe.com/substance-3d-player/home.html)。

<b>複製</b> 會複製所選的包裹。

<b>將複製的圖表和/或資源&#x200B;*貼</b>上到*&#x200B;所選套件中。

<b>關閉套件會</b> 關閉所有被選取的套件

<b>計算輸出</b> 會強制設計器計算套件中所有圖形的所有輸出。

<b>在檔案總管中顯示...</b> 會在作業系統檔案總管視窗中開啟該套件的位置

<b>相依性管理器</b> 會為所選套件開啟相依性管理器視窗。

<b>Open Dependencies</b> 會開啟 Explorer *[中的所有相依（僅限* Substance 圖）。](../../compositing-graphs/substance-compositing-graphs.md)

+++

+++物質圖

<b>開啟：</b>（返回）在圖檢視](../../interface/the-graph-view/the-graph-view.md)中開啟此圖[。

<b>複製：</b> *（Ctrl-C）* 將目前的圖表複製到剪貼簿。

<b>移除：</b> （刪除）從此套件中刪除圖表。

<b>重新命名：</b> （F2） 重新命名此圖表。

<b>3D 視圖中的視圖輸出：</b> 將此圖的輸出傳送至 [3D 視圖](../../interface/3d-view/3d-view.md)，以材質形式顯示。

<b>計算輸出：</b> 計算此圖的輸出並將它們保存在記憶體中。

<b>匯出輸出...：</b> 開啟匯 [出到點陣圖的對話框。](../../compositing-graphs/exporting-bitmaps/exporting-bitmaps.md)

+++

+++3D 場景資源

<b>開啟：</b>（返回）在3D視圖](../../interface/3d-view/3d-view.md)中使用此3D網格[，取代標準的立方體或平面。

<b>複製：</b> （Ctrl-C）將此資源複製到剪貼簿。

<b>貼上：</b> （Ctrl-V）從剪貼簿貼上資源。

<b>移除：</b> （Del） 從此套件中刪除資源。

<b>重新命名：</b> （F2） 重新命名此資源。

<b>重新載入：</b> 強制從磁碟重載這個網格。

<b>在檔案總管中顯示：</b> 在磁碟上資源所在位置開啟系統檔案瀏覽器視窗。

<b>重新定位：</b> 將此資源改為連結到另一個檔案。

<b>烘焙模型資訊...：</b> 開啟 [烘焙對話框。](../../bakers/bakers.md)

+++

+++資料夾

<b>新增：</b> 允許你在資料夾中建立新的圖表（[Substance 圖表](../../compositing-graphs/substance-compositing-graphs.md)、 [Substance 函數圖](../../function-graphs/function-graphs.md)、 [點陣](../../resources/bitmap-resource/bitmap-resource.md) 圖與 [向量圖形](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md) 資源，以及 *用於排序內容的資料夾* ）。

<b>匯入</b>與連結：</b>讓你能帶入[資源](../../resources/importing-linking-and-new/importing-linking-and-new-resources.md)並放入資料夾。<b>

<b>複製：</b> （Ctrl-C） 將資料夾及其所有內容複製到剪貼簿。

<b>貼上：</b> （Ctrl-V）從剪貼簿貼上資料夾及其所有內容。

<b>重新命名：</b> （F2） 重新命名此資料夾。

<b>移除：</b> *（Del）* 刪除資料夾及其所有內容。

<b>計算輸出：</b> 計算資料夾中所有圖形的輸出，並將其保存在記憶體中。

+++

## 底部工具列

Explorer 底座底部的工具列提供有關套件或套件資源的資訊：

<b>![](the-explorer-window.resources/the-explorer-window-08.jpg)相依性：</b> 當選擇套件時，其套件相依性會列在專用面板中。

<b>![](the-explorer-window.resources/the-explorer-window-09.jpg)資訊：</b> 提供與目前所選套件或資源相關的元資料：

* 套件：套件的完整檔案路徑
* [點陣資源](../../resources/bitmap-resource/bitmap-resource.md)：資源的完整檔案路徑、ICC [設定檔](../../color-management/color-management.md)、影像大小及 [匯入方式](../../resources/importing-linking-and-new/importing-linking-and-new-resources.md) （即 *連結* 或 *匯入*）

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![相依](the-explorer-window.resources/the-explorer-window-10.jpg "面板相依相依面板")

*相依關係*

</td>
<td style="border: 0;" valign="top">

![資訊面板](the-explorer-window.resources/the-explorer-window-11.jpg "資訊面板")

*資訊*

</td>
</tr>
</table>
