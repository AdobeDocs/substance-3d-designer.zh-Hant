---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/scripting/debugging-plugins-using-visual-studio-code.html"
breadcrumb-title: ''
description: 學習如何使用 Visual Studio Code 除錯 Substance 3D Designer 的 Python 外掛，以提升開發效率。
helpx_creative_field: ""
helpx_description: Designer > Scripting > Debugging plugins using Visual Studio Code
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 使用 Visual Studio Code 除錯外掛
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 0%

---


# 使用 Visual Studio Code 除錯外掛

作為許多開發者的工作流程標準， **Visual Studio Code IDE** 可用於除錯 Python 外掛。

>[!WARNING]
>
> <b>debugpy.listen（）</b> 方法可允許任何能連接指定埠的人在除錯程序中執行任意程式碼。
> 
> 因此，除錯應&#x200B;*<b>僅在安全網路*&#x200B;上設置與執行&#x200B;*</b>*。

為了建立 Visual Studio Code 與 Substance 3D Designer 之間的協同效應，請遵循以下步驟：

1. 安裝 **[Visual Studio Code**](https://code.visualstudio.com/) 和 **[Python 擴充功能](https://marketplace.visualstudio.com/items?itemName=ms-python.python)**。
1. 安裝 **[除錯 Python 模組](https://github.com/microsoft/debugpy)**。

   >[!NOTE]
   >
   > 確保 Designer 裡的 Python 直譯器能找到「*debugpy*」模組。 最簡單的方法是將「除錯&#x200B;*」模組所在*&#x200B;的目錄加入 **PYTHONPATH** 環境變數。另一個方法是修改腳本中的 sys.path，加入除錯模組的路徑。
1. 啟動應用程式，開啟 Python 編輯器並 **執行以下程式碼**：

   ```
   import sys 
   
   
   
   debugpy_path = '/path/to/debugpy/module' 
   
   debugpy_port = 5678 
   
   designer_py_interpreter = '/path/to/python/executable/bundled/in/designer' 
   
   
   
   if not debugpy_path in sys.path: 
   
       sys.path.append(debugpy_path) 
   
   
   
   import debugpy 
   
   
   
   debugpy.configure(python=designer_py_interpreter) 
   
   debugpy.listen(debugpy_port)
   ```

1. 在 Visual Studio Code 中，打開你的專案並建立一個 **launch.json** 檔案。 在檔案中新增以下內容：

   ```
   { 
   
       "name": "Attach to Designer", 
   
       "type": "python", 
   
       "request": "attach", 
   
       "port": <port number used in the script above>, 
   
       "host": "127.0.0.1" 
   
   }
   ```

1. 點擊 <b>除錯</b> 圖示，必要時建立或編輯除錯器設定。
1. 選擇 **Python：附加到 Designer** 設定，然後點選 **開始除錯**。

   你現在應該能設定斷點、逐步執行程式碼，並使用 Visual Studio Code 除錯器的所有其他功能。
