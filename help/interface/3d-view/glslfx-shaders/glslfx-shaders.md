---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/3d-view/glslfx-shaders.html"
breadcrumb-title: ''
description: 在 Substance 3D Designer 3D 視圖中使用 GLSLFX 著色器來自訂材質渲染與預覽效果。
helpx_creative_field: ""
helpx_description: Designer > Interface > 3D View > GLSLFX Shaders
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: GLSLFX 著色器
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '3098'
ht-degree: 0%

---


# GLSLFX 著色器

GLSLFX 檔案作為應用程式與 GLSL 著色器檔案之間的橋樑。\
它允許使用任何 glsl 著色器，而不必修改程式碼。

## 檔案格式

GLSLFX 檔案格式為 XML 檔案。 歡迎留言。

### 標頭與根節點

XML 根節點元素命名 <b>為 glslfx</b>。

```
<?xml version="1.0" encoding="UTF-8"?>

<glslfx version="1.0.0" author="allegorithmic.com">

    <!-- BODY -->

    <!-- ... -->

</glslfx>
```


### 車身

#### 技術

XML 元素描述一種技術。 技術是當前效果的變體。 GLSLFX 可以包含多種技術，但至少必須定義一種技術。

幾何體將使用應用程式定義的技術之一來渲染。

+++XML 元素定義
<b>名稱：</b> 技巧

<b>屬性：</b>

* 名稱：任何用來命名技術的字串

+++

XML 元素可以有多個子節點。 技術中定義的元素會覆蓋全局定義的元素。

例如，它用來覆寫某些均勻值，並取得此技術的效果變異。

#### 渲染通行證

XML 元素描述渲染通道。 渲染通行描述幾何圖形的渲染。

一個技術可以包含多個渲染過程，並依序執行。 包含不渲染通行的技術等同於包含「螢幕上」渲染通行的技術。

渲染通道中定義的元素會覆蓋母技術中定義的元素。

+++XML 元素定義
<b>名稱：</b> 山口

<b>屬性：</b>

* 輸出

* 畫面外：渲染會被設定成使用者定義的渲染目標

* 螢幕上：渲染會直接到預設的渲染目標

+++

#### 著色器

為每種類型設定 GLSL 著色器檔案。

XML 元素定義：

+++XML 元素定義
<b>名稱：</b> 著色器

<b>屬性：</b>

* 類型：GLSL 著色器類型;

* 檔名：glsl 著色器檔案的路徑。 可以是絕對的，也可以是相對於 GLSLFX 檔案的;

* primitiveType：渲染原始物件的方法。


| 「類型」值 | 說明 |
| --- | --- |
| 頂點 | 頂點著色器 |
| 幾何 | 幾何著色器 |
| Tess\_control | Tessellation Control 著色器 |
| Tess\_eval | Tessellation Evaluation 著色器 |
| 碎片 | 片段著色器 |



| 「primitiveType」值 | 說明 |
| --- | --- |
| 點 | 以點形式渲染 |
| 線環 | 渲染為線迴圈 |
| 補丁[1..N] | 以 [1..N] 頂點的補丁形式渲染 |


+++

#### 屬性

允許設定 OpenGL 狀態的某部分。

+++XML 元素定義
<b>名稱：</b> 財產

<b>屬性：</b>

* 名稱：要設定的屬性名稱。 名稱基於 OpenGL 函式或 glEnum 名稱：
  * 列舉語法：不加「GL\_」前綴，且用小寫。 範例：glEnable（GL\_BLEND\_ENABLE） => “”“， glDisable（GL\_CULL\_FACE） => ”“”
  * 函式語法：不加「gl」前綴，使用小寫，且所有單字以「\_」字元分隔。 範例：glBlendFunc（GL\_SRC\_ALPHA， GL\_ONE\_MINUS\_SRC\_ALPHA） => “”

* 列舉語法：不加「GL\_」前綴，且用小寫。 範例：glEnable（GL\_BLEND\_ENABLE） => “”“， glDisable（GL\_CULL\_FACE） => ”“”

* 函式語法：不加「gl」前綴，使用小寫，且所有單字以「\_」字元分隔。 範例：glBlendFunc（GL\_SRC\_ALPHA， GL\_ONE\_MINUS\_SRC\_ALPHA） => “”

* 價值：財產的價值。


