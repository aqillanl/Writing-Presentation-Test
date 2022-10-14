# **Writing and Presentation Test Week 4**
### **JavaScript Intermediate Asynchronous Fetch & Async Await**
#### JavaScript Intermediate Asynchronous Fetch
- Proses melakukan `fetch()` adalah salah satu proses asynchronous di JavaScript sehingga kita perlu menggunakan salah satu diantara promise atau async/await.
- Fetch dengan Promise
```javascript
fetch("https://jsonplaceholder.typicode.com/posts")
  .then(function (response) {
    return response.json();
  })
  .then(function (post) {
    console.log(post);
  });
```
- Fetch dengan async/await
```javascript
const tesFetchAsync = async () => {
  let response = await fetch("https://jsonplaceholder.typicode.com/posts");
  response = await response.json();
  console.log(response);
};
tesFetchAsync();
```
#### JavaScript Intermediate Asynchronous Async Await
- Async/await baru ada ketika update ES8  JavaScript dan dibangun menggunakan promise. Jadi sebenarnya async/await dan promise itu sama saja, namun hanya berbeda dari syntax dan cara penggunaannya.
- Ada 2 kata kunci yang memiliki pengertian sebagai berikut:
  - `async`, mengubah function synchronous menjadi asynchronous.
  - `await`, menunda eksekusi hingga proses asynchronous selesai.
- contoh pengunaan Async Await
```javascript
// Definisikan dahulu promise yang ingin digunakan
let condition = true;
let tesAsyncAwait = async (condition) => {
  if (condition) {
    return "Condition is fulfilled!";
  } else {
    throw "Condition is rejected!";
  }
};


// Membuat fungsi run menjadi asynchronous menggunakan async/await
const run = async (condition) => {
  try {
    const message = await tesAsyncAwait(condition);
    console.log(message);  // Output: Condition is fulfilled!
    console.log("After condition is fulfilled"); // Output: After condition is fulfilled
  } catch (error) {
    console.log(error);
  }
};

run(true);
```
### **Responsive Web Design**
- Responsive Web Design Merupakan sebuah tehnik untuk membuat layout atau tampilan website yang kita buat dapat menyesuaikan diri dengan ukuran layar device dimana web kita dibuka. Baik dari ukuran huruf, user interface, gambar dan tata letak akan menyesuaikan dengan lebar layar dan resolusi device yan digunakan.
 - Add viewport in HTML
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```
- Penjelasan kode di atas:
  - width=device-width memberitahu browser untuk mengikuti lebar layar dari perangkatnya. Sebab lebar layar tiap perangkat berbeda-beda.
  - initial-scale=1.0 memberitahu browser tingkat pembesaran (zoom level) dari halaman itu.
- Media Query digunakan untuk membuat bebrapa styles tergantung pada jenis device. 
- Jenis media query
  - Media query untuk responsive web design umumnya hanya menggunakan 2 jenis media query.
  - Keduanya yaitu min-width dan max-width.
- Ada 2 cara/pattern dalam menggunakan media query:
  1. Membuat files css berbeda untuk masing - masing device
  2. Menggabungkan 1 files CSS untuk setting styling berbagai device 
- Contoh penerapan media query 
  ``` 
  @media screen and (max-width: 600px)
  ```
- Breakpoint adalah perubahan yang terjadi pada tampilan tampilan saat berganti device atau ukuran width.
- Terdapat 3 jenis breakpoint yaitu desktop, ipad/tablet, dan mobile phone
- Penggunaan breakpoint pada media query dapat dilakukan dengan membuat range ukuran sesuai dengan tampilan device yang ingin dibuat
- Contoh breakpoint dapat ditulis seperti ini
  ```
  @media screen and (min-width: 500px) and (max-width: 700px) {
  body {
    background-color: grey 
    }
   }
  ```
### **Bootstrap5**
- Bootstrap adalah kerangka kerja CSS yang sumber terbuka dan bebas untuk merancang situs web dan aplikasi web. Kerangka kerja ini berisi templat desain berbasis HTML dan CSS untuk tipografi, formulir, tombol, navigasi, dan komponen antarmuka lainnya, serta juga ekstensi opsional JavaScript.
- Komponen utama bootstrap :
  - bootstrap.css
  - bootstrap.js
- Cara konfigurasi bootstrap :
  - Membuat tag boostrap di head. Cara memanggil css bootstrap dengan menggunakan href lalu mengganti link href css lokal dengan link boostrap online.
- Contoh penggunaan content bootstrap :
  - CSS : bootstrap.min.css, bootstrap-grid.css, dll
  - JS : bootstrap.bundle.js, bootstrap.min.js, dll
- Komponen Bootstrap sebagian besar dibangun dengan base-modifier nomenclature.Contohnya mengelompokkan beberapa properti kedalam kelas dasar seperti .btn, seperti .btn-primary or .btn-success.
- Penggunaan theme color pada boostrap dapat menggunakan keyword berikut :
  ```html
  $theme-colors: (
  "primary":    $primary,
  "secondary":  $secondary,
  "success":    $success,
  "info":       $info,
  "warning":    $warning,
  "danger":     $danger,
  "light":      $light,
  "dark":       $dark
  );
  ```
- Kapan kita menggunakan bootstrap?
  - Boostrap digunakan ketika membuat website sederhana dan tidak memerlukan load lama
- Layout pada boostrap :
  - Breakpoints merupakan suatu cara yang dilakukan untuk membuat desain responsif dengan mengontrol kapan tata letak yang disesuaikan dengan ukuran perangkat
    tertentu.
    - Breakpoints pada bootstrap ada 5 yaitu sm, md, lg, xl dan xxl.
    - Setiap breakpoint dipilih untuk menampung container yang lebarnya 12 dengan sehingga tersusun rapi. Breakpoint juga mewakili subset ukuran perangkat umum dan
    dimensi area pandang.
 - Container adalah blok dasar atau pembungkus boostrap yang terdiri dari contain, pad dan align  yang menyelaraskan konten website dalam perangkat atau area      
    pandang tertentu.
   - Terdapat 3 container pada boostrap yaitu :
    - .container, yang menerapkan lebar maksimum pada setiap breakpoint responsif
    - .container-{breakpoint}, menerapkan lebar 100% sampai dengan breakpoint yang ditentukan.
    - .container-fluid, menerapkan 100% ukurannya dari breakpoints
 - Grid System pada bootstrap yang terdiri dari 12 kolom default.
 - Grid system pada bootstrap menggunakan container,baris dan kolom untuk menata dan menyelaraskan konten,yang dibangun menggunakan flexbox dan itu sudah responsive.
  - contoh penggunaan grid system
   ```html 
     <div class="container text-center">
     <div class="row">
      <div class="col">
        Column
      </div>
      <div class="col">
        Column
      </div>
      <div class="col">
        Column
      </div>
     </div>
     </div>
   ```
- Grid system bootstrap :
  - .col-lg digunakan untuk mengatur grid pada ukuran monitor yang besar
  - .col-md digunakan pada monitor komputer berukuran sedang
  - .col-sm digunakan untuk mengatur monitor pada tablet
  - .col-xs digunakan untuk mengatur monitor pada handphone 
