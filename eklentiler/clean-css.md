<h1 align="center">Clean Css</h1>

<p align="center">
    <a href="https://jakubpawlowicz.github.io/clean-css/">cleancss</a> · 
    <a href="https://www.npmjs.com/package/gulp-clean-css">npmjs</a> · 
    <a href="https://github.com/scniro/gulp-clean-css">github</a>
</p>

Css dosyalarından gereksiz boşlukları kaldırarak minify eder (<i>sıkıştırır</i>), böylece dosya boyutunuda en aza indirmiş olur.

```css
/* Önce */
a {
    color: #000;
    display: inline-block;
    text-decoration: none;
}

/* Sonra */
a{color:#000;display:inline-block;text-decoration:none}
```

<h2>Kurulum</h2>

Aşağıdaki komut ile kurulum işlemini gerçekleştirebilirsiniz.

```sh
npm install gulp-clean-css --save-dev
```

<h2>Kullanımı</h2>

```js
var cleancss = require("gulp-clean-css"),
    gulp     = require("gulp");

gulp.task("css", function() {
    return gulp.src("./src/*.css")
        .pipe(cleancss())
        .pipe(gulp.dest("./dest"))
});
```

Yukarıdaki kod, css dosyalarını alıp sıkıştırma işlemi gerçekleştirecektir.

Tüm seçeneklere ulaşmak için <a href="https://github.com/jakubpawlowicz/clean-css">clean css dokümanı</a>na göz atabilirsiniz.

<a href="https://omergulcicek.github.io/gulp/eklentiler/concat">Sıradaki Eklenti: Concat</a>
