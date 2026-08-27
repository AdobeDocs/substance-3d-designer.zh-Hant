---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/mdl-graphs/substance-compositing-graphs-and-mdl-materials.html"
breadcrumb-title: ''
description: 學習 Substance 合成圖與 MDL 材質如何在 Substance 3D Designer 中協同運作以進行材質製作。
helpx_creative_field: ""
helpx_description: Designer > MDL graphs > Substance graphs and MDL materials
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 物質圖表與 MDL 材料
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '713'
ht-degree: 0%

---


# 物質圖表與 MDL 材料

本頁說明 Substance 圖[&#128279;](../../compositing-graphs/substance-compositing-graphs.md)與 MDL 圖之間的協同效應，以及如何將 Substance 圖[輸出](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)的紋理連接到 MDL 圖的輸入。

## 概觀

Substance 圖的輸出可 *透過兩種方式傳遞給 MDL 材料的公開參數* ，詳見本頁說明。

如果目前在 3D 視圖中套用的 MDL 材質有暴露參數，而該類型會&#x200B;*[變化](../../mdl-graphs/main-mdl-graph-concepts/main-mdl-graph-concepts.md)*——這個類型可以透過暴露參數屬性中的[類型修改器</b>選項設定<b>，這些參數可以連接到&#x200B;*貼圖*：](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)

* <b></b>顏色參數可以連接到 RGBA 材質
* 灰 <b>階材質的浮點</b> 參數

在這些情況下，原始均勻值會被提供變化值的貼圖取樣器取代。 這些取樣器在公開參數中定義了 <b>使用</b> 屬性，該使用法允許 Designer 將 Substance 圖形輸出的紋理與 MDL 材質中相應的參數連結，並匹配 *使用*&#x200B;情況。

## 3D 視圖中的實體圖

當使用 <b>3D 檢視</b>中的 View 輸出選項來處理 Substance 圖表，或從 Explorer</b> 面板拖曳 Substance 圖表<b>至 <b>3D 檢視時</b>，輸出會連接到目前 3D 檢視中顯示的 MDL 材質中匹配使用的&#x200B;*參數*。

Substance 圖中的個別紋理可透過在 Substance 圖節點上按 RMB 並拖曳至 3D 視圖，連接任何支援紋理取樣的 MDL 材質參數，無論識別碼為何。 會顯示可用的取樣器使用清單，你可以選擇所選材質的目標使用方式。

![暴露的 MDL 圖形輸入](../../assets/mdl-graph-inputs-samplers.png "暴露的 MDL 圖形輸入")

*Substance 圖輸出的貼圖會與 MDL 圖在 3D View 中暴露的參數相連*

## MDL 圖中的實體圖

實體圖實例可直接從 Explorer</b> 面板拖<b>入 MDL 圖中。來自Substance 3D檔案</b>（SBS）和<b>Substance 3D資產檔案</b>（SBSAR）的Substance圖<b>可用於MDL圖中。

+++Substance 3D 檔案（SBS）中的 Substance 圖表
![來自 MDL 圖](../../assets/mdl-sbs-instance-hl.png "中 SBS 檔案的實質圖 來自 MDL 圖中 SBS 檔案中的實質圖")



*[&#128279;](../../compositing-graphs/substance-compositing-graphs.md)MDL [圖中 Substance 3D 檔案](../../getting-started/overview/overview.md)（SBS）中的 Substance 圖實例*

+++

+++Substance 3D 資產（SBSAR）中的 Substance 圖表
![來自 MDL 圖](../../assets/mdl-sbsar-instance-hl.png "中 SBSAR 檔案的實質圖 來自 MDL 圖中 SBSAR 檔案中的實質圖")



*[&#128279;](../../compositing-graphs/substance-compositing-graphs.md)來自 Substance 3D 資產[&#128279;](../../getting-started/overview/overview.md)（SBSAR）在 MDL 圖中的實例*

+++

當建立 Substance 圖實例時，它會以&#x200B;**&#x200B;節點的形式呈現，具有以下特徵：

* 每個圖的輸出都配有 *打* 字輸出連接器。 輸出資料的類型如下：
  * RGBA 位圖：顏色（變化）
  * 灰階位圖：浮點（變化）
  * 數值：匹配值類型（可變）
* 輸入 ** 類型為 UV 座標，用以指定 UV 座標，並用於映射 Substance 圖所輸出的紋理。若未連通，預設值為 UV 空間中 X 與 Y 的經典 0-1 線性梯度
* 節點在 Substance 圖標籤之後標 *示* ——若未定義標籤則標示識別碼——並以縮圖形式輸出其第一個位圖

節點屬性允許你修改 *Substance 圖的所有動態屬性* ：

* 輸出大小
* 隨機種子
* 輸入參數
* …

節點屬性也允許你設定 MDL 材質中貼圖&#x200B;**&#x200B;的具體參數：

* 鋪磚
* 使用物理尺寸
* 標準格式
* 切空間

Substance 圖實例節點的輸出可連接至 MDL 圖中任何符合型態的節點輸入。

請注意，變更 SBS 基礎參數區塊中的任何參數<b>，需重新計算一個或多個 Substance 圖的輸出，這使用 <b>Substance 引擎</b>，且在 MDL 圖計算基礎上會產生&#x200B;*效能開銷*。</b>在 *修改實例化於 3D 視圖中 MDL 圖中的 Substance 圖* 時，預期會有效能影響。

>[!WARNING]
>
> 在 MDL 圖中使用 Substance 圖時，匯出 MDL 圖是將 Substance 圖的輸出烘焙成點陣圖，這些點陣圖會匯出成與匯出後的 MDL 檔案捆綁的貼圖。 這表示匯出後的 MDL 檔案中，Substance 圖的參數化特性會 *遺失* 。
