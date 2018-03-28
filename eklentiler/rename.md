<h1 align="center">Rename</h1>

<p align="center">
    <a href="https://www.npmjs.com/package/gulp-rename">npmjs</a> · 
    <a href="https://github.com/hparra/gulp-rename">github</a>
</p>

Dosya isimlerini kolayca değiştirmeyi sağlar.

<h2>Kurulum</h2>

Aşağıdaki komut ile kurulum işlemini gerçekleştirebilirsiniz.

```sh
npm install gulp-rename --save-dev
```

<h2>Kullanımı</h2>

```js
var gulp            = require("gulp"),
    rename          = require("gulp-rename");
    
gulp.src("./src/hello.txt")
    .pipe(rename("new.txt"))
    .pipe(gulp.dest("./dist"));
```

Yukarıdaki kod, `src` klasörünün içerisindeki `hello.txt` dosyasının adını `new.txt` yapar ve `dist` klasörünün içerisine atar.

<a href="https://omergulcicek.github.io/gulp/eklentiler/sass">Sıradaki Eklenti: Sass</a>
