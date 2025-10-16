# Lab4Web
## Membuat layout sederhana

### Membuat box elemen
Kode ini menampilkan empat kotak berwarna untuk menunjukkan cara kerja box element dan properti float. Tiga kotak pertama diatur dengan `float: left;` sehingga tampil sejajar ke kiri, sedangkan kotak keempat menggunakan `clear: left;` agar turun ke bawah dan tidak sejajar dengan yang lain. Contoh ini menjelaskan bagaimana elemen HTML dapat diatur posisinya menggunakan float dan clear dalam membuat layout sederhana.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Box Element Float</title>
    <style>
        div {
            float: left;
            padding: 10px;
            color: white;
            text-align: center;
            width: 100px;
        }
        .div1 { background: red; }
        .div2 { background: yellow; color: black; }
        .div3 { background: green; }
        .div4 {
            background: blue;
            clear: left;
            float: none;
        }
    </style>
</head>
<body>
    <section>
        <div class="div1">Div 1</div>
        <div class="div2">Div 2</div>
        <div class="div3">Div 3</div>
        <div class="div4">Div 4</div>
    </section>
</body>
</html>
```

<img width="953" height="360" alt="Cuplikan layar 2025-10-16 134338" src="https://github.com/user-attachments/assets/451f6ada-80db-4f68-b9ac-a90188ab819d" />

### Membuat layout sederhana

Kode ini membentuk struktur halaman web dengan layout sederhana menggunakan elemen semantik HTML5. Bagian `<header>` menampilkan judul halaman, sedangkan `<nav>` berisi menu navigasi agar pengguna bisa berpindah antarhalaman seperti Home, Artikel, About, dan Kontak. Bagian `<section id="hero">` digunakan sebagai tampilan pembuka atau banner utama yang berisi teks dan tombol. Selanjutnya, area utama halaman dibungkus dalam `<section id="wrapper">` yang terdiri dari `<main>` untuk konten utama berisi kotak dan artikel, serta `<aside>` sebagai sidebar yang menampilkan widget link dan teks tambahan. Di bagian bawah, `<footer>` menampilkan informasi hak cipta. Semua elemen dibungkus dalam `<div id="container">` agar tata letaknya mudah diatur menggunakan CSS.


```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Layout Sederhana</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div id="container">
        <header>
            <h1>Layout Sederhana</h1>
        </header>

        <nav>
            <a href="home.html" class="active">Home</a>
            <a href="artikel.html">Artikel</a>
            <a href="about.html">About</a>
            <a href="kontak.html">Kontak</a>
        </nav>

        <section id="hero">
            <h1>Hello World!</h1>
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem elit, iaculis in nisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla, vestibulum mi porta, faucibus felis.</p>
            <a href="home.html" class="btn btn-large">Learn more &raquo;</a>
        </section>

        <section id="wrapper">
            <section id="main">
                <div class="row">
                    <div class="box">
                        <img src="https://dummyimage.com/120/db7d25/fff.png" alt="" class="image-circle">
                        <h3>Heading</h3>
                        <p>Donec sed odio dui. Etiam porta sem malesuada magna mollis euismod.</p>
                        <a href="#" class="btn btn-default">View detail</a>
                    </div>
                    <div class="box">
                        <img src="https://dummyimage.com/120/3e73e6/fff.png" alt="" class="image-circle">
                        <h3>Heading</h3>
                        <p>Donec sed odio dui. Etiam porta sem malesuada magna mollis euismod.</p>
                        <a href="#" class="btn btn-default">View detail</a>
                    </div>
                    <div class="box">
                        <img src="https://dummyimage.com/120/71e6d4/fff.png" alt="" class="image-circle">
                        <h3>Heading</h3>
                        <p>Donec sed odio dui. Etiam porta sem malesuada magna mollis euismod.</p>
                        <a href="#" class="btn btn-default">View detail</a>
                    </div>
                </div>

                <hr class="divider">

                <article class="entry">
                    <h2>First featurette heading.</h2>
                    <img src="https://dummyimage.com/150/7b8a70/fff.png" alt="">
                    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem elit, iaculis in nisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla.</p>
                </article>

                <hr class="divider">

                <article class="entry">
                    <h2>Second featurette heading.</h2>
                    <img src="https://dummyimage.com/150/7b8a70/fff.png" alt="" class="right-img">
                    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem elit, iaculis in nisl volutpat, malesuada tincidunt arcu.</p>
                </article>
            </section>

            <aside id="sidebar">
                <div class="widget-box">
                    <h3 class="title">Widget Header</h3>
                    <ul>
                        <li><a href="#">Widget Link</a></li>
                        <li><a href="#">Widget Link</a></li>
                        <li><a href="#">Widget Link</a></li>
                        <li><a href="#">Widget Link</a></li>
                        <li><a href="#">Widget Link</a></li>
                    </ul>
                </div>

                <div class="widget-box">
                    <h3 class="title">Widget Text</h3>
                    <p>Vestibulum lorem elit, iaculis in nisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla.</p>
                </div>
            </aside>
        </section>

        <footer>
            <p>&copy; 2021 - Universitas Pelita Bangsa</p>
        </footer>
    </div>
