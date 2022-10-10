# WRITING & PRESENTATION TEST (WEEK-2)
## DAY-1 JAVASCRIPT INTERMEDIATE
## JavaScript - Array
* Array adalah tipe data list order yang dapat menyimpan tipe data apapun di dalamnya.
* Array dapat menyimpan tipe data String, Number, Boolean, dan  lainnya
* contoh array:
    ```
    let buah = ['pisang', 'semangka', 'mangga'];
    console.log(buah);
    ```
* Membuat array dengan menggunakan square brackets `[]`
*  Mengakses dan memangil array dengan nama array[index]
    ```
    console.log(buah[0]); //output: 'pisang'
    ```
* Array pada javascript dihitung dari index data ke-0. Data pertama adalah index ke-0.
* Data array bisa diupdate
    ```
    let buah = ['pisang', 'semangka', 'mangga'];

    buah[0] = 'melon';
    console.log(buah); //output: 'melon', 'semangka', 'mangga'
    ```
* Const in array
    * Jika menggunakan let, kita dapat mengubah array dengan array baru dan konten nilai yang ada di dalam array dengan nilai lain
    * Const tidak bisa melakukan update data. Namun pada Array kita dapat melakukan update  konten nilai di dalam array (mutable).
    * Yang tidak bisa adalah mengubah array dengan array yang baru jika menggunakan const
* Array properties
    
    Properties adalah fitur yang sudah disediakan oleh Javascript untuk memudahkan developer. Yang paling sering digunakan:
    * .length : length akan mengembalikan nilai dari jumlah panjang data suatu array
    * 
* Array method

    Array memiliki method atau biasa disebut built-in methods.Javascript sudah memudahkan kita dengan menyediakan function/method umum yang bisa kita gunakan. Contoh Array Built-in Methods
    * .push() : method untuk menambahkan item array pada urutan yang paling akhir
    * .pop() : method yang menghapus item array index terakhir
    * .shift() : method untuk menghapus item Array pada index pertama
    * .unshift() : method untuk menambahkan item Array pada index pertama
    * .sort() : method untuk mengurutkan secara Ascending atau Descending Alphanumeric
* Looping pada Array

    Array memiliki built in methods untuk melakukan looping yaitu `.map()` dan `.forEach()`
    * .forEach() adalah method untuk melakukan looping pada setiap elemen array. gunakan .forEach() jika hanya memerlukan looping untuk menampilkan saja atau menyimpan ke database.
    * .map() melakukan perulangan/looping dengan membuat array baru. Gunakan .map() jika akan melakukan operasi pada array seperti yang dapat mengubah nilai array sebelumnya.

    .map() dan forEach() sama-sama melakukan looping dan mengembalikan nilai baru dari operasi yang dilakukan.

    Perbedaannya adalah .forEach tidak dapat membuat Array barudari hasil operasi yang ada dalam looping

## JavaScript - Multidimensional Array
* Multidimensional Array dianalogikan sebagai array di dalam array
* Misalnya multidimensional ini seperti Table. Baris pada table itu menunjukan jumlah array. Column pada table itu menunjukan isi dari tiap array.
* Akses index multidimensional array
    ```
    let inventory = [
        ['kaos polos', 10],
        ['jaket hoodie', 12],
        ['topi', 24],
        ['celana jeans', 8],
    ];

    console.log(inventory[1][0]);
    //output: jaket hoodie
    ```
* Multidimensional array bisa menggunakan Property dan Method built-in Array
---
## DAY-2 JAVASCRIPT INTERMEDIATE
## JavaScript - Object
* Object adalah sebuah tipe data pada variabel yang menyimpan properti dan fungsi (method)
* Properti adalah data lengkap dari sebuah object.
* Method adalah action dari sebuah object. Apa saja yang dapat dilakukan dari suatu object.
* Mengakses Object dan Property Object
    * Dot notation
        ```
        console.log(person.name);
        ```
    * Bracket notation
        ```
        console.log(person['name']);
        ```
* Update pada variabel dengan tipe data Object
    * Object dapat mengupdate value dari key yang sudah tersedia
    * Object dapat menambahkan key dan value baru
    * Jika menggunakan constant pada variable object. Kita tidak bisa mengganti seluruh data object dengan object yang baru
    * Jika membutuhkan untuk update seluruh data object gunakan ‘let’ pada saat deklarasi variabel.
* Progammer dapat menghapus properti dari object menggunakan delete operator
* Method : Value yang kita masukkan pada property berupa function.
* console adalah global 
javascript object.
* log() adalah property yang berupa function dari object console.
* Nested Object : Data object yang kompleks. Object yang berasal dari turunan object lainnya.
* Passed by reference: Mengubah data yang ada pada object melalui sebuah function dan memasukkan object sebagai parameter function.
* Jika ingin menampilkan seluruh object properti bisa menggunakan Looping Object. Sehingga tidak perlu mengakses secara manual memanggil setiap properti nya
* Array of Object bisa menyimpan banyak data.
---
## DAY-3 JAVASCRIPT INTERMEDIATE
## JavaScript - Recursive
* Recursive adalah function yang memanggil dirinya sendiri sampai kondisi tertentu
* Recursive kebanyakan digunakan untuk case matematika, fisika, kimia, dan yang berhubungan dengan calculation
* Struktur recursive
    ```
    function recursive() {
        //...
        recursive();
        //...
    }
    ```
* Recursive akan berhenti memanggil dirinya sendiri jika kondisi terpenuhi
* Ciri dari recursive:
    * Selalu memiliki kondisi yang menyatakan kapan fungsi tersebut berhenti. 
    * Selalu memanggil dirinya sendiri sambil mengurangi atau memecahkan data masukan setiap panggilannya.
* Tujuan utama dari recursive adalah memecahkan masalah dengan
mengurangi masalah tersebut menjadi masalah-masalah kecil.
---

