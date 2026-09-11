---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/atomic-function-nodes/function-nodes.html"
breadcrumb-title: ''
description: 存取 Substance 3D Designer 功能圖中的功能節點，以呼叫並執行自訂功能圖。
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Function
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 功能
user-guide-description: ''
user-guide-title: ''
source-git-commit: f28a2ba2531cfc4456744ff151432ed8308275ec
workflow-type: tm+mt
source-wordcount: '451'
ht-degree: 1%

---


# 功能節點

函數節點會根據它們所代表的數學函數轉換輸入值。

雖然其輸入連接器通常不具型別，但並非支援所有值型別。

## 節點列表

+++砰
![Pow 節點圖示](function-nodes.resources/Pow_Node.jpg "Pow 節點圖示")



將第一個輸入的次方回傳為第二個輸入的冪次方： <b>X^Y</b>。

+++

+++2Pow
![2Pow 節點圖示](function-nodes.resources/2Pow_Node.jpg "2Pow 節點圖示")



回傳 2 的輸入值的冪次方： <b>2^X</b>。

+++

+++平方根
![平方根節點圖示](function-nodes.resources/SquareRoot_Node.jpg "平方根節點圖示")



回傳其輸入值的平方根： <b>√X</b>。

+++

+++指數
![指數節點圖示](function-nodes.resources/Exponential_Node.jpg "指數節點圖示")



回傳其輸入值的指數值： <b>e^X</b>

<b>e</b> 大約等於 2.7182818。

+++

+++對數
![對數節點圖示](function-nodes.resources/Logarithm_Node.jpg "對數節點圖示")



回傳其輸入值的自然對數：<b>ln（X）。</b>

+++

+++對數底數為2
![對數進位 2 節點圖示](function-nodes.resources/LogarithmBase2_Node.jpg "對數進位 節點 2 進位圖示")



回傳輸入值的底數 2 對數：<b>log2（X）。</b>

+++

+++絕對
![絕對節點圖示](function-nodes.resources/Absolute_Node.jpg "絕對節點圖示")



回傳其輸入的絕對值：<b>abs（X）。</b>

+++

+++凱爾
![Ceil 節點圖示](function-nodes.resources/Ceil_Node.jpg "Ceil 節點 圖示")



將輸入值向上取整。 它回傳最小的整數值，且不小於 X：<b>ceil（X）。</b>

+++

+++下限
![地板節點圖示](function-nodes.resources/Floor_Node.jpg "地板節點圖示")



將輸入值向下取整。 它回傳最大不大於 X：<b>floor（X）。</b>

+++

+++線性插值
![線性插值節點圖示線性插值節點圖示](function-nodes.resources/LinearInterpolation_Node.jpg "")



回傳兩個值之間線性插值值，該值為浮動值： <b>（1 - X）\*A + X\*B</b>。

+++

+++最低限度
![最小節點圖示 最小節點圖示](function-nodes.resources/Minimum_Node.jpg "")



回傳兩個輸入值中最低的值：<b>min（A， B）。</b>

+++

+++極限
![最大節點圖示 最大節點圖示](function-nodes.resources/Maximum_Node.jpg "")



回傳兩個輸入值中最高的：<b>max（A， B）。</b>

+++

+++餘弦
![餘弦節點圖示](function-nodes.resources/Cosine_Node.jpg "餘弦結圖示")



回傳其輸入值的餘弦值（弧度<b>）：cos（X）。</b>

+++

+++正弦
![正弦節圖示](function-nodes.resources/Sine_Node.jpg "正弦節圖示")



回傳其輸入值的正弦值（弧度<b>）：sin（X）。</b>

+++

+++正切
![切節點圖示切節點圖示](function-nodes.resources/Tangent_Node.jpg "")



回傳輸入值的切線（弧度<b>）：tan（X）。</b>

+++

+++弧切線2
![弧切線 2 節點圖示](function-nodes.resources/ArcTangent2_Node.jpg "弧切線 2 節點圖示")



回傳輸入二維向量與水平向量之間的角度。

它是笛卡兒</b>函數的<b>倒數。

不需像一般 <b>的 atan2</b> 函數那樣切換輸入向量的 X 和 Y 分量。

+++

+++笛卡兒
![絕對節點圖示](function-nodes.resources/Absolute_Node.jpg "絕對節點圖示")



將極座標轉換為笛卡爾座標。

它是弧切</b>2函數的倒數<b>：<b>長度 \* Float2（cos（Angle）， sin（Angle）。</b>

極座標是距離原點的距離以及與水平線的弧度角。

+++

+++隨機
![隨機節點圖示](function-nodes.resources/Random_Node.jpg "隨機節點圖示")



回傳一個介於 0 與輸入值 <b>X</b> 之間的隨機值。

+++
