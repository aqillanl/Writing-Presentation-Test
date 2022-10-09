# **Writing and Presentation Test Week 3**
## **JavaScript Intermediate**
### **JavaScript Intermediate Array & Multidimensional Array**
- Array adalah sebuah tipe data non-primitif yang mampu menyimpan banyak data serta mampu menyimpan berbagai macam tipe data. Cara menggunakan array adalah dengan menggunakan kurung kotak, seperti `let arr [ ]`. Contoh dari array sebagai berikut :
```javascript
let arr = ["Hallo", 1, true];
Atau bisa juga

let bunga = ['Melati',  'Tulip', 'Anggrek'];
console.log(bunga);
```
- Cara mengakses array, Array pada javascript dihitung dari index data ke-0. Data pertama adalah index ke-0. Contoh syntax :
```javascript
let buku = ["Buku Cerita", "Buku Pelajaran", "Buku Dongeng"];
console.log(buku);

Output :
Array(3)
0 : "Buku Cerita"
1 : "Buku Pelajaran"
2 : "Buku Dongeng"

Array sepanjang 3 serta terdapat 2 index dalam array.
```
- Update Array , cara mengupdate array yaitu :
```javascript
let buku = ["Buku Cerita", "Buku Pelajaran", "Buku Dongeng"];

buku[0] = "Buku Sejarah";
console.log(buku);

Output : ["Buku Sejarah", "Buku Pelajaran", "Buku Dongeng"]
```
- Const in array, Jika menggunakan let, kita dapat mengubah array dengan array baru dan konten nilai yang ada di dalam array dengan nilai lain. tetapi const tidak bisa melakukan update data. Namun pada Array kita dapat melakukan update konten nilai di dalam array (mutable). Contoh syntax :
```javascript
const warna = ['Merah', 'Putih', 'Biru'];
warna[1] = ['Kuning'];
 
console.log(warna);
Output : ['Merah', 'Kuning', 'Biru'];
```
- Array Properti, Properties adalah fitur yang sudah disediakan oleh Javascript untuk memudahkan developer.Array properti terdiri dari :
  - `.length`, length akan mengembalikan nilai dari jumlah panjang data suatu array. Contoh syntax :
    ```javascript
    let arr = ["Hallo", 1, true]
    console.log(arr.length);
    
    Output : 3
    ```
  - `.constructor`, constructor mengembalikan referensi ke fungsi array yang membuat objek.
  - `.prototype`, prototype mewarisi definisi array dengan menambah properti dan metode.
  - `.index`, mewakili indeks kecocokan berbasis nol dalam string.
  - `.input`, properti ini hanya ada dalam array yang dibuat oleh kecocokan ekspresi reguler.
