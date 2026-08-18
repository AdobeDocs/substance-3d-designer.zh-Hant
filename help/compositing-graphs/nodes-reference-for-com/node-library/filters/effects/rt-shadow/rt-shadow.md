---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/rt-shadow.html"
breadcrumb-title: ''
description: 使用 RT Shadows 節點從幾何體中即時計算陰影資訊，以創造動態光影效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > RT Shadows
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: RT 陰影
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 0%

---


# RT 陰影

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![RT Shadows 節點圖示](../../../../../../assets/rt-shadow.png "RT Shadows 節點圖示")

<b>收錄於：</b> *濾鏡/效果*

</td>
<td width="58.30%" style="border: 0;" valign="top">

## 說明

從高度圖輸入產生光線追蹤陰影。

由於計算時間，此節點不應與 CPU（SSE）引擎搭配使用。

</td>
</tr>
</table>

## 參數

<b>取樣</b> *整數*\
計算陰影所用的光線數量。\
較高的數值能提供更平滑且精確的結果，但代價是性能下降。

<b>模態</b> *整數*\
畫出表面陰影的方法。

<b>身高比例</b> *浮車*\
輸入高度圖強度的乘數。

<b>燈光位置 </b>*浮點2*\
光源在包圍表面的球體上的位置：
* <b>X</b>：水平位置，以轉數表示;
* <b>Y</b>：垂直位置，0.5為天頂，0/1為地平線。

<b>光強</b> *浮球*\
光源的強度。

<b>光線尺寸</b> *Float2*（模式設&#x200B;*為陰影*&#x200B;時<b></b>可用）\
光源的大小是長方形。

<b>光線比例（柔和陰影）</b> *浮標*\
光線</b>大小對光線方向的貢獻<b>是乘數。\
較高的陰影會更平滑。

<b>讓光明在地平線上</b> *布林值*\
如果 <b>光線位置</b> 設定為將光線置於地平線以下，這個參數會防止光線越過該門檻，意即 Y 值會被限制在 [0;1] 範圍。

<b>陰影不透明度</b> *浮動器*\
是陰影不透明度的倍數。

<b>影子衰減</b> *浮球*\
這是影子越遠離施法者，影子衰減的倍數。\
值為 0 則陰影均勻（柔和陰影仍會生效）。

<b>Max Shadows 長度</b> *浮球*\
影子從施法者能拉出的最大距離。\
值為 0 則不會有可見的陰影。

## 範例圖片

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![RT Shadows 節點 - 範例 1](../../../../../../assets/RTShadows-01.jpg "RT Shadows 節點 - 範例 1")

</td>
<td style="border: 0;" valign="top">

![RT Shadows 節點 - 範例 2](../../../../../../assets/RTShadows-02.jpg "RT Shadows 節點 - 範例 2")

</td>
<td style="border: 0;" valign="top">

![RT Shadows 節點 - 範例 3](../../../../../../assets/RTShadows-03.jpg "RT Shadows 節點 - 範例 3")

</td>
</tr>
</table>
