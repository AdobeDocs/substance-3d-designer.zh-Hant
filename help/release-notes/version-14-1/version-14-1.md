---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/release-notes/version-14-1.html"
breadcrumb-title: ''
description: 請參閱 Substance 3D Designer 14.1 版本的發行說明，了解節點排列工具以及新的樣條線與路徑節點。
helpx_creative_field: ""
helpx_description: Designer > Release Notes > Version 14.1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 版本 14.1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '1019'
ht-degree: 0%

---


# 版本 14.1

此更新引入新功能，提升你日常使用 Substance 3D Designer 的便利性：節點排列工具可快速優化圖表佈局，複製貼上參數可套用參數至其他節點，並在 2D 視圖中新增像素腳位，追蹤特定像素以除錯圖表。 它也新增了新內容，主要是為了完成樣條線和路徑節點集合。

*發行日期：2025年1月14日*

![樣條上的散射樣條](../../assets/fond.png)

## 樣條與路徑更新

樣條線和路徑節點是在 13.0 版本中引入的，感謝你的回饋，我們已經做了初步的改進。 首先，我們新增了 [散佈樣條](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/scatter-splines-splines/scatter-splines-on-splines.md)條節點上的散佈樣條，它將樣條線分布在父樣條線上，提供類似一般散佈節點的選項。 此外， [遮罩](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) 路徑節點也被強化，能更好地控制路徑上第一個頂點的位置。 我們也讓 Spline Bridge List](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-bridge-list/spline-bridge-list.md) 節點能引入隨機性[。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![散點樣條曲線動畫 1](../../assets/spline1.gif){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![樣條曲線2上的散射樣條](../../assets/spline2.gif){zoomable="yes"}

</td>
</tr>
</table>

## 節點對齊工具

如果你很想保持圖表乾淨易讀，節點 [對齊工具](../../interface/the-graph-view/node-alignment-tools/node-alignment-tools.md) 就是為你量身打造，並且已經徹底重新設計！ 現在可以將節點均勻排列（水平或垂直），且對齊節點可透過整齊堆疊避免重疊。 更棒的是：這兩個功能都考慮到節點的實際大小！

![對齊節點](../../assets/alignment.gif){zoomable="yes"}

## 複製/貼上參數

現在可以 [複製一個節點的參數並貼到另一個](../../compositing-graphs/manage-parameters/manage-parameters.md)節點，因此目標節點中所有匹配的參數都會更新為來源節點的值。 這非常有用，例如你想將色彩節點的參數帶到灰階版本，或反過來。 （例如，圖塊取樣器節點）

## 2D 視圖中的釘點像素

2D 視圖中的新 [色彩取樣器工具](../../interface/2d-view/color-sampler/color-sampler.md) 允許你透過在像素上放置一個針腳來追蹤該像素的數值。 這對於確保你在圖中多個節點上看到同一像素的資訊非常有用。 打開資訊面板來存取這個工具，試試看吧！

![色彩取樣器：使用 工具](../../assets/color-sampler-demo.gif "色彩取樣器：使用 工具"){width="640px" zoomable="yes"}

## 搜尋改進

[節點尋找](../../interface/the-graph-view/node-finder/node-finder.md)工具略有改進：

* 你現在可以啟用遞迴模式以進行更深入的搜尋;
* 若想搜尋精確詞彙，可以關閉模糊模式;
* 啟用節點尋找工具時，焦點會自動設定在搜尋欄位上;
* 工具列的佈局也經過重新設計以節省空間。

![搜尋工具列](../../assets/search-53.png){width="640px"}

## 影片

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

[![視頻散射樣條在樣條上](../../assets/video_spline.png)](https://www.youtube.com/watch?v=aUUWV1dYQdI)

</td>
<td style="border: 0;" valign="top">

[![影片使用者體驗功能](../../assets/video_ux.png)](https://www.youtube.com/watch?v=LwexybAEjaI)

</td>
</tr>
</table>

## 發行說明

### 14.1.0

*（2025年1月14日發行）*

### 新增內容

* [2D 視圖]在資訊面板中新增釘選的像素顯示
* [API]在圖視場景中暴露節點的 BBox 大小
* [內容]「材質高度混合」：新增「高度遮罩」輸出
* [內容]「路徑頂點處理器」：使用「編輯函數」按鈕來設定「每個頂點函數」參數
* [內容]自動等級：清除未使用的參數，調整標籤與提示
* [內容]遮罩到路徑 v2
* [內容]新最小變異數均值節點（MLV）
* [內容]新中位數濾鏡節點
* [內容]量化顏色：新增「最近」篩選選項
* [內容]樣條橋列表：加入隨機樣條偏移參數
* [內容]樣條鍵工具：新樣條（二次）節點
* [內容]三角形網格：改變三角測量方法並使用迴圈
* [內容]樣條節點上的新散射樣條
* [Cooker]將「像素比率」的基礎參數暴露為「$pixelratio」靜態變數
* [撞擊報告]整合新的撞擊報告視窗
* [引擎]加入Vulkan/Metal版本的混合引擎
* [圖表]材質模式：當選擇單一連結時，允許無使用輸入連接
* [圖]材料連結：允許當連結不模糊時標準連接
* [圖]節點對齊工具：新增水平/垂直分布、左右/上/底部對齊，並支援堆疊節點
* [函式庫]修正上下文選單中的文字顏色
* [參數]將參數從一個節點複製到另一個節點
* [屬性]「全部重設」：移除確認彈窗
* [資源]在「連結點陣圖」對話框中將格式設為「全格式」
* [搜尋]新增啟用/停用遞迴模式的方法
* [搜尋]新增啟用/停用模糊搜尋的方法
* [搜尋]啟用 Node Finder 時，請始終顯示並設定焦點於搜尋詞欄位，並使用其鍵盤快捷鍵
* [搜尋]重新設計篩選選項
* [捷徑]允許分配「V」、「H」和「S」鍵
* [第三方]升級至 Qt 6.5.7
* [用戶體驗]模態對話不應被最小化
* [用戶體驗]移除警報對話中的水平捲動

### 修正方法

* [內容]斜角：正常格式不受全域偏好影響
* [內容]色彩遮罩節點不會忽略 alpha
* [內容]方向距離：當輸入具有垂直影像比例時，結果錯誤
* [內容]洪水填充映射器：因缺失變數而發出警告
* [內容]直方圖計算：結果是應有值的16倍
* [內容]RT 焦散在非正方形解析度下無法運作
* [內容]樣條橋列表：使用開始/結束偏移時結果錯誤
* [內容]樣條線選擇：輸出樣條量可以大於輸入樣條量
* [內容]Spline Warp 在 SSE 引擎下產生黑色結果
* [內容]三角形格子：圖案無法正確鋪磚
* [內容]三角形格：在特定情況下，平鋪會被破壞
* [資料]在特定情況下更改圖形輸入識別碼時會當機
* [函數圖]長值在「浮點」節點上重疊
* [特效地圖]顯示象限節點屬性時當機
* [圖表][UDIM]在 UDIM 列表中有滾動條會產生 1..1 1..2 條目
* [圖][捷徑]使用捷徑建立的節點在節點複製後不會被放置在現有連結上
* [屬性]當值無效時參數顯示錯誤
* [發佈]互惠相依關係在發佈套件時會形成無限迴圈
* [發佈]在未載入相依的套件上使用「發佈」動作時，發生無聲失敗
* [使用者介面]「父大小」小工具展開時無法正確顯示，可能阻塞介面（僅限 macOS）
* [使用者介面]主視窗在某些情況下會落後於其他應用程式（僅限 Windows）