- Array Methods, Array memiliki method atau biasa disebut built-in methods. Kita tidak perlu membuat function lagi jika method yang kita butuhkan sudah tersedia.
 - `.push()` adalah method yang digunakan untuk menambah data diakhir. Contoh syntax :
   ```javascript
   let arrBuah = [
   "Jeruk",
   "Pepaya",
   "Rambutan"
   ];
   console.log(arrBuah);
   
   arrBuah.push("Duku")
   console.log(arrBuah); //Output : "Jeruk", "Pepaya", "Rambutan", "Duku"
   ```
 - `.unshift()` adalah method yang digunakan untuk menambahkan data didepan. Contoh syntax :
   ```javascript
   let arrBuah = [
   "Jeruk",
   "Pepaya",
   "Rambutan"
   ];
   arrBuah.unshift("Mangga")
   console.log(arrBuah); //Output : "Mangga", "Jeruk", "Pepaya", "Rambutan"
   ```
 - `.pop()` adalah method yang digunakan untuk menghapus elemen terakhir. Contoh syntax :
   ```javascript
   let arrBuah = [
   "Jeruk",
   "Pepaya",
   "Rambutan"
   ];
   arrBuah.pop()
   console.log(arrBuah); //Output : "Jeruk", "Pepaya"
   ```
 - `.shift()` adalah method yang digunakan untuk menghapus elemen depan. Contoh syntax :
   ```javascript
   let arrBuah = [
   "Jeruk",
   "Pepaya",
   "Rambutan"
   ];
   arrBuah.shift()
   console.log(arrBuah); //Output : "Pepaya", "Rambutan"
   ```
 - `.splice()` adalah method yang digunakan untuk menghapus ditengah. Dalam slice terdapat start atau awal/index, deletecount atau banyak data yang didelete, dan item atau data yang disisipkan. Contoh syntax :
   ```javascript
   let arrBuah = [
   "Jeruk",
   "Pepaya",
   "Rambutan",
   "Anggur",
   "Semangka"
   ];
   arrBuah.splice(2) 
   console.log(arraBuah); //Output : "Jeruk", "Pepaya"
   
   arrBuah.splice(2, 1)
   console.log(arrBuah); //Output : "Jeruk", "Rambutan", "Anggur", "Semangka"
  
   arrBuah.splice(2, 1, "Buah Naga")
   console .log(arrBuah); //Output : "Jeruk", "Buah Naga", "Rambutan", "Anggur", "Semangka"
   ```
 - `.slice()` digunakan untuk mengembalikan shallow to copy (copy data) atau mengambil data dengan cara copy data. Contoh script :
   ```javascript
   let arrBuah = [
   "Jeruk",
   "Pepaya",
   "Rambutan",
   "Anggur",
   "Semangka"
   ];
   let slice = arrBuah.slice(2, 4)
   console.log(slice); //Output: "Pepaya", "Anggur"
   
   let slice = arrBuah.slice(2)
   console.log(slice); //Output : "Rambutan", "Anggur", "Semangka"
   ```
- `Looping Array`, Array memiliki built in methods untuk melakukan looping yaitu `.map()` dan `.forEach()`. Contoh script looping :
   ```javascript
   let arrBuah = ["Anggur", "Jeruk", "Semangka", "Pepaya", "Rambutan", "Duku"];
   for(let i = 0; i<arrBuah.length; i++){
   console.log(arrBuah[i])
   };
   //Output : 
   Anggur
   Jeruk
   Semangka
   Pepaya
   Rambutan
   Duku
  
   Atau bisa juga
   for(let i = arrBuah.lengthh-1; i>0; i--){
   console.log(arrBuah[i])
   };
   //Output :
   Duku
   Rambutan
   Pepaya
   Semangka
   Jeruk
   Anggur
   ```
 - `.forEach()` adalah method untuk melakukan looping pada setiap elemen array. `ForEach` ini tanpa menggunakan return.Contoh script :
   ```javascript
   arrBuah.forEach((item) => {
    console.log(item)
   });
   //Output :
   Anggur
   Jeruk
   Semangka
   Pepaya
   Rambutan
   Duku
  
   Contoh lain
   arrBuah.forEach((index,item) =>{
   if(index %2 == 1){
    console.log(index,item)
   }
   });
   //Output :
   1. Jeruk
   3. Pepaya
   5. Duku
   Script diatas digunakan untuk menampilkan index array ganjil.
   ```
 - `.map()` melakukan perulangan/looping dengan membuat array baru.Contoh script :
   ```javascript
   let buah segar = arrBuah.map((item) =>{
   return item + " " + "segar"
   });
   //Output :
   0 : Anggur segar
   1 : Jeruk segar
   2 : Semangka
   3 : Pepaya
   4 : Rambutan
   5 : Duku
   ```
- `Array Multidimensional` Multidimensional Array bisa dianalogikan dengan array of array. Ada array didalam array. Contoh script :
   ```javascript
   let arrMulti = [
   ["nama", "alpha"],
   ["umur", 17],
   ["kelas",  "JS"],
   ]
   console.log(arrMulti[0][1];
   //Output : "alpha"
   
   Atau bisa juga
   arrMulti[2][1] = "CSS"
   console.log(arrrMulti);
   Script diatas berarti teks JS dirubah menjadi CSS
   ```
