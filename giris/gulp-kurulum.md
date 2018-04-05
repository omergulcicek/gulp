<h1>Gulp Kurulumu</h1>

Gulp kurulumu için öncelikle NodeJS kurmamız gerekiyor.

<h2>NodeJS Kurulumu</h2>

<i><a href="https://nodejs.org/en/">NodeJS</a> sitesine girip aşağıda görüldüğü gibi soldaki butona tıklayıp nodejs'i indiriyoruz.</i>

<img src="https://i.hizliresim.com/1Jn00N.png">

<i>Ardından klasik kurulumu tamamladıktan sonra <b>Node.js command prompt</b> programını çalıştırıp, kurulumlarımızı bu konsol üzerinden yapacağız.</i>

<h2>Kullanımı</h2>

İlk olarak <b>npm init</b>ialize etmek gerekiyor. 

```sh
npm init
```

`npm init` komutundan sonra bize projenin adı, versiyonu, açıklaması, geliştiricisi vb sorular soracak.

Son olarak `is this ok? (yes)` sorusunu da geçtikten sonra projemizin klasöründe `package.json` dosyası oluşmuş olacak. 

Ardından gulp indirme işlemine geçebiliriz. Aşağıdaki komutlar ile `gulp`u indirebiliriz.

```sh
npm install gulp
```

Gulp kurulumu tamamlandıktan sonra proje klasörümüze `gulpfile.js` adında bir dosya açarak, gulp tasklarımızı buraya yazacağız.

Bir `package` install ettiğimizde, `gulpfile.js` dosyasına `require` edip, tasklarımızı tanımlamaya başlayacağız.

<a href="https://omergulcicek.github.io/gulp/giris/gulp-fonksiyonlari">Sıradaki Konu: Gulp Fonksiyonları</a>
