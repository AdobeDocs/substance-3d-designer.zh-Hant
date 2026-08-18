---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-designer/glossary.html"
breadcrumb-title: ''
description: 請存取 Substance 3D Designer 詞彙表，查找術語、概念及技術術語的定義。
helpx_creative_field: ""
helpx_description: Designer > Glossary
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 詞彙表
user-guide-description: ''
user-guide-title: ''
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '4459'
ht-degree: 0%

---


# 學習 Designer 中使用的術語與概念。

## #

|  |  |
| --- | --- |
| <b><span id="three-d-scene"></span>3D 場景</b> | 一組用於表示與動畫化三維空間視覺化的物件與資料：<ul data-preserve-html="true"> <li data-preserve-html="true">[網格](#mesh)</li> <li data-preserve-html="true">[材料](#material)</li> <li data-preserve-html="true">攝影機</li> <li data-preserve-html="true">光源</li> <li data-preserve-html="true">動畫</li> <li data-preserve-html="true">模擬</li> <li data-preserve-html="true">...</li> </ul>[常用的 3D 場景儲存檔案格式](https://www.adobe.com/tw/products/substance3d/discover/3d-files-formats.html) 包括 Pixar [的 USD](#usd) 和 Autodesk 的 FBX。 並非所有檔案格式都支援所有這些元件 |

## A

|  |  |
| --- | --- |
| <b><span id="alpha"></span>阿爾法通道</b> | 彩色影像的第四通道，常用於描述不透明度。 |
| <b><span id="ambient-occlusion"></span>環境遮蔽</b> | 環境光在暴露較少、因此較難觸及的表面上衰減。 |
| <b><span id="anisotropy"></span>各向異性</b> | 依賴方向的特性。 換句話說，當測量或觀察到不同的座標軸時，結果會有所不同。 各向異性材料的外觀會因觀察地點而異，且各向異性濾光片並非均勻地應用於所有方向。 |
| <b><span id="api"></span>API</b> | 應用程式介面（API）是一組函式與程序，讓使用者能存取其他程式應用程式的功能與程序。 API 提供使用者與程式之間受控且安全的層。 它也可能使用其他程式語言，使該程式更易互動並更廣泛地取得。 Designer 提供 [Python API](../scripting/scripting.md) ，方便存取其多種功能，用於資料操作、建置自訂工具及加速工作流程。 |
| <b><span id="atomic-node"></span>原子節點</b> | 圖的基本構成要素。 所有[實例節點](#instance-node) 都可以拆解成原子節點的圖。每種圖類型都有自己的原子節點集合。 |

## B

|  |  |
| --- | --- |
| <b><span id="baking"></span>烘焙</b> | 從3D模型中計算資訊並儲存成 [貼圖](#texture)的過程。 資料會根據模型的 [UV](#uv) 配置到貼圖中。 |
| <b><span id="base-color"></span>底色</b> （Albedo） | 利用PBR金屬粗糙[度著色](#shader)模型定義的材料[&#128279;](#material)通道。底色是指表面的顏色，但沒有任何光照資訊。 它不應與 [擴散（Diffuse](#diffuse)）混淆。 |
| <b><span id="base-parameter"></span>基準參數</b> | 一個 Substance 圖中所有計算 [位圖](#bitmap)節點共有的參數。 這些包括點陣圖的核心面向，如解析度（[輸出大小](#output-size)）與 [位元深度](#bit-depth) （輸出格式），或點陣圖的計算方式，如 [平](#tiling) 鋪模式。 基礎參數通常[&#128279;](#inheritance)繼承自上游的其他節點或該節點所承載的圖。 |
| <b><span id="bilinear-filtering"></span>雙線性濾波</b> | 一種用於電腦影像的插值過程，當 [紋理樣本](#texture-sampling) 並非精確位於像素中心時。 例如，當影像被放大時，這種情況就可能發生。 |
| <b><span id="bit-depth"></span>位元深度</b> | 用來儲存紋理中像素值的位元數。 較高的位元深度允許編碼更多值，進而產生更平滑的梯度。 根據值的類型，有不同的位元深度可供選擇：- 整數值可用 8 位元（0 到 255）或 16 位元（0 到 65,535）來編碼。 - 浮點數值可用 16 位元（+32767.9999 至 -32768.0）或 32 位元（-3.4E+38 至 +3.4E+38）編碼。低動態範圍影像則使用整數值編碼 0 到 1 的階梯。 高動態範圍影像使用浮點數來編碼原始數值。 在 Substance 圖中，位元深度由輸出格式參數控制。 |
| <b><span id="bitmap"></span>位圖</b> | 一張數位影像。 最常見的影像類型有兩種：<ul data-preserve-html="true"> <li data-preserve-html="true">灰階影像只有一個通道：亮度（L）;</li> <li data-preserve-html="true">彩色影像有三個通道：紅、綠、藍（RGB）。 可能還有第四個：alpha （A），通常用於不透明度。 Designer 中的彩色影像總是 RGBA。</li> </ul>點陣圖可被視為數值的網格。 該格子的每個格子都是像素，像素是「圖片元素」的縮寫。 每個像素每個通道儲存一個值。 該值的類型取決於 [位圖的位元深度](#bit-depth) 。 |

## C

|  |  |
| --- | --- |
| <b><span id="cache"></span>快取</b> （記憶體） | 一組資料——例如： Node 的 [基礎參數](#base-parameter) 與輸出映像——儲存在記憶體中以便重複使用。 快取大幅加快圖形計算速度，因為它讓 [Substance Engine](#substance-engine) 只重新計算已改變的圖部分。 調整節點連接與參數時，之前所有節點不受這些變更影響，因此不需要 [再次評估](#evaluation) 以更新圖。 取而代之的是他們的快取。 在處理大型圖形中高解析度與位元深度時，快取可能會佔用顯著的記憶體。 |
| <b><span id="channel-packing"></span>通道包裝</b> | 一種優化技術，將獨立影像壓縮在單一彩色影像的 RGB（A） 通道中。 例如，RMA 材質是粗糙度貼圖（R）、金屬度貼圖（M）和環境遮蔽貼圖（A）全部壓縮在單一色彩貼圖中。 另一種常見技術是在法線貼圖的藍色通道中打包灰階紋理，因為藍色通道——即法向量的「向上」部分——可以在執行時重新計算。 [RGBA 合併](../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/rgba-merge/rgba-merge.md)節點對於實作此技術非常有用。 |
| <b><span id="color-space"></span>色彩空間</b> | 定義了一範圍的顏色如何被表示。數位編碼與解碼特定顏色需要這樣的定義，才能理解所使用的數字。 影像檔案會使用指定的色彩空間來儲存色彩值，這樣這些顏色就能在支援該色彩空間的顯示器上忠實地重現。 顯示器具備特定的色彩重現能力，使其能完全或部分支援特定色彩空間。 原始資料——例如 法線映射——總是在線性色彩空間中編碼與解碼，因為這些顏色並非用來視覺化的，且不應對該資料進行任何轉換。 sRGB 是一個廣泛支援的色彩空間。 其他常見的色彩空間包括 Adobe RGB、Rec。 2100 和 ProPhoto RGB。 |
| <b><span id="cooking"></span>烹飪 </b>（<span id="compilation"></span>合輯） | 將資料翻譯成另一種語言，以便能快速且有效地執行的過程。計算物質圖的結果需要先將其編譯。 編譯是圖 [評估](#evaluation) 過程的一部分。 此編譯是在扁平化圖上執行，意即 [所有實例節點](#instance-node) 被其來源圖「替換」，因此只剩下一個較大的圖，該圖即為被編譯的圖。 編譯後的圖表無法編輯。 如果參數是 [動態](#dynamic-parameter)的，則會保留公開參數，而 [靜態](#static-parameter) 參數則被鎖定並隱藏。 |
| <b><span id="culling"></span>淘汰</b> | 一種用於渲染 3D 場景的優化技術，當渲染圖形不可見時，會將其從計算中移除。 這可能包括相機錐體外的物件或多邊形（*錐體剔除*）、面向相機對面方向的物件（*背面剔除*），或完全被其他不透明物件遮蔽（*遮蔽剔除*）。 |

## D

|  |  |
| --- | --- |
| <b><span id="dependency"></span>依賴性</b> | 一個檔案 A 被另一個檔案 B 使用，導致當檔案 A 缺失時，檔案 B 無法如預期運作。 套件的依賴[&#128279;](#package)可以是另一個套件，因為它會參考其中的圖形、影像檔案、字型等。套件會儲存其依賴路徑，若在該路徑找不到依賴，會發出警告。缺少相依關係也 [可能導致圖中出現幽靈節點](#ghost-instance-node) 。 |
| <b><span id="diffuse"></span>彌漫</b> | 利用 PBR 鏡面光澤[著色](#shader)模型定義的材質[&#128279;](../glossary/glossary.md)通道。漫射指的是點亮時表面的顏色。 它不應與 [底色（Albedo）](#base-color)混淆。 |
| <b><span id="directx"></span>DirectX</b> | 一套用於處理多媒體內容的 API。 其 3D API Direct3D 廣泛應用於電子遊戲開發及其他 3D 產業。 Direct3D 將紋理的原點——也就是其 （0， 0） 座標——放在&#x200B;*左*&#x200B;上角（Y-down），而 OpenGL[&#128279;](#opengl) API 則將它放在&#x200B;*左*&#x200B;下角（Y-up）。這表示 DirectX 的法線貼圖&#x200B;*相較於 OpenGL，*&#x200B;通道是反轉的綠色。事實上，綠色通道承載了法向量的 Y 座標。 |
| <b><span id="displacement"></span>遷移</b> | 移動3D模型頂點的過程[&#128279;](#vertex)，通常是沿著其[法線](#normal)移動。位移常與鑲嵌[&#128279;](#tessellation)和[法線貼圖](#normal-map)結合使用，以在表面上建模更細緻的細節。 |
| <b><span id="dynamic-parameter"></span>動態參數</b> | 一個參數，該參數的值可能會改變。 換句話說，任何值不常的參數都是動態的。這包括暴露參數、受暴露參數影響的參數，以及任何受貼圖[&#128279;](#texture-sampling)取樣影響的參數值。與[靜態參數](#static-parameter)不同，動態參數的值可在圖彙編成 SBSAR 檔案後即時調整。 |

## E

|  |  |
| --- | --- |
| <b><span id="evaluation"></span>評價</b> | 解析圖中資料與參數傳播的過程。 評估是驗證圖及其連結的有效性，應用 [繼承，](#inheritance)並 [處理](#cooking) 圖。 在圖視圖中，當連接未被評估時，會以虛線表示。評估將連結轉化為實線。每當圖中參數被調整時，承載該參數的節點及所有下游節點都會被[&#128279;](#invalidation)取消，必須在渲染[&#128279;](#rendering)前重新評估。 |

## F

|  |  |
| --- | --- |
| <b><span id="filter"></span>濾波器</b> （節點） | 一個節點，對影像進行修改（例如變形）或從中提取資訊（例如遮罩）。 |

## G

|  |  |
| --- | --- |
| <b><span id="ghost-instance-node"></span>幽靈實例節點</b> | 若參考[&#128279;](#instance-node)的子圖無法找到——即缺少[依賴——](#dependency)的實例節點會被載入為幽靈實例節點。透過解決缺失的相依性並重新載入 [套件](#package)，幽靈實例節點會被恢復到預期狀態。 |
| <b><span id="glossiness"></span>光澤</b> | 利用 PBR 鏡面光澤[著色](../glossary/glossary.md)模型定義的材質[&#128279;](../glossary/glossary.md)通道[。光澤性指的是表面的粗糙度——即高度的微觀變化，也稱為 *微多面*。 高光澤度會帶來平滑的質感，而低光澤則會呈現粗糙且霧面的質感。 它是粗糙度](#roughness)的反面。 |

## H

|  |  |
| --- | --- |
| <b><span id="histogram"></span>直方圖（圖片）</b> | 在影像的情境中，直方圖代表給定範圍內數值的族群——通常是[0， 1]。 此族群以垂直條線視覺化，影像中出現的數值越多，該數值的條狀越大。條狀區域水平分布，從低（暗）到高（亮）。 彩色影像的直方圖通常會與其各通道的直方圖重疊——通常是 R、G、B。 |

## I

|  |  |
| --- | --- |
| <b><span id="inheritance"></span>繼承</b> | 在 Substance 圖的語境中，繼承描述節點從其上游節點或父圖獲取參數值的特性。 繼承的參數包括 [解析度](#resolution) （[輸出大小](#output-size)）、 [位元深度](#bit-depth) （[輸出格式](#output-format)）及 [平](#tiling) 鋪模式。 在此專頁[&#128279;](../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)了解更多關於繼承的資訊。 |
| <b><span id="instance-node"></span>實例節點</b> | 一個實例節點將圖 A 表示到另一個圖 B 中。此時，圖 A 可稱為 [圖 B 的子圖](#subgraph) 。圖 A 的任何變化都會傳播到所有代表該圖的實例節點。 實例節點會在圖 B 的情境中套用自己一套輸入參數的值。從這個意義上說，圖 B 可以承載多個實例節點，這些節點都參考圖 A，但每個節點會將不同的值或紋理作為輸入傳遞到圖 A。 Designer 函式庫中所有非 [原子節點](#atomic-node) 的節點皆為實例節點。 |
| <b><span id="invalidation"></span>無效化</b> | 宣告節點結果已過時的程序。 當參數被調整時，承載該參數的節點及所有下游節點都會失效，因此需要 [重新評估](#evaluation) 並[重新渲染](#rendering)。 |

## M

|  |  |
| --- | --- |
| <b><span id="material"></span>材料</b> | 物質在空間中的性質與行為集合，包括表面與體積。一個實體在三維空間中的外觀是由其材質所定義的。 材料的定義方式多樣，且所有定義都不支持折射、各向異性或光澤等所有性質。 [著色器](#shader)是材質定義的特定實作。  <b>重要提示：</b> 「材料」一詞是一個 *總稱* ，用來指稱多種事物，包括：<ul data-preserve-html="true"> <li data-preserve-html="true">[用於計算表面或體積外觀的著色器](#shader);</li> <li data-preserve-html="true">提供給著色器的貼圖[&#128279;](#texture)集合;</li> <li data-preserve-html="true">材質 ID，是 3D 圖元的一個屬性，用來區分使用不同材質的零件。</li> </ul> |
| <b><span id="mesh"></span>網狀</b> | 一個由 [頂點組成的](#vertex) 三維物件，頂點由邊連接形成多邊形——例如三角形——而這些多邊形再被組合成曲面。 這些表面可以是開放式或封閉式。 這些表面的外觀由 [分配給它們的材質](#material) 所定義。網格的細節程度也高度依賴於其 [多邊形數量](#polycount)。 |
| <b><span id="metadata"></span>元資料</b> | 提供關於檔案本身、其環境或與檔案資料相關資訊的資料。 常見的元資料包括檔案作者、創建與修改日期、版權及封面藝術。 在 Designer 中，套件[&#128279;](#package)的內容也可以包含元資料。例如，產生織物材料的物質圖可能包含織物物理特性的元資料。 |
| <b><span id="mipmap"></span>Mipmap</b> | 材質的縮小版，通常由自動計算。 貼圖可以有一個由自身較小版本組成的金字塔，這些版本在執行時可互換，以達到最佳品質與效能的最佳大小。 例如，高頻細節的紋理在較小尺寸下顯示，可能會產生 *莫爾痕* 跡。 此外，較大的紋理通常包含更多的 [紋理樣本](#texture-sampling)。 「mipmap」一詞源自MIP映射技術，其中MIP代表拉丁文「*multum in parvo*」，意指「小地方裡有許多事物」。 |

## N

|  |  |
| --- | --- |
| <b><span id="node"></span>節點</b> | 圖中的物件，執行計算並輸出一個或多個結果。 結果由輸入參數控制。 這些參數可以在屬性底座中列出為控制項，或作為節點本身的輸入連接器。 節點主要分為兩大類： [原子節點](#atomic-node) 與實例節點。 |
| <b><span id="noise"></span>噪音</b> | 一種非具象的圖像，代表形狀與顏色的隨機或偽隨機分布。 噪音常用於增加表面變化或變形。 Designer 的節點函式庫包含大量雜訊產生器，如 [BnW 斑點](../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/bnw-spots-2/bnw-spots-2.md)、[&#128279;](../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/perlin-noise/perlin-noise.md)雲[&#128279;](../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/clouds-2/clouds-2.md)、Perlin 雜訊或 [Voronoi](../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/voronoi/voronoi.md)。 |
| <b><span id="normal"></span>正常</b> | 在三維計算中，曲面的法線是一個 [垂直於該曲面的正規化](#normalization) 向量，從該曲面向外延伸。 此向量代表三維空間中表面的方向，並用於 [根據場景的光線與攝影機視角對該表面進行](#shader) 陰影。 [法線貼](#normal-map)圖可以套用到表面上，以修改其法線並增加細節。 |
| <b><span id="normal-map"></span>法線貼圖</b> | 貼圖貼在表面上以修改其法線。 它最常用來偽造那些在模型幾何中加入效率不高的細節。 使用此類映射可讓每頂點法線外，還能擁有每像素法線，從而獲得更多曲面資訊，進而提升曲面細節。 法向量的 X、Y 和 Z 座標分別編碼在地圖的紅、綠、藍通道中。 根據目標圖形 API（[DirectX](#directx) 或 [OpenGL），](#opengl)綠色通道可能會反轉。 |
| <b><span id="normalization"></span>正規化</b> | 將一組值重新映射到 [0， 1] 範圍的過程，其中最高的輸入值會重新映射為 1.0，最低的輸入值會重新映射為 0.0。 對於向量，正規化是將向量的長度（或稱「大小」）調整為 1.0。 |

## O

|  |  |
| --- | --- |
| <b><span id="opengl"></span>OpenGL</b> | 一款廣泛應用於電子遊戲開發及其他 3D 產業的 3D 圖形 API。 OpenGL 將紋理的原點——即其 （0， 0） 座標——置於&#x200B;*左*&#x200B;下角（Y-up），而 DirectX[&#128279;](#directx) API 則將其置於&#x200B;*左*&#x200B;上角（Y-down）。這表示 OpenGL 的法線貼圖相較於 DirectX 的&#x200B;*綠色通道*&#x200B;是反轉的。 事實上，綠色通道承載了法向量的 Y 座標。 |
| <b><span id="openusd"></span>OpenUSD</b> | 參見 [美元](#usd)。 |
| <b><span id="output-format"></span>輸出格式</b> | [Substance 圖中節點的基底參數](#base-parameter) ，描述該節點的 [位元深度](#bit-depth)。 |
| <b><span id="output-size"></span>輸出大小</b> | [Substance 圖中節點的基底參數](#base-parameter) ，描述該節點 [的解析度](#resolution)。 在此專頁[&#128279;](../compositing-graphs/output-size/output-size.md)了解更多關於輸出大小的資訊。 |

## P

|  |  |
| --- | --- |
| <b><span id="package"></span>包裝</b> | Substance 3D 檔案（SBS[&#128279;](#sbs-file)）稱為套件，因為它是資源容器：圖表、[點陣圖](#bitmap)、[3D 場景](#three-d-scene)等。套件同時儲存其[相依](#dependency)關係的路徑以及[元資料](#metadata)。 |
| <b><span id="pattern"></span>模式</b> | 一張應該作為模型或參考，用來製作另一張影像的影像。 在大多數情況下，圖案是用來重複呈現的影像（例如，拼貼、隨機散布或依照某套規則排列）。 |
| <b><span id="pixel-ratio"></span>像素比</b> | 此 [基礎參數](#base-parameter) 控制影像在像素層級的寬寬比補償。 換句話說：是否應該補償像素大小以守恆非正方形影像中的正方比。 此參數被非局部濾波器使用——即利用鄰近像素的值來計算像素值的濾波器。 |
| <b><span id="pixel-size"></span>像素尺寸</b> | 這個基礎參數定義了像素的水平與垂直大小。 它作為非局部濾波器的乘法器——也就是利用鄰近像素的值來計算像素值的濾波器。 |
| <b><span id="polycount"></span>多重計數</b> | 3D [網格](#mesh)中多邊形的數量。 事實上，polycount 是「polygon count」的簡稱。 更多的多邊形可以模擬更細緻的細節。 多邊形數量較少的網格稱為「低多邊形」，而多邊形數量較高的則稱為「高多邊形」。 |
| <b><span id="primary-input"></span>主要輸入</b> | 實例節點[&#128279;](#instance-node)的輸入連接器，該節點繼承[其基礎參數](#base-parameter)值。主要輸入端的連接器上有一個小點標示，標籤上則有「（Primary）」後綴。 使用多個輸入節點時，強烈&#x200B;**&#x200B;建議注意哪些輸入是主要輸入，以及這如何影響[整個圖的繼承](#inheritance)。 |
| <b><span id="procedural"></span>程序性</b> | 指的是依照電腦演算法而非手動產生的資料或產物。 Designer 採用程序式工作流程，演算法設計為節點圖。程序式工作流程允許更快的迭代，因為透過修改演算法及其參數，可以快速產生變化與調整。 當結果完全由演算法產生時，該結果俗稱為「100% 程序化」。 程序生成有時簡稱為「proc-gen」。 Designer 節點函式庫中的大多數產生器都是 100% 程序式的，因為它們不需要輸入影像就能產生結果。 |
| <b><span id="publishing"></span>出版（SBSAR）</b> | 在 Designer 中，發佈指的是將 [套件](#package) 匯出為 SBSAR 壓縮檔，該檔案包含 [已編譯](#compilation) 的圖表、其資源（點[陣](#bitmap)圖、字型等）、預設以及 [元資料](#metadata)。 產生的 SBSAR 檔案可透過 Substance 3D 外掛[&#128279;](https://substance3d.adobe.com/plugins/)分發並用於其他 Substance 3D 應用程式或第三方應用程式。 |

## R

|  |  |
| --- | --- |
| <b><span id="renderer"></span>渲染器</b> | 一個處理3D資訊（如燈光、網格和材質）以產生2D影像的程式。 |
| <b><span id="rendering"></span>渲染 </b>（3D 視圖） | 根據輸入資料計算影像的過程，使用像渲染 [器](#renderer)這樣的程式。 |
| <b><span id="resolution"></span>解決方法</b> | 組成點陣[&#128279;](#bitmap)圖的水平和垂直像素數量。更多像素可以呈現更細緻的細節。 在 Substance 圖中，節點計算[&#128279;](#node)的點陣圖解析度由該節點的「[輸出大小](#output-size)」[基參數](#base-parameter)控制。 |
| <b><span id="roughness"></span>粗糙度</b> | 利用PBR金屬粗糙[度著色](../glossary/glossary.md)模型定義的材料[&#128279;](../glossary/glossary.md)通道[。粗糙度指的是表面的粗糙度——即高度的微觀變化，也稱為 *微小面*。 高粗糙度會呈現霧面效果，低粗糙度則是光滑有光澤的質感。 它是光澤的](#glossiness)反向。 |

## S

|                                                                                                   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>取樣（</b> 取樣） | 獲取影像或函數在特定點的價值。 請參見 [紋理取樣](#texture-sampling)。 |
| <b><span id="sbs-file"></span>SBS 檔案</b> | SBS 代表「SuBStance 3D 檔案」。 此檔案用於儲存 Substance 3D Designer 專案。 其資料使用 [XML](#xml) 格式。詳見[包裝](#package)。 |
| <b><span id="sbsar-file"></span>SBSAR 檔案</b> | SBSAR 代表「SuBStance 3D ARchive」（SuBStance 3D ARchive）。 此壓縮檔用於儲存已編譯的 Substance 3D Designer 圖表及其所需資源（[點陣](#bitmap)圖、字型等）。 SBSAR 是主要用於分發可供其他 Substance 3D 應用程式及 Substance 3D 插件使用的 Substance 圖表。 由於儲存在 SBSAR 檔案中的圖表是被編譯的，因此無法在 Substance 3D Designer 中載入與編輯。 不過，SBSAR 檔案可透過 [7Zip](https://www.7-zip.org/) 開啟，以擷取其 [參數、預設與中繼資料，並嵌入 XML](#xml) 檔案。 |
| <span id="sdf"></span><b>SDF</b> | 請參見 [有符號距離場](#signed-distance-field)。 |
| <b><span id="shader"></span>著色器</b> | 該程式根據表面或體積的材料[&#128279;](#material)特性、接收到的光線以及觀看位置來計算表面或體積的外觀。著色器是材質定義的特定實作。 貼圖可能會提供給著色器來驅動其行為。 也可以使用原始數值。在 [3D 視圖](../interface/3d-view/3d-view.md)中，前往「材質」選單，查看目前場景中材質使用的著色器。 選單也讓你能存取 [著色器屬性](../interface/3d-view/3d-view.md)，以及著色器目前正在使用的材質和值。 「著色器」有時與「[材質](#material)」互換使用。 |
| <span id="sheen"></span><b>希恩</b> | 布料的光澤或光澤特性。 這個術語在紡織業中廣泛使用，用來描述一種反射性質，能帶來細微的色彩亮度。 |
| <b><span id="signed-distance-field"></span>有號距離域（SDF）</b> | <p>有符號距離場是一種數學函數，透過計算空間中任意一點到曲面上最近點的距離，來定義三維空間中的曲面。</p><p>想了解更多關於這個概念以及它在 Designer 中的應用，請點此： [與 SDF 函](../function-graphs/nodes-reference-for-fun/function-node-library/function-nodes-sdf-functions/working-with-sdf-functions.md#what-is-an-sdf-function)式合作。</p> |
| <b><span id="spline"></span>樣條</b> | 一般而言，這是用數學函數建模的曲線，能在任何解析度下繪製乾淨且平滑的形狀。 Designer 使用有損近似，並以自訂資料格式編碼在貼圖中。 樣條線提供直觀的長度與軌跡控制，包含厚度與高度等其他資料，並方便存取沿線任意點的距離與方向。 這些特質使它們成為繪畫與材質製作的強大工具。 |
| <b><span id="static-parameter"></span>靜態參數</b> | 一個參數，該參數的值不得改變。 與動態參數[&#128279;](#dynamic-parameter)相反[，當圖被編譯成 SBSAR 檔案時，靜態參數無法即時更改。它們只能在繪圖過程中在 Designer 中暴露與修改。 預覽模式在某些情況下會隱藏這些參數，因為它旨在盡可能匹配已發佈的 SBSAR 檔案的行為。 靜態參數清單可在此](../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)取得。 |
| <b><span id="subgraph"></span>子圖</b> | 一個在另一個圖 [中作為實例節點](#instance-node)使用的圖。 |
| <b><span id="substance-engine"></span>物質引擎</b> | 這是由Substance 3D團隊開發的專有技術，負責透過大量轉換、效果與合成輸入影像，效率極高。 Substance Engine 實作並計算 Designer 的 [原子節點](#atomic-node)。 該引擎依據所運行的平台（CPU、GPU 與作業系統）透過不同的後端實作。 在 Designer 中，後端可以透過 Tools [> Switch 引擎](../interface/the-main-toolbar/the-main-toolbar.md)切換。 有些後端的效能明顯優於其他的——例如，GPU 後端比 CPU 快得多——而且不同後端的結果可能略有不同。 |
| <b><span id="substance-graph"></span></b><b>Substance 圖</b>  （或 Substance 合成圖） | 一個輸出一個或多個 [位圖](#bitmap)的圖。 Substance 圖可用於多種用途：- 產生一組描述材料的紋理點陣圖;- 對一個或多個點陣圖輸入進行影像處理，作為濾波器;- 產生雜訊、圖案或原始資料，作為產生器。 |

## T

|  |  |
| --- | --- |
| <b><span id="tessellation"></span>鑲嵌</b> | 在電腦圖學中，鑲嵌是指將表面細分為更多多邊形的過程，通常是三角形。 此過程可在執行時動態增加 3D 模型的多邊形數量，常與位移[&#128279;](#displacement)與[法線貼圖](#normal-map)結合，利用新增多邊形來建模更細緻的細節。 |
| <b><span id="texel"></span>特塞爾</b> | 紋理[&#128279;](#texture)的資訊單元，類似像素是圖片的資訊單元。 |
| <b><span id="texture"></span>材質</b> | 一幅用於表示圖形、透過向著色器[&#128279;](#shader)提供[&#128279;](#material)數值描述表面材質屬性，以及在紋[素](#texel)中編碼原始資料的影像。貼圖是可以由 GPU 非常有效地解壓縮和操作的物件。 在大多數情況下，這種效率要求貼圖使用兩個解析度的冪次——例如 1024x1024、4096x4096、512x256 等。 |
| <b><span id="texture-sampling"></span>紋理取樣</b> | 在特定位置獲取紋理[&#128279;](#texture)的價值。有些演算法需要執行大量取樣來比較數值、平均值或其他操作。 如果取樣並非在像素的正中心執行，Designer 中有兩個選項來選擇應該取得的值：<ul data-preserve-html="true"> <li data-preserve-html="true"><b>最近：</b> 根據中心，最近像素的值</li> <li data-preserve-html="true"><b>雙線性濾波：</b> 指相鄰像素在水平與垂直方向的插值值，較近的像素權重較高。</li> </ul> |
| <b><span id="tiling"></span>鋪磚</b> | 影像在水平、垂直或兩者皆有重複，且無明顯接縫或視覺斷裂。 Designer 提供很多[&#128279;](#node)節點，可以產生[&#128279;](#noise)聲音或[圖案](#pattern)來鋪鋪。同樣地，許多 [濾波](#filter) 器節點設計成在保留平鋪的同時處理影像。 |

## U

|  |  |
| --- | --- |
| <b><span id="usage"></span>使用（輸出）</b> | 在 Substance 圖中，使用 Usage 是輸出節點的一個屬性[，用來讓應用程式知道如何將貼圖](#texture)連接到 [&#128279;](../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) [3D 視圖](../interface/3d-view/3d-view.md)中的[著色器](#shader)。當將 Substance 圖套用到 3D 視圖時，所有輸出都會根據相符的使用情況連接到著色器。 也就是說，從「底色」到「底色」，從「粗糙度」到「粗糙度」，依此類推。 在使用「Material」與「Compact Material」 [連結建立模式](../interface/the-graph-view/link-creation-modes/link-creation-modes.md)時，也用於匹配連接器。 |
| <b><span id="udim"></span>UDIM</b> （UV圖塊） | 一個標準，將 UV[&#128279;](#uv) 空間分割成具有獨特數值識別碼的圖塊，允許為每個圖塊指派不同的貼圖。UDIM 工作流程在 VFX 管線中相當普遍，因為高保真度資產需要極高的細節，因此需要多個高解析度材質。 在這種情況下，資產的 [UV](#uv)s 會被安排在多個 UDIM（或 UV 圖塊）上。 Designer 支援 UDIM 工作流程，並可依 UDIM 指派不同的 Substance 圖表。 |
| <b><span id="usd"></span>美元</b> （或稱OpenUSD） | [通用場景描述](https://openusd.org/release/index.html)（USD）是由皮克斯開發的3D場景描述格式，旨在實現跨應用程式與平台的互通性與資料交換。USD 檔案包含場景中使用的資料定義，以及該場景的組成及其所有相關內容：模型、材質、攝影機、動畫、模擬等。只要應用程式能存取 USD 外掛，才能正確讀取並使用該資料，USD 檔案可以包含任何類型的資料。 Adobe 參與 [了 OpenUSD](https://blog.adobe.com/en/publish/2023/08/01/powering-3d-interoperability-continued-collaboration-through-openusd) 聯盟，這是一個由 3D 產業參與者組成的聯盟，積極參與該格式的開發與標準化。 |
| <b><span id="uv"></span>紫外線</b> | UV 是 3D 模型在二維空間中的一種表示方式。 它們用於將二維空間的二維影像映射到三維空間中的模型表面。 製作 UV 的過程通常被描述為在模型上切割接縫以展開並使其平整。 |

## V

|  |  |
| --- | --- |
| <b><span id="vertex"></span>頂點</b> | 空間中獨特的一點，通常是兩條或多條線交會的地方。 |

## X

|  |  |
| --- | --- |
| <b><span id="xml"></span>XML</b> | 可擴充標記語言（XML）是一種用於以人類可讀格式儲存資料的格式。 與 HTML 類似，使用標籤&lt;>（）和值定義的資料會被標籤包圍。 [SBS](#sbs-file) 檔案格式使用 XML 來排列與儲存資料。 |
