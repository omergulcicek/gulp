<h1 align="center">Concat</h1>

<p align="center">
    <a href="https://www.npmjs.com/package/gulp-concat">npmjs</a> · 
    <a href="https://github.com/gulp-community/gulp-concat">github</a>
</p>

Css yada JavaScript dosyalarınızı birleştirerek tek dosya haline getirir.

```css
/* Kaydetmeden Önce */
style.css
custom.css
responsive.css
(vb.)

/* Kaydettikten Sonra */
all.css
```

<h2>Kurulum</h2>

Aşağıdaki komut ile kurulum işlemini gerçekleştirebilirsiniz.

```sh
npm install gulp-concat --save-dev
```

<h2>Kullanımı</h2>

```js
var concat          = require("gulp-concat"),
    gulp            = require("gulp");

gulp.task("css", function() {
    return gulp.src("./src/*.css")
        .pipe(concat("all.css"))
        .pipe(gulp.dest("./dest"))
});
```

Yukarıdaki kod, tüm css dosyalarını alıp `all.css` adında tek dosya haline getirir. Örnekte Css kodları üzerinden örnek verilmiş olsada aynı işlemi JavaScript içinde aynı şekilde gerçekleştirebilirsiniz.

<a href="https://omergulcicek.github.io/gulp/eklentiler/declaration-sorter">Sıradaki Eklenti: Declaration Sorter</a>
