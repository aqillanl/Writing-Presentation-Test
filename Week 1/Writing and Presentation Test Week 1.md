# Writing and Presentation Test Week 1

## Unix Command Line 
- Shell merupakan program yang digunakan untuk berkomunikasi atau memerintah system
- Command Line Interface, jenis shell yang berbasis teks- Command Line merupakan sebutan untuk shell yang berbasis teks 
- Command Line Interface adalah mekanisme interaksi dengan sistem operasi atau perangkat lunak komputer dengan mengetikkan perintah untuk menjalankan tugas tertentu. Contohnya sh, bash, zsh, dan cmd.
### a. Navigasi menggunakan CLI
- Filesystem :
Sebuah filesystem mengatur bagaimana data disimpan di dalam sebuah system,
Sistem operasi Windows & Unix-like menyusun file dan direktori menggunakan struktur yang bentuknya mirip tree.
- Pwd (Print working directory) yaitu, Command untuk melihat current working directory 
- Ls (lists), Command yang digunakan untuk melihat isi file yang ada di sebuah direktori 
- Cd (change directory), digunakan untuk berpindah direktori.
### b. Manipulasi file dan directory
- Command “head”, “tail”, dan “cat” untuk isi files di awal, akhir, dan keseluruhan.
- Command “touch” untuk membuat file
- Command “mkdir”  untuk membuat directory
- Command “cp” untuk menyalin file, “cp -R” untuk menyalin directory
- Command “mv” untuk memindahkan file, “mv -R” untuk memindahkan directory
- Command “rm” untuk menghapus file, “rm -R” atau “rm -d” untuk menghapus directory.


## Git dan Github 
- GIT sebagai Version Control System, Version Control System Tugasnya adalah mencatat setiap perubahan pada File (termasuk code yang kita buat) pada suatu proyek baik dikerjakan secara individu maupun tim.
Contoh tempat penyimpanan git repository adalah Github, Gitlab, Bitbucket
- Perbedaan antara Git & Github yaitu Git yang bertugas untuk mencatat perubahan seluruh file atau repository suatu project, sedangkan GitHub merupakan layanan cloud yang berguna untuk menyimpan dan mengelola sebuah project.
### Alur kerja Git
yang pertama yaitu membuat perubahan terhadap file yang ada di dalam directory, directory ini disebut Working Directory, perubahan tersebut dapat berupa Penambahan, Memodifikasi dan Menghapus file. Yang kedua menyiapkan perubahan yang siap “disimpan”.Tahap ini disebut tahap Draft, didalam git istilah tersebut adalah “Staging”,files yang telah kita tambah,hapus atau modifikasi tidak akan langsung tersimpan kita harus menambahkan ke staging area. Yang ketiga adalah menyimpan draft perubahan yang kita buat,perubahan yang kita simpan disebut Commit.
### Command pada git
- Konfigurasi git  
  git config --global user.name "aqillanl"
  git config --global user.email "aqilla.x.rpl3@gmail.com" 
- Membuat Repository 
  git init (dilakukan didalam folder yang dibuat) 
- git Status digunakan untuk melihat apakah terjadi perubahan atau tidak pada Git 
- git add untuk menambah file baru/file yang telah diubah pada Git  
- git remote menghubungkan remote repository dengan project local yang telah kita buat direktorinya 
- git commit -m "commit message" digunakan untuk menyimpan perubahan pada Git
- git push -u origin master digunakan untuk mengirimkan/perubahan file ke remote repository 
- git branch -b [nama branch] digunakan untuk membuat branch baru
- git checkout digunakan untuk berpindah branch
- git merge digunakan untuk menggabungkan branch cabang ke branch master ( git merge origin/(nama branch))

