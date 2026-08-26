---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/scripting/using-spot-colors.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Designer Python 腳本中使用專色，以處理專門的色彩工作流程。
helpx_creative_field: ""
helpx_description: Designer > Scripting > Using spot colors
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 使用專色
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 0%

---


# 使用專色

<b> SDSpotColorLibrary </b>類別可從 <b>SDApplication</b> 類別存取，包含 Designer 中包含的專色函式庫資訊。

利用此類別，可以列出色彩書和專色，並找到特定專色或最接近特定 RGB 色的專色。

使用 <b>OpenColorIO</b> 時，Designer 中無法使用&#x200B;**&#x200B;專色。此時，app.getSpotColorLibrary（） 會回傳 <b>None</b>。

>[!IMPORTANT]
>
> 使用 <b>OpenColorIO</b> 時，Designer 中無法使用&#x200B;**&#x200B;專色。此時，app.getSpotColorLibrary（） 會回傳 <b>None</b>。

```
import sd 

 

ctx = sd.getContext() 

app = ctx.getSDApplication() 

spotLib = app.getSpotColorLibrary() 

 

## Find a color by color book and color name.

col = spotLib.findSpotColorByName( 

    spotColorBookName="PANTONE+ Solid Coated", 

    spotColorName="PANTONE Yellow 012 C" 

) 

 

print(col) 

print(col.get()) 

 

print(spotLib.getSpotColorBookName(col)) 

print(spotLib.getSpotColorName(col)) 

 

## Find the closest spot color in a specific book, to an RGB color.

## The RGB color is specified in the working color space currently used by Designer.

col = spotLib.findClosestSpotColor( 

    spotColorBookName="PANTONE+ Solid Coated", 

    r=88 / 255.0, 

    g=132 / 255.0, 

    b=167 / 255.0 

) 

 

print(col) 

print(col.get()) 

print(spotLib.getSpotColorBookName(col)) 

print(spotLib.getSpotColorName(col))
```


專色可以從中擷取並設定到節點屬性中。

```
import sd 

from sd.api.sdbasetypes import * 

from sd.api.sdvaluecolorrgba import SDValueColorRGBA 

from sd.api.sdvaluespotcolor import SDValueSpotColor 

 

ctx = sd.getContext() 

app = ctx.getSDApplication() 

uiMgr = app.getUIMgr() 

spotLib = app.getSpotColorLibrary() 

 

node = uiMgr.getCurrentGraphSelection()[0] 

 

## Set RGBA color in node property.

rgbaColor = SDValueColorRGBA.sNew(ColorRGBA(0.7, 0.5, 0.2, 1)) 

node.setInputPropertyValueFromId("outputcolor", rgbaColor) 

 

## Set spot color in node property.

spotColor = spotLib.findSpotColorByName( 

    spotColorBookName="PANTONE+ Solid Coated", 

    spotColorName="PANTONE Yellow 012 C" 

) 

node.setInputPropertyValueFromId("outputcolor", spotColor) 

 

## Get color from node property (could be a SDValueColorRGBA or a SDValueSpotColor)

anyColor = node.getInputPropertyValueFromId("outputcolor") 

 

## Print the RGBA components of the color.

print(anyColor.get()) 

 

## Check if the color is a spot color.

if isinstance(anyColor, SDValueSpotColor): 

## Print the spot color information of the color.

    print(spotLib.getSpotColorBookName(anyColor)) 

    print(spotLib.getSpotColorName(anyColor)) 

 
```
