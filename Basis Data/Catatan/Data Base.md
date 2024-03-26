# Installing Termux
- untuk memulai database kalian harus download aplikasi **Termux**
 - pergi ke Chrome dan search **download termux**
 -  pilih web **F -Droid**
 -  lalu skrol dan bagian bawa ada unduh apk
 -  dan tunggu sampai selesai mendownload.
 -  Masuk ke apk termux

1.  berikan akses penyimpanan dengan mengetik **termux - setup - storage** lalu klik "allow". Dengan begitu termux telah mendapat akses untuk penyimpanan pasa handphone.
2. Lakukan upgrade&& update dengan mengetik **pkg update && upgrade -y** dan setelah nya klik "y" untuk mengkonfirmasi sampai proses selesai
3. Install mariadb dengan mengetik **pkg install mariadb** dan seperti sebelumnya ketik "y" untuk mengkonfirmasi.
4. Langkah selanjutnya ialah memberikan akses aman dengan mengetik **mysqld_safe** dan jika program tidak merespon lakukan **ctrl + Z** untuk mengulang lalu ketik **mysqld_safe**. 
![[Screenshot_20240130-133949_Termux.jpg]]
5. Setelah itu ketik **mysqld -u root** untuk masuk ke mariadb
![[IMG-20240130-WA0011.jpg]]
6. Tahap penginstalan sdh selesai dan siap digunakan untuk membuat database 

## membuat database
untuk membuat database kita menggunakan query `CREATE_DATABASE [nama_database]` setelah langkah ini *database*
akan terbuat.

## menampilkan database
untuk menampilkan *data base* kita bisa menggunakan `SHOW_DATABASES;` untuk menampilkan data base yang telah digunakan.
Contoh gambar:
![[Screenshot_20240130-141806_Termux.jpg]]

## menghapus database
lalu untuk menghapus *data base* kita menggunakan query `DROP DATABASE [nama_database]`dan *database* akan terhapus setelah menuliskan query ini.
Contoh gambar:
![[Screenshot_20240130-142117_Termux.jpg]]


## menggunakan database 
lalu yang terakhir untuk menggunakan *database* kita menggunakan query `USE [nama_database]`.
Contoh gambar: 
![[Screenshot_20240130-141608_Termux.jpg]]

# TIPE DATA 

## Angka
- INT: Untuk menyimpan nilai bilangan bulat (integer). Misalnya, INT dapat digunakan untuk menyimpan angka
  seperti 1, 100, -10, dan sebagainya.
- DECIMAL: Digunakan untuk menyimpan nilai desimal presisi tinggi, cocok untuk perhitungan finansial atau keuangan.
- FLOAT dan DOUBLE: Digunakan untuk menyimpan nilai desimal dengan presisi floating-point. DOUBLE memiliki.
presisi lebih tinggi dibandingkan FLOAT.
- TINYINT , SMALLINT , MEDIUMINT , dan BIGINT: Tipe data ini menyimpan bilangan bulat dengan ukuran yang berbeda-beda.
Contoh :
CREATE TABLE contoh_tabel (
id INT,
harga DECIMAL(10, 2),
jumlah_barang TINYINT
);

-  Dalam contoh tersebut, id menggunakan tipe data INT, harga menggunakan tipe data DECIMAL dengan presisi 10 digit dan 2 angka di belakang koma, dan jumlah_barang menggunakan tipe data TINYINT.

## Teks
- CHAR(N) Menyimpan string karakter tetap dengan panjang N. Contoh: CHAR(10) akan menyimpan string dengan panjang tepat 10 karakter.
- VARCHAR(N): Menyimpan string karakter dengan panjang variabel maksimal N. Misalnya, VARCHAR(255) dapat menyimpan string hingga 255 karakter, tetapi sebenarnya hanya menyimpan panjang yang diperlukan plus beberapa overhead.
- TEXT: Digunakan untuk menyimpan teks dengan panjang variabel, tanpa batasan panjang tertentu. Cocok untuk data teks yang panjangnya tidak terduga.
- ENUM: Memungkinkan Anda mendefinisikan set nilai yang mungkin dan membatasi kolom hanya dapat mengambil salah satu dari nilai tersebut.
- SET: Mirip dengan ENUM, namun dapat menyimpan satu atau lebih nilai dari himpunan yang telah ditentukan
Contoh :
CREATE TABLE contoh_tabel (
nama CHAR(50),
alamat VARCHAR(100),
catatan TEXT,
status ENUM('Aktif', 'Non-Aktif')
);

