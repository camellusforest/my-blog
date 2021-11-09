# JS讀書筆記30天 - Day23 Bootstrap的格線系統



# `container`和`container-fluid`

### 使用

在Bootstrap中，這兩個Class是一樣的地位，是用來定義最外層容器的。

使用格線系統時，補上`container`或`container-fluid`，版面會規整，不會有多餘的`padding`或`margin`出現。

### `container-fluid`

主要使用在滿版寬度。

會隨著版型寬度調整，適合用在不需要嚴謹的最大寬度版面使用。

### `container`

常用在版面有最大寬度限制的時候。

有時候對網頁美感和內容的每個階段都有需求時，用`container`可以在斷點前維持同一版型，因為會隨著斷點才變動版面，所以很適合在版型有最大寬度限制時使用。

### 斷點

斷點分為五個階段：

1. 寬度 < 576px：版面隨視窗縮放變化
2. 768px > 寬度 ≥ 576pxf：會以540px為版面寬度
3. 992px > 寬度 ≥ 768px：會以720px為版面寬度
4. 1200px > 寬度 ≥ 992px：會以960px為版面寬度
5. 寬度 ≥ 1200px：會以1140px為版面寬度



## `row`和`col`

### `row`

包覆`col`的Class，一定要寫在一個段落，作為放置`col`容器的`<div>`上面，因為在設計格線系統時，就是設計`row`包覆`col`外，如果沒有遵守，會造成破版的現象。

### `col`

為最內部的元件欄位，是column的縮寫，一般常說的兩欄式版面、三欄式版面，就是用`col`做為區隔`<div>`的Class。

要特別注意的是，因為Bootstrap是用`padding`作為欄與欄之間的間隔，所以不要在使用`col`Class的`<div>`上用`padding-left`、`padding-right`、`margin-left`、`margin-right`這些水平推移的CSS，以免造成破版。

在使用時，如果不給任何數字，單純的使用`col`，`row`會以當前`row`中`col`的數量來平分空間，形成均分的欄位排版。

如果要有大小欄差異的排版，在`col`後加上數字即可，範圍從1到12，分別代表該欄佔當下`row`幾等份，寫成`col-數字`。