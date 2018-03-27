<p align="center">
    <img src="https://cdn.worldvectorlogo.com/logos/browsersync.svg" height="150" />
</p>

<h1 align="center">Browser Sync</h1>

<p align="center">
    <a href="https://browsersync.io/">browsersync</a> · 
    <a href="https://www.npmjs.com/package/browser-sync">npmjs</a> · 
    <a href="https://github.com/BrowserSync/browser-sync">github</a>
</p>

Web sitesi oluştururken birden fazla tarayıcıyı ve cihazı senkronize halde gösterir. Kodunuzu kaydettiğiniz anda tarayıcıyı yeniler, `F5` yapmanıza gerek kalmaz; bu da bize oldukça zaman kazandırır ve hızlı kod yazmamızı sağlar.

<h2>Kurulum</h2>

Aşağıdaki komut ile kurulum işlemini gerçekleştirebilirsiniz.

```sh
npm install browser-sync --save-dev
```

<h2>Kullanımı</h2>

```js
var browsersync     = require("browser-sync"),
    gulp            = require("gulp");


gulp.task("browsersync", function() {
    browsersync({
        server: {
            baseDir: './'
        },
        open: false,
        online: false,
        notify: false
    });
});
```

`bworsersync` fonksiyonunu oluşturduktan sonra örneğin css dosyamızda değişiklik olduğunda tarayıcıyı yenilemek için şu kodu kullanın:

```js
gulp.task("css", function() {
    return gulp.src("./src/*.css")
        // burada birkaç işlem yapıldığını varsayalım
        .pipe(gulp.dest("./dest"))
        .pipe(browsersync.reload({stream: true}))
});
```

Css dosyaları alınıp bir kaç işlem gerçekleştikten sonra, son halini `dest` klasörüne atıyor, hemen ardından tarayıcıyı güncelliyor.

Gulp default fonksiyonuna `browsersync` fonksiyonumuzu eklemeyi unutmayalım:

```js
gulp.task("default", ["browsersync"]);
```

Browser Sync'ın Gulp için hazırladığı <a href="https://browsersync.io/docs/gulp">doküman</a>a göz atabilirsiniz.

<a href="https://omergulcicek.github.io/gulp/eklentiler/clean-css">Sıradaki Eklenti: Clean Css</a>
