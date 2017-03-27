# HTML {#html}

> 標籤語言的自白

### HTML 是什麼？ {#html-是什麼？}

> 超文件標示語言（英語：HyperText Markup Language，簡稱：HTML）是一種用於建立網頁的標準標示語言，HTML被用來結構化資訊：例如標題、段落和列表等等，也可用來在一定程度上描述文件的外觀和語意。HTML的語言形式為尖括弧，包圍的HTML元素，瀏覽器使用HTML標籤和指令碼來詮釋網頁內容，但不會將它們顯示在頁面上。維護HTML和CSS標準的組織為[全球資訊網協會（W3C）](https://www.w3.org/)。

上面這段只有三個重點

* HTML 是**標籤語言**，不是程式語言
* HTML 是由**“Tag”標籤**構成
* HTML 負責**告訴瀏覽器如何建構頁面**

> 簡單來說，如果網頁是臉，HTML就是用Tag標籤來規定你有幾個鼻子、幾個嘴巴、幾個耳朵、有沒有長頭髮。

## Tag標籤 {#tag標籤}

### 什麼是**“Tag”標籤**？ {#什麼是tag標籤？}

```html
<Tag></Tag>
```

OK?

那接下來讓我們看一段經典的html程式碼：

> 一段經典的HTML原始碼長這樣

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
...
</body>
</html>
```

> 喂喂喂等等，上面那是三毀!?!?

讓我們一步一步來：

```html
<!DOCTYPE html>
```

在第一行負責跟瀏覽器說：安安你好，我是份HTML文件，我要用W3C的標準規範進行建構與渲染[^1]。

```html
<html>
...
</html>
```

接著跟瀏覽器說：這份html開始了，在 `<html>`到`</html>` 的範圍內都是html。

```html
<head>
    <title>Title</title>
</head>
```

再告訴瀏覽器：這是我的“頭”，有個標題名稱叫Title。

> 小知識：
>
> &lt;head&gt;標籤在網頁中並不會被呈現，但卻是網頁中最為不可或缺的一個元素。
>
> html文件被瀏覽器載入時瀏覽器會先讀完這個部分並載入提供的預先載入內容，常用此處來連結外部樣式表、JavaScript或JavaScript framework，meta標籤也會在此處宣告。



```html
<meta charset="UTF-8">
```

這裡的&lt;meta&gt;[^2]標籤宣告此份html文件採用UTF-8作為編碼格式

[^1]: 為什麼要有這行？沒有這行瀏覽器不知道這是HTML嗎？答案是因為各家瀏覽器所使用的渲染引擎不一，當所有瀏覽器看到這行 DTD 宣告，就會去此對這份規範，依照此規範去解讀 HTML 標籤，這樣就比較不會有不相容的狀況發生。

[^2]: meta標籤還有更多用途，後面會提到 \[參見：\]。