## Tanggal 
- DATE : Menyimpan nilai tanggal dengan format YYYY-MM-DD.
-  TIME : Menyimpan nilai waktu dengan format HH:MM:SS.
- DATETIME : Menggabungkan nilai tanggal dan waktu dengan format YYYY-MM-DD HH:MM:SS.
- TIMESTAMP :Sama seperti DATETIME, tetapi dengan kelebihan diatur secara otomatis saat data dimasukkan atau diubah.
Contoh :
CREATE TABLE ContohTabel (
tanggal DATE,
waktu TIME,
datetimekolom DATETIME,
timestampkolom TIMESTAMP
);
## Boolean

- ==BOOL / BOOLEAN / TINYINT(1):== Digunakan untuk menyimpan nilai boolean, yang dapat mewakili kebenaran atau kesalahan. Representasi nilai benar adalah 1, sedangkan nilai salah direpresentasikan sebagai 0. Meskipun nilai selain 0 dianggap benar, secara umum, ketiganya seringkali digunakan secara bergantian. Seringkali, ketika Anda mendeklarasikan kolom sebagai BOOL atau BOOLEAN, MySQL mengonversinya secara otomatis menjadi TINYINT(1), yang juga dapat digunakan untuk menyimpan nilai boolean dengan 0 untuk false dan 1 untuk true.

1. Menggunakan BOOLEAN
sql
CREATE TABLE contohTabel (
    title VARCHAR(255),
    completed BOOLEAN
);
Dalam contoh diatas, kita mendefinisikan kolom completed sebagai tipe data BOOLEAN. Ini merupakan cara yang sah dan umum digunakan di MySQL. Nilai yang dapat disimpan dalam kolom ini adalah TRUE atau FALSE, atau dalam representasi angka, 1 atau 0.

2. Menggunakan BOOL
sql
CREATE TABLE contohTabel (
    title VARCHAR(255),
    completed BOOL
);

Dalam contoh ini, kita menggunakan BOOL sebagai tipe data untuk kolom completed. Perlu dicatat bahwa MySQL secara otomatis mengonversi BOOL menjadi TINYINT(1). Oleh karena itu, pada dasarnya, ini setara dengan contoh pertama. Namun, beberapa pengembang lebih suka menggunakan BOOLEAN untuk kejelasan.

3. Menggunakan TINYINT(1)
sql
CREATE TABLE contohTabel (
    title VARCHAR(255),
    completed TINYINT(1)
);

Dalam contoh ini, kita menggunakan TINYINT(1) sebagai tipe data untuk kolom completed. Ini adalah pendekatan yang valid karena MySQL mengonversi BOOL menjadi TINYINT(1) secara otomatis. Dalam hal ini, nilai yang dapat disimpan adalah 1 untuk TRUE dan 0 untuk FALSE.

# TABEL
Tabel adalah suatu struktur data dalam bentuk baris dan kolom yang digunakan untuk menyajikan informasi secara terstruktur. Dalam konteks HTML atau database, tabel terdiri dari sel-sel yang membentuk baris dan kolom.

## buat tabel
Untuk pembuatan table kita menggunakan format seperti di bawa ini:
```sql
create table pelanggan (
Id_pelanggan int(4) primery key not null,
Nama_depan varchar(25) not null,
Nama_belakang varchar(25) not null,
No_telp char(12) unique);


```
contoh kode :

![[Screenshot_20240130-153348_Termux.jpg]]
## tampilkan struktur tabel
Lalu setelah  membuat tabelkita dapat menampilkan struktur dari table yang telah kita buat dengan cara mengetik `DESC [nama_table]` dan hasilnya akan seperti berikut:
![[Screenshot_20240130-153845_Termux.jpg]]
**SHOW tables:**
Untuk menampilkan daftar tabel yang ada dalam database kita menggunakan query `SHOW TABLES;` dan hasil  yang akan tampil seperti berikut:
![[Screenshot_20240130-153727_Termux 1 1.jpg]] 

Pertanyaan:

1) **Mengapa hanya kolom id_pelanggan yang menggunakan constraint PRIMARY KEY?**
2) **Mengapa pada kolom no_telp yang menggunakan data CHAR bukan VARCHAR?**
3)  **Mengapa hanya kolom no_telp yang menggunakan constraint UNIQUE?**
4)  **Mengapa kolom no_telp tidak memakai constraint NOT NULL sementara kolom lainnya menggunakan constraint tersebut?**
5) **Tuliskan perbedaan antara PRIMARY KEY dengan UNIQUE?**

