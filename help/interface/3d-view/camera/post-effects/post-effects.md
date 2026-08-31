---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/3d-view/camera/post-effects.html"
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
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '732'
ht-degree: 2%

---


# 後續影響

![後期效果](post-effects.resources/post-effects-01.png "後期效果"){zoomable="yes"}

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
      <img src="post-effects.resources/post-effects-02.jpg" alt="後FXDisabled（特製化）">
      <br><i>之前</i>
    </td>
    <td>
      <img src="post-effects.resources/post-effects-03.jpg" alt="FXReinhard 之後">
      <br><i>之後</i>
    </td>
  </tr>
</table>



![後特效可化後特](post-effects.resources/post-effects-02.jpg "效可變")

![後FXReinhard](post-effects.resources/post-effects-03.jpg "後特效Reinhard")

+++

+++阿坦


<table>
  <tr>
    <td>
      <img src="post-effects.resources/post-effects-02.jpg" alt="後FXDisabled（特製化）">
      <br><i>之前</i>
    </td>
    <td>
      <img src="post-effects.resources/post-effects-04.jpg" alt="FXAtan 之後">
      <br><i>之後</i>
    </td>
  </tr>
</table>



![後特效可化後特](post-effects.resources/post-effects-02.jpg "效可變")

![後FXAtan](post-effects.resources/post-effects-04.jpg "後FXAtan")

+++

+++經驗


<table>
  <tr>
    <td>
      <img src="post-effects.resources/post-effects-02.jpg" alt="後FXDisabled（特製化）">
      <br><i>之前</i>
    </td>
    <td>
      <img src="post-effects.resources/post-effects-05.jpg" alt="FXExp 後期">
      <br><i>之後</i>
    </td>
  </tr>
</table>



![後特效可化後特](post-effects.resources/post-effects-02.jpg "效可變")

![後特效衍生](post-effects.resources/post-effects-05.jpg "後")

+++

+++日誌


<table>
  <tr>
    <td>
      <img src="post-effects.resources/post-effects-02.jpg" alt="後FXDisabled（特製化）">
      <br><i>之前</i>
    </td>
    <td>
      <img src="post-effects.resources/post-effects-06.jpg" alt="離開FXLog後">
      <br><i>之後</i>
    </td>
  </tr>
</table>



![後特效可化後特](post-effects.resources/post-effects-02.jpg "效可變")

![後FXLog](post-effects.resources/post-effects-06.jpg "後FXLog")

+++

+++A牌


<table>
  <tr>
    <td>
      <img src="post-effects.resources/post-effects-02.jpg" alt="後FXDisabled（特製化）">
      <br><i>之前</i>
    </td>
    <td>
      <img src="post-effects.resources/post-effects-07.jpg" alt="FXAces 後期">
      <br><i>之後</i>
    </td>
  </tr>
</table>



![後特效可化後特](post-effects.resources/post-effects-02.jpg "效可變")

![FX後 FX](post-effects.resources/post-effects-07.jpg "後")

+++

+++海爾


<table>
  <tr>
    <td>
      <img src="post-effects.resources/post-effects-02.jpg" alt="後FXDisabled（特製化）">
      <br><i>之前</i>
    </td>
    <td>
      <img src="post-effects.resources/post-effects-08.jpg" alt="FXHejl 之後">
      <br><i>之後</i>
    </td>
  </tr>
</table>



![後特效可化後特](post-effects.resources/post-effects-02.jpg "效可變")

![後FXHejl](post-effects.resources/post-effects-08.jpg "後期 FX後")

+++

+++中性


<table>
  <tr>
    <td>
      <img src="post-effects.resources/post-effects-02.jpg" alt="後FXDisabled（特製化）">
      <br><i>之前</i>
    </td>
    <td>
      <img src="post-effects.resources/post-effects-09.jpg" alt="FX之後 紐特拉爾">
      <br><i>之後</i>
    </td>
  </tr>
</table>



![後特效可化後特](post-effects.resources/post-effects-02.jpg "效可變")

![後FXNeutral](post-effects.resources/post-effects-09.jpg "後期")

+++

+++AGX


<table>
  <tr>
    <td>
      <img src="post-effects.resources/post-effects-02.jpg" alt="後FXDisabled（特製化）">
      <br><i>之前</i>
    </td>
    <td>
      <img src="post-effects.resources/post-effects-10.jpg" alt="FXAgx 之後">
      <br><i>之後</i>
    </td>
  </tr>
</table>



![後特效可化後特](post-effects.resources/post-effects-02.jpg "效可變")

![FXAgx](post-effects.resources/post-effects-10.jpg "之後")

+++

+++PBR 中性線


<table>
  <tr>
    <td>
      <img src="post-effects.resources/post-effects-02.jpg" alt="後FXDisabled（特製化）">
      <br><i>之前</i>
    </td>
    <td>
      <img src="post-effects.resources/post-effects-11.jpg" alt="之後FXPbrNeutral">
      <br><i>之後</i>
    </td>
  </tr>
</table>



![後特效可化後特](post-effects.resources/post-effects-02.jpg "效可變")

![後FXPbr中立後FXPbr中立](post-effects.resources/post-effects-11.jpg "後")

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
      <img src="post-effects.resources/post-effects-12.jpg" alt="bloomThreshold1">
      <br><i>之前</i>
    </td>
    <td>
      <img src="post-effects.resources/post-effects-13.jpg" alt="bloomThreshold4">
      <br><i>之後</i>
    </td>
  </tr>
</table>



![bloomThreshold1](post-effects.resources/post-effects-12.jpg "bloomThreshold1")

