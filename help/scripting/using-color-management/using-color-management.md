---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/scripting/using-color-management.html"
breadcrumb-title: ''
description: 學習如何使用 Substance 3D Designer Python 腳本中的色彩管理功能來獲得準確的色彩。
helpx_creative_field: ""
helpx_description: Designer > Scripting > Using color management
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 使用色彩管理
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 0%

---


# 使用色彩管理

<b> SDColorManagementEngine </b>類別可從 <b>SDApplication</b> 類別存取，包含目前色彩管理設定&#x200B;*的*&#x200B;資訊。

## 存取與查詢色彩管理引擎

```
import sd 

 

ctx = sd.getContext() 

app = ctx.getSDApplication() 

 

## Access the color management engine.

cm = app.getColorManagementEngine() 

 

## Currently getName can return "legacy", "ace" or "ocio"

## depending on the color management settings in the preferences.

cmName = cm.getName()  

print(cmName) 

 

print(cm.getWorkingColorSpaceName()) 

print(cm.getRawColorSpaceName()) 

 

if cmName == "ocio": 

## If OpenColorIO is enabled, print the config file name.

    print(cm.getOCIOConfigFileName()) 

 

## List all color spaces.

colorSpaces = cm.getColorSpaces() 

for cs in colorSpaces: 

    print(cs.get())
```


此外，也可以 *從 Python 為點陣資源指派色彩空間* 。

### 點陣圖資源的色彩空間設定

```
import sd 

import sd 

from sd.api.sdproperty import * 

from sd.api.sdresourcebitmap import SDResourceBitmap 

from sd.api.sdvaluestring import SDValueString 

from sd.api.sdvaluebool import SDValueBool 

 

ctx = sd.getContext() 

app = ctx.getSDApplication() 

pkgMgr = app.getPackageMgr() 

cm = app.getColorManagementEngine() 

 

colorSpaces = cm.getColorSpaces() 

 

## Get all the resources in the first package.

pkg = pkgMgr.getPackages()[0] 

resources = pkg.getChildrenResources(isRecursive=True) 

 

for res in resources: 

 if isinstance(res, SDResourceBitmap): 

  props = res.getProperties(SDPropertyCategory.Annotation) 

 

## Print the current color space for the resource.

  p0 = res.getPropertyFromId("bitmap_color_space", SDPropertyCategory.Annotation) 

  cs = res.getAnnotationPropertyValueFromId("bitmap_color_space") 

  print(cs.get()) 

 

## Print the current premultiplied alpha setting for the resource.

  p1 = res.getPropertyFromId("bitmap_premultiplied_alpha", SDPropertyCategory.Annotation) 

  cs = res.getAnnotationPropertyValueFromId("bitmap_premultiplied_alpha") 

  print(cs.get()) 

 

## Assign new values for the color space and premultiplied alpha properties.

  res.setPropertyValue(p0, colorSpaces[2]) 

  res.setPropertyValue(p1, SDValueBool.sNew(False))
```


## 撰寫帶有色彩空間轉換的 SDTexture

**SDTexture** 類別的 **save** 方法現在接受可選&#x200B;**的 outputColorSpace** 參數。指定後，色彩空間轉換會在儲存影像&#x200B;*前進行*。

若色彩管理模式支援嵌入的 ICC 設定檔 *，且* 目標檔案格式也支援，則色彩空間的 ICC 配置檔會嵌入 *於產生的影像檔案*&#x200B;中。
