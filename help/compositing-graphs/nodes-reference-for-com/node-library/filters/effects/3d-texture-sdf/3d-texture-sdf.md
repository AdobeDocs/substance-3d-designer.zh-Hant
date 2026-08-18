---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/3d-texture-sdf.html"
breadcrumb-title: ''
description: 使用 3D Texture SDF 節點，從 3D 資料產生有符號距離場紋理，以創造平滑的形狀與效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > 3D Texture SDF
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D 貼圖 SDF
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 2%

---


# 3D 貼圖 SDF

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesdf.png){width="200px"}

**收錄於：***濾波器/效果*

**很簡單**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## 說明

**3D Texture SDF** 節點會&#x200B;*從&#x200B;**輸入**&#x200B;的* 3D 材質&#x200B;*遮罩（代表形狀*&#x200B;體積&#x200B;*的切片）產生形狀的有符號距離場*。

</td>
</tr>
</table>

## 參數

### 輸入

* **遮罩輸入***灰階*\
  *3D 材質*&#x200B;遮罩代表形狀&#x200B;*體積*&#x200B;的切片。

### 參數

* **閾值***浮點*\
  當形狀體積以漸變梯度描述&#x200B;*時，會*&#x200B;設定形狀表面被&#x200B;*偵測到**的梯度*&#x200B;值。
* **輸出***整數*\
  應輸出的距離場類型：
  * *距離場*：輸出描述形狀外&#x200B;*距離*&#x200B;的距離場。
  * *有符號距離場*：輸出一個描述形狀外部&#x200B;*（正）與*&#x200B;內部&#x200B;*（負）距離*&#x200B;的距離場。

## 範例圖片

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesdf-variant.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesdf-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesdf-node.png){width="256px"}

</td>
</tr>
</table>
