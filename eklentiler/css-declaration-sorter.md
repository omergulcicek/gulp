<p align="center">
    <img src="https://camo.githubusercontent.com/16f040f0efabaca4e5c870692c39f272d228091d/68747470733a2f2f63646e2e7261776769742e636f6d2f5369696c77796e2f6373732d6465636c61726174696f6e2d736f727465722f6d61737465722f6c6f676f2e737667" height="150" />
</p>

<h1 align="center">CSS Declaration Sorter</h1>

<p align="center">
    <a href="https://www.npmjs.com/package/css-declaration-sorter">npmjs</a> · 
    <a href="https://github.com/Siilwyn/css-declaration-sorter">github</a>
</p>

CSS kodlarını düzenlemek için bir PostCSS eklentisidir. CSS kodlarını alfabetik yada farklı sıralar ile sıralabilirsiniz.

Alfabetik kaydetme örneğini inceleyelim:

```css
/* Kaydetmeden Önce */
body {
    display: block;
    animation: none;
    color: #C55;
    border: 0;
}

/* Kaydettikten Sonra */
body {
    animation: none;
    border: 0;
    color: #C55;
    display: block;
}
```

<h2>Kurulum</h2>

Aşağıdaki komut ile kurulum işlemini gerçekleştirebilirsiniz.

```sh
npm install css-declaration-sorter --save-dev
```

<h2>Kullanımı</h2>

```js
var alphabetical    = require("css-declaration-sorter"),
    gulp            = require("gulp"),
    postcss         = require("gulp-postcss");

gulp.task("css", function() {
    return gulp.src("./src/*.css")
        .pipe(postcss([alphabetical({order: "alphabetically"})]))
        .pipe(gulp.dest("./dest"))
});
```

Yukarıdaki kod, tüm css dosyalarını alfabetik olarak sıralayacaktır (<i>Şahsen ben alfabetik css kullanıyorum</i>).

<h2>Seçenekler</h2>

Farklı türde sıralama yapmak mümkün. Yukarıdaki örnekte `{order: "alphabetically"}` ile alfabetik sıralanma sağlanmıştır. Burada `alphabetically` yerine aşağıdaki kullanımları seçebilirsiniz.

<h3>smacss</h3>

Css kod sıralamasını `Box, Border, Background, Text, Other` şeklinde yapar.

```js
...
.pipe(postcss([alphabetical({order: "smacss"})]))
...
```

<h3>concentric-css</h3>

Css kod sıralamasını `Positioning, Visibility, Box model, Dimensions, Text` şeklinde yapar.

```js
...
.pipe(postcss([alphabetical({order: "concentric-css"})]))
...
```

Varsayılan olarak alfabetik sıralama yapar.

<a href="https://omergulcicek.github.io/gulp/eklentiler/imagemin">Sıradaki Eklenti: Imagemin</a>
