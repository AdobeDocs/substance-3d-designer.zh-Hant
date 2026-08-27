---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-mapper-grayscale.html"
breadcrumb-title: ''
description: 使用 Spline Mapper Grayscale 節點，將灰階材質沿著樣條路徑映射，並可自訂參數。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Mapper Grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 樣條映射器灰階
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '1109'
ht-degree: 0%

---


# 樣條映射器灰階

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![節點圖示](../../../../../../assets/spline-mapper-grayscale-icon.png "節點圖示")

<b>收錄於：</b> 樣條與路徑工具 > 樣條鍵工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

將輸入的灰階影像映射到沿輸入樣條線拉伸的原始圖形上。

原始形狀可以是平面、半圓柱或圓柱。 圓柱可沿樣條扭轉，以相應地變形映射影像。

</td>
</tr>
</table>

節點會輸出映射影像為灰階影像，並提供高度、UV（即影像座標）及獨立選擇每個映射樣條的 ID 遮罩等資訊。

>[!IMPORTANT]
>
> 使用非常低厚度值時，結果可能會在樣條包絡外出現不想要的雜訊。 這是已知的問題。

>[!NOTE]
>
> 另 [見樣條映射器顏色](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-mapper-color/spline-mapper-color.md)。

## 輸入連接器

<b>樣條座標</b> *色彩*&#x200B;輸入樣條點的座標編碼在彩色影像的 RGBA 通道中：\
<b>    R</b> - X 位置\
<b>    G</b> - Y 位置\
<b>    B</b> - 身高\
<b>A</b> - 打包資料：\
* 符號：樣條鍵為閉（負）或開（正）;\
* 絕對值：厚度 + 1。

<b>樣條資料</b> *色彩*&#x200B;輸入樣條的額外資料編碼於彩色影像的 RGBA 通道中。\
<b>    R</b> - 切線 X\
<b>    G</b> - 切線 Y\
<b>    B</b> - 未上場\
<b>    A</b> - 未上場

<b>樣條量</b> *整數*：輸入樣條的數量。

<b>色彩地圖</b> *灰階*&#x200B;輸入灰階影像應該沿著輸入樣條線映射。

<b>高度圖</b> *灰階*&#x200B;輸入的灰階高度圖應該沿著輸入樣條映射。

<b>扭轉曲線</b> *灰階*&#x200B;描述曲線的影像，使用第一排像素的值。\
當 <b>Shape</b> 參數設為 *半圓柱* 或 *半圓柱*&#x200B;時，這個輸入用來控制 UV 在形狀周圍的扭轉。 其影響由 Twist UV 的曲線乘法</b>參數控制<b>。\
曲線提供沿樣條曲線的旋轉量輪廓，列中的第一個像素是樣條曲線起始的旋轉，最後一個像素是末端的旋轉。 灰階值代表彎道數。\
你可以用 [Curve](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/curve/curve.md) 節點來撰寫曲線。

## 輸出連接器

<b>顏色</b> *灰階*&#x200B;將輸入彩色影像映射到輸入樣條線後，作為灰階影像。

<b>高度</b> *灰階*&#x200B;將輸入高度影像映射到輸入樣條曲線上的結果，作為灰階影像。

<b>紫外線</b> *色彩*&#x200B;將映射在輸入樣條上的 UV（即座標），編碼成彩色影像。

<b>身分證</b> *灰階*&#x200B;一種沿輸入樣條線映射的影像遮罩，白色值從一個樣條線遞增 1 次，讓每個形狀可以獨立選擇。

## 參數

<b>分段數量</b> *整數*&#x200B;樣條在影像座標穿越前會被簡化為段。\
線段越多，曲線上的映射就越平滑。

<b>自動縮放 UV</b> *布林*：自動調整座標的縮放，使在沿樣條線映射時仍呈現方形影像。<b></b>

<b>紫外線尺度</b> *Float2*&#x200B;調整映射座標的比例尺，X（水平）和Y（垂直）。\
數值越高，影像拼貼越密集。<b></b>

