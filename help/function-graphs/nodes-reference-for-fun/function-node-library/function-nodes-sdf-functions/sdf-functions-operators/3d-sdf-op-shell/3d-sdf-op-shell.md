---
title: 殼牌
description: Designer > Substance 合成圖 > Nodes 參考 Node 函式庫>> SDF 函式> Operator > Shell 的 Substance 合成圖
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 1%

---


# 殼牌

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![殼牌標誌](./3d-sdf-op-shell.png "殼牌")

<b>收錄於：</b> SDF 函數>運算元

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

使 SDF 形狀中空，厚度可調整以適應包絡。

</td>
</tr>
</table>

<a name='inputs'></a>

>[!INFO]
> 
> 欲了解更多涉及 SDF 函數的概念與工作流程，請前往專門頁面： [使用 SDF 函數](../../working-with-sdf-functions.md)

## 輸入

|  |  |
| :--- | :--- |
| <b>SDF</b> *浮標* | 輸入的 SDF 形狀。 |
| <b>厚度</b> *浮標* | 外殼的厚度，同時向內和向外施加。<br>厚度增加時，外殼會變圓。<br><br><i>預設值：0.02</i> |
