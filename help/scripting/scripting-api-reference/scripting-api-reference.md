---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/scripting/scripting-api-reference.html"
breadcrumb-title: ''
description: 存取完整的 Substance 3D Designer Python 腳本 API 參考，用於外掛開發。
helpx_creative_field: ""
helpx_description: Designer > Scripting > Scripting API reference
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 腳本 API 參考
user-guide-description: ''
user-guide-title: ''
source-git-commit: f320cf6842ff56ac24912ceda264f30c28317c05
workflow-type: tm+mt
source-wordcount: '1251'
ht-degree: 0%

---


# 腳本 API 參考

本頁說明 API 的主要概念。

欲了解更多詳細資訊，請參閱應用程式附帶的文件，該文件可在 <b>Python API 文件</b>說明中取得>。在此文件中，請快速 <b>搜尋</b> 模組名稱（括號內），即可輕鬆找到定義。

## 背景

context *（Context*）物件是 <b>API</b> 的主要入口。 使用者第一次取得時，透過 &#39;*sd*&#39; 模組中的 &#39;<b>*getContext（）*</b>&#39; 方法建立。

此物件允許基本上 <b>擷取應用程式</b> （*SDApplication*）物件。

## 申請（SDApplication）

應用程式（*SDApplication*）是允許 <b>存取主要 API 管理器</b> 的物件，例如：

* <b>管理應用程式所有<b>套件</b>的套件</b>管理器（*SDPackageMgr*）;
* <b></b>模組管理器（*SDModuleMgr*），管理應用程式所有<b>模組</b>;
* <b></b>UI 管理器（*SDUIMgr*）可在應用程式視窗中建立<b>選單與底座</b>。

你可以在應用程式中註冊 <b>回撥</b> ，當特定事件發生時會被呼叫。

## Package Manager （SDPackageMgr）

這個物件管理應用程式的所有 <b>套件</b>。 套件會顯示在「<b>*Explorer*</b>」元件中。

它允許您：

* <b>建立</b> 一個新的套件;
* <b>裝卸</b> 包裹;
* <b>儲存</b> 包裹;
* <b>找</b> 個包裹。

## 套件（SDPackage）

套件（*SDPackage*）是 <b>資源</b> 的集合（*SDResource*）。

套件內容可以透過 &#39;SDPackageMgr *&#39; 物件儲存<b></b>為副<b>檔名為 .sbs</b> 的檔案。*&#x200B;這個物件讓你能 <b>取得 </b>特定的資源。

要建立<b></b>特定資源，請參閱相關的物件靜態方法（例如：「*SDSBSCompGraph.sNew（）*」）。