<b>模式</b> *整數*&#x200B;選擇影像應映射的樣條的方法：\
*- 繪製樣條表*：輸入列表中的所有樣條線都會被使用;\
*- 繪製單樣條曲線*：僅使用指定索引的樣條曲線;\
*- 繪製樣條範圍*：僅使用包含在指定範圍內的樣條。

<b>繪製樣條指數</b> *整數* （當「模式」設為「繪製單樣條線」時可用）影像應依照的樣條曲線索引。

<b>拉取樣條範圍</b> *Integer2* （當「模式」設為「繪製樣條範圍」時可用）影像應沿用的樣條索引範圍。

<b>開始</b> *浮點*&#x200B;偏移是樣條線中應該映射的部分起始位置。\
該值代表樣條的正規化長度。

<b>結束</b> *浮點*&#x200B;偏移是樣條曲線末端，該部分應該被映射。\
該值代表樣條的正規化長度。

<b>厚度模式</b> *整數*&#x200B;設定映射影像厚度的方法：\
*- 手動*：以任意值明確設定厚度;\
*- 從樣條鍵*：使用樣鍵的厚度。

<b>厚度</b> *浮動* （當「厚度模式」設為「手動」時可用）映射影像在樣條線上的任意厚度值。<b></b>

<b>厚度倍增器</b> *浮點* （當「厚度模式」設為「從樣條鍵」時可用）一種全域乘法器，表示映射影像沿樣條曲線的厚度，當該厚度由樣條曲線的厚度驅動時。

<b>形狀</b> *整數*&#x200B;用於將影像座標映射到樣條曲線的原始形狀：\
*- 平面*：座標映射到平面;\
*- 半圓柱*：座標映射到底圓軸沿樣條方向的半圓柱;\
*- 圓柱*：座標映射到一個底圓軸沿樣條方向的圓柱。<b></b>

<b>汽缸高度倍增器</b> *浮點* （當「形狀」設定為「半圓柱」或「圓柱」時可用）為高度輸出中柱體高度貢獻強度的倍數。\
高度調整是累積的。

<b>汽缸高度偏移</b> *浮動* （當「形狀」設定為「半圓柱」或「圓柱」時可用）\
將圓柱形或半圓柱形狀輪廓的中心從花鍵表面偏移到表面下方一個直徑處。

<b>扭曲紫外線強度</b> *浮動* （當「形狀」設定為「半圓柱」或「圓柱」時可用）影像座標繞圓柱旋轉，以旋轉數計算。\
扭轉是指僅旋轉花鍵末端的圓柱。 接著沿著樣條線插值旋轉。

<b>扭曲 UV 曲線倍數</b> *浮動* （當「形狀」設定為「半圓柱」或「圓柱」時可用）扭轉曲線輸入對圓柱扭轉貢獻強度的乘數。\
曲線提供沿樣條曲線的旋轉量輪廓，列中的第一個像素是樣條曲線起始的旋轉，最後一個像素是末端的旋轉。 灰階值代表彎道數。

<b>扭曲 UV 曲線偏移</b> *浮動* （當「形狀」設定為「半圓柱」或「圓柱」時可用）對扭轉曲線提供的旋轉值套用全局偏移，以轉數為單位。

<b>花鍵高度倍數</b> *浮動*&#x200B;調整花鍵高度輸入對高度輸出的強度。\
高度調整是累積的。<b></b>

<b>輸入高度倍增器</b> *浮點*&#x200B;調整高度圖輸入對高度輸出的強度。\
高度調整是累積的。

<b>非正方修正&#x200B;</b>*布林*：調整點的位置與厚度，以在非正方形解析度下保留樣條形狀。\
這也影響均勻分布。

## 範例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineMapperColor-Variant1-Before.jpg" alt="SplineMapperColor-Variant1-Before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineMapperGrayscale-Variant1-After.jpg" alt="SplineMapper灰階變體1-之後">
      <br><i>之後</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![節點範例 2](../../../../../../assets/SplineMapperGrayscale-Demo.gif "節點範例 2")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![節點範例 3](../../../../../../assets/SplineMapperGrayscale-Variant1-After1.jpg "節點範例 3")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
