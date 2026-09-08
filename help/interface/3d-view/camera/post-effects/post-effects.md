---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/interface/3d-view/camera/post-effects.html"
breadcrumb-title: ''
description: 對 3D 視角相機套用後製效果，以增強材質預覽與視覺化效果。
helpx_creative_field: ""
helpx_description: Designer > Interface > 3D view > Camera > Post effects
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 後續影響
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '732'
ht-degree: 2%

---


# 後續影響

![後期效果](../../../../assets/postEffects.png "後期效果"){zoomable="yes"}

在相機屬性中，你可以啟用後期特效來強化渲染效果或檢查特定材質屬性。

這些效果是內部開發的，僅提供給 Rasterizer 和 GPU Pathtracer [渲染器](../../../../interface/3d-view/3d-renderers/3d-renderers.md)使用。

在儲存 [3D 場景資源](../../../../resources/3d-scene-resource/3d-scene-resource.md) 或 [場景狀態檔案](../../../../working-with-3d-scenes/working-with-3d-scenes.md) 時啟用的任何後製效果，都會被保存為場景狀態的一部分。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## 色調對應

</td>
<td style="border: 0;" valign="top">

### 光暈

</td>
<td style="border: 0;" valign="top">

### 景深

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

## 色調對應

根據特定演算法和/或查找表（LUT）重新映射渲染的顏色。

這樣可以改善不同塗裝間的顏色一致性。 例如，Blender 中也有 AgX 色調映射器。

+++Reinhard


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="後FXDisabled（特製化）">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXReinhard.jpg" alt="FXReinhard 之後">
      <br><i>之後</i>
    </td>
  </tr>
</table>



![後特效可化後特](../../../../assets/PostFXDisabled.jpg "效可變")

![後FXReinhard](../../../../assets/PostFXReinhard.jpg "後特效Reinhard")

+++

+++阿坦


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="後FXDisabled（特製化）">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXAtan.jpg" alt="FXAtan 之後">
      <br><i>之後</i>
    </td>
  </tr>
</table>



![後特效可化後特](../../../../assets/PostFXDisabled.jpg "效可變")

![後FXAtan](../../../../assets/PostFXAtan.jpg "後FXAtan")

+++

+++經驗


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="後FXDisabled（特製化）">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXExp.jpg" alt="FXExp 後期">
      <br><i>之後</i>
    </td>
  </tr>
</table>



![後特效可化後特](../../../../assets/PostFXDisabled.jpg "效可變")

![後特效衍生](../../../../assets/PostFXExp.jpg "後")

+++

+++日誌


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="後FXDisabled（特製化）">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXLog.jpg" alt="離開FXLog後">
      <br><i>之後</i>
    </td>
  </tr>
</table>



![後特效可化後特](../../../../assets/PostFXDisabled.jpg "效可變")

![後FXLog](../../../../assets/PostFXLog.jpg "後FXLog")

+++

+++A牌


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="後FXDisabled（特製化）">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXAces.jpg" alt="FXAces 後期">
      <br><i>之後</i>
    </td>
  </tr>
</table>



![後特效可化後特](../../../../assets/PostFXDisabled.jpg "效可變")

![FX後 FX](../../../../assets/PostFXAces.jpg "後")

+++

+++海爾


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="後FXDisabled（特製化）">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXHejl.jpg" alt="FXHejl 之後">
      <br><i>之後</i>
    </td>
  </tr>
</table>



![後特效可化後特](../../../../assets/PostFXDisabled.jpg "效可變")

![後FXHejl](../../../../assets/PostFXHejl.jpg "後期 FX後")

+++

+++中性


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="後FXDisabled（特製化）">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXNeutral.jpg" alt="FX之後 紐特拉爾">
      <br><i>之後</i>
    </td>
  </tr>
</table>



![後特效可化後特](../../../../assets/PostFXDisabled.jpg "效可變")

![後FXNeutral](../../../../assets/PostFXNeutral.jpg "後期")

+++

+++AGX


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="後FXDisabled（特製化）">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXAgx.jpg" alt="FXAgx 之後">
      <br><i>之後</i>
    </td>
  </tr>
</table>



![後特效可化後特](../../../../assets/PostFXDisabled.jpg "效可變")

![FXAgx](../../../../assets/PostFXAgx.jpg "之後")

+++

+++PBR 中性線


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="後FXDisabled（特製化）">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXPbrNeutral.jpg" alt="之後FXPbrNeutral">
      <br><i>之後</i>
    </td>
  </tr>
</table>



![後特效可化後特](../../../../assets/PostFXDisabled.jpg "效可變")

![後FXPbr中立後FXPbr中立](../../../../assets/PostFXPbrNeutral.jpg "後")

+++

## 光暈

模擬鏡頭內光線邊緣從非常明亮區域向外散射到光線較少區域的效果。

此效果受場景光線、相機曝光及發光材料影響。

+++臨界值
亮度值，光暈應該能看到。

*左：1.0 / 右：4.0*



<table>
  <tr>
    <td>
      <img src="../../../../assets/bloomThreshold1.jpg" alt="bloomThreshold1">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../assets/bloomThreshold4.jpg" alt="bloomThreshold4">
      <br><i>之後</i>
    </td>
  </tr>
</table>



![bloomThreshold1](../../../../assets/bloomThreshold1.jpg "bloomThreshold1")

![bloomThreshold4](../../../../assets/bloomThreshold4.jpg "bloomThreshold4")

+++

+++衰減
蓬鬆衰減斜坡，值越低，布隆半徑越短。

*左：1.0 / 右：0.6*



<table>
  <tr>
    <td>
      <img src="../../../../assets/bloomFalloff1.jpg" alt="bloomFalloff1">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../assets/bloomFalloff0-6.jpg" alt="bloomFalloff0-6">
      <br><i>之後</i>
    </td>
  </tr>