| 「名稱」價值 | 「價值」價值 | 說明 |
| --- | --- | --- |
| Blend_enabled | 布林值 | 啟用/停用混合模式 |
|  | 沒錯 |  |
|  | 短柄 |  |
| 混合_func | 弦，弦 | 設定來源和目標混合函數 |
|  | 零 | 對於 OpenGL enum GL\_ZERO |
|  | 一 | 對於 OpenGL 則是 enum GL\_ONE |
|  | SRC_color | 對於 OpenGL enum 則是 GL\_SRC\_COLOR |
|  | 一_minus\_src\_color | 對於 OpenGL enum 則是 GL\_ONE\_MINUS\_SRC\_COLOR |
|  | 夏令時_color | 對於 OpenGL 則是列舉 GL\_DST\_COLOR |
|  | 一_minus\_dst\_color | 對於 OpenGL enum GL\_ONE\_MINUS\_DST\_COLOR |
|  | SRC_alpha | 對於 OpenGL enum GL\_SRC\_ALPHA |
|  | 一_minus\_src\_alpha | 對於 OpenGL enum 則是 GL\_ONE\_MINUS\_SRC\_ALPHA |
|  | 夏令時間_alpha | 對於 OpenGL enum GL\_DST\_ALPHA |
|  | 一_minus_dst_alpha | 對於 OpenGL enum 來說，是 GL\_ONE\_MINUS\_DST\_ALPHA |
|  | 持續_color | 對於 OpenGL enum GL\_CONSTANT\_COLOR |
|  | 一_minus\_constant\_color | 對於 OpenGL enum 則是 GL\_ONE\_MINUS\_CONSTANT\_COLOR |
|  | 持續_alpha | 對於 OpenGL enum 為 GL\_CONSTANT\_ALPHA |
|  | 一_minus\_constant\_alpha | 對於 OpenGL enum 則是 GL\_ONE\_MINUS\_CONSTANT\_ALPHA |
|  | SRC\_alpha\_saturate | 對於 OpenGL enum 則是 GL\_SRC\_ALPHA\_SATURATE |
|  | SRC1\_color | 對於 OpenGL enum 則是 GL\_SRC1\_COLOR |
|  | 一_minus\_src1\_color | 對於 OpenGL enum 則是 GL\_ONE\_MINUS\_SRC1\_COLOR |
|  | SRC1\_alpha | 對於 OpenGL enum GL\_SRC1\_ALPHA |
|  | 一_minus\_src1_alpha | 對於 OpenGL enum 則是 GL\_ONE\_MINUS\_SRC1\_ALPHA |
| 卡爾\_face\_enabled | 布林值 | 啟用/停用面剔除 |
|  | 沒錯 |  |
|  | 短柄 |  |
| 卡爾\_face\_mode | 字串 | 設定臉部剔除模式 |
|  | 前面 | 對於 OpenGL enum GL\_FRONT |
|  | 退後/背面 | 對於 OpenGL enum GL\_BACK |
|  | 前_and\_back | 對於 OpenGL enum GL\_FRONT\_AND\_BACK |
| 深度_func | 字串 | 設定深度比較函數 |
|  | 從來沒有 | 對於 OpenGL enum GL\_NEVER |
|  | 更少 | 對於 OpenGL enum GL\_LESS |
|  | 利考爾 | 對於 OpenGL enum GL\_LEQUAL |
|  | 相等 | 對於 OpenGL enum GL\_EQUAL |
|  | Notequal | 對於 OpenGL enum GL\_NOTEQUAL |
|  | Gequal | 對於 OpenGL enum GL\_GEQUAL |
|  | 更偉大 | 對於 OpenGL enum GL\_GREATER |
|  | 永遠 | 對於 OpenGL enum GL\_ALWAYS |


+++

#### 制服

允許覆蓋部分全域定義或母技術中定義的統一。 這允許改變此技術或渲染通道的著色器行為。

請參閱<b></b>下方制服章節，了解更多關於制服定義的細節。

+++範例


+++

## 渲染目標

對於「螢幕外」渲染通道，必須在渲染通道中定義渲染目標。

+++XML 元素定義
<b>名稱：</b> 輸出

<b>屬性：</b>

* 附件：OpenGL 的連接點，靈感來自 OpenGL 名稱：\
  GL\_COLOR\_ATTACHMENT[0..3] => &#39;color[0..3]&#39;\
  GL\_DEPTH\_ATTACHMENT => 「深度」

附件：OpenGL 的連接點，靈感來自 OpenGL 名稱：\
GL\_COLOR\_ATTACHMENT[0..3] => &#39;color[0..3]&#39;\
GL\_DEPTH\_ATTACHMENT => 「深度」

* 名稱：渲染目標的名稱。\
  它可以在後續的渲染階段中用來綁定這個渲染目標作為取樣器。

名稱：渲染目標的名稱。\
它可以在後續的渲染階段中用來綁定這個渲染目標作為取樣器。

* 格式：渲染目標的內部格式。

格式：渲染目標的內部格式。

* clear：可選屬性，定義一個清晰值。\
  如果有，渲染目標會在渲染通道開始時被清除到這個值。\
  若缺少，渲染目標將保留先前的內容。

+++

>[!NOTE]
>
> 在「螢幕上」渲染通道中禁止使用色彩渲染目標，但深度渲染目標可以與任何渲染通道共用（但當場景混合多個材質時，可能會破壞渲染）。

<b>關於格式</b>

對於深度格式，支援所有僅深度（無模板）的 OpenGL 格式：

* GL\_DEPTH\_COMPONENT16 => &#39;depth26&#39;
* GL\_DEPTH\_COMPONENT24 => &#39;depth34&#39;
* GL\_DEPTH\_COMPONENT32 => &#39;depth42&#39;
* GL\_DEPTH\_COMPONENT32F => &#39;depth42f&#39;

對於色彩格式，名稱基於 OpenGL 的列舉名稱，且不使用 &#39;GL\_&#39; 前綴，且為小寫。\
不支援三通道格式（RGB），請改用 RGBA 格式。\
每個通道支援的位元深度：

* 正規化無符號整數：8、16
* 浮點數：16、32

例外的是支援的 GL\_R11F\_G11F\_B10F 格式。

