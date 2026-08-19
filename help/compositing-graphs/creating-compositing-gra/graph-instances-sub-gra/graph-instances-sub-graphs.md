---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/creating-a-substance-compositing-graph/graph-instances-sub-graphs.html"
breadcrumb-title: ''
description: 利用圖實例與子圖來建立可重複使用的圖元件與模組化材質工作流程。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Creating a Substance compositing graph > Graph instances and subgraphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 圖實例與子圖
user-guide-description: ''
user-guide-title: ''
source-git-commit: b0053a42604f68604350a6bb3a2148970536c3c7
workflow-type: tm+mt
source-wordcount: '615'
ht-degree: 0%

---


# 圖實例與子圖

![](../../../assets/sub-graph.png)

圖實例是指向 <b>另一個圖</b>的節點。 由宿主圖中實例節點所參考的圖，可以稱為 <b>宿主圖的子圖</b> 。

使用實例可以讓一個圖在一個或多個圖中多次重複使用，甚至跨越不同套件。

## 為什麼我應該使用圖形實例？

<b>將圖表拆分成多個子圖能</b>讓你更有效率<b>地工作&#x200B;**。</b>

當你在 Designer 裡複製一串節點時，你大概可以把那條鏈拆成子圖，這樣比較容易重複使用和更新。

>[!NOTE]
>
> 本文件的範例物質圖章節中，有一個示範自訂濾波器子&#x200B;**&#x200B;圖簡單設定的專案檔案可供參考[。](../../../compositing-graphs/sample-compositing-graphs/sample-substance-compositing-graphs.md)

### 你要怎麼建立一個圖實例？

從 Explorer 拖曳一個圖 A 到另一個圖 B，建立 <b>一個參考圖 A 的實例節點</b> 。

節點可透過選擇節點並在情境選單中使用「從選取中建立圖形」快速分割成新圖。 接著會提示你設定新圖的識別碼，該識別碼應該是唯一的。

請注意，如果所選節點連接圖中其他節點，你也應該在新圖中建立 [輸入](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md)和[輸出](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)節點，將這些連結帶到子圖。

此外，將原始節點替換為引用新圖的實例節點，則應在事後手動完成。

最後，你應該決定在將專案發佈到可共享的 SBSAR 檔案時，是否應該讓子圖暴露給使用者。 詳見圖屬性[&#128279;](../../../compositing-graphs/graph-parameters/graph-parameters.md)中的「SBSAR 暴露」參數。

### 關於繼承

使用子圖的另一個好處是，每個子圖實例都能 <b>適應其所處的情境</b> 。 換句話說，同一圖的兩個實例可能有不同的輸出解析度、位元深度和平鋪模式。

這是 <b>圖中工作的重要概念</b> ，我們強烈建議你在準備進一步研究實例時，進一步了解 [實質圖](../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) 中的繼承。

請注意，雖然圖實例與子圖概念同樣適用於 Substance 函數圖，但該頁所討論的繼承僅適用於 Substance 圖。

### 我可以把自己的圖實例加入節點函式庫嗎？

<b>是的，這是可行 </b>的，但需要特定的設定。 更多資訊請參閱[本文件中的「管理自訂內容與篩選」](https://helpx.adobe.com/tw/substance-3d/unlisted/documentation/sddoc/creating-library-filters-for-projects-170459772.html)頁面。

### 你能檢查圖實例的來源圖嗎？

![（勾選）](../../../assets/check.svg)是的，*且僅限*&#x200B;於從 Substance 3D 檔案（SBS）**載入**&#x200B;的圖形實例。這些實例節點帶有 *深紅色* 標籤。\
右鍵點擊該節點以開啟其情境選單，並選擇 **「開啟參考** 」選項。

>[!NOTE]
>
> 在檢查來源圖時，只要&#x200B;**在偏好設定[&#128279;](../../../interface/preferences-window/preferences-window.md)的圖**&#x200B;區段勾選&#x200B;***上下文編輯**&#x200B;選項，就可以使用實例圖*&#x200B;的輸入資料。

![（減）](../../../assets/forbidden.svg)**&#x200B;無法檢查從 &#x200B;** Substance 3D 資產（SBSAR）**&#x200B;實例載入的圖表，因為這些圖表已經被編譯完成。你只能在 &#x200B;** Explorer** 面板載入資產，檢查顯示的圖表列表及其參數。 這些實例節點有 *綠色* 標籤。\
右鍵點擊該節點以開啟其上下文選單，並選擇 **載入套件** 選項。

>[!NOTE]
>
> **原子節點**
> 
> *原子*&#x200B;節點是直接透過 Substance 引擎中的程式碼實作的，並非&#x200B;**&#x200B;圖的實例，因此稱為 atomic：它們是 *Substance 圖[&#128279;](../../../compositing-graphs/substance-compositing-graphs.md)中所有*&#x200B;其他節點最小&#x200B;*的建構單元*。
