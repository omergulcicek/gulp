<h1>Gulp Fonksiyonlari</h1>

<h2>src</h2>

`source (kaynak)`ın kısaltılmışıdır. Kaynak dosyaları seçmemize yarar.

Örneğin `css` klasörünün içerisindeki tüm `.css` uzantılı dosyaların üzerinde işlem yapmak istiyorsak, şu şekilde seçebiliriz:

```js
gulp.src("css/*.css")
```

Parametre olarak `string` yada `array` alır.

Tüm dosyalar yerine belirli dosyaları almak isterseniz dizi olarak dosyaları seçebilirsiniz:

```js
gulp.src(["css/turkuaz.css", "css/style.css"])
```

<h2>dest</h2>

`destination (hedef)`ın kısaltılmışıdır. İşlenmiş dosyaları belirlenen konuma atar.

Örneğin `src` ile tüm css'leri seçip minift edip `build` klasörüne atalım:

```js
gulp.src("css/*.css")
    .pipe(minify())
    .pipe(gulp.dest("build"));
```

<h2>task</h2>

`task (görev)` demektir. Gulp'a görev verme işlemlerini bu fonksiyonlar yardımı ile yapacağız.

Örnek kullanımı şu şekildedir:

```js
gulp.task('görevİsmi', function() {
  // Kodlar
});
```

Her taska bir isim vermek zorundayız, task isimlerinde boşluk karakteri olmamalıdır.

<h2>watch</h2>

`watch (izle)` demektir. Gulp dosyalarını izler ve değişiklik olduğunda belirlediğiniz taskı çalıştırır.

Örnek kullanımı şu şekildedir:

```js
gulp.task("watch", function() {
    gulp.watch("css/*.css", ["css"]);
    gulp.watch("js/*.js", ["javascript"]);
});
```

Yukarıdaki Gulp taskı, `css` klasörü içerisindeki tüm `.css` uzantılı dosyaları izler ve değişiklik yaptığınız anda `css` taskını çalıştırır.

Aynı şekilde `.js` uzantılı dosyalarda değişiklik yapıldığında `javascript` taskını çalıştırır.

<h2>default</h2>

`default (varsayılan)` demektir. Gulp'un varsayılan olarak temel görevi `default` taskıdır.

Örneğin `css`, `js`, `img` adında tasklar oluşturmuş olalım. `gulp css`, `gulp js`, `gulp img` diyerek tek tek o taskları çalışmak yerine, `default` taskına hepsini eklersek tek kerede hepsini çağırabiliriz. Konsola `gulp` yazdığınızda varsayılan olarak `gulp default` taskı çalışacak ve bu taskta diğer tasklarınızı çalıştırmış olacaktır.

Örnek kullanımı şu şekildedir:

```js
gulp.task('default', function() {
    //varsayılan tasklarımız
});

//yada şu şekilde kullanabilirsiniz:
gulp.task("default", ["css", "javascript", "watch"]);
```

<i>Genel gulp bilgisi bu kadar. Bu aşamadan sonra en sık kullanılan eklentilerin anlatımına geçiş yapılacaktır.</i>

<a href="https://omergulcicek.github.io/gulp/eklentiler/autoprefixer">Sıradaki Eklenti: Autoprefixer</a>
