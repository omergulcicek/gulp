<p align="center">
  <img src="https://camo.githubusercontent.com/f265315f74ed08b94e473cd7f6f04c291e59a8e2/687474703a2f2f706f73746373732e6769746875622e696f2f6175746f70726566697865722f6c6f676f2e737667" height="150" />
</p>

<h1 align="center">Autoprefixer</h1>

<p align="center">
  <a href="https://autoprefixer.github.io/">autoprefixer</a> · 
  <a href="https://www.npmjs.com/package/autoprefixer">npmjs</a> · 
  <a href="https://github.com/postcss/autoprefixer">github</a>
</p>

PostCSS eklentisi olan autoprefixer, CSS'i ayrıştırır ve <a href="http://caniuse.com/">caniuse.com</a>'daki değerleri kullanarak CSS kodunuza diğer tarayıcılara uyumlu olması için gerekli ön ekleri dahil eder. Siz ön ekleri unutun ve yalnızca saf CSS kodunuzu yazın.

Örnek vermek gerekirse, aşağıdaki kodu yazdığınızı düşünelim:

```css
a {
    display: flex;
}
```

Autoprefixer eklentisi tüm tarayıcı ön eklerini koda dahil ederek şu çıktıyı verecektir:

```css
a {
    display: -webkit-box;
    display: -webkit-flex;
    display: -ms-flexbox;
    display: flex;
}
```

<h2>Kurulum</h2>

Aşağıdaki komut ile kurulum işlemini gerçekleştirebilirsiniz.

```sh
npm install autoprefixer --save-dev
```

<h2>Kullanımı</h2>

Post Css ile birlikte autoprefixer eklentisini kullanabilirsiniz.

Gerekli eklentileri sayfaya dahil ederek, `autoprefixer` adında bir `task` oluşturalım.

```js
var autoprefixer = require('autoprefixer'),
    gulp         = require("gulp"),
    postcss      = require('gulp-postcss');

gulp.task('autoprefixer', function () {
    return gulp.src('./src/*.css')          // 1
        .pipe(postcss([ autoprefixer() ]))  // 2
        .pipe(gulp.dest('./dest'));         // 3
});
```

1. `src` klasörünün içerisindeki tüm `.css` uzantılı dosyaları alır

2. `autoprefixer` ile gerekli ön ekleri koda ekler

3. kodun son halini `dest` klasörünün içerisinde oluşturur

<h2>Seçenekler</h2>

<h3>browsers (array)</h3>

Kodunuzun tarayıcıların hangi sürümlerine uyumlu olacağını belirleyebilirsiniz:

```js
gulp.task('autoprefixer', function () {
    return gulp.src('./src/*.css')
        .pipe(postcss([ autoprefixer( { browsers: ['last 2 versions'], cascade: false } ) ]))
        .pipe(gulp.dest('./dest'));
});
```

Fakat bu seçenek yerine `package.json` dosyasındaki `browserslist`i kullanmanızı öneririz.

```js
{
  "private": true,
  "dependencies": {
    "autoprefixer": "^6.5.4"
  },
  "browserslist": [
    "> 1%",
    "last 2 versions"
  ]
}
```

Kullanılabilir tüm değerleri görmek için <a href="https://github.com/ai/browserslist#queries">Browserslist dokümanı</a>na göz atın.

<i>Eklemeler yapılacaktır.</i>

<a href="https://omergulcicek.github.io/gulp/eklentiler/browser-sync">Sıradaki Eklenti: Browser Sync</a>
