<h1 align="center">Uglify</h1>

<p align="center">
    <a href="https://www.npmjs.com/package/gulp-uglify">npmjs</a> · 
    <a href="https://github.com/terinjokes/gulp-uglify">github</a>
</p>

JavaScript kodlarını minify eder (<i>sıkıştırır</i>).

```css
/* Önce */
Array.prototype.forEach.call(tabs, function(el, i) {
    el.classList.remove("aktif");
});

/* Sonra */
Array.prototype.forEach.call(tabs,function(el,i){el.classList.remove("aktif")});
```

<h2>Kurulum</h2>

Aşağıdaki komut ile kurulum işlemini gerçekleştirebilirsiniz.

```sh
npm install gulp-uglify --save-dev
```

<h2>Kullanımı</h2>

```js
var gulp            = require("gulp"),
    uglify          = require("gulp-uglify");

gulp.task("javascript", function() {
    return gulp.src("./src/*.js")
        .pipe(uglify())
        .pipe(gulp.dest("./dest"))
});
```

Yukarıdaki kod, javascript kodlarını alıp minify eder (<i>sıkıştırır</i>).

<a>Sıradaki Eklenti: </a>