### **JavaScript Intermediate Object**
- Object adalah tipe data pada variabel yang menyimpan properti dan fungsi (method). Properti adalah data lengkap dari sebuah object. Method adalah action dari sebuah object.
- Membuat sebuah object Sama seperti tipe data sebelumnya. Object dapat diassign kedalam sebuah variabel. Contoh script :
   ```javascript
   let siswa = {
    nama : 'terra',
    umur : 17,
    hobi : 'memancing', 
    "nomor handphone" : 08256814086
    }
    console.log(siswa);
    ```
- Cara akses object Dalam mengakses object terdapat 2 cara yaitu menggunakan dot notation dan bracket. Selain itu, bisanya dalam mengakses object yaitu menggunakan `console.log(object)`.
  - dot notation, misalnya `console.log(siswa.nama);` maka output yang dihasilkan yaitu terra
  - bracket, misalnya `console.log(siswa['nama']);` 
- Memanggil nama object dengan variable contohnya :
    ```javascript
    let properti = "umur"
    console.log(siswa[properti]);
    ```
- Menambahkan properti baru ke dalam object Contoh script:
    ```javascript
    Cara 1
    let buku = {
     Judul : "Mantan jadi manten",
     Penulis : "Hayati",
     "Jumlah halaman" : 250,
     };
     buku.tahun : 2022;
     buku.terjual : 3000;
     console.log(bukuu);
     //Output :
     Judul : Mantan jadi manten
     Penulis : Hayati
     Jumlah halaman : 250
     buku.tahun : 2022
     buku.terjual : 3000
     
     Cara 2
     buku["penerbit"] : "gramedia";
     console.log(buku);
     //Output :
     Judul : Mantan jadi manten
     Penulis : Hayati
     Jumlah halaman : 250
     buku.tahun : 2022
     buku.terjual : 3000
     penerbit : gramedia
     ```
- Ganti properti lama contoh script : 
     ```javascript
     Cara 1
     let hewan = {
      nama : 'kucing',
      kaki : 4,
      warna : 'putih',
     };
     hewan.nama : 'kelinci',
     hewan.warna : 'hitam',
     console.log(hewan);
     //Output 
     nama : kelinci
     kaki : 4
     warna : hitam
     
     Cara 2
     hewan["kaki"]=2;
     console.log(hewan)
     nama : kelinci
     kaki : 2
     warna : hitam
     ```
- Delete Properti contoh script :
     ```javascript
      let hewan = {
      nama : 'kucing',
      kaki : 4,
      warna : 'putih',
     };
     delete.hewan.warna;
     delete.hewan.kaki;
     console.log(hewan);
     //Output : nama : kucing
     ```
- Method adalah ketika ingin menambahkan sebuah function. Ada 2 method dalam object, yaitu :
  - const greeting contoh script :
    ```javascript
    const greeting = {
     welcome : function(){
      return "halo selamat datang";
    };
     afterpay:function(){
     return "terimakasih sudah membeli produk kami";
     }
    };
    console.log(greeting.welcome()); //Output : halo selamat datang
    ```
  - nested object contoh script :
    ```javascript
    let buku = {
     Judul : "Tips jago Javascript",
     Tahun : 2022;
     Penulis {
        Penulis1 : {
           Nama : "Reyhan",
           Umur : 28,
           Kota : "Jakarta"
           }
        Penulis2 : {
           Nama : "Fala",
           Umur : 25,
           Kota : "Madiun"
           }
        Penulis3 : {
           Nama : "Diana",
           Umur : 20,
           Kota : "Bandung"
           }
         }
    };
     console.log(buku.penulis.penulis1.nama);//Output : Reyhan
    ```
- Built In Method (Object menjadi array) 
     ```javascript
     let siswa = {
       nama : "Fala",
       umur : 20,
       hobi : "Berenang",
     };
     console.log(object.keys.(siswa)); //Output : 'nama', 'umur', 'hobi'
     console.log(object.values.(siswa)); //Output : 'Fala', '20', 'Berenang'
     ```