![bloomThreshold4](post-effects.resources/post-effects-13.jpg "bloomThreshold4")

+++

+++衰減
蓬鬆衰減斜坡，值越低，布隆半徑越短。

*左：1.0 / 右：0.6*



<table>
  <tr>
    <td>
      <img src="post-effects.resources/post-effects-14.jpg" alt="bloomFalloff1">
      <br><i>之前</i>
    </td>
    <td>
      <img src="post-effects.resources/post-effects-15.jpg" alt="bloomFalloff0-6">
      <br><i>之後</i>
    </td>
  </tr>
</table>



![bloomFalloff1](post-effects.resources/post-effects-14.jpg "bloomFalloff1")

![bloomFalloff0-6](post-effects.resources/post-effects-15.jpg "bloomFalloff0-6")

+++

+++關卡
那綻放的強烈程度。 較高的光度會帶來更明亮、更明顯的光線條紋。

*左：8.0 / 右：2.0*



<table>
  <tr>
    <td>
      <img src="post-effects.resources/post-effects-16.jpg" alt="bloomLevel8">
      <br><i>之前</i>
    </td>
    <td>
      <img src="post-effects.resources/post-effects-17.jpg" alt="bloomLevel2">
      <br><i>之後</i>
    </td>
  </tr>
</table>



![bloomLevel8](post-effects.resources/post-effects-16.jpg "bloomLevel8")

![bloomLevel2](post-effects.resources/post-effects-17.jpg "bloomLevel2")

+++

+++顏色偏移
將受花影響區域的色調偏向較暖色調。

*左：0.0 / 右：0.8*



<table>
  <tr>
    <td>
      <img src="post-effects.resources/post-effects-18.jpg" alt="bloomColorShift0">
      <br><i>之前</i>
    </td>
    <td>
      <img src="post-effects.resources/post-effects-19.jpg" alt="bloomColorShift0-8">
      <br><i>之後</i>
    </td>
  </tr>
</table>



![bloomColorShift0](post-effects.resources/post-effects-18.jpg "bloomColorShift0")

![bloomColorShift0-8](post-effects.resources/post-effects-19.jpg "bloomColorShift0-8")

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
      <img src="post-effects.resources/post-effects-20.jpg" alt="景深最大半徑32">
      <br><i>之前</i>
    </td>
    <td>
      <img src="post-effects.resources/post-effects-21.jpg" alt="景深最大半徑4">
      <br><i>之後</i>
    </td>
  </tr>
</table>



![景深最大半徑32](post-effects.resources/post-effects-20.jpg "景深最大半徑32")

![景深最大半徑4](post-effects.resources/post-effects-21.jpg "景深最大半徑4")

+++

+++複合強度
從對焦距離向外擴散的模糊效果大小。

*左邊：0.2 / 右邊：0.05*



<table>
  <tr>
    <td>
      <img src="post-effects.resources/post-effects-22.jpg" alt="景深複合強度0-2">
      <br><i>之前</i>
    </td>
    <td>
      <img src="post-effects.resources/post-effects-23.jpg" alt="景深複合強度0-05">
      <br><i>之後</i>
    </td>
  </tr>
</table>



![景深複合強度0-2](post-effects.resources/post-effects-22.jpg "景深複合強度0-2")

![景深複合強度0-05](post-effects.resources/post-effects-23.jpg "景深複合強度0-05")

+++

+++縱向像差
在遠離焦距時，像差的強度。

像差模擬不同波長光的焦距略有差異，導致顏色看起來偏移，且焦距有細微差異。

*左：0.0 / 右：1.0*



<table>
  <tr>
    <td>
      <img src="post-effects.resources/post-effects-24.jpg" alt="景深縱向像差0">
      <br><i>之前</i>
    </td>
    <td>
      <img src="post-effects.resources/post-effects-25.jpg" alt="景深縱向像差1">
      <br><i>之後</i>
    </td>
  </tr>
</table>



![景深縱向像差0](post-effects.resources/post-effects-24.jpg "景深縱向像差0")

![景深縱向像差1](post-effects.resources/post-effects-25.jpg "景深縱向像差1")

+++

+++消色差像差
規定該像差是否應為消色差，意即部分或所有顏色具有相同的焦距。

這使得模糊效果看起來更均勻分布。

*左：真 / 右：假*



<table>
  <tr>
    <td>
      <img src="post-effects.resources/post-effects-26.jpg" alt="景深消色變差 是的">
      <br><i>之前</i>
    </td>
    <td>
      <img src="post-effects.resources/post-effects-27.jpg" alt="景深無色差 無色差 無">
      <br><i>之後</i>
    </td>
  </tr>
</table>



![景深消色差 是](post-effects.resources/post-effects-26.jpg "的 景深消色差 是的")

![景深消色差 景](post-effects.resources/post-effects-27.jpg "深 消色差 像差 無")

+++

+++貓眼
在場景中啟用貓眼效果，模擬斜角進入的光線並非進入圓盤，而是進入不均勻的橢圓，造成失真。

這種效應在較大光圈時更明顯——也就是光圈值較低。

*左：真 / 右：假*



<table>
  <tr>
    <td>
      <img src="post-effects.resources/post-effects-28.jpg" alt="景深無色貓眼是的">
      <br><i>之前</i>
    </td>
    <td>
      <img src="post-effects.resources/post-effects-29.jpg" alt="景深消色貓眼不">
      <br><i>之後</i>
    </td>
  </tr>
</table>



![景深無色貓眼是](post-effects.resources/post-effects-28.jpg "的景深無色貓眼是的")

![景深消色貓眼無](post-effects.resources/post-effects-29.jpg "景深消色貓眼無景深")

+++
