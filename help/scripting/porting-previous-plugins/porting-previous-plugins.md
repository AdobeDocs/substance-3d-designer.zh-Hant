---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/scripting/porting-previous-plugins.html"
breadcrumb-title: ''
description: 學習如何將 Substance Designer 舊版本的外掛移植到目前的 Python API。
helpx_creative_field: ""
helpx_description: Designer > Scripting > Porting previous plugins
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 移植先前的插件
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 0%

---


# 移植先前的插件

因為為了支援 Qt for Python 所做的變更， **之前的外掛將無法運作**。\
特別是，請注意以下幾點：

## 插件載入與卸載

插件現在在應用程式<b>啟動</b>時載入，退出時<b></b>卸載。\
因此， *插件不必* 繼承自「*sdplugins.*」plugin&#39;。

欲了解更多資訊，請參閱 [插件基礎](../../scripting/plugin-basics/plugin-basics.md) 章節。

## 建立使用者介面元素

**&#x200B;插件不需要再定義 &#39;*sdplugins.&#39;PluginDesc*&#39; 了。\
相反地，外掛可以使用<b> 新的 [UI manager]（https://helpx.adobe.com/tw/substance-3d/unlisted/documentation/sddoc/scripting-api-next-172825023.html） 物件</b> 和 <b>Python 的</b> Qt 來建立所需的使用者介面元素。

你可以在 [「建立使用者介面元素](../../scripting/creating-user-interface/creating-user-interface-elements.md) 」區找到小型程式碼範例。

## 取代地點上下文的使用方式

「*SDLocationContext*」類別已 *從 Python API 中移除* 。\
外掛程式可以使用 <b>[UI manager]（https://helpx.adobe.com/tw/substance-3d/unlisted/documentation/sddoc/scripting-api-next-172825023.html） 物件</b> 來存取目前啟用的圖形和選取。

你可以在 [「存取圖表與選擇](../../scripting/accessing-graphs-and-sel/accessing-graphs-and-selections.md) 」區找到一些範例。
