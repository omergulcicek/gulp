<h1 align="center">SASS</h1>

<p align="center">
    <a href="https://www.npmjs.com/package/gulp-sass">npmjs</a> · 
    <a href="https://github.com/dlmanning/gulp-sass">github</a>
</p>

SASS kodlarını CSS'e çevirir.

```sass
/* Kaydetmeden Önce */
$backgroundColor: #f5f5f5;
$width: 250px;
.square {
    width: $width;
    height: 250px;

    .color {
        background-color: $backgroundColor;
    }
}

/* Kaydettikten Sonra */
.square {
    width: 250px;
    height: 250px;
}

.square .color {
    background-color: #f5f5f5;
}
```

<h2>Kurulum</h2>

Aşağıdaki komut ile kurulum işlemini gerçekleştirebilirsiniz.

```sh
npm install gulp-sass --save-dev
```

<h2>Kullanımı</h2>

```js
var gulp            = require("gulp"),
    sass            = require("gulp-sass"),

gulp.task("css", function() {
    return gulp.src("./src/*.sass")
        .pipe(sass())
        .pipe(gulp.dest("./dest"))
});
```

Yukarıdaki kod, tüm sass kodlarını alıp normal css kodu haline getirir. 

`sass({outputStyle: "compressed"})` şeklinde kullanırsanız, dönüştürülen kodu minify eder (<i>sıkıştırır</i>).

<a href="https://omergulcicek.github.io/gulp/eklentiler/sourcemaps">Sıradaki Eklenti: Sourcemaps</a>
