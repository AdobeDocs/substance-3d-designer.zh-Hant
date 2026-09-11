---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/mlv-grayscale.html"
breadcrumb-title: ''
description: 使用 MLV 灰階模糊濾鏡，將動態模糊效果套用到灰階材質上，營造動態效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > MLV grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: MLV 灰階
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5efb14d81ad72b1982785319e446d7eb318c9a03
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 1%

---


# MLV 灰階

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![MLV 灰階：圖示](mlv-grayscale.resources/MLV_Grayscale_Icon.png "MLV 灰階：圖示")

<b>收錄於：</b> 模糊>濾鏡

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

MLV 代表<b>「最小變異數均值」（Mean of Least Variance）。</b>這個濾鏡能強化影像的邊緣並平滑雜訊。

濾鏡會尋找影像中的結構區域，並利用這些區域來銳化和壓平影像。 在某些情況下，這可能導致梯度上的階梯比結構區域更寬。

</td>
</tr>
</table>

>[!NOTE]
>
> 另 [見MLV色彩](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/mlv-color/mlv-color.md)。

<a name="inputs"></a>

## 輸入

|  |  |
|:---|:---|
| <b>輸入</b> <i>灰階</i> | 應該處理的灰階影像。 |

<a name="outputs"></a>

## 輸出

|  |  |
|:---|:---|
| <b>產出</b> <i>灰階</i> | 濾鏡灰階影像。 |

<a name="parameters"></a>

## 參數

|  |  |
|:---|:---|
| <b>強度</b> *浮標* | 濾波強度施加在影像上。<br><br>較高的數值會使細節和雜訊更平滑，並延伸到較平坦的區域。 |
| <b>平滑度</b> *浮標* | 對結構區域施加的平滑強度，使區域變得更圓潤，並減少在較高過濾強度下可能出現的階梯效應。 |
| <b>標準</b> *整數* | 用來選擇定義影像結構區域的數值的準則。<br><br>換句話說，像素應該 *被分組* 成應該平滑的區域。<br><br>*- 變異數：* 選擇平均數周圍散佈最低的值，導致像素群彼此相似&#x200B;<br>*- 變異係數：* 在考慮平均值的同時選擇數值，導致較亮區域的變異較小，反向減少 |
| <b>高斯分布</b> *布林值* | 使用高斯分布來將像素分組成結構區域。<br><br>當「True」時，會讓區域更平滑，且扁平效果會減少。 |
| <b>迭代</b> *整數* | 過濾執行次數，每次迭代都套用在前一次的結果上。<br><br>更多迭代會產生更平坦且銳利的結構區域。 |

## 範例

<table>
  <tr>
    <td>
      <img src="mlv-grayscale.resources/MLV_Variant1A.png" alt="MLV_Variant1A">
      <br><i>之前</i>
    </td>
    <td>
      <img src="mlv-grayscale.resources/MLV_Variant1B.png" alt="MLV_Variant1B">
      <br><i>之後</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="mlv-grayscale.resources/MLV_Variant2A.png" alt="MLV_Variant2A">
      <br><i>之前</i>
    </td>
    <td>
      <img src="mlv-grayscale.resources/MLV_Variant2B.png" alt="MLV_Variant2B">
      <br><i>之後</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="mlv-grayscale.resources/MLV_Variant2A.png" alt="MLV_Variant2A">
      <br><i>之前</i>
    </td>
    <td>
      <img src="mlv-grayscale.resources/MLV_Variant2C.png" alt="MLV_Variant2C">
      <br><i>之後</i>
    </td>
  </tr>
</table>