Jawaban:

1) Untuk membedakan id Pelanggan  yang sama, mencegah duplikasi, dan mempermudah pencarian data.
2) Tipe data char menyimpan data dalam karakter panjang lebih efisien. pencarian pada kolom tipe data `CHAR` dapat lebih cepat
3) Karna no_telp tidak ada yang sama semua pasti berbeda dan nilainya unik maka menggunakan constrains unique artinya data dalam tabel id_telpon berbeda tidak ada yang sama. 
4) Nomor telpon dianggap opsional. nomor telepon hanya menjadi wajib saat pengguna melakukan langkah-langkah tertentu, Anda mungkin tidak ingin mengharuskan pengguna mengisinya pada tahap awal.
5) PRIMERY KEY untuk membedakan data yang sama dan hanya boleh 1 dan tidak boleh tidak ada. Kalau UNiQUE sebuah kolom yang memiliki data yang berbeda atau tidak sama unique boleh 1,2,3 Dan seterusnya dan boleh tidak ada.

## INSERT
Setelah mempelajari cara untuk membuat, melihat struktur dan menampilkan daftar table sekarang kita akan mempelajari cara memasukan data pada table serta menampilkan hasil dari table tersebut, untuk melakukannya kita akan membaginya menjadi dua bagian yaitu Insert dan Select.
**STRUKTUR**:
```mysql
INSERT INTO [NAMA_TABEL]
VALUES (nilai1, nilai2,nilai3)
```

**CONTOH**:
```mysql
Insert into pelanggan
Values 
(2,"rahmat","ramadhan","09876123452")

```

**analisa**:
  
`Insert`adalah istilah yang sering digunakan dalam konteks basis data dan pengolahan data. Ini mengacu pada operasi untuk menambahkan data baru ke dalam tabel atau struktur data lainnya.


![[Screenshot_20240220-140731_Termux.jpg]]
**KESIMPULAN :
Kesimpulannya ialah **insert** bertugas untuk memasukkan nilai pada table yang telah dibuat dan **Select** berfungsi untuk menampilkan hasil dari table yang telah dibuat dan di input datanya dari *Query* sebelumnya, lalu **Select** ini dapat menampilkan semua sesuai dengan yang kita menggunakan misalnya jika ingin menampilkan seluruh table kita menggunakan simbol "`*`" atau All lalu jika ingin menampilkan beberapa field kita dapat menggunakan format hanya perlu memanggil nama fieldnya.

Lalu yang terakhir ialah kondisi "Where" dimana kita dapat memanggil nama field dengan menggunakan simbol aritmatika, misalnya kita ingin memanggil field "Nama_Pelanggan" tapi hanya ''Id_Pelanggan" 2 kita dapat menggunkan format seperti ini `SELECT Nama_Kolom FROM Nama_Table WHERE Id_Pelanggan=2;`

## SELECT 
untuk menampilkan hasil dari seluruh table yang telah dibuat/menampilkan seluruh baris dan kolom kita menggunakan format seperti dibawah ini :

```mysql 
SELECT * from [nama_tabel]
```

Hasil nya akan seperti berikut:
![[Screenshot_20240213-141524_Termux 3.jpg]]

Analisa:

## SELECT lanjutan

SELECT AND adalah sebuah jenis select yang berfungsi untuk menampilka

AND 
```mysql 
SELECT [nama_kolom],[nama_kolom],from [nama_tabel]WHERE [nama_kolom]= nilai1 And [nama_kolom]= nilai2;
```
CONTOH:
```mysql 
 select warna,pemilik from mobil where warna="merah" and pemilik="rehan";
```
**analisa**:
`AND`adalah operator logika yang digunakan dalam SQL (Structured Query Language) dan dalam banyak bahasa pemrograman lainnya. Dalam SQL, "AND" digunakan untuk menggabungkan dua atau lebih kondisi dalam klausa `WHERE`, yang menentukan kriteria pencarian untuk data yang akan diambil atau diubah.
![[Screenshot_20240220-143301_Termux.jpg]]

