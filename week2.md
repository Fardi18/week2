# JavaScript : Scope dan Fucntion

- ## Scope

  Scope adalah konsep dalam flow data variabel. Menentukan suatu variabel bisa diakses pada scope tertentu atau tidak.

  - ### Blocks
    Blocks adalah code yang berada didalam curly braces {} (kurung kurawal). Conditional, function, dan looping adalah contoh yang menggunakan blocks.
  - ### Global Scope

    Global scope berarti variabel yang telah dideklarasikan dapat diakses dimanapun dalam suatu file. Agar menjadi Global Scope, suatu variabel harus dideklarasikan diluar Blocks.

    - Contohnya :

      ```javascript
      let nama = "Fardi";

      function sapaNama() {
        return nama; // Fardi
      }
      sapaNama();
      console.log(sapaNama()); // Fardi
      ```

      > variable nama adalah variable dengan scope global karena dideklarasikan di luar blocks yaitu function.

  - ### Local Scope

    Local scope berarti kita mendeklarasikan variabel didalam blocks seperti function, conditional, dan looping. Maka variabel hanya bisa diakses didalam blocks saja. Tidak bisa diakses diluar blocks.

    - Contohnya :

      ```javascript
      function sapaNama() {
        let nama = "Fardi";
        return nama; // Fardi
      }
      console.log(sapaNama()); // Fardi
      console.log(nama); // Error karena nama adalah memiliki scope local
      ```

      > variable nama adalah variable dengan scope local karena dideklarasikan di dalam blocks yaitu function.

- ## Function

  Function adalah sebuah blok kode dalam sebuah grup untuk menyelesaikan 1 task/1 fitur. Saat kita membutuhkan fitur tersebut nantinya, kita bisa kembali menggunakannya. Fungsi dapat beridiri sendiri atau disimpan di dalam sebuah variable. Fungsi dapat dipanggil cukup dengan menambahkan tanda kurung () setelah nama fungsi.

  - ### Membuat Function
    ```javascript
    function greeting() {
      return "Hello, World!";
    }
    ```
    > function : function keyword, greeting : nama fungsi, dan return 'Hello, World! : function bodynya.
  - ### Memanggil Function
    ```javascript
    greeting();
    console.log(greeting());
    ```
  - ### Parameter dan Argumen
    - #### Parameter
      Parameter : syarat input yang harus dimasukkan ke dalam suatu fungsi dan dideklarasikan bersama dengan deklarasi fungsi. Dengan parameter, function dapat menerima sebuah inputan data dan menggunakannya untuk melakukan task/tugas. Saat membuat function/fitur, kita harus tahu data-data yang dibutuhkan. Misalnya saat membuat function penambahan 2 buah nilai, maka data yang dibutuhkan adalah 2 buah nilai tersebut.
      ```javascript
      function tambahDuaAngka(a, b) {
        return a + b;
      }
      ```
      > a dan b adalah parameter
    - #### Argumen
      Argumen : nilai yang dimasukan ke dalam suatu fungsi, sesuai dengan persyaratan parameter, di mana argument dituliskan bersamaan dengan pemanggilan fungsi. Argumen adalah nilai yang digunakan saat memanggil function. Jumlah argumen harus sama dengan jumlah parameternya. Jadi jika di function penambahan ada 2 parameter nilai saat membuat function. Saat memanggil function kita gunakan 2 buah nilai argumen.
      ```javascript
      function tambahDuaAngka(a, b) {
        return a + b;
      }
      console.log(tambahDuaAngka(5, 6)); // outputnya : 11
      ```
      > 5 dan 6 adalah argumen
  - ### Default Parameter

    Default paramaters digunakan untuk memberikan nilai awal/default pada parameter function. Default parameters bisa digunakan jika kita ingin menjaga function agar tidak error saat dipanggil tanpa argumen.

  - ### Arrow Function
    Arrow function adalah cara lain menuliskan function. Ini adalah fitur terbaru yang ada pada ES6 (Javascript Version)
    ```javascript
    let luasPersegiPanjang = (a, b) => {
      return a * b;
    };
    ```
  - ### Short Syntax Function
    - 0 Parameter
      ```javascript
      let namaFungsi = () => {};
      ```
    - 1 Parameter
      ```javascript
      let namaFungsi = (parameter1) => {};
      ```
    - 2 atau lebih Parameter
      ```javascript
      let namaFungsi = (parameter1, parameter2) => {};
      ```
    - Single-Line Block
      ```javascript
      let sumNumbers = (number) => number + number;
      ```
    - Multi-Line Blocks
      ```javascript
      let sumNumbers = (number) => {
        let sum = number + number;
        return sum;
      };
      ```
      <br><br><br>

