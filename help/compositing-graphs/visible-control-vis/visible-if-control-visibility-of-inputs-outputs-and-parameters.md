---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/visible-if-control-visibility-of-inputs-outputs-and-parameters.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Designer 中使用可見的 if 表達式，根據條件控制參數的可見性。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Exposing a parameter > Visible if expressions
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 可見的 if 表達式
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '504'
ht-degree: 1%

---


# 可見的 if 表達式

「可見的如果」表達式讓你能 <b>控制圖形中輸入、輸出和參數的可見性</b> 。

在暴露參數[&#128279;](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)時，你可能想根據其他參數的狀態隱藏或顯示參數或節點連接器。例如，只有當布林參數按鈕設為 `true`時才會顯示滑桿，否則不會有影響，可能會讓使用者感到困惑。

為達成此目標，你可以在 Visible if</b> 屬性中輸入&#x200B;*邏輯表達<b>*&#x200B;式：

* 圖的 [輸入參數](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md);
* 圖的 [輸入](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md) 節點;
* 圖的 [輸出](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) 節點。

![切換輸入參數可見](visible-if-control-visibility-of-inputs-outputs-and-parameters.resources/visible-if-example.gif "性切換輸入參數可見性"){width="512px"}

如果邏輯運算式的值值為 `true`，該參數、輸入或輸出會在所有 [代表當前圖的實例節點](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md) 中顯示。 否則，它會被 *隱藏*&#x200B;起來。

只要有陳述這些條件的邏輯表達式有效，複數條件是可能的。

>[!NOTE]
>
> 注意事項
> 
> * 此功能 *僅* 影響使用者介面中是否顯示參數或連接器，對 *圖形的計算與結果無影響* 。
> * 當將函式暴露或套用到任何用於「可見 if」語句的參數時，這些語句會被 *忽略* ，並預設為「true」。

>[!IMPORTANT]
>
> 雖然此功能在 Substance 3D 生態系統內運作，但部分整合可能不支援。 若不支援，可見性條件預設為 `true`。

## 撰寫「可見 if」表達式

### 存取輸入參數

任何可見的 If 表達式都需要至少使用一個輸入，這可以透過以下語法完成：

```
input.identifier 

input["identifier"]
```


>[!WARNING]
>
> **識別**&#x200B;碼必須是&#x200B;*現有輸入參數&#x200B;**Identifier**&#x200B;屬性的精確*&#x200B;名稱，且必須區&#x200B;*分*&#x200B;大小寫。你 *不能* 用標籤來指稱參數。\
>  若不存在參考參數，或邏輯表達式無效，*則會在 Visible if **屬性上顯示**&#x200B;警告*。

### 可用營運商

「可見 if」欄位接受以下參數：

* 布林、浮點數和整數輸入。
* `true` 以及 `false` 數值（大小寫區分，無大寫！）
* `.x` ： 存取子參數
* `&&`<b> </b>：且
* `||`<b> </b>： 或
* `!`<b> </b>：不是
* `<`<b>， </b>`>`<b>， ， </b>`<=`<b></b>`>=`<b>， </b>`==`<b>， ， ： </b>`!=` 比較
* `()` ：括號

### 必須總是以布林值來評估

「IF」陳述的條件是使用可見的 If 表達式，表示它必須總是結果為 `true` 或 `false`。

* 布林值可以直接作為條件來計算。 一個布林值的簡單按鈕只需要這個。 請參考以下範例，第一個案例;
* 非布林參數通常需要比較&#x200B;**&#x200B;運算。比較運算子見上方，以下為範例;
* 有些非布林值可能是 *真值* 或 *誤差*&#x200B;值，這表示它們可以根據 `true` 來 `false` 評估——例如： 整數值 被 `0` 評估為假。

## 範例

| 條件（「如果」） | 公式 | 備註 |
| --- | --- | --- |
| 真 | ` input["my_input"]   input.my_input `  ` input["my_input"] == true   input.my_input == true ` | my\_input 是一個布林值 |
| 假 | ` !input["my_input"]   !input.my_input `  ` input["my_input"] == false   input.my_input == false `  ` input["my_input"] != true   input.my_input != true ` | my\_input 是一個布林值 |
| 比 | ` input["my_input"] < 3   input.my_input < 3 ` | my\_input 是一個整數值 |
| 等於 | ` input["param1"] == 2   input.param1 == 2 ` | param1 是一個浮點數或整數值 |
| 比 | ` input["my_input"].y < 3   input.my_input.y < 3 ` | my\_input 是一個具有一個或多個成分的浮點數或整數值——例如 float2（x， y）、integer3（x， y， z） |
| 或 | ` input["param1"] \|\| input["param2"]   input.param1 \|\| input.param2 ` | Param1 和 Param2 是布林值 |
| 與 | ` input["param1"] > 0 && input["param2"] > 1   input.param1 > 0 && input.param2 > 1 ` | Param1 和 Param2 是浮點數或整數值 |