## UPDATE
Jika ingin mengganti nilai dari sebuah kolom tertentu kita bisa menggunakan Query Update lalu formatnya seperti berikut:
```mysql
Format:
>UPDATE [nama_tabel] SET [nama_kolom]="nilai_pengganti" WHERE kondisi

Contoh:
>UPDATE pelanggan SET No_telp="098612345432" WHERE id pelanggan;
```
Analisa:
`UPDATE`adalah pernyataan dalam bahasa SQL yang digunakan untuk mengubah atau memperbarui data yang sudah ada dalam satu atau lebih baris dalam tabel. Dengan menggunakan pernyataan UPDATE, Anda dapat mengubah nilai-nilai dalam kolom yang ada berdasarkan kriteria tertentu.



Contoh  pengaplikasian dan hasil dari penggunaan update:
![[Screenshot_20240213-141528_Termux.jpg]]


## DELETE
kita juga dapat menghapus baris pada tabel dengan Query delete berikut formatnya:
```mysql
Format:
>DELETE FROM [nama_tabel] WHERE [nama_kolom];

Contoh:
>DELETE FROM pelanggan WHERE id pelanggan=3;
```
Analisa:
`DELETE` adalah pernyataan dalam bahasa SQL yang digunakan untuk menghapus satu 0atau lebih baris data dari sebuah tabel dalam basis data. Dengan menggunakan pernyataan DELETE, Anda dapat menghapus data yang tidak diperlukan atau data yang tidak lagi relevan dari tabel. Misalnya, Anda dapat menghapus baris-baris yang memenuhi kondisi tertentu.

KESIMPULAN:


Contoh  pengaplikasian dan hasil dari penggunaan delete:

![[Screenshot_20240213-141941_Termux.jpg]]

# OR
### STRUKTUR
```mysql
select nama_kolom1,nama_kolom2 from nama_tabel where nama_kolom3"nilai_kolom1" or nama_kolom4"nilai_kolom2";
```

#### CONTOH
```mysql
select warna,pemilik from desc_mobil where warna="Hitam" or pemilik="Ibrahim";
```

#### HASIL 
![[Screenshot_20240220-143301_Termux.jpg]]

#### ANALISIS
-  `SELECT`: Ini adalah kata kunci yang digunakan untuk memilih kolom-kolom tertentu dari tabel.
-  `warna, pemilik`: Ini adalah daftar kolom yang dipilih untuk diekstraksi dari tabel `desc_mobil`. Dalam hal ini, kita akan mendapatkan nilai dari kolom `warna` dan `pemilik`.
-  `FROM desc_mobil`: Ini menentukan bahwa data akan diambil dari tabel bernama `desc_mobil`.
-  `WHERE`: Ini adalah kata kunci yang digunakan untuk memberikan kriteria seleksi untuk baris-baris yang akan diambil. Hanya baris-baris yang memenuhi kriteria ini yang akan ditampilkan.
-  `warna="Hitam" or pemilik="Ibrahim"`: Ini adalah kriteria seleksi. Ini berarti kita hanya ingin baris-baris di mana nilai kolom `warna` adalah "Hitam" atau nilai kolom `pemilik` adalah "Ibrahim".

#### KESIMPULAN

Jadi, secara keseluruhan, ini akan mengembalikan semua baris dari tabel `desc_mobil` di mana nilai kolom `warna` adalah "Hitam" atau nilai kolom `pemilik` adalah "Ibrahim", dan hanya kolom `warna` dan `pemilik` yang akan ditampilkan.

# BETWEEN-AND

#### STRUKTUR 
```mysql 
select * from nama_tabel where nama_kolom not between nilai_kolom1 and nilai_kolom2;
```
#### CONTOH
```MYSQL
select * from desc_mobil where harga_rental not between 100000 and 200000;
```

#### ANALISIS
- `SELECT *` : Memilih semua kolom dari tabel.
 
 - `FROM desc_mobil`: Menentukan tabel yang digunakan untuk melakukan seleksi, yaitu tabel desc_mobil.

- `WHERE harga_rental NOT BETWEEN 100000 AND 200000`: Mengaplikasikan kondisi dimana nilai dalam kolom harga_rental tidak berada di antara 100.000 dan 200.000.

Jadi, hasil query akan mengembalikan semua baris dari tabel desc_mobil dimana nilai dalam kolom harga_rental tidak berada di antara 100.000 dan 200.000.
#### KESIMPULAN 
memilih semua entri dari tabel `desc_mobil` di mana nilai kolom `harga_rental` tidak berada di antara 100.000 dan 200.000. Ini akan mengambil semua data mobil yang memiliki harga sewa di luar rentang tersebut.