## HTML
- HTML adalah singkatan dari Hypertext Markup Language. HTML digunakan untuk menampilkan konten pada browser. Contoh konten yang dapat ditampilkan seperti Text, Image, Video, Link, dan masih banyak lainnya.
- Tools yang dibutuhkan untuk membuat HTML Ada 2 tools utama yang harus dipersiapkan untuk membuat HTML Browser dan Code Editor.
Contoh  code editor yaitu Visual Studio Code, Visual Studio Code adalah code editor yang dikembangkan oleh tim engineer Microsoft.
### 1.	HTML Structure
``` 
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Aqilla Noor Lazuardi</title>
  </head>
  <body>
    <div>
      <h1 class="header">Hello Guys</h1>
      <p>Tech 4 Impact</p>
    </div>
  </body>
</html>
```

- HTML Element terdiri atas opening tag, content, dan closing tag 
Opening Tag :  `` <p> ``
Content     : Hello World 
Closing Tag : `` </p> ``
- HTML Attributes : properties dari sebuah element HTML. Contohnya yaitu id,class,name
- Single Tag atau singular tag 
``<br/>``  
`` <hr/> `` 
`` <img src= " " alt= " "/>``
- Paired Tag atau double Tag 
``<h1> </h1>``
- HTML Comment digunakan untuk memberi keterangan pada suatu line code `` <!--  --> ``
### 2.	HTML Tag popular
- Image
```html
<img src="image.jpg" alt="image">
```
- Video
```html
<video controls>
  <source src="video.mp4" type="video/mp4">
</video>
```
- Tabel 
```html
<table>
      <thead>
          <tr>
              <td>Nama</td>
              <td>Umur</td>
              <td>Hobby</td>
          </tr>
      </thead>
      <tbody>
          <tr>
              <td>Aqilla</td>
              <td>20 yo</td>
              <td>football</td>
          </tr>
      </tbody>
  </table>
```
### 3. Semantic HTML 
- Semantic HTML yaitu menggunakan elemen HTML sesuai dengan kebutuhan konten. Contoh yaitu header, footer, nav, section, aside, dll.
```html
<body>
      <!-- header artikel -->
      <header>
        <h1>Aqilla Noor lazuardi</h1>
      </header>
      <!-- navigasi artikel -->
      <nav>
        <a href="#">Home</a> |
        <a href="#">About</a> |
        <a href="#">Contact</a>
      </nav>
      <!-- isi artikel -->
      <article>
        <h1>Hallo Guys</h1>
        <p>Perkenalkan nama saya Aqilla Noor Lazuardi. kali ini aku sedang belajar membuat html.
        </p>
      </article>
      <!-- footer artikel -->
      <footer>
        Copyright &copy; 2022 by Aqilla
      </footer>
</body>
```

## CSS
- Apa itu CSS (Cascading Style Sheets), CSS adalah bahasa yang digunakan untuk mendesain halaman website. Dengan CSS, kita bisa mengubah warna, menggunakan font custom, editing text format, mengatur tata letak, dan lainnya
- Ada 3 cara bagaimana kita dapat menggunakan CSS tersebut yang pertama yaitu Inline Styles, Internal, dan Eksternal.
### 1. Inline Style
```html
<p style="color: blue">Coba inline css warna biru</p>
```
### 2. Internal style
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
    <style>
      body {
        background-color: silver;
      }
      h1 {
        color: yellow;
      }
      p {
        color: red;
      }
    </style>
  </head>
  <body>
    <h1>Mencoba mengguanakan CSS Internal</h1>
    <p>Terima Kasih</p>
  </body>
</html>
```

### 3. Eksternal Style
- index.html
```html
 <!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    <h1>Mencoba mengguanakan CSS Internal</h1>
    <p>Terima Kasih</p>
  </body>