* GL\_RGBA8 => &#39;rgba8&#39;
* GL\_RGBA16F => &#39;rgba16f&#39;
* GL\_SRGB8\_ALPHA8 => &#39;srgb8\_alpha8&#39;
* GL\_R11F\_G11F\_B10F => &#39;r11f\_g11f\_b10f&#39;
* GL\_RG16 => 「rg16」

### 取樣器

允許覆蓋部分全域定義的取樣器，這些取樣器無法在技術中定義。 這允許定義該渲染通道的取樣器使用方式，或從渲染目標讀取先前渲染通道的讀取。

欲了解更多定義，請參閱 <b>取樣器</b> 章節。

+++範例


+++

## 輸入頂點格式

這允許定義頂點著色器中每個屬性的語意。

<b>XML 元素定義：</b>

名稱：「vertexformat」

屬性：

* 「name」：頂點著色器中定義的屬性名稱。
* 「語意」：屬性的語意。

| 「語意」價值 | 說明 |
| --- | --- |
| 職位 | 頂點位置（float3） |
| 正常 | 頂點法線（float3） |
| texcoord[0..N] | 頂點紋理座標緩衝區 N（float2） |
| 切線[0..N] | 頂點切緩衝區 N（float4） |
| 雙常態[0..N] | 頂點雙正規緩衝區 N（float4） |

範例：

```
<?xml version="1.0" encoding="UTF-8"?>

<glslfx version="1.0.0" author="allegorithmic.com">

     <!-- BODY -->

     <!-- ... -->



     <!-- INPUT VERTEX FORMAT -->

     <vertexformat name="iVS_Position" semantic="position"/>

     <vertexformat name="iVS_Normal" semantic="normal"/>

     <vertexformat name="iVS_UV" semantic="texcoord0"/>

     <vertexformat name="iVS_Tangent" semantic="tangent0"/>

     <vertexformat name="iVS_Binormal" semantic="binormal0"/>

</glslfx>
```


## 取樣器

這讓每個取樣器的使用方式都得以定義。\
應用程式會用它來知道在指定的取樣器中要設定哪種材質。

<b>XML 元素定義：</b>

名稱：「sampler」

屬性：

* &#39;name&#39;：著色器檔案中取樣器變數的名稱。
* 「使用」：取樣器的使用。 它與圖中輸出節點所指定的使用量相符。

| 「使用」價值 | 說明 |
| --- | --- |
| 彌漫性 | 漫射映射 |
| 不透明度 | 不透明度映射 |
| 發光/放射 | 發射映射 |
| 環境遮蔽 | 環境遮蔽圖 |
| 環境音樂 | 環境地圖 |
| 面罩/口罩 | 遮罩映射 |
| detailnormal（詳細正常） | 細節法線貼圖 |
| 正常 | 法線貼圖 |
| 凸塊 | 凹凸圖 |
| 高度 | 高度圖 |
| 遷移 | 位移圖 |
| 高階級 | 鏡面關卡地圖 |
| 鏡面色 | 鏡面色彩圖 |
| 鏡面 | 鏡面地圖 |
| 光澤感 | 光澤度圖 |
| 粗糙度 | 粗糙度地圖 |
| 各向異性 | 異性層級圖 |
| 各向異性 | 異角圖 |
| 透射式 | 透透映射 |
| 反思 | 反射映射 |
| 折射 | 折射圖 |
| 環境 | 環境地圖（立方體地圖） |
| 全景 | 全景地圖（緯度/經度地圖） |
| 藍噪音面具 | 一個 256x256 的抖動紋理 |

* 支援多種使用方式。
  * 範例：

```
   <!-- SAMPLERS -->

    <sampler name="baseColorMap" usage="basecolor,diffuse"/>

     <!-- ... -->
```


&#39;isHidden&#39;：布林值，指示取樣器是否應該出現在圖形介面中

* 範例：

```
     <!-- SAMPLERS -->

    <sampler name="bluenoiseMask" usage="bluenoisemask" ishidden="true"/>

     <!-- ... -->
```


包裝模式：

<table data-preserve-html="true"><tbody><tr><th>名稱</th><th>價值</th></tr><tr><td rowspan="4">texture_wrap_s，texture_wrap_t，texture_wrap_r<br/><br/><br/></td><td>clamp_to_edge</td></tr><tr><td>clamp_to_border</td></tr><tr><td colspan="1">mirrored_repeat</td></tr><tr><td colspan="1">重複<br/><br/></td></tr></tbody></table>

貼圖濾鏡

<table data-preserve-html="true"><tbody><tr><th>名稱</th><th>價值</th></tr><tr><td rowspan="6">texture_min_filter，texture_mag_filter<br/><br/><br/></td><td>最近</td></tr><tr><td>線性</td></tr><tr><td colspan="1">nearest_mipmap_nearest</td></tr><tr><td colspan="1">linear_mipmap_nearest</td></tr><tr><td colspan="1">nearest_mipmap_linear</td></tr><tr><td colspan="1">linear_mipmap_linear</td></tr></tbody></table>

範例：

```
<?xml version="1.0" encoding="UTF-8"?>

<glslfx version="1.0.0" author="allegorithmic.com">

     <!-- BODY -->

     <!-- ... -->



     <!-- SAMPLERS -->

     <sampler name="baseColorMap" usage="basecolor,diffuse"/>

     <sampler name="heightMap" usage="height"/>

     <sampler name="normalMap" usage="normal"/>

     <sampler name="detailNormalMap" usage="detailNormal"/>

     <sampler name="environmentMap" usage="environment"/>

     <sampler name="bluenoiseMask" usage="bluenoisemask" ishidden="true"/>

     <sampler name="sssDiffuseMap" usage="sssDiffuse"/>

</glslfx>
```


