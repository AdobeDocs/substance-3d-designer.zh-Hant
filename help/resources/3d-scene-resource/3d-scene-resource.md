---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/resources/3d-scene-resource.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Designer 中匯入並使用3D場景資源，進行材質預覽與測試。
helpx_creative_field: ""
helpx_description: Designer > Resources > 3D scene resource
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D 場景資源
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '506'
ht-degree: 0%

---


# 3D 場景資源

本頁說明 **Substance 3D Designer 中的 3D 場景** 資源類型，包括其支援的檔案格式及使用方式。

## 概觀

3D 場景資源可用於多種工作流程：

* [烘焙網格貼圖](../../bakers/bakers.md)
* *在 3D 檢視中預覽 Substance 圖表的](../../compositing-graphs/substance-compositing-graphs.md)[貼圖* [](../../interface/3d-view/3d-view.md)

支援以下 3D 場景檔案格式：

* [美元](https://graphics.pixar.com/usd/release/index.html) （\*.usd）
* [美國農業部（USDA](https://graphics.pixar.com/usd/release/index.html) ）（\*.usda）
* [USDZ](https://graphics.pixar.com/usd/release/index.html) （\*.usdz）
* [Autodesk FBX](https://www.autodesk.com/products/fbx/overview) （\*.fbx）
* [波前 OBJ](https://www.fileformat.info/format/wavefrontobj/egff.htm) （\*.obj）
* [Autodesk 3D Studio 網格](https://knowledge.autodesk.com/support/3ds-max/learn-explore/caas/CloudHelp/cloudhelp/2022/ENU/3DSMax-Data-Exchange/files/GUID-A16ECF7F-70E5-4F9F-8EAD-35F5CFB485A2-htm.html) （\*.3ds）
* [Collada](https://www.khronos.org/collada/) （\*.dae）
* [Autodesk AutoCAD 繪圖](https://knowledge.autodesk.com/support/autocad/learn-explore/caas/CloudHelp/cloudhelp/2019/ENU/AutoCAD-Core/files/GUID-D4242737-58BB-47A5-9B0E-1E3DE7E7D647-htm.html) （\*.dxf）

## 網狀儲存

3D 場景 *只能* 連結，也就是說它們會停留在磁碟上的位置，只是在應用程式中被參考。

當包含 3D 場景資源的套件以 Substance 3D](https://www.adobe.com/products/substance3d/3d-augmented-reality.html) 資產（SBSAR）發佈[時，該網格不會被&#x200B;*嵌入*，而是被丟棄。

## 烘焙網格貼圖

將 3D 場景連結到你的套件中，是唯一能從 [該場景幾何體中烘焙出網格貼圖](../../bakers/bakers.md) 的方法。 您可以採取以下步驟開始：

* 點選 *套件的 RMB* ，並在情境選單中選擇 <b>連結> 3D 網格</b> 選項
* 選擇任何支援的 3D 場景檔案
* 如果 <b>跳出「連結成 Udim 網格</b> 」對話框提示，請點擊 *「否* 」，除非你想烘焙 UV 圖塊
* 在資源總管載[入後，點選&#x200B;*右鍵*，然後在情境選單中選擇<b>「烘焙模型資訊</b>](../../interface/the-explorer-window/the-explorer-window.md)」選項
* [會出現烘焙模型資訊](../../bakers/bakers.md)對話框，讓你可以設定並執行任何網格貼圖烘焙

![烘焙網格貼圖](3d-scene-resource.resources/3d-scene-resource-01.gif "烘焙網格貼圖"){width="512px"}

## UDIM/UV-tile 的使用

當一個網格資源被連結，且應用程式偵測到 UV 範圍超出 0-1 範圍時，系統會詢問該網格是否應該被視為 UDIM 網格（也稱為 UV 磚塊）。 這個設定可以之後再調整，除非你確定自己用的是 UV-Tiles，否則答案應該是 <b>「否</b>」。

如果 UV-Tile 行為是啟用的，烘焙的行為會不同，會為每個偵測到的 UV-Tile 烘焙貼圖。

## 資源/場景與狀態

應用程式會將你在 3D 視圖中看到的資訊分成兩個獨立檔案。 實際的 3D 模型或網格，是檔案總管中可見的資源。 燈光、攝影機及其他設定的設定稱為「<b>狀態</b>」。 狀態可以儲存在外部 .sbsscn 檔案，之後再載入。 .sbsscn 檔案不是資源，而是只能透過 [3D 視圖場景選單載入的額外設定檔。](../../interface/3d-view/3d-view.md)