</table>



![bloomFalloff1](../../../../assets/bloomFalloff1.jpg "bloomFalloff1")

![bloomFalloff0-6](../../../../assets/bloomFalloff0-6.jpg "bloomFalloff0-6")

+++

+++關卡
那綻放的強烈程度。 較高的光度會帶來更明亮、更明顯的光線條紋。

*左：8.0 / 右：2.0*



<table>
  <tr>
    <td>
      <img src="../../../../assets/bloomLevel8.jpg" alt="bloomLevel8">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../assets/bloomLevel2.jpg" alt="bloomLevel2">
      <br><i>之後</i>
    </td>
  </tr>
</table>



![bloomLevel8](../../../../assets/bloomLevel8.jpg "bloomLevel8")

![bloomLevel2](../../../../assets/bloomLevel2.jpg "bloomLevel2")

+++

+++顏色偏移
將受花影響區域的色調偏向較暖色調。

*左：0.0 / 右：0.8*



<table>
  <tr>
    <td>
      <img src="../../../../assets/bloomColorShift0.jpg" alt="bloomColorShift0">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../assets/bloomColorShift0-8.jpg" alt="bloomColorShift0-8">
      <br><i>之後</i>
    </td>
  </tr>
</table>



![bloomColorShift0](../../../../assets/bloomColorShift0.jpg "bloomColorShift0")

![bloomColorShift0-8](../../../../assets/bloomColorShift0-8.jpg "bloomColorShift0-8")

+++

## 景深

模擬相機鏡頭引起的光學現象，使得距離遠近的物體變得模糊。

此效果會受到相機的「光圈」與「對焦距離」參數影響。

>[!TIP]
>
> 要快速調整相機對焦，將游標放在你想對焦的場景位置，按下 Ctrl+LMB（Windows）或 Cmd+LMB（macOS），即可自動將對焦距離設定到該位置。

+++最大半徑
模糊效果的最大半徑。

*左：32.0 / 右：4.0*



<table>
  <tr>
    <td>
      <img src="../../../../assets/depthOfFieldMaxRadius32.jpg" alt="景深最大半徑32">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../assets/depthOfFieldMaxRadius4.jpg" alt="景深最大半徑4">
      <br><i>之後</i>
    </td>
  </tr>
</table>



![景深最大半徑32](../../../../assets/depthOfFieldMaxRadius32.jpg "景深最大半徑32")

![景深最大半徑4](../../../../assets/depthOfFieldMaxRadius4.jpg "景深最大半徑4")

+++

+++複合強度
從對焦距離向外擴散的模糊效果大小。

*左邊：0.2 / 右邊：0.05*



<table>
  <tr>
    <td>
      <img src="../../../../assets/depthOfFieldCompositeStrength0-2.jpg" alt="景深複合強度0-2">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../assets/depthOfFieldCompositeStrength0-05.jpg" alt="景深複合強度0-05">
      <br><i>之後</i>
    </td>
  </tr>
</table>



![景深複合強度0-2](../../../../assets/depthOfFieldCompositeStrength0-2.jpg "景深複合強度0-2")

![景深複合強度0-05](../../../../assets/depthOfFieldCompositeStrength0-05.jpg "景深複合強度0-05")

+++

+++縱向像差
在遠離焦距時，像差的強度。

像差模擬不同波長光的焦距略有差異，導致顏色看起來偏移，且焦距有細微差異。

*左：0.0 / 右：1.0*



<table>
  <tr>
    <td>
      <img src="../../../../assets/depthOfFieldLongitudinalAberration0.jpg" alt="景深縱向像差0">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../assets/depthOfFieldLongitudinalAberration1.jpg" alt="景深縱向像差1">
      <br><i>之後</i>
    </td>
  </tr>
</table>



![景深縱向像差0](../../../../assets/depthOfFieldLongitudinalAberration0.jpg "景深縱向像差0")

![景深縱向像差1](../../../../assets/depthOfFieldLongitudinalAberration1.jpg "景深縱向像差1")

+++

+++消色差像差
規定該像差是否應為消色差，意即部分或所有顏色具有相同的焦距。

這使得模糊效果看起來更均勻分布。

*左：真 / 右：假*



<table>
  <tr>
    <td>
      <img src="../../../../assets/depthOfFieldAchromaticAberrationYes.jpg" alt="景深消色變差 是的">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../assets/depthOfFieldAchromaticAberrationNo.jpg" alt="景深無色差 無色差 無">
      <br><i>之後</i>
    </td>
  </tr>
</table>



![景深消色差 是](../../../../assets/depthOfFieldAchromaticAberrationYes.jpg "的 景深消色差 是的")

![景深消色差 景](../../../../assets/depthOfFieldAchromaticAberrationNo.jpg "深 消色差 像差 無")

+++

+++貓眼
在場景中啟用貓眼效果，模擬斜角進入的光線並非進入圓盤，而是進入不均勻的橢圓，造成失真。

這種效應在較大光圈時更明顯——也就是光圈值較低。

*左：真 / 右：假*



<table>
  <tr>
    <td>
      <img src="../../../../assets/depthOfFieldAchromaticCatsEyeYes.jpg" alt="景深無色貓眼是的">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../assets/depthOfFieldAchromaticCatsEyeNo.jpg" alt="景深消色貓眼不">
      <br><i>之後</i>
    </td>
  </tr>
</table>



![景深無色貓眼是](../../../../assets/depthOfFieldAchromaticCatsEyeYes.jpg "的景深無色貓眼是的")

![景深消色貓眼無](../../../../assets/depthOfFieldAchromaticCatsEyeNo.jpg "景深消色貓眼無景深")

+++
