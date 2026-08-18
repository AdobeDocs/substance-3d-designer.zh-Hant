---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/3d-view/switching-your-shaders-to-opengl-core-profile.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Designer 3D 視圖中切換到 OpenGL 核心設定檔，以提升相容性與效能。
helpx_creative_field: ""
helpx_description: Designer > Interface > 3D View > Switching your shaders to OpenGL Core Profile
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 將你的著色器切換到 OpenGL 核心設定檔
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 0%

---


# 將你的著色器切換到 OpenGL 核心設定檔

自 2018.2.0 版本起，3D 視口使用 OpenGL 核心配置檔。\
這次，我們將應用程式提供的部分著色器從 GLSL 版本 120 更新到 GLSL 版本 330。

你可能想更新自己的著色器，以利用新的 GLSL 函式，或是讓你的 GLSL 程式碼更現代化。 請注意，在 MacOS 上，舊的著色器可能已經無法使用。\
若想完整了解新功能，我們強烈建議您閱讀官方 OpenGL 文件。 你可以看看 [OpenGL 著色語言規範 3.30](https://www.khronos.org/registry/OpenGL/specs/gl/GLSLangSpec.3.30.pdf)。\
否則，這裡有一份快速指南，可以幫助你將 GLSL 1.20 著色器轉換成 GLSL 3.30：

## 更新版本號

首先，將你之前的 `#version` 指令 `#version 330`替換（或如果還沒有的話，可以加到檔案頂端）。

### 把你的「屬性」和「變化」換成「內」或「外」

現在， `attribute` `varying` 變數會根據著色器階段明確宣告為 `in` 或 `out` 是：

在頂點著色器中， `attribute`頂點的 s 被宣告為 `in`，而 `varying`要傳遞給片段著色器的 s 則宣告為 `out`。\
例如：

```
## version 120



attribute vec3 vertexPosition;

attribute vec3 vertexNormal;

attribute vec2 vertexUV;



varying vec3 fragmentNormal;

varying vec2 fragmentUV;
```


變成：

```
## version 330



in vec3 vertexPosition;

in vec3 vertexNormal;

in vec2 vertexUV;



out vec3 fragmentNormal;

out vec2 fragmentUV;
```


同樣地，在 fragment shader 中，變化也成為了 in。 你也應該宣告一個 out 變數，取代 gl\_FracColor（這已經不再內建）：

```
## version 120



varying vec3 fragmentNormal;

varying vec2 fragmentUV;



void main() {

...

gl_FragColor = vec4(myColor.rgb, 1.0);

}
```


變成：

```
## version 330



in vec3 fragmentNormal;

in vec2 fragmentUV;



out vec4 outColor; //you could choose any name you want here



void main() {

...

outColor = vec4(myColor.rgb, 1.0);

}
```


### 使用新的材質查詢函式

在新版本的著色語言中，材質查詢 API 既簡化又增強。

， `texture1D()`&#x200B;`texture2D()`， `texture3D()`， 與`textureCube()`函數皆成為 的`texture()`過載。\
同理，變為 `textureLod()`， `texture2DGrad()` `textureGrad()`變，`texture2DLod()`依此類推。

你現在也能使用有用的功能，例如 `textureSize()` （查詢取樣器以 texel 計算大小）、 `textureOffset()` （取樣目標位置的鄰居）、 `textureFetch()` （提供像素取樣位置）等等。
