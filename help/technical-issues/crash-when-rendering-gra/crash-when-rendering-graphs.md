---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/technical-issues/crash-when-rendering-graphs.html"
breadcrumb-title: ''
description: 在 Substance 3D Designer 中排解圖表渲染時的崩潰問題，並尋找解決方法來避免這些問題。
helpx_creative_field: ""
helpx_description: Designer > Technical issues > Crash when rendering graphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 渲染圖表時崩潰
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 0%

---


# 渲染圖表時崩潰

本頁列出在 Substance 3D Designer 繪圖過程中發生的當機，並提供每一次的故障排除步驟。

## TDR（僅限 Windows）

<b>[![（錯誤）](../../assets/error.svg）]（https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/technical-support/technical-issues/gpu-issues/gpu-drivers-crash-with-long-computations-tdr-crash） 問題</b>

系統的 <b>逾時偵測與恢復（TDR）</b> 計時 *器過短* ，無法讓 Substance 3D Designer 在圖形驅動 *程式重新啟動*&#x200B;前完成當前運算。

Substance 3D Designer 執行的運算可能非常繁重，且會大量使用圖形驅動程式，導致 *一段時間內無法回應* 作業系統。\
為了穩定性與安全措施，作業系統 *會重新啟動顯示卡驅動程式*，縮短計算過程，導致 Substance 3D Designer *當*&#x200B;機。

<b>![（打了](../../assets/check.svg） 推薦步驟</b>

TDR 計時器值需要提高&#x200B;**，以防止此類當機。你可以依照](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/technical-support/technical-issues/gpu-issues/gpu-drivers-crash-with-long-computations-tdr-crash) Substance 3D Painter 文件頁面中的[指示操作，這些指示同樣適用於 Substance 3D Designer。