套件中也包含一個元資料字典（SDMetadataDict）。 你可以在這裡找到更多關於元資料[&#128279;](../../package-metadata/package-metadata.md)的資訊。

## 資源（SDResource）

資源（*SDResource*）是一種可以 <b>被其他資源參考的</b> 物件。

資源有多種 <b>類型</b>：

* 資料夾（*SDResourceFolder*）;
* 圖形（*SDGraph*）;
* 點陣圖（*SDResourceBitmap*）;
* SVG 影像（*SDResourceSVG*）;
* 字型（*SDResourceFont*）;
* 場景（*SDResourceScene*）;
* BSDF測量（*SDResourceBSDFMeaserment*）;
* 光源設定檔（*SDResourceLightProfile*）。

資源可<b>由靜態方法「*sNew（）*」在以下條件下建立</b>：

* 一個包裹;
* 一個資料夾。

一個資源可以擁有多個 <b>屬性</b> （*SDProperty*）。

## UI Manager （SDUIMgr）

UI 管理器允許 <b>在 Substance Designer 主視窗中建立使用者介面元素</b> ，如 <b>選單</b>、 <b>停靠</b> 區，並允許 <b>在使用者介面相關事件發生時註冊回調</b> 。

此外，UI 管理器還能存取<b>目前的活躍圖</b>，並選擇<b></b>該活躍圖。

## 圖形（SDGraph）

圖（*SDGraph*）是一個包含以下內容的物件：

* <b>節點（</b>*SDNode*）;
* <b>圖形物件</b> （*SDGraphObjects*）;
* <b>物業 </b>（*SDProperty*）。

圖有四種不同類型：

* 物質圖（*SDSBSCompGraph*）
* 實體函數圖（*SDSBSFunctionGraph*）
* Substance FXMap 圖（*SDSBSFxMapGraph*）

圖可以有一個或多個 <b>輸出</b> 節點。 輸出節點代表 <b>圖的結果</b> 。

所有可用的圖節點都可以<b>用 &#39;*getNodeDefinitions（）*&#39; 的方法檢索</b>。

可以使用 <b>&#39;*newNode（）*&#39; 的方法建立</b>一個新節點。

可透過 &#39;*newInstanceNode（）*&#39; 的方法從資源（*SDResource*）建立一個新的<b>實例</b>節點。

## Node（SDNode）

節點（*SDNode*）代表對物件執行的 <b>操作</b> 。

它可以由以下方式創造：

* 定義（<b></b>*SDDefinition*）（參見「*SDGraph.newNode（）」）*;
* 一個 <b>資源</b> （*SDResource*）（參見「*SDGraph.newInstanceNode（）」）*。

一個節點可以有多種 <b>屬性</b>。

節點有多種 <b>類型</b> ：

* *<b>SDSBSCompNode</b>*：物質圖&#x200B;*（SDSBSCompGraph*）中的一個節點;
* *<b>SDSBSFunctionNode</b>*：物質函數圖（*SDSBSFunctionGraph*）中的一個節點;
* *<b>SDSBSFxMapNode</b>*：Substance FXMap 圖（*SDSBSFxMapGraph*）中的一個節點;

## 圖物件（SDGraphObjects）

圖物件（*SDGraphObject*）是一種為 <b>圖增加額外資訊</b> 的物件，但在 <b>*圖評估過程中未* 被考慮</b> 。

圖物件有 <b>三種類型</b> ：

* <b>釘圖</b> （*SDGraphObjectPin*）
* <b>留言</b> （*SDGraphObjectComment*）
* <b>框架</b> （*SDGraphObjectFrame*）

關於如何<b>建立</b>這些物件，請參閱靜態方法「*sNew（）」。*

## 物業（SDProperty）

屬性（*SDProperty*）是一種描述<b></b>另一個物件</b>屬性<b>的物件（圖、節點、資源等）。

它屬於特定 <b>類別</b> （*SDPropertyCategory*）：

* <b>輸入</b>：分類物件的輸入屬性，通常<b> 影響當前物件所執行的操作</b> ;
  * 例如：在物質圖中，統一色彩節點的屬性「*顏色*」是輸入屬性;
* <b>輸出</b>：分類物件的輸出屬性。 它用來識別 <b>物件的結果</b> ;
* <b>註解</b>：分類不&#x200B;*影響</b>物件操作的屬性<b>*;
  * 例如：圖的「*標籤*」是一種註解性質，因為它不影響圖的計算。

該委員會包含以下 <b>成員</b>：

* <b>Id</b>：在其類別語境中對財產的識別;
* <b>類型</b>：目前屬性所支援的類型。 有些屬性可支援 *多種* 類型：『*int*』、『*float*』等;
  * 例如：&#39;*sbs：:function:：add*&#39; 節點的輸入屬性可以支援不同類型：&#39;*int&#39;*、&#39;*int2&#39;*、&#39;*int3&#39;*、&#39;*int4&#39;*、&#39;*float&#39;*、float2 *、*&#39;*float3&#39;*、&#39;*float4&#39; 等等;*
* <b>類別</b>：屬性所屬的類別（輸入、輸出、註解）;
* <b>標籤</b>：物業的標籤，僅&#x200B;*用於展示*;
* <b>描述</b>：物業描述;
* <b>DefaultValue</b>：預設值;
* <b>IsConnectable</b>：表示是否能&#x200B;*在此屬性上進行連線*（SDConnection *）;*
* <b>isReadyOnly</b>：表示該屬性是否為唯讀。 若為真，則該數值不可&#x200B;**&#x200B;更改;
* <b>isVariadic</b>：若為真，此性質將以 *物件上的多個* 性質表示;
* <b>isPrimary</b>：表示指定的屬性是否是&#x200B;**&#x200B;控制其他屬性的主要屬性。*注意：* 這是針對物質 *合成* 節點（*SDSBSCompNode*）特有的）。

舉例：

* &#39;*sbs：:compositing:：input*&#39; 節點的性質：

<table data-preserve-html="true"><colgroup><col style="width: 276.0px;"/><col style="width: 129.0px;"/><col style="width: 283.0px;"/></colgroup><tbody><tr><th colspan="3" style="text-align: center;">SBS：:compositing:：input</th></tr><tr><td style="text-align: left;"><strong>輸入</strong></td><td style="text-align: left;"><strong>註解</strong></td><td style="text-align: left;"><strong>輸出</strong></td></tr><tr><td>$outputsize</td><td>標籤</td><td><p>unique_filter_output（可連接）</p></td></tr><tr><td>$format</td><td>描述</td><td><br/></td></tr><tr><td>$pixelsize</td><td>識別碼</td><td><br/></td></tr><tr><td>$pixelratio</td><td>使用者資料</td><td><br/></td></tr><tr><td>$tiling</td><td>團體</td><td><br/></td></tr><tr><td>$randomseed</td><td>可見若</td><td><br/></td></tr><tr><td><p>位圖資源路徑</p></td><td>用途</td><td><br/></td></tr></tbody></table>

* &#39;*sbs：:compositing:：blend*&#39; 節點的特性：

<table data-preserve-html="true"><colgroup><col style="width: 278.0px;"/><col style="width: 129.0px;"/><col style="width: 283.0px;"/></colgroup><tbody><tr><th colspan="3" style="text-align: center;">SBS：:compositing:：blend</th></tr><tr><td style="text-align: left;"><strong>輸入</strong></td><td style="text-align: left;"><strong>註解</strong></td><td style="text-align: left;"><strong>輸出</strong></td></tr><tr><td>$outputsize</td><td><br/></td><td>unique_filter_output（可連接）</td></tr><tr><td>$format</td><td><br/></td><td><br/></td></tr><tr><td>$pixelsize</td><td><br/></td><td><br/></td></tr><tr><td>$pixelratio</td><td><br/></td><td><br/></td></tr><tr><td>$tiling</td><td><br/></td><td><br/></td></tr><tr><td>$randomseed</td><td><br/></td><td><br/></td></tr><tr><td>source.connector（可連接）</td><td><br/></td><td><br/></td></tr><tr><td><p>destination.connector（可連接）</p></td><td><br/></td><td><br/></td></tr><tr><td>opacity.connector（可連接）</td><td><br/></td><td><br/></td></tr><tr><td>Opacitymult</td><td><br/></td><td><br/></td></tr><tr><td colspan="1">混合模式</td><td colspan="1"><br/></td><td colspan="1"><br/></td></tr><tr><td colspan="1">色彩混合</td><td colspan="1"><br/></td><td colspan="1"><br/></td></tr><tr><td colspan="1">遮罩矩形</td><td colspan="1"><br/></td><td colspan="1"><br/></td></tr></tbody></table>

## 類型（SDType）

一個型別（*SDType*）包含某個值 <b>型態</b>的資訊，例如：

* <b>Id</b>：該類型的識別碼;
* <b>修飾符</b>：可以是「*SDTypeModifier」*<b>列舉</b>值之一的型別修飾符：
  * *汽車*;
  * *均勻*：每次運算評估 *一次* 值;
  * *變換*：每次操作（例如：每個像素）會多次評估&#x200B;**&#x200B;該值。

定義了多種類型，例如：

* <b>enums</b> （*SDTypeEnum*）：描述 <b>一種列舉</b> 類型及其所有屬性;
* <b>structures</b> （*SDTypeStruct*）：描述 <b>具有所有屬性的結構</b> 類型;
* <b>array</b> （*SDTypeArray*）：描述一個 <b>陣列</b>。
* 等等。

詳見 Substance Designer 的 *Python API 文件* 。

## Values （SDValue）

值（SDValue *）是一種封裝</b>*&#x200B;基底型別&#x200B;*值的物件<b>。*

例如：

* 一個「<b>*SDValueInt*</b>」物件封裝了一個「*int*」值;
* 一個 &#39;<b>*SDValueFloat4*</b>&#39; 物件封裝了一個 &#39;*float4*&#39; 值;
* 等等。

基礎型別值通常<b>可以用 &#39;<b>get（）</b>&#39; 方法取得</b>，但這會依回傳的 &#39;*SDValue&#39;* 類型&#x200B;*而異*。

## 連線（SDConnection）

連線（*SDConnection*）代表<b>兩個不同<b>節點</b>兩個不同<b>屬性</b>之間的連結</b>。

內容包括：

* <b>目標節點</b>;
* <b>目標節點的目標屬性</b>;

所有 <b>連線操作</b> 皆在節點上執行：

* <b>建立</b> 新連線，請參見 &#39;*SDNode.newPropertyConnection（）*&#39;
* <b>刪除</b> 現有連線，請參見「*SDNode.deletePropertyConnection（）*」
* <b>要取得</b> 屬性的連接，請參見 &#39;*SDNode.getPropertyConnections（）*&#39;

## 模組（SDModule）

模組是 <b>一組定義與型別</b>。

它允許輕鬆檢索所有可建立節點的資訊，以及列舉和結構。

內容包括：

* 一個<b>在模組管理器&#x200B;*中唯一存在的識別碼</b>（* Id *）（SDModuleMgr*）;
* 定義列表<b></b>（*SDDefinition*）;
* 一份類型</b>列表<b>（*SDType*）。

## 定義（SDDefinition）

定義（*SDDefinition*）物件包含基於<b>屬性</b>（如「*SDNode」*&#x200B;等）定義特定物件</b>的<b>資訊。

內容包括：

* <b>Id</b>：定義的識別碼;
* <b>標籤</b>：定義的標籤;
* <b>說明</b>：定義的描述;
* <b>屬性</b>：所有可用屬性 *類別* （*SDPropertyCategory*）的屬性。