</body>
</html>
```

## CSS style

Kode CSS ini mengatur tampilan layout web agar terlihat rapi dan terstruktur. Font *Open Sans* diimpor dari Google Fonts, dan reset CSS digunakan untuk menghapus margin serta padding bawaan. Bagian `header` dan `nav` mengatur tampilan judul serta menu navigasi dengan warna biru dan efek hover. Elemen `#hero` digunakan sebagai banner utama dengan teks besar dan latar abu muda. Bagian `#main` dan `#sidebar` diatur sejajar menggunakan float untuk membentuk dua kolom. Widget di sidebar diberi border, warna biru pada judul, serta efek saat tautan diarahkan. Footer diberi latar hitam dan teks abu terang di bagian bawah halaman. Kelas `.box` membuat tiga kolom konten sejajar dengan gambar lingkaran, sedangkan `.entry` mengatur artikel agar rapi dengan garis pemisah di antaranya.

```css
/* import google font */ 
@import url('https://fonts.googleapis.com/css2?family=Open+Sans:ital,wght@0,300;0,400;0,600;0,700;0,800;1,300;1,400;1,600;1,700;1,800&display=swap'); 
@import url('https://fonts.googleapis.com/css2?family=Open+Sans+Condensed:ital,wght@0,300;0,700;1,300&display=swap'); 

/* Reset CSS */ 
* { 
    margin: 0; 
    padding: 0; 
} 

body { 
    line-height:1; 
    font-size:100%; 
    font-family:'Open Sans', sans-serif; 
    color:#5a5a5a; 
} 

#container { 
    width: 980px; 
    margin: 0 auto; 
    box-shadow: 0 0 1em #cccccc; 
} 

/* header */ 
header { 
    padding: 20px; 
} 

header h1 { 
    margin: 20px 10px; 
    color: #b5b5b5; 
} 

/* navigasi */ 
nav { 
    display: block; 
    background-color: #1f5faa; 
} 

nav a { 
    padding: 15px 30px; 
    display: inline-block; 
    color: #ffffff; 
    font-size: 14px; 
    text-decoration: none; 
    font-weight: bold; 
} 

nav a.active, 
nav a:hover { 
    background-color: #2b83ea; 
} 

/* Hero Panel */ 
#hero { 
    background-color: #e4e4e5; 
    padding: 50px 20px; 
    margin-bottom: 20px; 
} 

#hero h1 { 
    margin-bottom: 20px; 
    font-size: 35px; 
} 

#hero p { 
    margin-bottom: 20px; 
    font-size: 18px; 
    line-height: 25px; 
} 

/* main content */ 
#wrapper { 
    margin: 0; 
} 

#main { 
    float: left; 
    width: 640px; 
    padding: 20px; 
} 

/* sidebar area */ 
#sidebar { 
    float: left; 
    width: 260px; 
    padding: 20px; 
} 

/* widget */ 
.widget-box { 
    border:1px solid #eee; 
    margin-bottom:20px; 
} 

.widget-box  .title { 
    padding:10px 16px; 
    background-color:#428bca; 
    color:#fff; 
} 

.widget-box ul { 
    list-style-type:none; 
} 

.widget-box li { 
    border-bottom:1px solid #eee; 
} 

.widget-box li a { 
    padding:10px 16px; 
    color:#333; 
    display:block; 
    text-decoration:none; 
} 

.widget-box li:hover a { 
    background-color:#eee; 
} 

.widget-box p { 
    padding:15px; 
    line-height:25px; 
} 

/* footer */ 
footer { 
    clear:both; 
    background-color:#1d1d1d; 
    padding:20px; 
    color:#eee; 
} 

/* box */ 
.box { 
    display:block; 
    float:left; 
    width:33.333333%; 
    box-sizing:border-box; 
    -moz-box-sizing:border-box; 
    -webkit-box-sizing:border-box; 
    padding:0 10px; 
    text-align:center; 
} 

.box h3 { 
    margin: 15px 0; 
} 

.box p { 
    line-height: 20px; 
    font-size: 14px; 
    margin-bottom: 15px; 
} 

box img { 
    border: 0; 
    vertical-align: middle; 
} 

.image-circle { 
    border-radius: 50%; 
} 

.row { 
    margin: 0 -10px; 
    box-sizing: border-box; 
    -moz-box-sizing: border-box; 
    -webkit-box-sizing: border-box; 
} 

.row:after, .row:before, 
.entry:after, .entry:before { 
    content:''; 
    display:table; 
} 

.row:after, 
.entry:after { 
    clear:both; 
} 

.divider { 
    border:0; 
    border-top:1px solid #eeeeee; 
    margin:40px 0; 
} 

/* entry */ 
.entry { 
    margin: 15px 0; 
} 

.entry h2 { 
    margin-bottom: 20px; 
} 

.entry p { 
    line-height: 25px; 
} 

.entry img { 
    float: left; 
    border-radius: 5px; 
    margin-right: 15px; 
} 

.entry .right-img { 
    float: right; 
}
```

