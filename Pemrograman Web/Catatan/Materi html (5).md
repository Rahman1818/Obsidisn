# struktur dasar
## contoh program 

```html
<!DOCTYPE html>
<html>
  <head>
    <title>ini adalah judul </title>
  </head>
  <body>
    <p> ini adalah paragraf</p>
  </body>
</html>
```

## hasil program
![[Screenshot_20240117-135709_Acode 1.jpg]]

## penjelasan program
- Tag<!DOCTYPE html> memberitahukan web browser bahawa dokumen **HTML** adalah versi 5.

- Tag pembuka ` <html>` menandai awal sebuah dokumen HTML sampai dengan tag penutup `</html>``
- Tag pembuka `<head>` berisi informasi tentang halaman penutup `</head>`biasanya dalam tag head terdapat tag `<title>` untuk memberikan judul HTML
- apapun Tag yang berada di tag pembuka `<body>`sampai dengan tag penutup `</body>`akan tampil di web browser








# ANATOMI Elemen HTML

## contoh program
```html
<!DOCTYPE html>
<html>
  <head>
    <title>ini adalah judul </title>
  </head>
  <body>
    <p> jika ingin login ke instagram klik link di bawah </p>
    <a href="https://www.instagram.com/"> login instagram</a>
  </body>
</html>
```
## hasil program

![[Screenshot_20240117-144258_Acode.jpg]]
![[Screenshot_20240124-092427_Acode.jpg]]
![[Screenshot_20240117-144258_Acode.jpg]]
![[Screenshot_20240124-092427_Acode.jpg]]
## penjelasan
- `<a href="https://www.instagram.com/">` merupakan tag pembuka.
- `href` merupakan *nama atribut*.
- `"https://www.instagram.com/"` merupakan *nilai atribut*.
- ==Login Instagram== merupakan *nama link*.
- `</a>` merupakan tag penutup




# Penjelasan tag

## Tag pembuka penutup

<> disebut sebagai tag dalam program, dan setiap tag memiliki fungsinya masing masing.
"<>" ialah tag pembuka dan "</ >" ialah tag penutup.

## Tag dasar 

```
<!DOCTYPE html> menunjukkan bahwa html yang digunakan ialah versi ke-5.
<html> berfungsi untuk menyusun dokumen html.
<head> ialah tag untuk menunjukkan kepala pada website.
<title>untuk membuat judul pada website.
<body> ialah tag untuk menunjukkan bada dari website.
```

## atribut dan isi  konten

`<a href="https://www.instagram.com/">` merupakan tag pembuka.
- `href` merupakan *nama atribut*.
- `"https://www.instagram.com/"` merupakan *nilai atribut*.
- ==Login Instagram== merupakan *nama link*.
- `</a>` merupakan tag penutup.
- terdapat juga *tag* yang tidak memerlukan *tag penutup*, contohnya seperti `<br>`.

## heading
`<h>` ialah teks heading yang memiliki 6 tingkat sesuai ketebalan dan ukurannya.
## paragraf

`<p>` ialah teks untuk membuat paragraf.
`<b>` ialah tag untuk mempertebal teks.
`<u>` ialah tag untuk menggaris bawahi teks.
`<i>` ialah tag untuk memiringkan teks.
`<br>` ialah tag untuk membuat barus baru.










# TAG list dan multimedia

## tag list
dalam html ada sebuah tag yang dapat membantu kita dalam membuat list dengan menggunakan tag `<ul>` dan tag `<ol>` tag ini memiliki fungsi yang sama yaitu membuat list namun memiliki perbedaan yaitu tag `<ul> `atau "unordered list"membuat list yang tidak beraturan, sedangkan `<ol> `atau "ordered list" membuat list yang beraturan. contohnya ialah seperti berikut :
Kode program:

```html
<!DOCTIPE htm>
<html>
  <head>
    <title>ini adalah judul</title>
  </head>
 <body>
   <p>list nama teman </p>
<ul>
<li>rahmat</li>
<li>rehan</li>
</ul>
  </body>
</html>
```

Hasil program:
![[Screenshot_20240124-110822_Acode.jpg]]

## menambah komentar
untuk membuat komentar yang tidak dapat di terlihat di browser dan hanya dapat di baca oleh programmer dengan cara contohnya seperti dibawah ini :
Kode program :
```html
<!DOCTIPE htm>
<html>
  <head>
    <title>ini adalah judul</title>
  </head>
 <body>
 <!--ini adalah beberapa orang-->
 <p>ini adalah sebuah teks dan akan di tampilkan pada browser
  </body>
</html>
```

## hasil program:
![[Screenshot_20240124-111255_Acode.jpg]]
dengan menuliskan komentar dapat membantu program untuk mengingat hal hal penting dan dapat dituliskan tanpa terbaca di browser.

## multimedia
untuk html kita dapat menambahkan foto video serta audio dalam vscode untuk dimasukkan di browser caranya ialah seperti berikut 

## menambah foto
untuk menambah foto pada teks editor A code kita menggunakan tag <img> dengan dibantu atribut "src" lalu masukkan lah link foto yang ingin dimasukkan. lalu untuk mengatur tinggi dan lebar dengan atribut tinggi : "height" dan lebar : "weight".
Kode program:
```html
!DOCTIPE htm>
<html>
  <head>
 <img src="https://img.antaranews.com/cache/800x533/2022/12/20/000_334T4YP-1.jpg.webp" width="300" height="300">
  </body>
