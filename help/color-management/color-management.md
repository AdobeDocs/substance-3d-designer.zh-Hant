---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/color-management.html"
breadcrumb-title: ''
description: 學習 Substance 3D Designer 中的色彩管理，包括色彩空間、設定檔及專色工作流程。
helpx_creative_field: ""
helpx_description: Designer > Color Management
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 色彩管理
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '1678'
ht-degree: 0%

---


# 色彩管理

本頁說明 Substance 3D Designer 中的色彩管理功能與設定。

Substance 3D Designer 可設定為使用 [OpenColorIO](https://opencolorio.org/) （OCIO）或 Adobe Color Engine（ACE）進行色彩管理。 這讓你能在多個應用程式中保持一致&#x200B;**&#x200B;的色彩轉換和影像顯示。

在此模式下，Designer 內部可處理 **線性 RGB** 色彩。 由於 8 位元深度通常不足以表示線性顏色，因此建議圖形中的[&#128279;](../compositing-graphs/substance-compositing-graphs.md)色彩紋理至少使用&#x200B;**&#x200B;**&#x200B;16位元**&#x200B;深度。

>[!WARNING]
>
> 有效的色彩管理工作流程依賴於正確 *校正的* 顯示器，市面上也有第三方解決方案，能利用專業硬體為你的工作環境正確校準螢幕。
> 
> OpenColorIO 使用者應為其顯示器使用相符的 OpenColorIO 色彩空間。\
> Adobe ACE 使用者應確認作業系統中選擇&#x200B;*的 ICC 設定檔與他們的*&#x200B;螢幕相符&#x200B;*。*

## 配置

色彩管理設定可在偏好設定[&#128279;](../interface/preferences-window/preferences-window.md)對話框的[專案](../interface/preferences-window/project-settings/project-settings.md)標籤中設定。你可以設定以下設定：

### 色彩管理模式

|  |  |
| --- | --- |
| <b>色彩管理</b> | 此設定允許你在 Substance 3D Designer 中選擇 Legacy[&#128279;](../color-management/color-management.md)、[OpenColorIO](#opencolorio) 或 [Adobe ACE](#adobe-ace) 模式來進行色彩管理。*預設：傳承* |

## OpenColorIO

### OpenColorIO 設定

使用 OpenColorIO 模式進行色彩管理時，設計者會利用儲存在 <b>設定檔</b> （*\*.config*）中的資訊來執行色彩轉換、識別色彩空間並設定預設值。

Substance 3D Designer 提供以下配置：

* 實質：包含共同色彩空間的簡單配置
* [ACES 1.0.3](https://github.com/hpd/OpenColorIO-Configs/tree/master/aces_1.0.3)：功能完整的 [Academy 色彩編碼系統](https://www.oscars.org/science-technology/sci-tech-projects/aces) （ACES）配置，為色彩管理工作流程的業界標準

你可以在 <b>Designer 安裝檔案的 ocio</b> 資料夾>資源中找到這些設定檔。

|  |  |
| --- | --- |
| <b>OpenColorIO 設定</b> | 這個設定讓你可以選擇 OpenColorIO 設定檔，在整個設計器中使用。 或者，你也可以使用 OCIO 環境變數設定 OpenColorIO 的設定檔。  當設定檔存在時，該設定檔會在 Designer 中被 *鎖定* 。 仍然可以更改預設色彩空間和顯示變換（見下方設定）。  **提醒：** 加入環境變數後，建議關閉 Designer，先 *從作業系統中的使用者會話登出* ，再重新登入。 這確保在啟動 Designer 時，環境變數仍然生效。 你也可以用命令列建立臨時環境變數，並從同&#x200B;*一個*&#x200B;命令列環境啟動 Designer。*預設：實質* |
| **自訂設定檔** | 如果&#x200B;**在 OpenColorIO 設定**&#x200B;中設定&#x200B;**了自訂**&#x200B;選項，你可以在此欄位中選擇&#x200B;*特定的 \*.config 檔&#x200B;*作為設定檔使用。*&#x200B;預設值：由 OpenColorIO 設定檔或 OCIO 環境變數設定* |

### 點陣色彩空間預設值

|  |  |
| --- | --- |
| <b>8 位元影像</b> | 設定 8 位元點陣圖的預設色彩空間。 *預設：由 OpenColorIO 設定檔設定* |
| <b>16 位元影像</b> | 設定 16 位元點陣圖的預設色彩空間。 *預設：由 OpenColorIO 設定檔設定* |
| <b>浮點影像</b> | 設定浮點精度點陣圖的預設色彩空間，例如 *\*.exr *或*\*.hdr* 格式的 *HDR* 影像。*預設：由 OpenColorIO 設定檔設定* |
| <b>使用檔名來偵測色彩空間</b> | 讓設計師自動指派色彩空間，前提是&#x200B;*位圖檔名*&#x200B;的後綴&#x200B;*與目前 OpenColorIO*&#x200B;設定&#x200B;*中包含的色彩空間小寫名稱完全*&#x200B;相同。舉例來說：一個點陣圖資源 *mybitmap\_aces\_acescg.png* 會自動設定為 *ACES - ACEScg* 色彩空間，並會對工作色彩空間套用相應的變換。 *預設：已勾選* |

### 2D 與 3D 視圖顯示預設

|  |  |
| --- | --- |
| <b>2D 與 3D 視圖顯示預設</b> | 設定 2D 視圖與 [3D 視](../interface/3d-view/3d-view.md)圖視窗的預設&#x200B;*顯示*&#x200B;色彩空間[&#128279;](../interface/2d-view/2d-view.md)。*預設值：由 OpenColor IO 設定檔設定* |
| <b>色彩管理縮圖</b> | 讓 Designer 自動將節點 *縮圖* 轉換成 *圖形中的工作* 色彩空間。 *預設：已勾選* |

## Adobe ACE

### 色彩設定

使用 Adobe ACE 色彩管理模式時，Substance 3D 設計師會利用 ICC 設定檔</b>（*\*.icc / \*.icm*）中的<b>資訊來執行色彩轉換並識別色彩空間。

Designer 附帶多款 ICC 檔案。 你可以在 `resources > icc` Designer 安裝檔案的資料夾中找到這些設定檔的檔案。\
你可以&#x200B;*將這些檔案`Adobe/Adobe Substance 3D Designer/icc`放在目前系統使用者的文件資料夾中**，新增你自己的* ICC 設定檔。

|  |  |
| --- | --- |
| <b>工作空間</b> | 此設定允許你選擇工作色彩空間，在 *Substance 3D Designer 中執行色彩操作* 。 *預設值：sRGB IEC61966-2.1* |
| <b>呈現意圖</b> | 這個選項讓你可以控制顏色&#x200B;*在工作色彩空間範圍之外***&#x200B;時，該如何轉換顏色。*預設：相對比色* |

### 點陣色彩空間預設值

|  |  |
| --- | --- |
| <b>8 位元影像</b> | 設定預設 ICC 配置檔用於 8-bit bitmap。 *預設值：* sRGB IEC61966-2.1 ** |
| <b>16 位元影像</b> | 將預設 ICC 設定檔設為使用 16 位元位圖。 **預設值： *sRGB IEC61966-2.1*** |
| <b>浮點影像</b> | 設定預設的 ICC 配置檔用於浮點精度點陣圖，例如 *\*.exr *或*\*.hdr* 格式的 *HDR* 影像。*預設：原始設定（即未套用設定檔）* |
| <b>若有，請使用內嵌的 ICC 設定檔</b> | 讓設計師使用嵌入點陣圖中的 ICC 設定檔，取代上述預設設定。 *預設：已勾選* |

### 2D 與 3D 視圖顯示預設空間

|  |  |
| --- | --- |
| <b>2D 與 3D 視圖顯示預設</b> | 設定 2D 視圖與 [3D 視](../interface/3d-view/3d-view.md)圖視窗的預設&#x200B;*顯示*&#x200B;色彩空間[&#128279;](../interface/2d-view/2d-view.md)。*預設：***&#x200B;主畫面的 ICC 設定檔，從作業系統擷取&#x200B;**&#x200B;** |

### 圖形顯示

|  |  |
| --- | --- |
| <b>色彩管理縮圖</b> | 勾選後&#x200B;*，Designer 會將節點縮圖*&#x200B;轉換&#x200B;*成目前*&#x200B;的工作色彩空間&#x200B;*。**預設：***&#x200B;未勾選&#x200B;**&#x200B;** |

## 舊有模式

使用 <b>舊有</b> 模式時，Designer 中會 *關閉* 色彩管理——

在此模式下，圖表與影像的行為與先前版本完全相同。 這表示只要不動這個設定&#x200B;*，你之前版本的工作流程就完全*&#x200B;不會受影響&#x200B;*。*&#x200B;不過，還是有一些有用的補充：

你可以選擇使用 <b>ACES sRGB</b> *在 3D 視圖中進行*<b>色調映射，以匹配其他軟體的輸出，例如&#x200B;*[虛幻引擎*](https://docs.unrealengine.com/en-US/Engine/Rendering/PostProcessEffects/ColorGrading/index.html)。</b>

你可以在本頁的「輸出[&#128279;](#exporting-outputs)輸出」區塊中描述，為匯出點陣&#x200B;*設定色彩空間*。可用的色彩空間如下：

* sRGB
* 線性
* 原始

在舊有模式下，Designer 使用 <b>sRGB 工作色彩空間，該色彩空間</b>可被大多數顯示器重現。

考慮到「Raw」選項是直接從圖表寫入影像資料&#x200B;**——也就是使用圖形工作色彩空間——這表示 <b>Raw</b> 和 <b>sRGB</b> 選項&#x200B;*輸出的顏色*&#x200B;是一樣的。

預設情況下，包含 *色彩資訊* 的輸出（例如基色、發射）會設定「sRGB」選項，而「原始」選項則設定給儲存 *純資料* 的輸出（例如粗糙度、金屬感、高度、法線）。 如前所述，這些預設實際上會產生相同的顏色，且僅設定用 *來區分輸出的最終用途* 。

<b>線性</b>選項是&#x200B;*唯一*&#x200B;會對&#x200B;*影像進行色彩轉換*&#x200B;的選項，且僅<b>可用於高動態範圍</b>（HDR）影像，這類影像通常在線性色彩空間中使用&#x200B;*浮點精度*（即16F或32F位元深度）。這使得這些影像能在多種色彩空間與製作環境中使用。

>[!NOTE]
>
> 如需更多關於影像匯出的資訊，可以參考 [文件中的「匯出點陣圖](../compositing-graphs/exporting-bitmaps/exporting-bitmaps.md) 」頁面。

## 匯入點陣圖

你可以為匯入並連結的點陣圖指派 <b>色彩空間</b> （OCIO）或 <b>ICC 設定檔</b> （Adobe ACE）。

在匯入或連結點陣圖時，色彩空間或 ICC 設定檔會&#x200B;**&#x200B;預設設定為點陣資源，使用專案設定[&#128279;](../interface/preferences-window/project-settings/project-settings.md)中色彩管理標籤中點陣色彩空間</b>預設</b>區<b>段的選項<b>。

你可以隨時更改點陣圖的色彩空間，這個選項在點陣圖資源的 <b>屬性</b>裡。

>[!NOTE]
>
> **僅限 OpenColorIO**
> 
> 特別是，**檔案名稱**&#x200B;可用來自動&#x200B;*設定適當的色彩空間*。請注意，檔名中的色彩空間名稱必須 *與 OpenColorIO 設定檔中的名稱* 相符（例如 *myImage\_utility - 線性 -srgb.png* 會設定為 *Utility - Linear - sRGB* 色彩空間）。

![位圖色彩空間設定](../assets/2019-3-0-bitmap-clr-space.png "位元色彩空間設定")

## 出口產品

使用<b>匯出輸出</b>對話框時，可以為每個&#x200B;*輸出指派<b>色彩空間</b>（OCIO）或附加 <b>ICC 設定檔</b>（Adobe ACE）。*\
Designer 會在 *儲存影像檔案前，先將圖片轉換* 成指定的色彩空間。

![匯出輸出對話框](../assets/2019-3-0-clr-mgt-export-outputs.png "匯出輸出對話框"){width="512px"}

你也可以為從 2D View[&#128279;](../interface/2d-view/2d-view.md) 儲存的*影像*&#x200B;指派色彩空間（OCIO）或附加 ICC 設定檔（Adobe ACE）。

![2D 檢視匯出選項](../assets/2019-3-0-clr-mgt-save-image.png "2D 檢視匯出選項")

## 2D 與 3D 視圖

### 顯示工具列

你可以 *隨時透過顯示工具列的下拉選單切換* 色彩管理並更改 *視圖的顯示變換* 。

![2D 檢視](../assets/2019-3-0-clr-mgt-display-toolbar.png "中的色彩空間設定 2D 檢視中的色彩空間設定"){width="512px"}

### 函式庫 HDRI 環境

Designer 附帶的 HDRI 環境屬於 <b>線性 sRGB</b> 色彩空間。\
當使用 OpenColorIO 配置，且場景線性色彩空間 *不是* 線性 sRGB（如 [ACES](https://acescentral.com/t/getting-started-with-aces/1372) 配置）時，環境會顯示 *錯誤的顏色*。

在這種情況下，圖書館 HDRI 環境的色彩空間應該在 3D 檢視面板<b>的環境</b>選單中手動&#x200B;*設定*。

![3D 檢視環境](../assets/2019-3-0-clr-mgt-hdri-env.png "的色彩空間設定 3D 檢視環境的色彩空間設定"){width="512px"}

## 色彩轉換節點

函 [式庫](../interface/the-library/the-library.md) 包含以下節點，用於與 ACEScg 色彩空間的 <b>轉換</b> ：

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

[物質圖](../compositing-graphs/substance-compositing-graphs.md)

* ACEScg 轉為線性 sRGB
* 線性 sRGB 轉 ACEScg
* ACEScg 轉為 sRGB
* sRGB 轉 ACEScg

</td>
<td style="border: 0;" valign="top">

[實體函數圖](../function-graphs/function-graphs.md)

* ACEScg 轉為線性 sRGB
* 線性 sRGB 轉 ACEScg

</td>
</tr>
</table>

這些工具在處理未使用&#x200B;*色彩管理或 [Substance 3D 素材](https://substance3d.adobe.com/assets)庫材質的*&#x200B;圖表時非常有用。

![函式庫](../assets/2019-3-0-clr-mgt-nodes.png "中的色彩轉換節點函式庫中的色彩轉換節點"){width="512px"}

## 已知限制

Substance 3D Designer 目前的色彩管理實作有以下限制：

* 目前 *Python API[&#128279;](../scripting/scripting.md) 中並未*&#x200B;公開色彩管理功能;
* [OpenColorIO](https://opencolorio.org/) *外觀**不*&#x200B;被支援。
