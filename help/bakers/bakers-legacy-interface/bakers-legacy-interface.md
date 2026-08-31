---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/bakers/bakers-legacy-interface.html"
breadcrumb-title: ''
description: 熟悉舊版本的使用者，了解 Substance 3D Designer 烘焙者的舊介面。
helpx_creative_field: ""
helpx_description: Designer > Bakers > Bakers Legacy Interface
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Bakers 傳承介面
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 2%

---


# Bakers 傳承介面

以下是 Adobe Substance 3D Designer[&#128279;](https://www.adobe.com/products/substance3d-designer.html) 6.0.4 版本前所提供的烘焙介面說明。

## 概觀

![](bakers-legacy-interface.resources/bakers-legacy-interface-01.png)

烘焙面板分為四個部分：

### 1：場景

![](bakers-legacy-interface.resources/bakers-legacy-interface-02.png)

讓你定義網格中哪個部分參與烘焙過程。

版本 6 新增內容，你還可以依材質選擇：

![](bakers-legacy-interface.resources/bakers-legacy-interface-03.png)

### 2：烘焙師

![](bakers-legacy-interface.resources/bakers-legacy-interface-04.png)

按下 ![](bakers-legacy-interface.resources/bakers-legacy-interface-05.png) 按鈕，你可以將想要的烘焙師加入加工清單

>[!NOTE]
>
> 烘焙的處理順序依照清單順序（從上到下）：如果你想在其他烘焙過程中重複使用烘焙結果（像法線貼圖），這點可能很重要

點擊烘焙師排版中的「+」可以把烘焙師加到堆疊中（你可以把任意數量的烘焙師放進堆疊裡）。

.![](bakers-legacy-interface.resources/bakers-legacy-interface-06.png)

你可以按 ![](bakers-legacy-interface.resources/bakers-legacy-interface-07.png)

你可以選擇烘焙流程並使用 ![](bakers-legacy-interface.resources/bakers-legacy-interface-08.png)

### 3：麵包師參數

![](bakers-legacy-interface.resources/bakers-legacy-interface-09.png)

此區塊顯示目前所選烘焙師的具體選項。

### 4：共同參數

![](bakers-legacy-interface.resources/bakers-legacy-interface-10.png)

顯示烘焙師間共享的參數。

>[!NOTE]
>
> 預設情況下，更改這些參數之一;會影響所有烘焙器，除非你勾選所有烘焙器共用的覆蓋參數：此時變更將發生在目前烘焙器上。

* **資源名稱** 欄位允許你更改產生的點陣圖名稱（如有需要）。
* **檔案格式** 下拉選單可讓你從預設格式（Windows 或 OS/2 點陣圖格式，「BMP」）更改檔案格式。
* **&#x200B;**&#x200B;**「將資源放入**&#x200B;網格特定資料夾」的勾選框可以讓你選擇生成的點陣圖是否與模型相同層級，或是存放在一個名為「資源」的新子資料夾中。
* **此方法** 允許你決定新的點陣資源是要連結還是嵌入到 Substance 套件中。
* **&#x200B;**&#x200B;資料夾可以讓你定義要儲存地圖的位置。

按下烘焙視窗右下角的確定鍵，烘焙過程就會開始。

版本 6 新增功能：你現在可以用取消按鈕取消烘焙過程：

![](bakers-legacy-interface.resources/bakers-legacy-interface-11.png)
