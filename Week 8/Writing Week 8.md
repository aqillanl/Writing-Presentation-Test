# **Writing Test Week 8**
## **React JS Lanjutan**
#### **React Context**
- Context menyediakan cara untuk oper data melalui diagram komponen tanpa harus oper props secara manual di setiap tingkat.
- Dalam aplikasi React yang khusus, data dioper dari atas ke bawah (parent ke child) melalui props, tetapi ini bisa menjadi rumit untuk tipe props tertentu (mis. preferensi locale, tema UI) yang dibutuhkan oleh banyak komponen di dalam sebuah aplikasi. Context menyediakan cara untuk berbagi nilai seperti ini di antara komponen tanpa harus oper prop secara explisit melalui setiap tingkatan diagram.
- Sebelum Menggunakan Context
  - Context terutama digunakan ketika beberapa data harus dapat diakses oleh banyak komponen pada tingkat bersarang yang berbeda. Gunakan dengan hemat karena membuat penggunaan kembali komponen menjadi lebih sulit.
  - Jika Anda hanya ingin menghindari mengoper beberapa props melalui banyak tingkatan, komposisi komponen seringkali menjadi solusi yang lebih sederhana daripada context.
- Kapan Menggunakan Context
  - Context dirancang untuk berbagi data yang dapat dianggap “global” untuk diagram komponen React, seperti pengguna terotentikasi saat ini, tema, atau bahasa yang disukai.
#### **React Testing**
- Unit testing adalah sebuah pekerjaan dimana kita melakukan pengujian pada suatu bagian pada aplikasi yang kita buat. Tujuan dari unit testing sendiri yaitu untuk melakukan validasi setiap unit pada kode aplikasi agar berfungsi seperti yang diharapkan. Unit yang dimaksud bisa berupa kode, fungsi, metode, prosedur, modul, atau objek tersendiri. 
- Alasan unit testing itu penting diantaranya:
  1. Membantu memperbaiki bug di awal pada siklus software development,
  2. Membantu developer untuk memahami basis kode dan memungkinkan mereka membuat perubahan dengan cepat,
  3. Berfungsi sebagai dokumentasi proyek,
  4. Membantu reusability code pada projek baru.
- React testing framework jest </br>
Jest adalah framework pengujian JavaScript yang menyenangkan dengan fokus pada kesederhanaan. Ia bekerja dengan projek yang menggunakan: Babel, TypeScript, Node, React, Angular, Vue, dan lainnya!
- React testing react testing library </br>
React Testing Library adalah solusi yang sangat ringan untuk menguji komponen React. Ini menyediakan fungsi utilitas ringan di atas react-dom dan react-dom/test-utils, dengan cara yang mendorong praktik pengujian yang lebih baik.
- Step Sebuah Testing terdapat 3:
  1. Assert, Hasil yg diharapkan: Langkah-langkah tindakan harus menimbulkan semacam tanggapan. Terkadang, pernyataan sesederhana memeriksa nilai numerik atau string. Di lain waktu, mungkin memerlukan pemeriksaan beberapa aspek sistem. Pernyataan pada akhirnya akan menentukan apakah tes lulus atau gagal.
  2. Arrange, Input dan Target : Mengatur langkah-langkah harus mengatur kasus uji. Apakah tes memerlukan objek atau pengaturan khusus, apakah perlu menyiapkan database dan apakah perlu masuk ke aplikasi web
  3. Act, Berdasarkan Perilaku Target: Langkah-langkah tindakan harus mencakup hal utama yang akan diuji. Ini bisa berupa memanggil fungsi atau metode, memanggil REST API, atau berinteraksi dengan halaman web. Juga agar tindakan tetap fokus pada perilaku target.

