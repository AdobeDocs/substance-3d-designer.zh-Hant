---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/blend/blending-modes-description.html"
breadcrumb-title: ''
description: 了解 Substance 3D Designer 中可用的混合模式，用於結合材質與不同合成效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Blend > Blending modes
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 混合模式
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '555'
ht-degree: 0%

---


# 混合模式

[混合](../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md)節點提供以下混合模式：

## 複製

*複製*&#x200B;混合模式會把前景放在背景上。

![混合模式：複製](blending-modes-description.resources/blending-modes-description-01.png "混合模式：複製"){zoomable="yes"}

對於彩色影像，透明度預設會考慮 alpha 通道。

這可以透過使用「Alpha blending」參數來改變。

![混合模式：複製（2）](blending-modes-description.resources/blending-modes-description-02.png "混合模式：複製（2）"){zoomable="yes"}

## 加法（線性閃避）

*新增*&#x200B;混合模式會將前景輸入值加入背景中對應的每個像素。

![混合模式：加（線性閃避）](blending-modes-description.resources/blending-modes-description-03.png "混合模式：加（線性閃避）"){zoomable="yes"}

## 減法

*Substract* 混合模式會從背景中每個對應像素中扣除前景輸入值。

若減法結果小於0，則該值上限為0，結果為純黑色。

![混合模式：減法](blending-modes-description.resources/blending-modes-description-04.png "混合模式：減法"){zoomable="yes"}

## 乘法

*乘法*&#x200B;混合模式會將背景輸入值乘以前景中對應的每個像素。

由於每個像素的值介於 0 與 1 之間，結果總是相等或更低（較暗）。

![混合模式：乘法](blending-modes-description.resources/blending-modes-description-05.png "混合模式：乘法"){zoomable="yes"}

## 新增字幕

*新增字幕*&#x200B;混合模式的運作方式如下：

* 前景像素值大於 0.5 的像素會加入各自的背景像素。
* 前景像素值低於 0.5 的像素會從其對應的背景像素中扣除。

![混合模式：新增字幕](blending-modes-description.resources/blending-modes-description-06.png "混合模式：新增字幕"){zoomable="yes"}

## 麥克斯（Lighten）

*最大*&#x200B;混合模式會選擇背景與前景之間的較高值。

![混合模式：最大（變亮）](blending-modes-description.resources/blending-modes-description-07.png "混合模式：最大（變淺）"){zoomable="yes"}

## 敏（暗黑）

*最小*&#x200B;混合模式會選擇背景與前景之間的較低值。

![混合模式：最小（加深）](blending-modes-description.resources/blending-modes-description-08.png "混合模式：最小化（加深）"){zoomable="yes"}

## 切換

*Switch* 的混合模式與複製模式相似，但有一個&#x200B;*關鍵*&#x200B;差異：

* 「不透明度」設為 0：連接到「前景」輸入 *的節點串流不會被計算*。
* 「不透明度」設為 1：連接到「背景」輸入 *的節點串流不會被計算*。

因此，此模式可用來提升圖表的效能。

[Switch](../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blending/switch/switch.md) 和 [Switch 灰階](../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blending/switch/switch.md)節點會設定成在這些特定配置中使用混合節點。

![混合模式：切換](blending-modes-description.resources/blending-modes-description-01.png "混合模式：切換"){zoomable="yes"}

## 分界

*除法*&#x200B;混合模式會將背景輸入像素的值除以前景中對應的每個像素。

![混合模式：除](blending-modes-description.resources/blending-modes-description-09.png "法 混合模式：分割"){zoomable="yes"}

## 疊加層

*疊加*&#x200B;混合模式結合了乘法與螢幕混合模式：

* 
  * 若下層像素值低於 0.5，則 *會套用乘法* 混合
  * 若下層像素值高於 0.5，則 *會套用 Screen* 類型的混合

![混合模式：疊加](blending-modes-description.resources/blending-modes-description-10.png "混合模式：疊加"){zoomable="yes"}

## 螢幕

在螢幕混合模式下，兩個輸入的像素值會被反轉、乘以，然後再反轉。

結果與乘法相反，且相較於原始效果總是相等或更高（更亮）。

![混合模式：螢幕](blending-modes-description.resources/blending-modes-description-11.png "混合模式：螢幕"){zoomable="yes"}

## 柔和的光線

柔光混合模式會根據前景色的亮度，產生細微的亮或暗效果。

亮度超過 50% 的混合色會讓背景像素變亮，而亮度低於 50% 的顏色會讓背景像素變暗。

![混合模式：柔光](blending-modes-description.resources/blending-modes-description-12.png "混合模式：柔光"){zoomable="yes"}