# Data Type Built in Prototype & Method

- ## Tipe Data

  Tipe data adalah jenis data yang bisa disimpan di dalam suatu variable seperti defisini variable yaitu tempat untuk menyimpan suatu nilai atau data yang dimana data tersebut merupakan tipe data.
  Terdapat beberapa jenis tipe data di dalam bahasa JavaScript, tetapi secara garis besar dibagi menjadi dua bagian, yaitu :

  - Tipe data primitif:
    - String, adalah deretan karakter yang diapit oleh sepasang tanda kutip
    - Number, adalah bilangan baik itu bilangan bulat, pecahan, dll.
    - Boolean, adalah tipe data yang memiliki nilai true dan false
    - Null, adalah sebuah nilai kosong atau merujuk pada nilai yang tidak ada
    - Undefined, adalah menandakan kondisi variable yang belum diberi sebuah nilai
    - Symbol, adalah sebuah nilai unik yang dihasilkan tiap kali kita memanggil fungsi Symbol(). Nilai unik ini memiliki beberapa kegunaan seperti memberi nomor identifikasi unik dan berperan sebagai nama properti unik sebuah objek
  - Tipe data non-primitif:
    - Object, adalah sekumpulan pasangan properti dan value.

- ## Prototype and Method
  Properti diiabaratkan sebagai ciri-ciri sedangkan method adalah apa yang bisa dilakukan.
  - ### String
    Di sini hanya diberikan beberapa method string saja, lengkapnya cek
    [di sini.](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/charAt)
    - Propertinya
      - length
        Digunakan untuk mengetahui panjang dari suatu karakter.
    - Methodnya
      - toLowerCase()
        Digunakan untuk mengubah string menjadi huruf kecil (dikonversi menjadi lower case)
      - toUpperCase()
        Digunakan untuk mengubah string menjadi huruf besar (dikonversi menjadi upper case)
      - charAt()
        Digunakan untuk mengembalikan karakter sesuai dengan index yang dipanggil.
      - includes()
        Digunakan untuk melakukan pencarian terhadap string, jika ada maka akan menghasilkan nilai true, jika tidak maka akan menghasilkan nilai false
      - split()
        Digunakan untuk memisah sebuah string menjadi sebuah array berdasarkan pola yang ditentukan, contohnya dipisahkan berdasarkan spasi atau koma yang ada pada string.
  - ### Number
    Di sini hanya diberikan beberapa properti dan method number saja, lengkapnya cek [di sini.](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number/isNaN)
    - Propertinya
      - MAX_VALUE
      - MIN_VALUE
      - NaN
    - Methodnya
      - isInteger()
        Digunakan untuk menentukan apakah suatu nilai merupakan integer atau tidak, memiliki dua keluaran yaitu true atau false.
      - isNan()
        Digunakan untuk menentukan apakah suatu nilai merupakan NaN (Not-A-Number) dan akan mengembalikan dua nilai yaitu true dan false
  - ### Math
    Di sini hanya diberikan beberapa properti dan method Math sajalengkapnya cek [di sini.](https://developer.mozilla.org/en-US/docs/WeJavaScript/Reference/Global_Objects/Math?retiredLocale=id)
    - Propertinya
      - Math.E
        Digunakan untuk mengembalikan nilai e (pada matematika) = 2.718
      - Math.PI
        Digunakan untuk memberikan nilai phi (biasa diguanakan untumenghitung luas lingkaran pada matematika) = 3.14
    - Methodnya
      - ceil()
        Digunakan untuk membulatkan bilangan ke atas.
      - flor()
        Digunakan untuk membulatkan bilangan ke bawah.
      - sqrt()
        Digunakan untuk menentukan akar suatu bilangan.
      - min()
        Digunakan untuk menentukan nilai terkecil.
      - max()
        Digunakan untuk menentukan nilai terbesar.
        <br><br><br>

# DOM (Document Object Model)

Document Object Model (DOM) adalah sebuah interface yang memungkinkan developer untuk memanipulasi halaman web baik dari segi struktur, tampilan dan kontennya. DOM bisa dianggap sebagai jembatan penghubung antara bahasa pemrograman dengan dokumen HTML.
Beberapa hal yang dapat dilakukan oleh DOM adalah:

- Mengubah elemen HTML pada halaman website
- Mengubah atribut HTML pada halaman website
- Mengubah CSS style pada halaman website
- Menmabah/menghapus elemen maupun atribut HTML
- Menambah HTML event
- Berinteraksi dengan semua HTML event di website
  Di dalam HTML DOM, semua elemen HTML dari sebuah website dianggap sebagai objek. Sebagaimana objek pada JavaScript pada umumnya, objek elemen HTML di HTML DOM juga memiliki properti dan method yang lebih dikenal dengan sebutan DOM Property dan DOM Method. Jadi, untuk mengubah value property dari elemen HTML, kita bisa menggunakan DOM Property dan untuk memanggil fungsi dari suatu elemen HTML, kita bisa menggunakan DOM Method.
- ## Mengakses Elemen HTML

  - getElementByID("id") <br>
    Method yang digunakan untuk mengakses elemen HTML berdasarkan nilai atribut id-nya.
  - getElementsByTagName("tag-name") <br>
    Method yang digunakan untuk mengakses elemen HTML berdasarkan jenis tag-nya.
  - getElementsByClassName("class") <br>
    Method yang digunakna untuk mengkases elemen HTML berdasarkan nilai atribut class-nya
  - querySelectorALL <br>
    Method yang digunakan untuk mengakses elemen HTML berdasarkan CSS selector-nya HTML
  - children <br>
    Method yang digunakan untuk mengakses semua elemen anak dari elemen saat ini
  - parentElement <br>
    Method yang digunakan untuk mengakses elemen induk dari elemen saat ini

- ## Manipulasi DOM

  Dengan menggunakan DOM kita bisa memanipulasi elemen HTML, berikut beberapa method yang digunakan:

  - createElement <br>
    Digunakan untuk membuat elemen HTML pada struktur suatu website (HTML) seperti menambahkan paragraf, heading, dll.
  - createTextNodes <br>
    Digunakan untuk membuat sebuah text atau kalimat
  - append() <br>
    Digunakan untuk menambahkan element baik berupa object node maupun DOMSring
  - appendChild() <br>
    Hanya bisa menambahkan Node Object tapi tidak bisa untuk menambahkan elemen berupa DOM String
  - innerHTML <br>
    Mengembalikan sebuah teks berdasarkan tag HTML yang dituliskan, misal
    ```javascript
    p.innerHTML = "<p>Ini adalah paragraf</p>"; // akan menghasilkan paragraf
    ```
  - innerText <br>
    Digunakan untuk menampilkan konten berupa teks di halaman website.
  - textContent <br>
    Digunakan untuk mendapatkan konten berupa teks pada elemen HTML
  - remove <br>
    Digunakan untuk menghapus elemen HTML pada sebuah website
  - .attributes
    Digunakan untuk mencaritahu atribut apa saja yang dimiliki oleh suatu elemen HTML
  - .getAtrribute() <br>
    Digunakan untuk mendapatkan/mengambalikan atribut dari suatu elemen HTML
  - .setAttribute() <br>
    Digunakan untuk menyetting atau mengatur atribut serta value dari suatu elemen HTML
  - .hasAttribute() <br>
    Digunakan untuk mengetahui apakah suatu node atau elemen HTML memiliki atribut atau tidak, jika iya akan mengembalikan nilai true dan sebaliknya adalah false.
  - .style.color <br>
    Digunakan untuk memberikan style color pada suatu elemen HTML tertentu
  - .style.backgroundColor <br>
    Digunakan untuk memberikan stye berupa background-color pada suatu elemen HTML tertentu
  - classList <br>
    Digunakan untuk memanipulasi class yang ada pada element HTML

- ## Event DOM

  Event adalah suatu kejadian, peristiwa, atau kegiatan yang dilakukan/terjadi di website, contohnya adalah saat user menekan tombol, menyorot suatu link/tombol, dll.
  Terdapat 3 cara memberikan Event DOM, antara lain adalah :

  1. HTML attribute

  ```html
  <!-- html -->
  <h1 onclick="alert('Selamat Datang!')">Hallo</h1>
  <!-- atribut onclick merupakan dom event dan akan menghasilkan pop-up (alert) berupa text yaitu Selamat Datang! jika user menekan heading satu dengan konten Hallo -->
  ```

  2. Event property

  ```javascript
  // file html
  <p id="paragraf">Click Me</p>;

  // file javascript
  let paragraf = document.getElementByID("paragraf");
  paragraf.onclick = function () {
    alert("ini dari paragraf");
  };
  ```

  3. addEventListener()

  ```javascript
  // file html
  <button id="btn">Click Me</button>;

  // file javascript
  let tombol = document.getElementByID("btn");
  tombol.addEventListener("click", function () {
    alert("ini dari button");
  });
  ```

  Secara sederhana, terdapat beberapa macam event DOM, antara lain adalah:

  - click
  - submit
  - focus
  - hover
  - blur
  - scroll
  - change
