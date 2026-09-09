---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/manage-parameters/parameter-presets.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Designer 中建立並使用參數預設來儲存並套用參數設定。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Exposing a parameter > Parameter presets
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 參數預設
user-guide-description: ''
user-guide-title: ''
source-git-commit: 69056338cc47db71e0754c72495d33a2a3c36dea
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 0%

---


# 參數預設

參數預設讓使用者能夠儲存並轉移大量預設參數的值。它們在許多情境下都能發揮作用，尤其當存在大量參數且可能性範圍廣泛時，效果尤為顯著。

儲存和載入預設有兩種方式，兩者的使用情境不同，詳述如下。

![載入/儲存預設下拉選單](parameter-presets.resources/preset-menu.gif "載入/儲存預設下拉選單"){width="512px"}

## 外部預設

外部預設包含磁碟上的外部檔案，一個 \*。SBSPRS 檔案。 它們可以在不同的圖和節點間轉移，但只能在應用程式內部進行。 它們的主要目的就是：轉移過多無法逐一複製的數值。

外部預設可用於所有圖實例的特定參數[、大多數原子節點](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/atomic-nodes.md)的特定[&#128279;](../../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)參數（[例外為無法暴露](../../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)的參數），以及實體圖[參數](../../graph-parameters/graph-parameters.md)參數中暴露的輸入參數。

它們只需儲存並透過這個選單載入即可。 已儲存的 SBSPRS 檔案可載入於任何其他節點或圖形上。

>[!NOTE]
>
> 即使是部分匹配也能運作：儲存在 SBSPRS 中且載入節點上不存在的參數，將被直接忽略。 這表示你可以在大多數 [相似的節點間轉移屬性，例如彩色與灰階版本的 Tile Sampler](../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md)！ 所有共用參數都會載入。 匹配是根據識別碼和類型進行的。

![嵌入預設](parameter-presets.resources/preset-embed.gif "編輯 嵌入預設編輯"){width="512px"}

## 嵌入式預設

嵌入式預設的運作方式與外部預設不同。 它們的主要優點是它們包含在 SBS 或 SBSAR 檔案中，因此可以輕鬆地在 Substance Painter、Maya 和 3DS Max（目前 Substance 3D Sampler、UE4 和 Unity 中無法使用）中傳輸和載入。 使用者也不必去動 SBSPRS 檔案。

它們有不同的用途：無法在節點和圖形之間轉移（你必須用外部預設）。 它們也只能在圖屬性的輸入參數上建立，且僅限於預覽模式中。

工作流程如下：

1. 切換到 <b>預覽模式</b> 以控制 <b>輸入參數</b>
1. 將數值設為期望結果
1. 點擊 <b>預設下拉選單旁的 +</b> 鍵來建立新的嵌入預設，該預設會立即被建立並儲存

嵌入的預設在之後無法修改，但可以重新命名。 修改或移除它們只需點擊下拉選單旁的齒輪圖示和 + 圖示即可。 按預設旁邊的負號可以移除它。

啟用預設不需要做更多：一旦以 SBSAR 發佈，匯入後你的預設就會在 Substance Painter 中使用。

>[!IMPORTANT]
>
> <b>使用[上下文編輯](../../../interface/preferences-window/preferences-window.md)時，預設</b>標籤是被停用的。