- Looping Object Looping sendiri berarti perulangan. Contoh scriptnya :
    ```javascript
    let siswa = {
     nama : "Reyhan",
     umur : 22,
     kota : "Jakarta",
    };
    for(let key in siswa){
      console.log(siswa[key]); 
    //Output :
    Reyhan
    22
    Jakarta
    ```
- Array of Object adalah array yang menyimpan banyak object sebagai nilainya. Contoh script :
    ```javascript
    let users = {
      {
       Nama : "Reyhan",
       Umur : 28,
       Kota : "Jakarta",
      },
      {
       Nama : "Fala",
       Umur : 20,
       Kota : "Bandung",
      },
      {
       Nama : "Diana",
       Umur : 24,
       Kota : "Madiun",
      },
    };
    console.log(user);
    
    Dengan menggunakan Map, maka
    let data = users.map((el) => {
     console.log(el.nama);
    });
    //Output :
    Reyhan
    Fala
    Diana
    ```
### **JavaScript Intermediate Recursive & Modules**
- Rekrusif adalah function atau algoritma yang memanggil dirinya sendiri sampai kondisi tertentu. Rekrusif ini mirip seperti looping. Misalnya pada gambar ada gambar di dalam gambar. Terdapat 2 kunci pada rekrusif,yaitu base case atau titik berhenti dan recrusion case atau titik memanggil function. Contoh script :
  ```javascript
  Menampilkan bilangan 1 2 3 4 5
  
  function deretAngka(n){
   if (n == 1) {
     console.log(n)
   } else {
     deretAngka(n-1)
     console.log(n);
    }
  }
  deretAngka(3)
  
  Atau contoh lain :
  Mencari angka faktorial
  Misalnya 5!
  Solusinya jika dijabarkan 5 x 4 x 3 x 2 x 1

  function faktorial(n) {
    if (n == 1) {
      return 1
    } else {
      return n * faktorial(n - 1)
    }
  }
  console.log(faktorial(3))
  //Output = 6
  ```
- Modules adalah cara untuk memisahkan kode ke file yang berbeda. Keuntungan dari modules yaitu mudah untuk mengelola kode serta kode tidak menumpuk di dalam satu file. Terdapat 2 kata kunci pada modules yaitu export dan import. Contoh script :
  ```javascript
  // File Jepang.js
  export let motor = ["suzuki", "yamaha", "honda", "kawasaki"]
  
  let entertainment = ["anime", "manga", "wibu", "dorama"]
  export default entertainment
  
  export function sayHello() {
   console.log("hallooo")
  }
  
  import {apple} from './amerika.js';
   console.log(apple);
  
  // File Indonesia.js
  import {motor} from "./Jepang.js"
   console.log(motor);
   
  import Entertainment, { motor as motorJepang, sayHello  } from "./jepang.js"
  console.log(Entertainment);
  
  // File Amerika.js
  let apple = ["iphone", "macbook", "imac"]
    export {apple}
  
  Berdasarkan script diatas,
  - Indonesia hanya bisa import, karena dia file utama.
  - Jepang bisa melakukan import dan export.
  - Amerika hanya melakukan export.
  ```
- Hal hal yang harus dilakukan saat membuat modules adalah menambahkan type="module" pada script utama, lalu siapkan script ke-2 dan sebagainya untuk melakukan export, serta lakukan import pada file atau script utama.
### **JavaScript Intermediate Asynchronous Introduction & Promise**
- Asynchronous yang biasa dikenal juga dengan sebutan non-blocking mengizinkan komputer kita untuk memproses perintah lain sambil menunggu suatu proses lain yang sedang berlangsung. Ini artinya kita bisa melakukan lebih dari 1 proses sekaligus (multi-thread). Eksekusi perintah dengan asynchronous tidak akan melakukan blocking atau menunggu perintah sebelumnya selesai. Jadi sambil menunggu kita bisa mengeksekusi perintah lain.
- Analoginya seperti saat kita mencuci baju di mesin cuci. Agar lebih produktif, sambil menunggu cucian selesai kita bisa melakukan pekerjaan lain misalnya menyapu dan mengepel. Artinya disini kita melakukan 3 proses sekaligus.
#### Menjalankan Asynchronous pada JavaScript
Jika JavaScript secara default bersifat synchronous, maka bagaimana jika ingin menerapkan proses asynchronous ? Ada beberapa cara untuk membuat proses asynchronous. Kami membatasi hanya memberikan 2 cara ini:

