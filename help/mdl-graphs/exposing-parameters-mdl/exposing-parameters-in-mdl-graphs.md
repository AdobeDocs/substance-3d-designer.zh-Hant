---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/mdl-graphs/exposing-parameters-in-mdl-graphs.html"
breadcrumb-title: ''
description: 學習如何在 MDL 圖中暴露參數，使材質可自訂且可重複使用於 Substance 3D Designer 中。
helpx_creative_field: ""
helpx_description: Designer > MDL graphs > Exposing parameters in MDL graphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: MDL 圖中參數的暴露
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '833'
ht-degree: 0%

---


# MDL 圖中參數的暴露

本頁說明如何在 MDL 圖中暴露參數，使其能與圖&#x200B;*中其他節點*&#x200B;或外部來源&#x200B;*提供的*&#x200B;值與紋理連結。

![節點輸入](exposing-parameters-in-mdl-graphs.resources/mdl-node-inputs-hl.png "的暴露狀態 節點輸入的暴露狀態")

*節點輸入的暴露狀態*

## 暴露節點輸入

在大多數情況下， *節點屬性的輸入連接器* 可以被暴露，因此其 *值由圖中其他節點* 設定。 這是 *MDL 圖形工作流程中至關重要* 的一環，應該被充分理解。

當節點在圖視圖中</b>被選取<b>時，其屬性會顯示在<b>屬性</b>面板中。大多數物業標示後，標籤右側有一組按鈕：

* **![](exposing-parameters-in-mdl-graphs.resources/mdl-expose-new-node.png)將值複製到新節點並連結到這個參數**：*建立一個輸入連接器*，並連接到&#x200B;*輸出該屬性目前值的新節點*
* **![](exposing-parameters-in-mdl-graphs.resources/mdl-expose-new-input.png)為此參數**&#x200B;建立輸入腳位：為此屬性建立&#x200B;*輸入連接器*
* **![](exposing-parameters-in-mdl-graphs.resources/mdl-expose-reset.png)將此參數重設為預設值**：當該屬性的輸入連接器沒有連接值時，則將其值重置為預設值

![](exposing-parameters-in-mdl-graphs.resources/mdl-expose-input.gif)

*操作節點輸入*

點擊前兩個按鈕中的任一，節點 *會新增一個輸入連接器* 。 節點的屬性會根據 *此連接器的連線狀態* 做出反應：

* **未連接**：參數仍可在 **屬性** 面板中調整，且該面板的值輸入會被 *套用*
* **連接**：該參數在屬性&#x200B;**面板中不再可**&#x200B;調整，面板中的輸入值被&#x200B;*輸入*&#x200B;連接器接收&#x200B;*的值取代*，屬性無法重置為預設值

輸入連接器可&#x200B;*透過再次&#x200B;**點擊「為此參數**&#x200B;建立輸入腳位」按鈕來移除*。此時，屬性值會回到屬性&#x200B;**面板中**&#x200B;設定的值。

![暴露節點參數](exposing-parameters-in-mdl-graphs.resources/mdl-exposed-float-hl.png "暴露節點參數")

*外露節點參數*

## 圖形輸入的暴露

在 MDL 圖中，將參數暴露於圖層級——即呈現為 MDL 材料輸入參數——是透過暴露輸出該值的節點來完成的。

可被暴露的節點在其上下文選單中有 <b>「</b> 曝光」選項。 在大多數情況下，這些節點會產生像浮點、顏色或紋理座標等值或資料。

![節點上下文選單中的「曝光」選項「節點上下文選單](exposing-parameters-in-mdl-graphs.resources/mdl-expose-float-menu-hl.png "中的曝光」選項")

*節點情境選單中的「暴露」選項*

暴露的參數是直接在 *暴露節點*&#x200B;中設定，而非圖的屬性中。 暴露參數的性質如下：

* <b>識別碼</b>：目前圖中此輸入參數的唯一名稱
* <b>預設值</b>：此參數的預設值。 它也可以用作 *預覽* 輸入參數在 Designer 中會呈現的樣貌。 <b>顯示名稱</b>、<b>群組中</b><b>及範圍</b>屬性皆用於最精確的預覽
* <b>射程</b>：
  * *軟範圍*：設定用於顯示此參數的小工具的預設範圍——例如滑桿。 此特性僅用於介面用途，超出軟範圍的數值可手動輸入
  * *硬範圍*：設定此參數可接受值的範圍。 低於範圍的數值會被夾到最小值，而高於範圍的數值則會被夾到最大值。 參數的預設值與軟範圍值會 *自動調整* 以符合此範圍。
* <b>描述</b>：參數的描述
* <b>在群組</b>中：該輸入參數所屬的參數群組。 若非空白，該參數會在 Designer 中以該群組命名的可摺疊區段顯示
* <b>顯示名稱</b>：介面中顯示的參數名稱
* <b>隱藏</b>：當參數設為 True 時，該參數在圖輸入和 MDL 材料屬性中看不到
* <b>Gamma 類型</b>：從與此參數相關的紋理取樣值時應使用的伽瑪
* <b>預設</b>可見：在某些參數可能隱藏的情況下，設定此參數在 MDL 整合中可見
* <b>類型修飾符</b>：設定值是均勻還是變化。 當設定為自動時，參數會繼承此特性（例如，對於 Float 值：連接 Float 時均勻，連接貼圖時變化）
* <b>取樣器使用</b>：參數使用頻率的識別碼， *用於連接多個輸出同時連接到 MDL 材質時的貼圖*。 例如，當將 Substance 圖[&#128279;](../../compositing-graphs/substance-compositing-graphs.md)與 3D 視圖中的 MDL 材質連接時，紋理會根據其使用識別碼匹配，連接到正確的輸入。

>[!WARNING]
>
> 雖然圖輸入是在節點層級設定&#x200B;*，但其排序則在圖屬性[&#128279;](../../mdl-graphs/creating-an-mdl-graph/creating-an-mdl-graph.md)**的圖輸入**&#x200B;區段管理**。*

![將節點暴露於圖輸入](exposing-parameters-in-mdl-graphs.resources/mdl-expose-parameter.gif "將節點暴露於圖輸入")

*將節點暴露於圖輸入中*
