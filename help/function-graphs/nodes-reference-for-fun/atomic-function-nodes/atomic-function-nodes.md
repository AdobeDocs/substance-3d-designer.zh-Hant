---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/atomic-function-nodes.html"
breadcrumb-title: ''
description: 了解原子函數節點，這是Substance函數圖中最小的節點單位，用於建構自訂函數。
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Atomic function nodes
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 原子函數節點
user-guide-description: ''
user-guide-title: ''
source-git-commit: 953b99bc5f48c431e7ace47a23b0b451cceaa0db
workflow-type: tm+mt
source-wordcount: '1108'
ht-degree: 1%

---


# 原子函數節點

類似 [於 Substance 圖](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/atomic-nodes.md)中的原子節點，Substance 函數圖中的原子節點是該圖中最小的節點單位。

它們可依用途分為數個類別：

| 類別 | 節點 | 輸入類型 | 輸出類型 | 說明 |
|:---------------------------------------------------------------------------------------------------------------------------------------|:----------------------|:-----------------------|:------------------|:---------------------------------------------------------------------------------------------------|
| [恆定](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/constant-nodes/constant-nodes.md) | 浮標 | - | 浮標 | 定義一個恆定浮動值，例如 0.1 |
|                                                                                                                                        | Float2 | - | Float2 | 定義一個由兩個浮動值組成的常數向量，例如 （0.1， 0.2） |
|                                                                                                                                        | Float3 | - | Float3 | 定義一個由三個浮動值組成的常數向量，例如 （0.1， 0.2， 0.3） |
|                                                                                                                                        | Float4 | - | Float4 | 定義一個由四個浮動值組成的常數向量，例如 （0.1， 0.2， 0.3， 0.4） |
|                                                                                                                                        | 整數 | - | 整數 | 定義一個常數整數值，例如 1 |
|                                                                                                                                        | 整數2 | - | 整數2 | 定義一個由兩個整數值組成的常數向量，例如 （1， 2） |
|                                                                                                                                        | 整數3 | - | 整數3 | 定義一個由三個整數值組成的常數向量，例如 （1， 2， 3） |
|                                                                                                                                        | 整數4 | - | 整數4 | 定義一個由四個整數值組成的常數向量，例如 （1， 2， 3， 4） |
|                                                                                                                                        | 布林值 | - | 布林值 | 定義一個常數布林值，例如 True（真）或假（False） |
|                                                                                                                                        | 弦 | - | 弦 | 定義一個固定的字串值，例如「Substance」 |
| [向量](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/vector-and-swizzle-nodes/vector-and-swizzle-nodes.md) | 向量 Float2 | Float1 | 浮筒2 | 在一個座標為 2 的向量中，輸出兩個浮點值 |
|                                                                                                                                        | 向量 Float3 | Float1 / Float2 | 浮標3 | 在一個有三個座標的向量中鑄造兩個浮點值 |
|                                                                                                                                        | 向量浮4 | 浮動1 / 2 / 3 | 浮動4 | 在一個座標為 4 的向量中投射兩個浮點值 |
|                                                                                                                                        | Swizzle Float1 | 向量浮子 | Float1 | 從向量中提取浮動座標 |
|                                                                                                                                        | Swizzle Float2 | 向量浮子 | Float2 | 從向量中提取兩個浮點座標 |
|                                                                                                                                        | Swizzle Float3 | 向量浮子 | Float3 | 從向量中提取 3 個浮動座標 |
|                                                                                                                                        | 旋轉漂浮4 | 向量浮子 | Float4 | 從向量中提取 4 個浮動座標 |
|                                                                                                                                        | 向量整數2 | 整數2 | 向量整數2 | 在一個座標為 2 的向量中鑄造兩個整數值 |
|                                                                                                                                        | 向量整數3 | 整數3 | 整數3 | 在一個座標為 3 個的向量中鑄造 2 個整數值 |
|                                                                                                                                        | 向量整數4 | 整數4 | 整數4 | 在一個有 4 個座標的向量中鑄造 2 個整數值 |
|                                                                                                                                        | Swizzle 整數1 | 向量整數 | 整數1 | 從向量中提取整數座標 |
|                                                                                                                                        | Swizzle 整數2 | 向量整數 | 整數2 | 從向量中提取兩個整數座標 |
|                                                                                                                                        | Swizzle 整數3 | 向量整數 | 整數3 | 從向量中提取 3 個整數座標 |
|                                                                                                                                        | 旋轉整數4 | 向量整數 | 整數4 | 從向量中提取 4 個整數座標 |
| [變數](../../../function-graphs/variables/variables.md) | 場景 | 任何 | 輸入類型 | 設定一個變數 |
|                                                                                                                                        | 取得整數1 | - | 整數1 | 取得一個函數或圖形的整數值輸入 |
|                                                                                                                                        | 取得 Integer2 | - | 整數2 | 取得一個函數或圖形 整數 2 值輸入 |
|                                                                                                                                        | 取得整數3 | - | 整數3 | 取得一個函數或圖形 Integer3 的值輸入 |
|                                                                                                                                        | 取得 Integer4 | - | 整數4 | 取得一個函數或圖形 Integer4 值輸入 |
|                                                                                                                                        | 取得 Float1 | - | Float1 | 取得函數或圖形浮動值輸入 |
|                                                                                                                                        | 取得 Float2 | - | Float2 | 取得函數或圖形 Float2 的值輸入 |
|                                                                                                                                        | 取得 Float3 | - | Float3 | 取得函數或圖形 Float3 的值輸入 |
|                                                                                                                                        | 取得 Float4 | - | Float4 | 取得函數或圖形 Float4 值輸入 |
|                                                                                                                                        | 取得布林值 | - | 布林值 | 輸入一個函數或圖的布林值 |
| 取樣器 | 格雷樣本 | 向量 Float2 | Float4 | 回傳輸入影像在給定 UV 座標（float2）的灰階值 |
|                                                                                                                                        | 範例色彩 | 向量 Float2 | Float4 | 回傳輸入影像在給定 UV 座標的顏色值（float2） |
| 演員陣容 | 漂浮 | 整數1 | Float1 | 將整數轉換成浮點數 |
|                                                                                                                                        | To Float2 | 整數2 | Float2 | 將整數2轉換為float2 |
|                                                                                                                                        | To Float3 | 整數3 | Float3 | 將整數3轉換為float3 |
|                                                                                                                                        | 前往 Float4 | 整數4 | Float4 | 將整數4轉換為float4 |
|                                                                                                                                        | 轉為整數 | Float1 | 整數1 | 將浮點數轉換為整數 |
|                                                                                                                                        | 致整數2 | Float2 | 整數2 | 將 float2 轉換為整數 |
|                                                                                                                                        | 到 Integer3 | Float3 | 整數3 | 將 float3 轉換為整數 |
|                                                                                                                                        | 轉為 Integer4 | Float4 | 整數4 | 將 float4 轉換為整數 |
| [操作員](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/operator-nodes/operator-nodes.md) | 新增 | 向量浮點數 / 整數 | a 與 b 的類型 | 相加兩個相同類型的值：a + b |
|                                                                                                                                        | 減法 | 向量浮點數 / 整數 | a 與 b 的類型 | 減去兩個相同類型的值：a - b |
|                                                                                                                                        | 乘法 | 向量浮點數 / 整數 | a 與 b 的類型 | 將兩個相同類型的值相乘：a \* b |
|                                                                                                                                        | 純量乘法 | 向量浮子 | 類型 | 將一個值乘以浮動值：一個 \* 標量 |
|                                                                                                                                        | 分區 | Float1 / 整數1 | a 與 b 的類型 | 將同類型的兩個值除以：a / b |
|                                                                                                                                        | 否定 | Float1 / 整數1 | 類型 | 回傳否定值：-a |
|                                                                                                                                        | 模數 | Float1 / 整數1 | 類型 | 回傳模數值：mod（a， 除子） |
|                                                                                                                                        | 點積 | 向量浮子 | a 與 b 的類型 | 回傳兩個相同類型的點積：dot（a， b） |
| [合乎邏輯](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/logical-nodes/logical-nodes.md) | 與 | 布林值 | 布林值 | 若兩個布林條目為真，則回傳為真。 若其中一項為 false，則回傳 false。 |
|                                                                                                                                        | 或 | 布林值 | 布林值 | 若布林元素中有 1 個為真，則會回傳真。 如果兩者皆為假，則回傳為假。 |
|                                                                                                                                        | 非 | 布林值 | 布林值 | 回傳該項目的否定布林值：！a |
| [比較](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/comparison-nodes/comparison-nodes.md) | 等於 | Float1 / 整數1 | 布林值 | 若 a = b 則返回為真 |
|                                                                                                                                        | 不等於 | Float1 / 整數1 | 布林值 | 若 a ！= b 則返回為真 |
|                                                                                                                                        | 更偉大 | Float1 / 整數1 | 布林值 | 若 a > b 則回傳為真 |
|                                                                                                                                        | 大或相等 | Float1 / 整數1 | 布林值 | 若 a >= b 則返回為真 |
|                                                                                                                                        | 下層 | Float1 / 整數1 | 布林值 | 若 &lt; b |
|                                                                                                                                        | 低或相等 | Float1 / 整數1 | 布林值 | 若 &lt;= b |
| 功能 | 絕對 | Float1 / 整數1 | Float1 | 回傳 a 的絕對值：abs（a） |
|                                                                                                                                        | 下限 | Float1 / 整數1 | Float1 | 回傳低於或等於 a 的最高值：floor（a） |
|                                                                                                                                        | 凱爾 | Float1 / 整數1 | Float1 | 回傳最小值 a：ceil（a） |
|                                                                                                                                        | 餘弦 | Float1 / 整數1 | Float1 | 回傳 a 的餘弦值：cos（a） |
|                                                                                                                                        | 正弦 | Float1 / 整數1 | Float1 | 回傳 a 的正弦值：sin（a） |
|                                                                                                                                        | 正切 | Float1 / 整數1 | Float1 | 回傳 a 的切值：tan（a） |
|                                                                                                                                        | 弧線 2 切線 | 向量 Float2 | Float1 | 回傳向量2項的arc tan 2值：arctan2（xa， ya） |
|                                                                                                                                        | 笛卡兒 | Float1 | Float2 | 將兩個極座標轉換為笛卡兒座標：carth（rho， theta） |
|                                                                                                                                        | 平方根 | Float1 / 整數1 | Float1 | 回傳 的平方根值 |
|                                                                                                                                        | 對數 | Float1 / 整數1 | Float1 | 回傳 a 的對數值：log（a） |
|                                                                                                                                        | 指數 | Float1 / 整數1 | Float1 | 回傳 a 的指數值：exp（a） |
|                                                                                                                                        | 砰 2 | Float1 / 整數1 | Float1 | 回傳 的 2 的冪次方 |
|                                                                                                                                        | 線性插值 | Float1 / 整數1 | Float1 | 回傳兩個值之間的線性插值值，依浮點值而定：（1-x）a + x \* b |
|                                                                                                                                        | 最低限度 | Float1 / 整數1 | a 與 b 的類型 | 回傳 a 與 b 之間的最小值 |
|                                                                                                                                        | 極限 | Float1 / 整數1 | a 與 b 的類型 | 回傳 a 與 b 之間的最大值 |
| 隨機 |                       | Float1 | Float1 | 產生一個介於 0 與 之間的浮動值 |
| [控制](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/control-nodes/control-nodes.md) | 序列 | 任何 | 輸入類型 | 允許選擇先計算兩個值中的哪一個。 |
|                                                                                                                                        | 如果......否則 | 布林 / a 與 b | a 與 b 的類型 | 若 條件為真，則回傳真。 如果是假，則回傳 false。 |