## 制服

這讓你能新增關於每個著色器制服的額外資訊。

<b>XML 元素定義：</b>

名稱：「制服」

屬性：

「name」：著色器檔案中制服的名稱。

| 「語意」價值 | 說明 |
| --- | --- |
| 世界 | 世界矩陣（float16） |
| 世界逆轉置 | 世界反轉置矩陣（float16） |
| 世界觀投影 | 世界觀投影矩陣（float16） |
| ViewInverse | 世界逆矩陣（float16） |
| 世界觀 | 世界觀矩陣（float16） |
| 模型檢視 | 模型檢視矩陣（float16） |
| 投影 | 投影矩陣（float16） |
| 環境音樂 | 場景環境色彩（float3） |
| 光線位置[0..N] | 場景第 N 盞燈（float3）的位置 |
| 光色[0..N] | 場景第N盞燈（float3）的顏色 |
| 光強度[0..N] | 場景第N盞燈（浮點）的強度 |
| 全球時光 | 目前時間（秒數）（浮點數） |
| 解決 | 視窗解析度（int2） |
| 滑鼠 | 滑鼠位置（int2） |
| Samplespostablesize | 計算環境光照（int）時可使用的樣本數 |
| 輻照度的天線 | 球面諧波向量陣列（float3[10]） |
| 全景地圖高度 | 全景地圖（浮點）中 mipmap 等級的數量 |
| 全景旋轉 | 角度旋轉全景圖（浮動圖）的角度 |
| 全景強度 | 全景地圖強度（浮動圖） |
| computebinormalinfragmentshader | 雙常態是每個片段的計算量嗎？ （若不行，則依頂點）（布爾） |
| 是直接的，是正常的 | 法線貼圖格式是 DirectX 嗎？ （布爾） |
| UVWSCALE | 你、v、w （float3） 的縮放值 |
| 渲染圖 | 只渲染一個 UV 圖塊？ （布爾） |
| Uvtile座標 | UV 圖塊座標與渲染 （int2） |

「語義」：制服的語義。 （所有矩陣皆為float16）。

範例：

```
<?xml version="1.0" encoding="UTF-8"?>

<glslfx version="1.0.0" author="allegorithmic.com">

     <!-- BODY -->

     <!-- ... -->



     <!-- MATRICES -->

     <uniform name="worldMatrix" semantic="world"/>

     <uniform name="worldViewProjMatrix" semantic="worldviewprojection"/>

     <uniform name="worldViewMatrix" semantic="worldview"/>

     <uniform name="worldInverseTransposeMatrix" semantic="worldinversetranspose"/>

     <uniform name="viewInverseMatrix" semantic="viewinverse"/>

     <uniform name="modelViewMatrix" semantic="modelview"/>

     <uniform name="projectionMatrix" semantic="projection"/>

</glslfx>
```


範例：

```
<?xml version="1.0" encoding="UTF-8"?>

<glslfx version="1.0.0" author="allegorithmic.com">

    <!-- BODY -->

    <!-- ... -->



    <!-- SCENE PARAMETERS -->

    <uniform name="AmbiColor" semantic="ambient"/>

    <uniform name="Lamp0Pos" semantic="lightposition0"/>

    <uniform name="Lamp0Color" semantic="lightcolor0"/>

    <uniform name="Lamp1Pos" semantic="lightposition1"/>

    <uniform name="Lamp1Color" semantic="lightcolor1"/>

</glslfx>
```


### 其他參數

其他可新增至各制服的資訊：

* 定義預設值
* 夾位值
* 控制制服在應用程式中的顯示方式：
* 設定標籤
* 設定用於編輯應用程式值的小工具資訊：
* 小工具名稱、最小值、最大值、遞增/遞減步驟
* 群組小工具中的群組統一

由於制服可以針對每種技術覆蓋，因此能顯示每種技術的專用 GUI 設定。

<b>XML 元素定義：</b>

名稱：「制服」

屬性：

* 「name」：著色器檔案中制服的名稱。
* 「預設值」：統一的預設值
* 「最小」：效度範圍的最小值
* 「max」：有效性範圍的最大值
* 「guiName」：應用程式介面中制服的名稱
* &#39;guiGroup&#39;：將制服放入應用程式 GUI 的群組名稱
* &#39;guiWidget&#39;：用於編輯應用程式圖形介面中統一值的小工具名稱

| &#39;guiWidget&#39; 值 | 說明 |
| --- | --- |
| 滑桿 | floatN 的滑桿小工具 |
| 角 | 浮點的角度小工具 |
| 顏色 | float3 的顏色小工具，float4 顏色 |
| 勾選框 | 布爾的勾選框小工具 |

* 「guiMin」：小工具的最小值
* &#39;guiMax&#39;：小工具的最大值

## 範例：鑲嵌/視差

### 視差頂點著色器檔案

位於 .\tessellation\_parallax\parallax\vs.glsl

內容：

> #version 120

