# Lab7Web PHP Dasar
## Nama : Rony Eltom Atibaman
## NIM : 312010003
## Kelas : TI.20.D.1

### Instal XAMPP
* Unduh XAMPP dari http://www.apechefriends.org/download.html dan pilih versi portable untuk memudahkan proses instalasi. kemudian exctract file tersebut, sesuaikan directorinya (misal: c:\xampp).<br>
![Gambar1](screenshot/a.png)<br>

### Menjalankan Web Server
* untuk menjalankan web server dari menu XAMPP Control<br>
![gambar2](screenshot/b.png)<br>

### Memulai PHP
* Buat folder lab7_php_dasar pada root directory web server (c:\xampp\hotdocs).<br>
![gambar3](screenshot/c.png)<br>
* kemudian untuk mengakses directory tersebut pada web server dengan mengakses URL:http://localhost/lab7_php_dasar/ <br>
![gambar4](screenshot/d.png)

### PHP Dasar
* Buat file baru dengan nama php_dasar.php pada directory tersebut. Kemudian buat kode seperti berikut.<br>
```<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
   <title>PHP Dasar</title>
</head>
<body>
    <h1>Belajar PHP  Dasar</h1>
    <?php
        echo "Hello World";
    ?>
</body>
</html>
```

> kemudian untuk mengakses hasilnya melalui URL: http://localhost/lab7_php_dasar/php_dasar.php<br>

contoh gambar:<br>
![gambar5](screenshot/2.png)

### variable PHP
* Menambahkan variable pada program.
``` <h1>Menggunakan Variabell</h1>
    <?php
    $nim = "312010003";
    $nama = 'Rony Eltom Atibaman';
    echo "NIM : " . $nim . "<br>";
    echo  "Nama : $nama";
    ?> 
```
contoh gambar :<br>
![gambar6](screenshot/4.png)

### Predefine Variable
``` <?php
    echo 'Selamat Datang ' . $_GET['nama'];
    ?>
```
> untuk mengaksesnnya gunakan URL: http://localhost/lab7_php_dasar/latihan2.php?nama=Rony <br>

contoh gambar:<br>
![gambar7](screenshot/6.png)

### Membuat Form Input
* form di HTML dapat kita buat dengan tag `<form>`. tag ini memiliki beberapa atribut yang harus diberikan, seerti: `action` untuk menentukan aksi yang akan dilakukan saat data dikirim: `method` metode pengiriman data.

```<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    
    <title>PHP Dasar</title>
</head>
<body>
<h2>Form Input</h2>
<form method="post">
    <label>nama: </label>
    <input type="text" name="nama">
     <input type="submit" value="kirim">
</form>
    <?php
    echo 'Selamat Datang ' . $_GET['nama'];
    ?>
    
</body>
</html>
```
> contoh gambar:<br>
![gambar8](screenshot/8.png)

### Operator
* Membuat operator pada program.

```<h1>Operator</h1>
    <?php
    $pajak = 0.1 ;
    $gaji = 1000000;
    $thp = $gaji - ($gaji * $pajak);
        echo "Gaji sebelum pajak = Rp. $gaji <br>";
        echo "Gaji yang dibawa pulang = Rp. $thp";
    ?>
```
> contoh gambar:<br>
![gambar9](screenshot/10.png)

### Kondisi IF
* Pengambilan keputusan (kondisi IF) digunakan untuk mengantisipasi kondisi yang terjadi saat jalannya program dan menentukan tindakan apa yang akan diambil sesaui dengan kondisi.
```<h1>Kondisi IF</h1>
    <?php
    $nama_hari = date("1");
    if ($nama_hari == "Sunday") {
        echo "Minggu";
    } elseif ($nama_hari == "Monday") {
        echo "Senin";
    } else {
        echo "Selasa";
    }
    ?>
```
> contoh gambar:<br>
![gambar10](screenshot/12.png)

### Kondisi Switch
* kondisi SWITCH CASE adalah percabangan kode program dimana kita membandingkan isi sebuah variabel dengan beberapa nilai. jika proses perbandingan tersebut menghasilkan true, maka block kode program akan di proses.

```<h1>Kondisi Switch</h1>
    <?php
    $nama_hari =date("1");
    switch ($nama_hari) {
        case "Sunday":
            echo "Minggu";
            break;
        case "Monday" :
            echo "Senin";
            break;
        case "tuesday":
            echo "Selasa";
            break;
        default :
            echo "Sabtu"; }
    ?>
```
> contoh gambar:<br>
![gambar11](screenshot/14.png)

### Perulangan for 
* perulangan for biasanya menggunakan suatu variabel untuk mengendalikan berapa kali tubuh loop akan dieksekusi dan menentukan kapan loop akan berhenti.

```<h1>Perulangan For</h1>
    <?php
    echo "Perulangan 1 sampai 10 <br />";
    for ($i=1; $i<=10; $i++) {
        echo "Perulangan ke: " . $i . '<br />';
    }

    echo "Perulangan Menurun dari 10 ke 1 <br />";
    for ($i=10; $i>=1; $i--) {
        echo "Perulangan ke: " . $i . '<br />';
    }
    ?>
```
> contoh gambar: <br>
![gambar12](screenshot/16.png)

### Perulangan While
* perulangan while adalah perulangan yang bersifat indefinite alias tidak pasti, atau bahkan tidak terbatas. Sebuah blok kode akan dilakukan terus-menerus selama suatu kondisi terpenuhi. Jika suatu kondisi ternyata tidak terpenuhi pada interasi ke 10, maka perulangan akan berhenti.

```<h1>Perulangan while</h1>
    <?php
    echo "Perulangan 1 sampai 10 <br />";
    $i=1;
    while ($i<=10) {
        echo "Perulangan ke : " . $i . '<br />';
        $i++;
    }
    ?>
```
> contoh gambar:<br>
![gambar13](screenshot/18.png)

### Perulangan do While
* Perulangan DO While merupakan modifikasi dari perulangan WHILE, yakni dengan memindahkan posisi pemeriksaan kondisi ke akhir perulangan. Artinya, lakukan dulu sebuah perulangan, beru periksa apakah kondisi variabel counter sudah terpenuhi atau belum di akhir perulangan.

```<h1>Perulangan dowhile</h1>
    <?php
    echo "Perulangan 1 sampai 10 <br />";
    $i=1;
    do {
        echo "Perulangan ke : " . $i . '<br />';
        $i++;
    } while ($i<=10);
    ?>
```
> contoh gambar:<br>
![gambar14](screenshot/20.png)