</html>
```
- style.css
```html
body {
  background-color: whitesmoke;
}
h1 {
  color: darkgoldenrod;
}
p {
  color: black;
}
```
### CSS Syntax
- CSS Syntax adalah syntax yang digunakan untuk menunjuk atau memilih HTML element mana yang ingin diberi style (dihias). CSS syntax terdiri dari selector, property, dan value.
- Contoh CSS Syntax:
```html
h1 {
  color: darkgoldenrod;
}
```
- Penjelasan 
    - h1 di atas tersebut merupakan sebuah selector berupa element HTML yang akan diubah,
    - Color adalah sebuah properti berupa bagian mana dari element HTML yang akan diubah. Contoh diatas kita akan mengubah warna dari teks yang ada di element h1,
    - Darkgoldenrod Adalah value yaitu nilai/hiasan berupa warna darkgoldenrod.

### FLEXBOX
- Flexbox adalah bagaimana cara kita untuk mengatur layout, Flexbox memiliki kemampuan untuk menyesuaikan layout secara otomatis.
- Contoh Penggunaan Flexbox
- index.html
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    <div class="container">
      <div class="item">Contoh</div>
      <div class="item">Contoh</div>
      <div class="item">Contoh</div>
    </div>
  </body>
</html>
```
- style.css
```html 
.cotainer {
  display: flex;
  border: 3px solid silver;
}

.item {
  border: 1px solid;
  width: 200px;
  height: 200px;
  background-color: orange;
}
```

## Algorithm and Pseudocode
- Apa itu Algoritma, Algoritma adalah deskripsi berupa step-step yang dibutuhkan untuk menyelesaikan suatu masalah. 
- Kenapa harus mempelajari algotima :
  - Pemrograman merupakn algoritma dan struktur data,
  - Data struktur dgunakan untk mngelola sebuah data,
  - Algoritma menyelesaikan suatu permsalahan mnggunakn sbuah data tersebut.
- Kualitas suatu algoritma :
  - Input & output harus jelas/ didefinisikan terlebih dahulu dgn tepat
  - Setiap step harus benar -benar clear dan tidak ambigu
  - Algoritma seharusnya tidak mengandung suatu code pada bahas pemrograman tertentu.algoritma harus dibuat agar dapat digunakan dlm bahas pemrograman apapun

- Contoh Algoritma 
  - Menghitung Luas Persegi Panjang
    - Analisis:
      - Input : p (panjang) dan l (lebar),
      - Luas Persegi Panjang  L = p*l.
    - Algoritma:
      - Input panjang,
      - Input lebar,
      - Rumus untuk menghitung L  yaitu L= p*l,
      - Nilai  L (Luas ) akan dicetak sebagai output ke perangkat output (keluaran).


- Pseudocode merupakan tools yang digunakan untuk menulis algoritma 
- Panduan menulis pseudocode :
  - Huruf kapital digunakan untuk menulis perintah
  - 1 statement hanya terdiri dari 1 baris
  - Menggunakan indentasi
  - Harus bersifat spesifik dan simple
- contoh Pseudocode
  - Pseudocode untuk menentukan luas persegi panjang
```
Deklarasi
var panjang, lebar, luas : integer;
Implementasi 
Read(panjang);
Read(lebar);
luas ← panjang*lebar;
Write (luas);
```
- Jenis Pseudocode :
  - Procedural : Procedural adalah cara berpikir secara runtun. Artinya serangkaian perintah yang berurutan.
  - Conditional: Conditional digunakan saat dibutuhkan percabangan kasus. Komputer akan melakukan suatu tindakan jika suatu kondisi terpenuhi. 
  - Looping    : sebuah perintah yg diulang-ulang
  - Recursive  : Recursive adalah pola pikir dalam algoritma yang memanggil method/function didalam sebuah function.

## Intro To Java Script
- Apa itu Javascript
Javascript adalah bahasa pemograman yang sangat powerful yang digunakan untuk logic pada sebuah website.Javascript juga dapat membuat website menjadi interaktif dan dinamis.
- Bagaimana menjalankan Javascript,Javascript dijalankan melalui browser pada device setiap user.
  ### 1. Tipe Data Java Script
  Tipe data adalah klasifikasi yang kita berikan untuk berbagai macam data yang digunakan dalam programming.