attribute vec4 iVS\_Position;\
attribute vec4 iVS\_Normal;\
attribute vec2 iVS\_UV;\
attribute vec4 iVS\_Tangent;\
屬性 vec4 iVS\_Binormal;

變化 vec3 iFS\_Normal;\
變化的 vec² iFS\_UV;\
變化的 vec3 iFS\_Tangent;\
變化 vec3 iFS\_Binormal;\
變化 vec3 iFS\_PointWS;

uniform mat4 worldMatrix;\
uniform mat4 worldViewProjMatrix;

虛空主（）\
{\
gl\_Position = worldViewProjMatrix \&#42; iVS\_Position;\
iFS\_Normal = iVS\_Normal.xyz;\
iFS\_UV = iVS\_UV;\
iFS\_Tangent = iVS\_Tangent.xyz;\
iFS\_Binormal = iVS\_Binormal.xyz;\
iFS\_PointWS = （worldMatrix \&#42; iVS\_Position）.xyz;\
}

### 鑲嵌頂點著色器檔案

位於 .\tessellation\_parallax\tessellation\vs.glsl

內容：

>> 

#version 120

attribute vec4 iVS\_Position;\
attribute vec4 iVS\_Normal;\
attribute vec2 iVS\_UV;\
attribute vec4 iVS\_Tangent;\
屬性 vec4 iVS\_Binormal;

變化 vec4 oVS\_Normal;\
變化的 vec² oVS\_UV;\
變化的 vec4 oVS\_Tangent;\
變化的 vec4 oVS\_Binormal;

虛空主（）\
{\
gl\_Position = iVS\_Position;\
oVS\_Normal = iVS\_Normal;\
oVS\_UV = iVS\_UV;\
oVS\_Tangent = iVS\_Tangent;\
oVS\_Binormal = iVS\_Binormal;\
}

### 鑲嵌控制著色器檔案

位於 .\tessellation\_parallax\tessellation\tcs.glsl

內容：

>> 

#version 400 核心\
#extension GL\_ARB\_tessellation\_shader ： 啟用

layout（頂點數 = 3）向外;

在 vec4 oVS\_Normal[];\
in vec2 oVS\_UV[];\
in vec4 oVS\_Tangent[];\
in vec4 oVS\_Binormal[];

out vec4 oTCS\_Normal[];\
out vec2 oTCS\_UV[];\
out vec4 oTCS\_Tangent[];\
out vec4 oTCS\_Binormal[];

均勻浮點鑲嵌因子;

虛空主（）\
{\
gl\_TessLevelOuter[0] = 鑲嵌因子;\
gl\_TessLevelOuter[1] = 鑲嵌因子;\
gl\_TessLevelOuter[2] = 鑲嵌因子;\
gl\_TessLevelInner[0] = 鑲嵌因子;\
GL\_out[GL\_InvocationID].GL\_Position = gl\_in[gl\_InvocationID].gl\_Position;

oTCS\_Normal[gl\_InvocationID] = oVS\_Normal[gl\_InvocationID];\
oTCS\_UV[gl\_InvocationID] = oVS\_UV[gl\_InvocationID];\
oTCS\_Tangent[gl\_InvocationID] = oVS\_Tangent[gl\_InvocationID];\
oTCS\_Binormal[gl\_InvocationID] = oVS\_Binormal[gl\_InvocationID];\
}

### Tessellation Evaluation 著色器檔案

位於 .\tessellation\_parallax\tessellation\tcs.glsl

內容：

>> 

#version 400 核心

佈局（三角形、等於_spacing、CCW）在內;

在 vec4 oTCS\_Normal[];\
在 vec2 oTCS\_UV[];\
in vec4 oTCS\_Tangent[];\
在 vec4 oTCS\_Binormal[];

uniform mat4 worldMatrix;\
uniform mat4 worldViewProjMatrix;

uniform sampler2D heightMap;

均勻浮子鋪磚 = 1.0f;\
均勻浮點高度MapScale = 1.0f;

出 vec3 iFS\_Normal;\
出 vec2 iFS\_UV;\
出 vec3 iFS\_Tangent;\
出 vec3 iFS\_Binormal;\
出 vec3 iFS\_PointWS;

vec3 interpolate3D（vec3 v0， vec3 v1， vec3 v2， vec3 uvw）\
{\
回傳 UVW.x \&#42; v0 + UVW.Y \&#42; v1 + UVW.z \&#42; V2;\
}

vec2 interpolate2D（vec2 v0， vec2 v1， vec2 v2， vec3 uvw）\
{\
回傳 UVW.x \&#42; v0 + UVW.Y \&#42; v1 + UVW.z \&#42; V2;\
}