<img width="1213" height="920" alt="Cuplikan layar 2025-10-16 172252" src="https://github.com/user-attachments/assets/5de762de-c38f-48e7-9b1d-9fd7cc8d8e32" />

<img width="1221" height="921" alt="Cuplikan layar 2025-10-16 172312" src="https://github.com/user-attachments/assets/6683db74-1a54-44cb-b47d-a6280ff4e006" />

## Membuat tampilan about

Bagian `<header>` menampilkan judul halaman, sedangkan `<nav>` berisi menu navigasi agar pengguna dapat berpindah ke halaman lain seperti Home, Artikel, dan Kontak. Pada bagian `<section id="main">`, terdapat dua bagian utama yaitu deskripsi singkat tentang tujuan website dan daftar portfolio berupa beberapa project yang pernah dibuat. Terakhir, `<footer>` menampilkan informasi hak cipta di bagian bawah halaman. Seluruh elemen dibungkus dalam `<div id="container">` agar layout lebih teratur dan mudah diatur tampilannya dengan CSS.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tentang Kami</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div id="container">
        <header>
            <h1>Tentang Kami</h1>
        </header>

        <nav>
            <a href="home.html">Home</a>
            <a href="about.html" class="active">About</a>
            <a href="artikel.html">Artikel</a>
            <a href="kontak.html">Kontak</a>
        </nav>

        <section id="main">
            <h2>Deskripsi</h2>
            <p>Website ini dibuat sebagai latihan dasar layout menggunakan HTML5 dan CSS Float.</p>

            <h2>Portfolio</h2>
            <ul>
                <li>Project 1 - Desain Web</li>
                <li>Project 2 - Sistem Informasi Penjualan</li>
                <li>Project 3 - Aplikasi kalkulator</li>
            </ul>
        </section>

        <footer>
            <p>&copy; 2025 - Universitas Pelita Bangsa</p>
        </footer>
    </div>
