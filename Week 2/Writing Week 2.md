# Writing and Presentation Test Week 2
## JavaScript Dasar
### 1. JavaScript - Scope & Function
#### JavaScript Scope
- Scope adalah konsep dalam flow data variabel. Menentukan suatu variabel bisa diakses pada scope tertentu atau tidak.
- Scope meiliki 2 macam pilihan yaitu global scope dan local scope
- Global Scope
Global scope berarti variabel yang kita buat dapat diakses dimanapun dalam suatu file. Agar menjadi Global Scope, suatu variabel harus dideklarasikan diluar Blocks.
Contoh Global Scope :
```javascript
let myName = "aqilla" ; 
    function greeting()
        return myName;
    {
        console.log(myName);
```
- Local Scope
Local scope berarti kita mendeklarasikan variabel didalam blocks seperti function, conditional, dan looping. Maka variabel hanya bisa diakses didalam blocks saja. Tidak bisa diakses diluar blocks.
```javascript
function greeting() {
    let myName = 'aqilla';
    return myName;
}
console.log(greeting())
console.log(myName);
```
#### JavaScript Function
- Apa itu Function?
- Function adalah sebuah blok kode dalam sebuah grup untuk menyelesaikan 1 task/1 fitur. Saat kita membutuhkan fitur tersebut nantinya, kita bisa kembali menggunakannya.
- membuat function
```javascript
function greeting() {
      return 'Hello World' ;
   };
```
- memanggil function
```javascript
greeting()
console.log(greeting());
```
- Contoh function :
- Parameter Function
function dapat menerima sebuah inputan data dan menggunakannya untuk melakukan task/tugas.
contoh parameter
```javascript
function penambahan(a, b){
  return a + b;
}
```
- Argumen Function
Argumen adalah nilai yang digunakan saat memanggil function. Jumlah argumen harus sama dengan jumlah parameternya
contoh argumen
```javascript
function penambahan(a,b){
   return a + b;
}
  console.log(penambahan(4,4))
```
- Default Parameters
Default paramaters digunakan untuk memberikan nilai awal/default pada parameter function. Default parameters bisa digunakan jika kita ingin menjaga function agar tidak error saat dipanggil tanpa argumen
contoh default parameter
```javascript
function multiply(a, b = 1) {
  return a * b;
}
console.log(multiply(5, 2));
console.log(multiply(5));
```
- Arrow Function
Arrow function adalah cara lain menuliskan function. Ini adalah fitur terbaru yang ada pada ES6 (Javascript Version)
contoh arrow function
```javascript
const greeting = (a, b) => {
    return a + b;
}
```
### 2. Data Type Built in Prototype & Method
#### a. Data Type
- Data Type ada 2 contoh yaitu data type Primitive & Non Primitive
  - Primitive 
    - String
    - Number
    - Boolean
    - Null
    - Undefined
    - Symbol
  - Non Primitive
    - Object
    - Function
    - Array
    - Date
    - RegExp
    - Error
#### b. Prototype & Method
- Data Type Built-in - String
  <br> deretan karakter yang diapit oleh sepasang tanda kutip (" "), berguna untuk menyimpan data yang dapat direpresentasikan dalam bentuk teks
    - Properties
     1. Constructor
        Mengembalikan fungsi yang dibuat string prototipe objek
     2. Length
        Mengembalikan panjang string JavaScript
        ```javascript
        const str = 'Aqilla';
        console.log(str.length); // Output: 6
        ```
     3. Prototype
        Menambah metode dan properti ke dalam sebuah objek
        ```javascript
        String.prototype.reverse = function(){ 
          let s = " "    
          for (let i = String(this).length-1; i >= 0; i-- { 
            s = s + String(this)[i]
          } 
          return s 
        }
        console.log("Aqilla".reverse()) //Output: 'alliqa'
        ```
    - Method
    1. charAt()
        <br> Mengembalikan karakter pada index yang spesifik (posisi)
        ```Javascript
        let nama = 'aqilla';
        console.log(nama.charAt(2)); //Output : i
        ```
    2. replace()
        <br> Cari string untuk nilai dan kembalikan string baru dengan nilai yang diganti
        ```javascript
        const str = 'aku sedang belajar menggunakan replace';
        console.log(str.replace('aku', 'saya')); // saya sedang belajar menggunakan replace
        ```
    3. toUpperCase()
         <br> Ubah string menjadi huruf besar
         ```javascript
         const str = 'aqilla';
         console.log(str.toUpperCase()); //Output: AQILLA
         ```
     4. toLowerCase()
         <br> Ubah string menjadi huruf kecil
         ```javascript
         const str = 'AQILLA';
         console.log(str.toLowerCase()); //Output: aqilla
         ```
