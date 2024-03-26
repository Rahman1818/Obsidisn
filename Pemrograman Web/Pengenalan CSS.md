

# percobaan kedua 

# Anatomi CSS

## Kode Program 
```CSS
.merah{
color:red;
}
```
#  ​Hasil
![[Screenshot_20240304-110326_Acode 1.jpg]]

# Percobaan I
# Kode Program
```HTML
<!DOCTYPE html>
<html>
    <head>
        <title>Belajar CSS 1</title>
        <style>
            p {
                color: red;
            }
        </style>
    </head>
    <body>
        <p>Welcome CSS</p>
    </body>
</html>
```

# Hasil
![](aset/cssss5.png)


# Penjelasan
1. `<!DOCTYPE html>`: Mendefinisikan jenis dokumen HTML yang digunakan, dalam hal ini HTML5.
2. `<html>`: Elemen utama yang memuat seluruh konten dokumen.
3. `<head>`: Bagian yang berisi informasi tambahan tentang dokumen, seperti judul dan link ke stylesheet eksternal.
4. `<title>`: Menentukan judul halaman web yang akan ditampilkan di tab browser.
5. `<style>`: Bagian di mana Anda dapat menambahkan aturan CSS untuk mengubah tampilan elemen HTML di halaman.
6. `p { color: red; }`: Aturan CSS yang mengubah warna teks pada semua elemen `<p>` menjadi merah.
7. `<body>`: Bagian yang berisi konten aktual halaman web, seperti teks, gambar, atau elemen lainnya.
8. `<p>Welcome CSS</p>`: Elemen paragraf dengan teks "Welcome CSS", yang akan ditampilkan dengan warna merah karena aturan CSS yang telah ditentukan sebelumnya.


# Percobaan II
## Kode Program
```css
button{
                width: 150px;
                height: 50px;
                color: white;
                font-size: 20px;
                text-align: right;
            }
```

## Color

### Before

![](aset/cssss1.png)

  

### After

![](aset/cssss3.png)

  

> [!Penjelasan] Penjelasan
> Gambar before merupakan gambar yang menunjukkan bahwa tag button nya belum di modifikasi sedangkan pada gambar after merupakan gabar yang menunjukkan bahwa tag button nya sudah di modifikasi dengan menggunakan property color   
  
## Font-size
### Before

![](aset/cssss1.png)
    
### After

![](aset/cssss2.png)

> [!NOTE] Penjelasan
> Jadi gambar before yang diatas merupakan gambar yang dimana tag button belum di modifikasi sedangkan gambar after merupakan gambar yang dimana tag button sudah di modifikasi dengan menggunakan property Font-size    
  

## Text-align

### Before

![](aset/cssss1.png)
### After

![](aset/cssss4.png)

> [!NOTE] Penjelasan
> Jadi gambar before merupakan gambar yang dimana tag button nya belum di modifikasi sedangkan gambar after merupakan gambar yang dimana tag button nya telah di modifikasi dengan menggunakan property Text-align
# Cara Pemanggilan CSS
Cara untuk memanggil css ke html ada 3 cara yaitu inline, internal, dan external.

## Inline
jadi Inline merupakan salah satu cara untuk memanggil css yaitu dengan cara memanggilnya kedalam baris yang sama dengan tag yang ingin di modifikasi contoh

### Kode Program
```CSS

```


# Selector


# Materi Text


# Materi Backgraund


# Materi Font
# kode css

```css
<!DOCTYPE html>
<html>
  <head>
    <title>pengenalan css</title>
  </head>
  <body>
    <style>
      p{
        color: red
        ;
      }
        button{
        width: 150px;
        height: 50px;
        color: blue;
        font-weight: bold;
      font-size: 25px;;
      }
        
      
    </style>
    <p>welcom css</p>
    <p>welcom css</p>
    
    <button>klik aku</button>
  </body>
</html>
```

## color
```css
button{
        width: 150px;
        height: 50px;
        color: blue;
      }
```
Penjelasan:
- `width: 150px;`: Properti ini mengatur lebar dari elemen `<button>` menjadi 150 piksel. Ini akan membuat tombol memiliki lebar sebesar 150 piksel.
- `height: 50px;`: Properti ini mengatur tinggi dari elemen `<button>` menjadi 50 piksel. Ini akan membuat tombol memiliki tinggi sebesar 50 piksel.
- `color: blue;`: Properti ini mengatur warna teks pada tombol menjadi biru. Dengan demikian, teks yang terdapat pada tombol akan ditampilkan dalam warna biru.`color: blue;`: Properti ini mengatur warna teks pada tombol menjadi biru. Dengan demikian, teks yang terdapat pada tombol akan ditampilkan dalam warna biru.

Contoh hasil:
![[Screenshot_20240219-120707_Acode.jpg]]
### font-weight 
```css
button{
        width: 150px;
        height: 50px;
        font-weight: bold;
      }
```
Penjelasan:
- `font-weight: bold;`: Properti ini mengatur ketebalan teks pada tombol menjadi tebal atau bold. Dengan demikian, teks pada tombol akan ditampilkan dengan ketebalan yang lebih besar dari biasanya.

Contoh hasil:
![[Screenshot_20240219-121449_Acode.jpg]]
#### font - size
```css
button{
        width: 150px;
        height: 50px;
        font-size: 30px;
      }
```
Penjelasan:

- `font-size: 30px;`: Properti ini mengatur ukuran teks pada tombol menjadi 30 piksel. Dengan demikian, teks pada tombol akan ditampilkan dalam ukuran yang lebih besar dari biasanya.

Contoh hasil:
![[Screenshot_20240219-122027_Acode.jpg]]