- Tipe data ;
    - number, Tipe data number adalah tipe data yang mengandung semua angka termasuk angka desimal.
    contoh :
    ```javascript
    let number1 = 12;
    ```
    - string, Tipe data string adalah grup karakter yang ada pada keyboard laptop/PC kita yaitu letters (huruf), number (angka), spaces (spasi), symbol, dan lainnya.
    contoh :
    ```javascript
    let nama = "Aqilla";
    ```
    - boolean, adalah tipe data yang hanya mempunyai 2 buah nilai.
    contoh :
    ```javascript
    let benar = "True";
    let salah = "False";
    ```
    - null, tipe data yang diartikan bahwa sebuah variable/data tidak memiliki nilai.
    contoh
    ```javascript
    let data1 = "";
    console.log(data1);
    ```
    - object, koleksi data yang saling berhubungan (related). Tipe data pbject dapat menyimpan data dengan tipe data apapun (number, string, boolean, dan lainnya).
    contoh :
    ```javascript
    var person = {
        nama :"Aqilla",
        umur :20,
    };
    ```
  ### 2. Operator pada Java Script
- Arithmetic Operator
Arithmetic operator adalah operator yang melibatkan operasi matematika.
    - Tambah (+),
    - Kuramg (-),
    - Perkalian (*),
    - Pembagian (/),
    - Modulus (%).
- Comparison Operator
Comparison operator adalah operator yang membandingkan satu nilai dengan nilai lainnya.
    - Lebih kecil dari (<),
    - Lebih besar dari (>),
    - Lebih kecil atau sama dengan (<=),
    - Lebih besar atau sama dengan (>=),
    - Sama dengan (===),
    - Tidak sama dengan (!==).
- Logical Operator
Logical operator biasa digunakan untuk sebuah CONDITIONAL pada pemograman.
    - AND operator (&&),
    - OR operator (||),
    - NOT operator (!).
  ### 3. control flow 
- Conditional
Conditional merupakan statement percabangan yang menggambarkan suatu kondisi.
- Contoh Conditional 
    - IF Statement
    Digunakan jika kode bernilai true.
    ```javascript
    if (true) {
     console.log("selamat pagi");
    }
    ```
    - IF … ELSE Statement
    Else akan mengeksekusi sebuah statement/code jika suatu kondisi bernilai FALSE.
    ```javascript
    if (makan) {
      console.log("sudah kenyang");
    } else {
      console.log("lapar");
    }
    ```
    - IF … ELSE IF Statement
    Else … If statement dapat kita gunakan jika kita mempunyai berbagai kondisi.
    ```javascript
    if (time < 10) {
        greeting = "Good morning";
    } else if (time < 20) {
        greeting = "Good day";
    } else {
        greeting = "Good evening";
    }
    ```
    - Switch Case Conditional
    Gunakan switch case jika kondisi dan percabangan terlalu banyak
    ```javascript
    let tombol1 = 2;

    switch (tombol1) {
      case 1:
        console.log("sctv");
        break;
      case 2:
        console.log("indosiar");
        break;
      case 3:
        console.log("trans");
        break;
      case 4:
        console.log("net");
        break;
      default:
        console.log("channel tidak ditemukan");
    }
    ```
- Looping
Looping adalah statement yang mengulang sebuah instruksi hingga kondisi terpenuhi atau jika kondisi stop/berhenti tercapai.
- contoh looping
    - For
    FOR LOOP merupakan instruksi pengulangan yang dapat kita berikan pada program yang kita kembangkan.
    ```javascript
    for (let i = 1; i <= 10; i++) {
      console.log(i);
    }
    ```
    - While
    WHILE LOOP akan menjalankan instruksi pengulangan kondisi bernilai TRUE.
    ```javascript
    let i = 1;
    while (i < 10) {
    console.log("Angka"+i)
      i++;
    }
    ```
    - Do While 
    Pengulangan 1 kali sebelum dilakukan pengecekan kondisi.
    ```javascript
    let i = 1;
    do {
    console.log("Urutan"+i)
      i++;
    }
    while (i < 24);
    ```


