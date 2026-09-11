---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/scripting/application-callbacks.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Designer Python 外掛中使用應用程式回調來回應應用程式事件。
helpx_creative_field: ""
helpx_description: Designer > Scripting > Application callbacks
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 應用程式回撥
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 0%

---


# 應用程式回撥

你可以在特定事件發生時，向應用程式物件註冊 <b>Python 回調</b> 。

使用者介面物件，如選單和按鈕，可使用 <b>Qt for Python</b> 函式庫觸發回調。 欲了解更多資訊，請參閱 [建立使用者介面元素](../../scripting/creating-user-interface/creating-user-interface-elements.md)。

```
import sd 

 

## Our callbacks.

def onBeforeFileLoadedCallback(filePath): 

    print("Before file loaded, file: %s" % filePath) 

 

def onAfterFileLoadedCallback(filePath, succeed, updated): 

    print("After file loaded, file: %s, succeed: %s, updated: %s" % (filePath, succeed, updated)) 

     

def onBeforeFileSavedCallback(filePath, parentPackagePath): 

    print("Before file saved, file: %s, parentPackage: %s" % (filePath, parentPackagePath)) 

 

def onAfterFileSavedCallback(filePath, succeed): 

    print("After file saved, file: %s, succeed: %s" % (filePath, succeed)) 

 

## Get the application.

app = sd.getContext().getSDApplication() 

 

## Register our callbacks.

beforeFileLoadedCallbackID = app.registerBeforeFileLoadedCallback(onBeforeFileLoadedCallback) 

afterFileLoadedCallbackID = app.registerAfterFileLoadedCallback(onAfterFileLoadedCallback) 

beforeFileSavedCallbackID = app.registerBeforeFileSavedCallback(onBeforeFileSavedCallback) 

afterFileSavedCallbackID = app.registerAfterFileSavedCallback(onAfterFileSavedCallback) 

 

## Unregister callbacks when no longer needed.

app.unregisterCallback(beforeFileLoadedCallbackID) 

app.unregisterCallback(afterFileLoadedCallbackID) 

app.unregisterCallback(beforeFileSavedCallbackID) 

app.unregisterCallback(afterFileSavedCallbackID)
```