1. `setTimeout(function, milliseconds)` digunakan untuk simulasi pemanggilan kembali proses asynchronous yang sedang/sudah selesai dijalankan. Pemanggilan hanya dilakukan 1 kali.
2. `setInterval(function, milliseconds)` digunakan untuk simulasi pemanggilan proses asynchronous yang sedang/sudah dijalankan dalam interval waktu tertentu. Pemanggilan dilakukan berkali-kali sesuai interval waktu yang ditentukan.

- Callback adalah sebuah function, namun bedanya dengan function pada umumnya adalah pada cara eksekusinya. Jika function pada umumnya dieksekusi secara langsung, sedangkan callback dieksekusi di dalam function lain melalui parameter.
- Promise merupakan suatu object dan digunakan hanya untuk satu event dengan menyimpan hasil dari sebuah operasi asynchronous baik itu hasil yang diinginkan (resolved value) atau alasan kenapa operasi itu gagal (failure reason).
-  Async-Await merupakan fitur yang hadir sejak ES2017 bekerja dengan cara menunda eksekusi hingga proses asynchronous selesai.
- Fetch merupakan cara baru dalam melakukan network request yang memanfaatkan sebuah Promise dalam penggunaanya. Karen Fetch mengembalikan sebuah Promise maka respon handling yang digunakan adalah then jika promise mengembalikan resolve dan catch jika promise mengembalikan nilai reject.
    #### API dan HTTP Request
- API merupakan singkatan dari Application programming interface
- API sebagai alat untuk berbicara antar perangkat lunak 
- API dapat digunakan untuk sistem berbasis web,sistem operasi, sistem basis data dan perangkat lunak
- HTTP merupakan singkatan dari Hypertext transfer protocol
- HTTP di desain untuk memungkinkan komunikasi antar klien dan server. 
- HTTP berfungsi sebagai protokol Request-Response antara klien dan server. 
- HTTP Request yaitu Keadaan dimana server membaca apa yang dikirimkan oleh client melalui aplikasi web server
- HTTP Method :
  - GET digunakan untuk meminta data dari sumber tertentu
  - POST digunakan untuk mengirim data ke server untuk membuat/memperbarui resource
  - PUT digunakan untuk mengirim data ke server untuk membuat/memperbarui resource.
  - DELETE untuk menghapus spesifiksi resource
### **JavaScript Intermediate Web Storage**
- Ada beberapa cara untuk menyimpan data pengguna seperti pencarian, artikel berita, dan lain-lain ke lokal (browser) menggunakan web storage seperti cookies, local storage, dan session storage. Data ini dimanfaatkan oleh situs web tersebut untuk merekam kebiasaan pengguna agar dapat memberikan rekomendasi sesuai preferensi si pengguna tersebut.
#### Cookies
- Cookies adalah data kecil yang dikirim dari situs web dan disimpan di komputer kita oleh web browser saat kita menjelajah. Disebut data kecil karena maksimum data yang dapat disimpan dalam cookies adalah 4096 bytes (4 KB).
- Biasanya data yang disimpan di cookies adalah access token pengguna saat login atau data pencarian saat melakukan pencarian pada situs web tertentu. Hal ini yang biasanya dilakukan oleh situs pencarian untuk melacak pencarian kita dan menampilkan iklan yang berhubungan dengan pencarian kita sebelumnnya.
- Namun ada beberapa kekurangan yang perlu kita perhatikan mengenai cookies di antaranya:
  1. Setiap kita mengakses situs web, cookies juga kembali dikirim sehingga memperlambat aplikasi web kamu dengan mengirimkan data yang sama.
  2. Cookies disertakan pada setiap HTTP request, sehingga mengirimkan data yang tidak dienkripsi melalui internet, maka saat kita ingin menyimpan data dalam cookies kita harus mengenkripsinya terlebih dahulu.
  3. Cookies hanya dapat menyimpan data sebanyak 4KB.
  4. Lalu cookies juga memiliki tanggal kadaluarsa. Tanggal ini telah ditentukan sehingga web browser bisa menghapus cookies jika tanggal sudah kadaluarsa atau tidak dibutuhkan.
