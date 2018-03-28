<h1 align="center">Imagemin</h1>

<p align="center">
    <a href="https://www.npmjs.com/package/gulp-imagemin">npmjs</a> · 
    <a href="https://github.com/sindresorhus/gulp-imagemin">github</a>
</p>

PNG, JPEG, GIF ve SVG uzantılı görselleri minify eder (<i>sıkıştırır</i>).

<h2>Kurulum</h2>

Aşağıdaki komut ile kurulum işlemini gerçekleştirebilirsiniz.

```sh
npm install gulp-imagemin --save-dev
```

<h2>Kullanımı</h2>

```js
var gulp            = require("gulp"),
    imagemin        = require("gulp-imagemin");

gulp.task("image", function() {
    return gulp.src("./src/img/*")
        .pipe(imagemin())
        .pipe(gulp.dest("./dest/img"))
});
```

Yukarıdaki kod, `src/img` klasörü içerisindeki tüm görsel dosyaları sıkıştırıp `dest/img` klasörüne atacaktır.

<a href="https://omergulcicek.github.io/gulp/eklentiler/post-css">Sıradaki Eklenti: Post Css</a>
