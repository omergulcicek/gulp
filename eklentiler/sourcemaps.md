<h1 align="center">Sourcemaps</h1>

<p align="center">
    <a href="https://www.npmjs.com/package/gulp-sourcemaps">npmjs</a> · 
    <a href="https://github.com/gulp-sourcemaps/gulp-sourcemaps">github</a>
</p>

CSS ve Javascript kodlarının tam olarak hangi klasörden geldiğini belirtir.

<h2>Kurulum</h2>

Aşağıdaki komut ile kurulum işlemini gerçekleştirebilirsiniz.

```sh
npm i gulp-sourcemaps
```

<h2>Kullanımı</h2>

```js
var gulp            = require('gulp'),
    sourcemaps      = require('gulp-sourcemaps');
    
gulp.task('css', function() {
  gulp.src('src/*.scss')
    .pipe(sourcemaps.init())
      .pipe(plugin1())
      .pipe(plugin2())
    .pipe(sourcemaps.write())
    .pipe(gulp.dest('dist'));
});
```

Yukarıdaki kod, `src` klasörünün içerisindeki tüm `.scss` uzantılı dosyaları alıp çeşitli pluginleri (*sass, minify, autoprefixer vb*) kullandıktan sonra dist klasörüne atar. Normalde tek bir css dosyası çıktısı olacağı için (*özellikle büyük projelerde*) hangi kodun tam olarak hangi dosyadan geldiğini anlamayabilirsiniz. `sourcemaps` eklentisi size o kodun kaynak dosyasını gösterecektir.

<a href="https://omergulcicek.github.io/gulp/eklentiler/uglify">Sıradaki Eklenti: Uglify</a>