- Kita dapat memanfaatkan jenis web storage yang lain untuk mengatasi kekurangan yang dimiliki cookies.
#### Local Storage & Session Storage
- Pernahkah kita saat melakukan pencarian pada sebuah situs lalu situs tersebut menampilkan riwayat pencarian kita? Iya, data pencarian tersebut disimpan ke dalam local storage untuk diolah menjadi riwayat pencarian. Itulah salah satu contoh penerapan dari local storage pada aplikasi web.
- Berbeda dengan local storage, walaupun masuk ke dalam web storage, data yang tersimpan pada session storage akan hilang ketika session dari sebuah laman berakhir.
- Karakteristik Local Storage:
  1. Menyimpan data tanpa tanggal kadaluarsa.
  2. Data tidak akan dihapus ketika web browser ditutup dan akan tersedia seterusnya selama kita tidak menghapus data local storage pada web browser.
  3. Dapat menyimpan data hingga 5MB.
  4. Hanya dapat menyimpan data string.
- Sedangkan Karakteristik Session Storage:
  1. Data yang disimpan pada session storage akan terus tersimpan selama browser terbuka dan tidak hilang jika laman di-reload.
  2. Membuka banyak tab/window dengan URL yang sama, akan menciptakan session storage yang berbeda di masing-masing tab/window.
  3. Menutup tab/window akan mengakhiri session dan menghapus data yang tersimpan di session storage pada tab/window tersebut.
  4. Data yang tersimpan dalam session storage harus berbentuk string.
  5. Hanya dapat menyimpan data sebanyak 5MB.
##### Mengakses Local Storage & Session Storage
1. Local Storage
  - Menyimpan Data
  Untuk menyimpan data pada local storage, kita menggunakan method `setItem()` yang membutuhkan 2 parameter. Parameter pertama adalah key yang ingin kita simpan dan parameter kedua adalah data (value) dari key yang akan disimpan.
    ```javascript
    localStorage.setItem('key', value);
    ```
  - Mengambil Data
  Untuk mengambil data yang telah tersimpan pada local storage, kita dapat menggunakan method `getItem()` yang membutuhkan 1 parameter. Parameter tersebut adalah key dari data yang kita inginkan.
      ```javascript
      localStorage.getItem('key');
      ```
  - Menghapus Data
  Untuk menghapus data yang telah tersimpan pada local storage, kita dapat menggunakan method `removeItem()` yang membutuhkan 1 parameter. Parameter tersebut adalah key dari data yang ingin kita hapus.
    ```javascript
    // menghapus key tertentu
    localStorage.removeItem("key");

    // menghapus semua key
    localStorage.clear();
    ```
2. Session Storage
  - Menyimpan Data
  Sama dengan local storage, sintaks untuk menyimpan data pada session storage adalah sebagai berikut:
    ```javascript
    // menambah session storage
    sessionStorage.setItem('key', value);
    ```
  - Mengambil Data 
  Sama seperti local storage, cara mendapatkan data dari session storage juga menggunakan `getItem(),` seperti berikut ini:
    ```javascript
    // mendapatkan session storage
    sessionStorage.getItem('key');
    ```
  - Menghapus Data
  Syntax untuk menghapus data dari session storage ada 2, yaitu:
    ```javascript
    // menghapus session storage satu persatu berdasarkan key
    sessionStorage.removeItem('key');

    // menghapus seluruh session storage sekaligus
    sessionStorage.clear();
    ```