- Data Type Built-in - number 
  <br> bilangan bulat, pecahan, dan lain-lain yang berbentuk angka
  - Properties (jarang digunakan, kebanyakan menggunakan methods number)
  - Method
    1. toString()
        <br> untuk mengubah angka menjadi string
        ```javascript
        let angka = 24
        angka.toString() //Output: '24'
        ```
    2. parseInt() dan Number()
        <br> mengubah string menjadi number
        ```javasript
        myString = "1932";
        console.log(parseInt(myString)); // Output: 1932
        console.log(Number(myString)); //Output: 1932
        ```
- Data Type Built-in - Math
<br> mempermudah dalam perhitungan matematika
<br> contoh :
```javascript
Math.pi //Output: 3.1415
Math.LOG2E //Output: 1.4426
Math.sqrt2 //Output: 1.4426 {menghitung akar dua}
```
- Method
1. Math.abs()
      <br> mengembalikan nilai negatif menjadi nilai positif
      ```
      Math.abs(-13) //Output: 13     
      ```
   2. Math.pow()
      <br> menghitung pangkat
      ```
      Math.pow(3, 2) //Output: 9
      ```
   3. Math.sqrt()
      <br> menghitung akar
      ```
      Math.sqrt(9) //Output: 3
      ```
   4. Math.round()
      <br> membulatkan angka
      ```
      Math.round(123.456) //Output: 123
      ```
### 3. JavaScript DOM
- DOM merupakan cara memanipulasi html agar website lebih dinamis dan interaktif
- Cara memanggil DOM Value yaitu :
  - Memanggil tag HTML berdasarkan ID
  `` console.log(document.getElementByID("header))``
  - Memanggil tag HTML berdasarkan Class Name 
  `` console.log(document.getElementByClassName("text-color-blue"))``
  - Memanggil tag html berdasarkan query selector
  `` console.log(document.querySelector("#header "))`` 
  `` console.log(document.querySelector(".text-color-blue"))``
- Memanipulasi content
  Cara memanipulasi content :
  1. Deklarasi varible header sebagai wadah untuk menyimpan tag HTML
  `` let header = document.getElementById("header"); ``
  2. Memanipulasi Content pada Header Content dari pemilik element dengan ID Header dengan text.Content
  `` document.getElementById("header").textContent = "Teks Heading" `` <br />
     Memanipulasi Content didalam sebuah element dengan .innerHTML
  ```javascript
  <ul id= "list"></ul>

  document.getElementById("list").innerHTML = "<li> item1 </li> <li> item2 </li>"
  ```
- Membuat element HTML
- contohnya :
  ```javascript
  const heading = dosument.createElement("h1)
  heading.textContent = "Ini Heading"

  document.getElemntByID("header").appendChild(heading)
  ```
#### DOM Events
- DOM events Memiliki tugas untuk membantu user dapat berinteraksi dengan document HTML
- Contoh DOM Events
  - Click
  - Scroll
  - Change
  - Focus
  - Hover
  - Submit
  - Blur
- Menangkap Interaksi User
  - Element.addEventListener(“event”)
  - Element.onevent
- EventListener
Dengan cara Element.addEventListener(“event”)
  - Bisa dihilangkan
  - Bisa ada beberapa event listener yang sama untuk 1 element
  - Memiliki argument tambahan { options }
- EventListener - Click
Misalkan kita mempunyai element ``<input id=”user-input” />``  dan ``<button id=”alert-button”>show</button>``. 
Kita ingin menampilkan pop up box yang berisi teks di dalam input tadi.
  ```javascript
  const input = document.getElementById(“user-input”)
  const button = document.getElementById(“alert-button”)
  // baru tambahkan event listener
  button.addEventListener(“click”, function() {
  	  alert(input.value)
  })

  // atau
  button.onclick = function() { alert(input.value) }
  ```
- EventListener - Blur
“Blur”, lawan dari “focus”, adalah event di mana sebuah element kehilangan fokus dari user (misal user klk mouse di luar element tersebut atau user klik tab untuk berpindah element)
Misalkan kita ingin memvalidasi isi dari ``<input id=”username” />`` agar panjangnya minimal 6 karakter.
  ```javascript
  // cari dulu element tersebut berdasarkan id-nya

  const input = document.getElementById(“username”)

  // tambahkan event listener
  input.addEventListener(“blur”, () => {
	  if(input.value.length < 6) alert(“Panjang username minimal 6”)
  })
  ```
- EventListener - Form Submission
Misalkan kita mempunyai element beberapa input dalam sebuah form ``<input name=”email />`` dan ``<input type=”password” name=”password” />``. Bagaimana caranya  kita mendapatkan isi dari kedua input tersebut saat submit form?
Pasang event listener di form, lalu gunakan FormData untuk mengambil data dari masing-masing input
  ```javascript
  const form = document.getElementById(“form”)

  form.addEventListener(“submit”, function(event) {
	  // cegah page refresh
	  event.preventDefault()

	  const formData = new FormData(form)
	  const values = Object.fromEntries(formData) // { email: ... }
  })
  ```

 



















