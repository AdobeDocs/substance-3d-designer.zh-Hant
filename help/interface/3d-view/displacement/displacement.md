---
helpx_url: ""
breadcrumb-title: ""
description: 使用位移彈出視窗快速調整 3D 場景中套用在網格上的位移與細分。
helpx_creative_field: ""
helpx_description: ""
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D 視圖 - 位移彈出視窗
user-guide-description: ""
user-guide-title: ""
source-git-commit: 10be7678f386c925d4bff6d59e2b85ffc04becd8
workflow-type: tm+mt
source-wordcount: '499'
ht-degree: 0%
---

# 位移彈出視窗

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="vertical-align: top; border: 0">
        <td style="border: 0">
            <p>3D 檢視工具列中的位移彈出視窗提供直接控制網格的位移與細分。</p>
            <p>有三個參數：<ul>
                <li>身高比例</li>
                <li>高度</li>
                <li>無鑲嵌</li></ul>
        </td>
        <td style="width: 60%; margin-left: 32px; border: 0">
            <img src="./displacement.resources/3d-view-displacement-popup-mograph.gif" alt="3D 視圖中的位移彈出視窗" />
        </td>
    </tr>
</table>

## 身高比例

網格頂點沿法線的最大位移距離，以場景單位計算。<br>
這是高度圖中值為 1.0 時的行駛距離。

當 Substance 圖連接到材料，且該圖包含 [一個輸出節點](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) 時高度比例尺<code></code>然後彈出視窗中的高度比例參數會被&#x200B;*該材質禁用*&#x200B;因為目前是由圖驅動的。

>[!TIP]
> 
>使用 [「高度到標準世界單位](../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/height-normal-world-units/height-to-normal-world-units.md) 」節點，並讓其「高度深度」參數與「高度比例」值相符
>以確保使用位移時的正確遮蔽。

## 高度

高度圖中的灰階值，作為 *位移高度的中點* 。
也就是說，作為 0.0 高程的閾值。

低於該閾值的數值會導致頂點向後移動，而高於該閾值的數值則是頂點被向前移位移。

## 無鑲嵌

鑲嵌是指在網格的各個面上加一個頂點，然後再連接起來，將各個網格面細分所有頂點都指向其中心的新頂點，使得該 1 面變成 **6**。

參數定義了面應遞迴細分的次數。

*鑲嵌參數的範圍*&#x200B;會依&#x200B;*目前使用的渲染器*&#x200B;而異：可以套用每個網格或每個材質。

### 每個網格

使用 [光柵化器](../3d-renderers/3d-renderers.md#rasterizer) 或 [GPU Pathtracer](../3d-renderers/3d-renderers.md#gpu-pathtracer) 渲染器時，場景中的每個網格物件都有 *獨立的*&#x200B;細分值。

細分是情境性化的：它優化的方式是只有具有 *非均勻高度值* 的表面，或&#x200B;*非平面高度圖*&#x200B;會被細分，無論參數值為何。

>[!TIP]
>
>鑲嵌技術包含一個無論實際是否進行鑲嵌都會持續的準備步驟。 （也就是說） `Tessellation factor = 1`
>對於高多邊形網格，此步驟可能耗時且在使用位移時顯著影響效能。
>
>如果不需要鑲嵌，你可以在場景瀏覽器[&#128279;](../scene-browser/scene-browser.md#scene-tree)中物件的屬性`Mesh`中設定 **Refine level** 參數為 ，`0`完全停用此技術。

### 依材質分類

使用 [OpenGL](../3d-renderers/3d-renderers.md#opengl) 渲染器時，場景中的每個材質都有 *獨立* 的細分值，該值套用 *到所有使用該材質*&#x200B;的面。

細分並非情境性：曲面會被細分指定次數，無論其當前情況如何高度值或材質。

## 拼圖的視覺化

你可以透過檢查 **網格的線框** 來視覺化鑲嵌的結果。<br>
以下說明顯示每個渲染器線框的步驟：

### 光柵化器/GPU 路徑追蹤器

使用該 <img src="../3d-view.resources/3d-view-scene-toolbar-render-settings.png" width="22" /> **渲染器設定**&#x200B;然後在屬性底座裡，進入&#x200B;**診斷模式**>渲染設定，選擇線框圖&#x200B;**（世界空間）** 選項。

### OpenGL

使用該 <img src="../3d-view.resources/3d-view-scene-toolbar-wireframe.png" width="22" /> **線框**&#x200B;按鈕。