虛空主（）\
{\
VEC3 UVW = GL\_TessCoord.xyz;

vec3 newPos = interpolate3D（gl\_in[0].gl\_Position.xyz， gl\_in[1].gl\_Position.xyz， gl\_in[2].gl\_Position.xyz， uvw）;\
vec3 newNormal = normalize（interpolate3D（oTCS\_Normal[0].xyz， oTCS\_Normal[1].xyz， oTCS\_Normal[2].xyz， uvw））;\
vec3 newTangent = normalize（interpolate3D（oTCS\_Tangent[0].xyz， oTCS\_Tangent[1].xyz， oTCS\_Tangent[2].xyz， uvw））;\
vec3 newBinormal = normalize（interpolate3D（oTCS\_Binormal[0].xyz， oTCS\_Binormal[1].xyz， oTCS\_Binormal[2].xyz， uvw））;\
vec2 newUV = 插值2D（oTCS\_UV[0]， oTCS\_UV[1]， oTCS\_UV[2]， uvw）;

float heightTexSample = texture（heightMap， newUV \&#42; tileling）.x \&#42; 2.0 - 1.0;\
newPos += newNormal \&#42; heightTexSample \&#42; heightMapScale;

vec4 obj\_pos = vec4（newPos， 1）;\
gl\_Position = worldViewProjMatrix \&#42; obj\_pos;

iFS\_UV = newUV \&#42; 平鋪;\
iFS\_Tangent = newTangent;\
iFS\_Binormal = newBinormal;\
iFS\_Normal = newNormal;\
iFS\_PointWS = （worldMatrix \&#42; obj\_pos）.xyz;\
}

### 片段著色器檔案

位於 .\tessellation\_parallax\fs.glsl

內容：

>> 

#version 120

#define ALG\_NORMAL\_DIRECTX\
#define ALG\_NORMAL_OPENGL

#ifdef ALG\_NORMAL\_DIRECTX\
#define 翻_NORMAL_X\
#define 翻_NORMAL_Y\
#define 翻_NORMAL\_Z\
#endif //#ifdef ALG\_NORMAL\_DIRECTX

#ifdef ALG\_NORMAL\_OPENGL\
#define 翻_NORMAL_X\
#define 翻_NORMAL_Y\
#define 翻_NORMAL\_Z\
#endif //#ifdef ALG\_NORMAL\_OPENGL

變化 vec3 iFS\_Normal;\
變化的 vec² iFS\_UV;\
變化的 vec3 iFS\_Tangent;\
變化 vec3 iFS\_Binormal;\
變化 vec3 iFS\_PointWS;

均勻 vec3 Lamp0Pos = vec3（0.0f， 0.0f， 70.0f）;\
均勻 vec3 燈泡色 = vec3（1.0f， 1.0f， 1.0f）;\
均勻 vec3 Lamp1Pos = vec3（70.0f， 0.0f， 0.0f）;\
均勻 vec3 燈泡1Color = vec3（0.198f， 0.198f， 0.198f）;\
均勻布爾翻轉法則 = 真;\
均勻浮點 TilingDetail = 3.0f;\
均勻浮點 SpecExpon = 50.0;\
均勻浮點 Ks = 1.0;\
均勻整數視差\_mode = 0;\
均勻浮點鑲嵌因子 = 4.0;\
均勻浮點高度MapScale = 1.0f;\
均勻浮子深度 = 0.5 f_detail;\
均勻浮子 Kr = 0.5f;\
uniform int KF\_on = 1;\
均勻浮子KFs = 1.0f;\
均勻 vec3 AmbiColor = vec3（0.07f，0.07f，0.07f）;\
均勻浮子鋪磚 = 1.0f;\
uniform int enableTilingInFS = 0;

uniform sampler2D heightMap;\
uniform sampler2D normalMap;\
uniform sampler2D detailNormalMap;\
均勻取樣器2D 發射映射;\
uniform sampler2D diffuseMap;\
均勻取樣器2D specularMap;\
uniform sampler2D 不透明度圖;\
uniform samplerCube environmentMap;

uniform mat4 worldMatrix;\
uniform mat4 worldInverseTransposeMatrix;\
均勻 mat4 視圖逆矩陣;

vec4 litFct（float NdotL， float NdotH， float specExp）\
{\
浮點環境 = 1.0;\
float diffuse = max（NdotL， 0.0）;\
float 鏡面 = step（0.0， NdotL） \&#42; pow（max（0.0， NdotH）， specExp）;\
回傳 vec4（環境、漫射、鏡面、1.0）;\
}

vec3 lerpFct（vec3 v0， vec3 v1， float percent）\
{\
回放 V0 + （V1-V0） \&#42; 百分比;\
}

蓬遮陽\
虛空的 Phong\_shading（\
在 vec3 LightColor，\
在 vec3 正規 WS 中，\
在 vec3 pointToLightDirWS 中，\
在 vec3 pointToCameraDirWS，\
inout vec3 DiffuseContrib，\
內含 vec3 SpecularContrib）\
{\
vec3 Hn = normalize（pointToCameraDirWS + pointToLightDirWS）;\
vec4 litV = litFct（dot（normalWS， pointToLightDirWS）， dot（normalWS， Hn）， SpecExpon）;\
DiffuseContrib = litV.y \&#42; LightColor;\
SpecularContrib = litV.y \&#42; litV.z \&#42; Ks \&#42; LightColor;\
}

vec3 fixNormalSample（vec3 v）\
{\
VEC3 結果 = v - VEC3（0.5,0.5,0.5）;

#ifdef 翻_NORMAL_X\
result.x = -result.x;\
#endif // ifdef FLIP\_NORMAL\_X\
#ifdef 翻_NORMAL_Y\
result.y = -result.y;\
#endif // ifdef FLIP\_NORMAL\_Y\
#ifdef 翻_NORMAL_Z\
result.z = -result.z;\
#endif // 如果 def FLIP\_NORMAL\_Z

回傳結果;\
}

vec3 normalVecOSToWS（vec3 normal）\
{\
返回正常;\
}