</body>
</html>
```

<img width="1223" height="451" alt="image" src="https://github.com/user-attachments/assets/f69b1c9f-b2bb-4efd-b148-1d8b1dcb4f07" />

## Membuat tampilan artikel

Bagian `<header>` menampilkan judul utama situs, sedangkan `<nav>` berisi menu navigasi agar pengguna bisa berpindah ke halaman lain seperti Home, About, dan Kontak. Pada bagian `<main>`, terdapat dua artikel yang ditulis menggunakan tag `<article>`. Masing-masing artikel memiliki judul, gambar, dan paragraf isi. Artikel pertama menampilkan gambar di kiri, sedangkan artikel kedua menggunakan kelas `right-img` agar gambar berada di kanan. Di sisi kanan halaman terdapat `<aside>` yang berisi *widget* berjudul “Artikel Lain” yang menampilkan daftar tautan artikel tambahan. Terakhir, bagian `<footer>` menampilkan informasi hak cipta di bagian bawah halaman. Semua elemen dibungkus dalam `<div id="container">` agar tata letaknya rapi dan mudah diatur dengan CSS.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Artikel</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div id="container">
    <header>
      <h1>Layout Sederhana</h1>
    </header>

    <nav>
      <a href="home.html">Home</a>
      <a href="artikel.html" class="active">Artikel</a>
      <a href="about.html">About</a>
      <a href="kontak.html">Kontak</a>
    </nav>

    <section id="wrapper">
      <section id="main">
        <article class="entry">
          <h2>Judul Artikel Pertama</h2>
          <img src="https://dummyimage.com/150/7b8a70/fff.png" alt="">
          <p>
            Ini adalah contoh artikel pertama. Kamu bisa menuliskan isi artikel atau berita di sini.
            Artikel ini menggunakan elemen <code>&lt;article&gt;</code> yang termasuk bagian dari HTML5 semantic element.
          </p>
        </article>

        <hr class="divider">

        <article class="entry">
          <h2>Judul Artikel Kedua</h2>
          <img src="https://dummyimage.com/150/3e73e6/fff.png" alt="" class="right-img">
          <p>
            Ini adalah contoh artikel kedua. Kamu bisa menambahkan gambar dan teks sesuai kebutuhan.
            Gambar bisa berada di kiri atau kanan sesuai kelas CSS yang digunakan.
          </p>
        </article>
      </section>

      <aside id="sidebar">
        <div class="widget-box">
          <h3 class="title">Artikel Lain</h3>
          <ul>
            <li><a href="#">Tips Desain Web</a></li>
            <li><a href="#">Belajar CSS Layout</a></li>
            <li><a href="#">Responsive Design</a></li>
          </ul>
        </div>
      </aside>
    </section>

    <footer>
      <p>&copy; 2025 - Universitas Pelita Bangsa</p>
    </footer>
  </div>
</body>
</html>
```

<img width="1219" height="921" alt="image" src="https://github.com/user-attachments/assets/baa61c7c-05bf-4274-b7cf-7657da2a49e1" />

## Membuat tampilan kontak

Kode ini membuat halaman “Kontak Kami” yang berfungsi sebagai tempat pengguna mengirim pesan atau pertanyaan. Bagian `<header>` menampilkan judul halaman, sedangkan `<nav>` berisi menu navigasi untuk berpindah ke halaman lain seperti Home, Artikel, dan About. Pada bagian `<section id="main">`, terdapat formulir kontak yang dibuat menggunakan elemen `<form>`. Di dalamnya terdapat input untuk nama, email, serta kolom teks `<textarea>` untuk menulis pesan. Tombol `<button type="submit">` digunakan untuk mengirim data formulir. Terakhir, bagian `<footer>` menampilkan teks hak cipta di bawah halaman. Semua elemen dibungkus dalam `<div id="container">` agar tampilan halaman rapi dan terpusat.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Kontak Kami</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div id="container">
        <header>
            <h1>Kontak Kami</h1>
        </header>

        <nav>
            <a href="home.html">Home</a>
            <a href="artikel.html">Artikel</a>
            <a href="about.html">About</a>
            <a href="kontak.html" class="active">Kontak</a>
        </nav>

        <section id="main">
            <h2>Hubungi Kami</h2>
            <form>
                <label>Nama:</label><br>
                <input type="text" name="nama" placeholder="Masukkan nama"><br><br>

                <label>Email:</label><br>
                <input type="email" name="email" placeholder="Masukkan email"><br><br>

                <label>Pesan:</label><br>
                <textarea name="pesan" rows="5" placeholder="Tulis pesan Anda..."></textarea><br><br>

                <button type="submit">Kirim</button>
            </form>
        </section>

        <footer>
            <p>&copy; 2025 - Universitas Pelita Bangsa</p>
        </footer>
    </div>
</body>
</html>
```

<img width="1221" height="629" alt="image" src="https://github.com/user-attachments/assets/72e7c461-7e6c-4ad9-9382-03ce8c5e4378" />
