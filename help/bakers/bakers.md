---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/bakers.html"
breadcrumb-title: ''
description: 學習如何使用 Substance 3D Designer 烘焙工具，將網格資訊計算成貼圖檔案。
helpx_creative_field: ""
helpx_description: Designer > Bakers
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 烘焙師
user-guide-description: ''
user-guide-title: ''
source-git-commit: 68389d2a09ef1db6c14073029efdbfd9d48c83c8
workflow-type: tm+mt
source-wordcount: '597'
ht-degree: 0%

---


# 烘焙師

烘焙是指將網格資訊轉移到貼圖中的&#x200B;**動作**。這些資訊接著會被著色器和/或 Substance 濾鏡讀取，以產生更進階的效果或貼圖。

>[!NOTE]
>
> 想了解更多烘焙知識，請參考 [烘焙說明](https://experienceleague.adobe.com/en/docs/substance-3d/bakers/home)。

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

烘焙視窗可以透過檔案總管[&#128279;](../interface/the-explorer-window/the-explorer-window.md)視窗中的網格檔案進入。右鍵點擊網格名稱，選擇「**烘焙模型資訊**」以開啟烘焙視窗。

</td>
<td width="33.33%" style="border: 0;" valign="top">

![3D 場景資源情境選單中的「烘焙模式資訊」選項 3D 場景資源情境選](../assets/sd-mesh-right-click.png "單中的「烘焙模式資訊」選項")

</td>
</tr>
</table>

![烘焙窗口](../assets/sd-window-overview.png "烘焙窗口")

## 概觀

烘焙窗口分為數個面板，以下將說明。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### 烘焙元素

這個面板控制低多邊形網格的哪一部分將用於烘焙。

它列出了低多邊形網格檔案中所呈現的幾何體。 預設情況下，列表是根據檔案中發現的個別材質，但當需要時，也可以切換到子網格。 你可以取消勾選烘焙過程中應該忽略的元素。

</td>
<td style="border: 0;" valign="top">

![](../assets/sd-mesh-selection.png)

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### 輸出

這個面板控制烘焙貼圖的位置。

</td>
<td style="border: 0;" valign="top">

![](../assets/sd-output.png)

</td>
</tr>
</table>

| *參數* | *描述* |
| --- | --- |
| **方法** | 控制烘焙後的貼圖如何與 Substance 套件一起儲存。可能的數值：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Embedded</strong> ：烘焙的貼圖會儲存在 Substance 套件旁邊的子資料夾中，並有特定命名。</li><li data-preserve-html="true"><strong>連結</strong> （預設）：烘焙的貼圖會儲存在定義的資料夾中，然後再被引用到打包的 Substance 中。</li></ul> |
| **資料夾** | 儲存後烘焙材質的位置。 點擊三點按鈕開啟檔案對話框並選擇匯出資料夾。右側會有一個勾選標記，用來表示該資料夾是否真實存在。 |
| **名稱** | 烘焙材質的命名慣例。 點擊三點按鈕打開下拉選單，並插入其他佔位符（烘焙名稱、自訂、材質、網格）。 |
| **範例** | 模擬一個檔名來測試命名慣例。 |
| **將資源放入特定網格的資料夾** | 啟用後，烘焙的材質會儲存在一個名為網格檔案的資料夾中。 |

### 高解析度網格

這個面板控制高多邊形網格列表及相關設定。 更多資訊請參閱 [常見參數](https://experienceleague.adobe.com/en/docs/substance-3d/bakers/bakers-settings/common-parameters) 。

![高解析度網格](../assets/sd-high.png "高解析度網格")

### 預設值

更多資訊請參閱 [常見參數](https://experienceleague.adobe.com/en/docs/substance-3d/bakers/bakers-settings/common-parameters) 。

![預設值](../assets/sd-default-values.png "預設值")

### Baker 渲染清單與設定

**Bakers 的渲染清單**&#x200B;是你可以選擇想要產生哪種烘焙材質的地方。預設情況下，清單是空的。

* **新增烘焙師：** 點擊「新增烘焙師」按鈕。
* **移除烘焙師：** 在列表中選擇烘焙師，然後點擊「刪除烘焙師」按鈕。
* **將烘焙師移到頂部：** 在列表中選擇烘焙師，然後點擊「拉到頂部」按鈕。
* **往下移動烘焙師：** 在列表中選擇烘焙師，然後點擊「向下推」按鈕。

每個烘焙師預設繼承預設值（見上文）。 例如，點擊烘焙師行中的儲存格即可覆蓋大小（解析度）。 這點對線上其他設定也適用。

點擊清單中的烘焙器時，烘焙者參數檢視會更新其特定參數。

欲了解更多具體參數，請參閱： [Bakers 設定](https://experienceleague.adobe.com/en/docs/substance-3d/bakers/bakers-settings/bakers-settings)。

![Bakers 渲染列表](../assets/sd-baker-list.png "Bakers 渲染列表")