虛空主（）\
{\
vec3 cameraPosWS = viewInverseMatrix[3].xyz;\
vec3 pointToLight0DirWS = normalize（Lamp0Pos - iFS\_PointWS）;\
vec3 pointToLight1DirWS = normalize（Lamp1Pos - iFS\_PointWS）;\
vec3 pointToCameraDirWS = normalize（cameraPosWS）;\
vec3 normalOS = normalize（iFS\_Normal）;\
vec3 tangentOS = normalize（iFS\_Tangent）;\
vec3 binormalOS = normalize（iFS\_Binormal）;

// ------------------------------------------\
確保 TBN 是正交標準化的\
binormalOS = normalize（cross（normalOS， tangentOS））;\
tangentOS = normalize（cross（binormalOS， normalOS））;

vec3 累積NormalOS = normalOS;

// ------------------------------------------\
更新UV\
float a = dot（normalOS，-pointToCameraDirWS）;\
vec3 s = vec3（dot（pointToCameraDirWS，tangentOS）， dot（pointToCameraDirWS，binormalOS）， a）;\
vec2 uv = enableTilingInFS == 0 ？ iFS\_UV ： （iFS\_UV \&#42; 平鋪）;\
float height = texture2D（heightMap，uv）.x \&#42; 2.0 - 1.0 ;\
浮動視差 = 視差\_mode == 0 ？ （tessellationFactor / 100000.f + heightMapScale / 500.f） ： （heightMapScale / 50.f）;\
UV +=（高度 \&#42; S.xy \&#42; 視差）;

// ------------------------------------------\
從法線貼圖新增法線\
vec3 normalTS = texture2D（normalMap，uv）.xyz;\
normalTS = fixNormalSample（normalTS）;\
vec3 normalMapOS = normalTS.x\&#42;tangentOS + normalTS.y\&#42;binormalOS;\
累積NormalOS = 累積NormalOS + normalMapOS;\
cumulatedNormalOS = normalize（curmulatedNormalOS）;

// ------------------------------------------\
新增細節法線貼圖\
vec3 normalDetailTS = texture2D（detailNormalMap，uv\&#42;TilingDetail）.xyz;\
normalDetailTS = fixNormalSample（normalDetailTS）;\
vec3 變數NormalDetailTS = lerpFct（vec3（0.0,0.0,0.5），normalDetailTS，Depth\_detail）;\
vec3 normalDetailOS = variableNormalDetailTS.x\&#42;tangentOS + variableNormalDetailTS.y\&#42;binormalOS;\
累積正常OS = 累積正常OS + normalDetailOS;\
cumulatedNormalOS = normalize（curmulatedNormalOS）;

如果 （length（normalTS）&lt;0.0001)\
累積 NormalOS = normalOS;

vec3 累積NormalWS = normalVecOSToWS（累積NormalOS）;

// ------------------------------------------\
計算漫射與鏡面

光 0 貢獻\
vec3 diffContrib = vec3（0， 0， 0）;\
vec3 specContrib = vec3（0， 0， 0）;\
phong\_shading（Lamp0Color， cumulatedNormalWS， pointToLight0DirWS， pointToCameraDirWS， diffContrib， specContrib）;

光 1 的貢獻\
vec3 diffContrib2 = vec3（0， 0， 0）;\
vec3 specContrib2 = vec3（0， 0， 0）;\
phong\_shading（Lamp1Color， cumulatedNormalWS， pointToLight1DirWS， pointToCameraDirWS， diffContrib2， specContrib2）;

diffContrib += diffContrib2;\
specContrib += specContrib2;

vec4 diffuseColor = texture2D（diffuseMap，uv）;

vec3 specularColor = texture2D（specularMap，uv）.rgb;\
vec3 R = reflect（pointToCameraDirWS，累積NormalWS）;\
vec3 reflColor = Kr \&#42; textureCube（environmentMap，R.xyz）.bgr;

FallofRefl 浮動;

若 （KFs >= 0.0）\
FallofRefl = max（（1-dot（pointToCameraDirWS/（KFs），累積NormalWS）），0）\&#42;KF\_on;\
否則\
FallofRefl = （1-max（（（1-dot（pointToCameraDirWS/（-KFs），累積NormalWS）），0））\&#42;KF\_on;

如果 （KF\_on == 0）\
FallofRefl=1.0;

vec3 Ambiant\_final = diffuseColor.rgb\&#42;AmbiColor;

// ------------------------------------------\
vec3 emissive = texture2D（emissiveMap，uv）.xyz;

VEC3 Finalcolor = 環境音_final\
+ specularColor\&#42;specContrib\
+ diffuseColor.rgb\&#42;diffContrib\
+ （reflColor\&#42;specularColor\&#42;FallofRefl）\
+ 發射;

最終色彩\
vec4 finalColor4 = vec4（finalcolor， texture2D（opacityMap，uv））;

gl\_FragColor = finalColor4;\
}

### GLSLFX 檔案

glslfx 檔案定義了兩種渲染幾何體的技術：

* 其中一種是硬體鑲嵌技術
* 另一種是基於視差效應，當使用者硬體不支援拼接時，會用作備用方案。

位於 .\tessellation\_parallax\fs.glsl

內容：