</html>
```
Hasil program:
![[Screenshot_20240124-125023_Acode.jpg]]


# menambahkan vidieo
untuk menambah video pada teks editor A code kita menggunakan tag  dengan dibantu atribut "src" lalu masukkan lah link video yang ingin dimasukkan. lalu untuk mengatur tinggi dan lebar dengan atribut tinggi : "height" dan lebar : "weight".
Contoh program:
```html
<!DOCTYPE html>
<html>
   <head>
<title>Tag video</title> 
</head> 
 <body> 
<video src ="/Aset/Kelass.mp4" controls width="300"height="400">  </video>
  </body>
</html>
```
menampilkan elemen `<video>` untuk memutar video. Video yang ditampilkan berasal dari path "/Aset/Kelass.mp4".

Hasil program:
![[Screenshot_20240129-114941_Acode.jpg]]

# menambahkan audio

# halaman web lain
Elemen `<iframe>` dapat digunakan untuk menampilkan halaman website lain dalam suatu website. Atau menampilkan dokumen html dalam sebuah website. Mudah nya bisa di bilang website dalam website

**dalam tag `iframe` ada beberapa atribut yang penting seperti** :

- **src** untuk mencari sumber halaman html atau web yang akan di tampilkan di **iframe**
- **width dan haight** untuk mengatur ukuran pajang dan lebar dari frame

Contoh program:
```html
<!DOCTYPE html>
<html>
<head>
    <title>Pembuatan iframe</title>
</head>
<body>
    <iframe src="https://www.smkn7makassar.sch.id/" width="300" height="300"></iframe>
</body>
</html>
```
Hasil program:
![[Screenshot_20240129-132441_Acode.jpg]]

Penjelasan:
membuat halaman web dengan sebuah iframe. Iframe ini menampilkan konten dari situs web "``
[https://www.smkn7makassar.sch.id/](https://www.smkn7makassar.sch.id/)". Atribut "width" dan "height" mengatur ukuran iframe di halaman. Dengan menggunakan iframe.





# tabel
Tabel dalam html didefinisikan dengan tag `<table>`
- setiap baris tabel didefinisikan dengan tag `<tr>` .
- header (judul) tabel didefinisikan dengan tag `<th>`.secara default,header tabel memiliki teks tebal dan berada di tengah.
- data tabel/sel didefinisikan dengan tag `<td>`. Karena sel merupakan sel merupakan bagian terkecil dari tabel maka dari itu tag ini selalu berada di dalam tag `<tr>`.


Contoh program:
```html
<!DOCTYPE html>
<html>
<head>
    <title>Pembuatan Table </title>
</head>
<body>
   <table border="2">
    <tr>
        <th rowspan="2">Nama</th>
        <th colspan="2">Asal Institusi</th>
    </tr>
    <tr>
        <th>Sekolah</th>
        <th>Kampus</th>
    </tr>
    <tr>
        <td>Rahman</td>
        <td>SMA 16 Makassar</td>
        <td>Universitas Hasanuddin</td>
    </tr>
    <tr>
        <td>Hayril Abizali</td>
        <td rowspan="2">SMK 7 Makassar</td>
        <td align="center" rowspan="2">Kerja</td>
    </tr>
    <tr>
        <td>Rahmat Ramadhan</td>
    </tr>
    <tr>
        <td>Fachri Ramadhan</td>
        <td>MAN 1 Makassar</td>
        <td>Universitas Muhammadiyah</td>
   </table>
</body>
</html>
```

Hasil program:
![[Screenshot_20240129-133923_Acode.jpg]]
![[Screenshot_20240129-133923_Acode.jpg]]

Penjelasan:
-  Mempunyai dua sel kolom yang digabungkan dengan atribut "rowspan". Sel pertama berisi "Nama" dan selanjutnya, "Asal Institusi" yang di-colspan menjadi dua kolom.
    
- Memiliki dua sel kolom, masing-masing berisi "Sekolah" dan "Kampus".
    
-  Data yang terdiri dari Nama, Asal Sekolah, dan Asal Kampus, dimana beberapa sel digabungkan atau diatur menggunakan atribut "rowspan" dan "align".

# DIV&SPAN
## DIV
adalah elemen HTML yang digunakan untuk membuat suatu bagian atau blok di dalam halaman web. Ini adalah elemen pembungkus yang tidak memiliki arti khusus dalam halaman web, tetapi dapat digunakan untuk menata dan mengelompokkan konten bersama-sama dalam suatu blok. Elemen `<div>` sering digunakan bersama dengan CSS untuk mengatur tata letak dan gaya halaman web.

## SPAN

Di dalam konteks web development, elemen `<span>` digunakan sebagai kontainer inline untuk teks dan elemen lainnya. Ini berarti `<span>` tidak mengubah alur atau tata letak alami teks di sekitarnya seperti halnya elemen blok seperti `<div>`. Elemen `<span>` sering digunakan bersama dengan CSS untuk memberikan gaya atau memberikan identifikasi khusus pada bagian-bagian kecil dari teks atau elemen lain di dalam dokumen HTML.