```
<?xml version="1.0" encoding="UTF-8"?>

<!DOCTYPE sbsbatchnode SYSTEM "glslfx.dtd">

<glslfx version="1.0.0" author="allegorithmic.com">



    <!-- TECHNIQUES -->

    <technique name="Tesselation">

        <!-- PROPERTIES -->

        <property name="blend_enabled" value="true"/>

        <property name="blend_func" value="src_alpha,one_minus_src_alpha"/>

        <property name="cull_face_enabled" value="true"/>

        <property name="cull_face_mode" value="back"/>



        <!-- SHADERS -->

        <shader type="vertex" filename="tessellation_parallax/tessellation/vs.glsl" primitiveType="patch4"/>

        <shader type="tess_control" filename="tessellation_parallax/tessellation/tcs.glsl"/>

        <shader type="tess_eval" filename="tessellation_parallax/tessellation/tes.glsl"/>

        <shader type="fragment" filename="tessellation_parallax/fs.glsl"/>



        <!-- UNIFORMS -->

        <uniform name="parallax_mode" guiName="Parallax Mode" min="0" max="0" />

        <uniform name="enableTilingInFS" guiName="Tiling Enabled In FS" min="0" max="0" />

        <uniform name="tessellationFactor" guiName="Tessellation Factor" default="4" min="1" max="64" guiStep="1" guiWidget="slider"/>

    </technique>



    <technique name="Parallax">

        <!-- PROPERTIES -->

        <property name="blend_enabled" value="true"/>

        <property name="blend_func" value="src_alpha,one_minus_src_alpha"/>

        <property name="cull_face_enabled" value="true"/>

        <property name="cull_face_mode" value="back"/>



        <!-- SHADERS -->

        <shader type="vertex" filename="tessellation_parallax/parallax/vs.glsl"/>

        <shader type="fragment" filename="tessellation_parallax/fs.glsl"/>



        <!-- UNIFORMS -->

        <uniform name="parallax_mode" guiName="Parallax Mode" min="1" max="1" />

        <uniform name="enableTilingInFS" guiName="Tiling Enabled In FS" min="1" max="1" />



    </technique>



    <!-- INPUT VERTEX FORMAT -->

    <vertexformat name="iVS_Position" semantic="position"/>

    <vertexformat name="iVS_Normal" semantic="normal"/>

    <vertexformat name="iVS_UV" semantic="texcoord0"/>

    <vertexformat name="iVS_Tangent" semantic="tangent0"/>

    <vertexformat name="iVS_Binormal" semantic="binormal0"/>



    <!-- SAMPLERS -->

    <sampler name="diffuseMap" usage="diffuse"/>

    <sampler name="heightMap" usage="height"/>

    <sampler name="normalMap" usage="normal"/>

    <sampler name="detailNormalMap" usage="detailNormal"/>

    <sampler name="emissiveMap" usage="emissive"/>

    <sampler name="specularMap" usage="specular"/>

    <sampler name="opacityMap" usage="opacity"/>

    <sampler name="environmentMap" usage="environment"/>



    <!-- MATRICES -->

    <uniform name="worldMatrix" semantic="world"/>

    <uniform name="worldViewProjMatrix" semantic="worldviewprojection"/>

    <uniform name="worldViewMatrix" semantic="worldview"/>

    <uniform name="worldInverseTransposeMatrix" semantic="worldinversetranspose"/>

    <uniform name="viewInverseMatrix" semantic="viewinverse"/>

    <uniform name="modelViewMatrix" semantic="modelview"/>

    <uniform name="projectionMatrix" semantic="projection"/>



    <!-- SCENE PARAMETERS -->

    <uniform name="AmbiColor" semantic="ambient"/>

    <uniform name="Lamp0Pos" semantic="lightposition0"/>

    <uniform name="Lamp0Color" semantic="lightcolor0"/>

    <uniform name="Lamp1Pos" semantic="lightposition1"/>

    <uniform name="Lamp1Color" semantic="lightcolor1"/>



    <!-- UNIFORMS -->

    <uniform name="tiling" guiName="Tiling" default="1" min="1" guiWidget="slider" guiMax="10"/>

    <uniform name="heightMapScale" guiGroup="Height" guiName="Scale" default="1" min="0" guiWidget="slider" guiMin="-50" guiMax="50" />

    <uniform name="TilingDetail" guiGroup="Detail Normal" guiName="Tiling" default="3" min="1" guiWidget="slider" guiMax="10"/>

    <uniform name="Depth_detail" guiGroup="Detail Normal" guiName="Intensity" default="0.5" min="0" max="1" guiStep="0.05" guiWidget="slider"/>

    <uniform name="SpecExpon" guiGroup="Specular" guiName="Power" default="50" min="1" guiWidget="slider" guiMax="128"/>

    <uniform name="Ks" guiGroup="Specular" guiName="Intensity" default="1" min="0" guiWidget="slider" guiMax="3"/>

    <uniform name="Kr" guiGroup="Reflection" guiName="Intensity" default="0.5" min="0" max="1" guiStep="0.01" guiWidget="slider"/>

    <uniform name="KF_on" guiGroup="Reflection" guiName="Falloff" default="1" min="0" max="1" guiStep="1" guiWidget="slider"/>

    <uniform name="KFs" guiGroup="Reflection" guiName="Falloff Size" default="1" min="-1" max="1" guiStep="0.05" guiWidget="slider"/>



</glslfx>
```
