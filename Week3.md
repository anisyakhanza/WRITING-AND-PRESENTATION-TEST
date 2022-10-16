# WRITING & PRESENTATION TEST (WEEK-3)
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
## DAY-4 JAVASCRIPT INTERMEDIATE
## JavaScript Asynchronous - Introducing
* Asynchronous programming : teknik yang memungkinkan sebuah progam untuk memulai tugas yang berpotensi berjalan lama dan masih dapat responsif terhadap peristiwa lain saat tugas itu berjalan, daripada menunggu sampai tugas itu selesai. Setelah tugas itu selesai, program Anda disajikan dengan hasilnya.
* Banyak function yang memakan waktu lama, karena itu tidak sinkron (asynchronous). contoh:
    * Membuat permintaan HTTP menggunakanfetch()
    * Mengakses kamera atau mikrofon pengguna menggunakangetUserMedia()
    * Meminta pengguna untuk memilih file menggunakanshowOpenFilePicker()
* Synchronous programming
    ```
    const name = 'Miriam';
    const greeting = `Hello, my name is ${name}!`;
    console.log(greeting);
    // "Hello, my name is Miriam!"
    ```
    * Mendeklarasikan string yang disebut name.
    * Mendeklarasikan string lain yang disebut greeting, yang menggunakan name.
    * Menampilkan salam ke konsol JavaScript.
    * Browser menunggu baris untuk menyelesaikan pekerjaannya sebelum melanjutkan ke baris berikutnya. Ini harus dilakukan karena setiap baris tergantung pada pekerjaan yang dilakukan pada baris sebelumnya. membuat ini menjadi program yang sinkron . Itu akan tetap sinkron bahkan jika kita memanggil fungsi yang terpisah. seperti :
        ```
        function makeGreeting(name) {
        return `Hello, my name is ${name}!`;
        }

        const name = 'Miriam';
        const greeting = makeGreeting(name);
        console.log(greeting);
        // "Hello, my name is Miriam!"
        ```
    * makeGreeting()adalah fungsi sinkron karena pemanggil harus menunggu fungsi tersebut menyelesaikan pekerjaannya dan mengembalikan nilai sebelum pemanggil dapat melanjutkan
* Ada beberapa masalah dasar dengan synchronous functions ang berjalan lama, sehingga yang dibutuhkan adalah
    * Mulai operasi yang berjalan lama dengan memanggil fungsi.
    * Suruh fungsi tersebut mulai beroperasi dan segera kembali, agar program kita tetap bisa responsif terhadap event-event lainnya.
    * Beritahu kami dengan hasil operasi ketika akhirnya selesai.
* Event handlers (Penangan acara) benar-benar merupakan bentuk pemrograman asinkron: Anda menyediakan fungsi (penangan acara) yang akan dipanggil, tidak segera, tetapi kapan pun peristiwa itu terjadi. event adalah perubahan status beberapa objek.
* Callbacks : fungsi yang diteruskan ke fungsi lain, dengan harapan bahwa panggilan balik akan dipanggil pada waktu yang tepat.
* jika nanti harus memanggil callback di dalam callback, kita mendapatkan doOperation()fungsi yang sangat bersarang, yang jauh lebih sulit untuk dibaca dan di-debug. Ini kadang-kadang disebut "callback hell" atau "pyramid of doom" (karena lekukannya terlihat seperti piramida di sisinya).

* JavaScript asynchronous:
    * Callback
    * Promises
    * Async await

## JavaScript Asynchronous - Promise

* Sebuah janji memiliki 3 keadaan:
    * Tertunda (pending) : hasilnya tidak ditentukan (undefined)
    * Terpenuhi (Fulfilled) : hasilnya adalah nilai (a result value)
    * Ditolak (Rejected) : hasilnya objek error (an error object)
* Dengan API berbasis promise, fungsi asinkron memulai operasi dan mengembalikan Promise objek. Kemudian nantinya dapat melampirkan penangan ke objek promise ini, dan penangan ini akan dieksekusi ketika operasi berhasil atau gagal.
* Cara menggunakan promise:
    ```
    myPromise.then(
    function(value) { /* code if successful */ },
    function(error) { /* code if some error */ }
    );
    ```
    * Promise.then() mengambil dua argumen, panggilan balik untuk sukses dan satu lagi untuk kegagalan.
    * Keduanya opsional, sehingga nantinya dapat menambahkan callback hanya untuk keberhasilan atau kegagalan.
---
## DAY-5 JAVASCRIPT INTERMEDIATE
## JavaScript - Web Storage

* Ada beberapa cara untuk menyimpan data pengguna seperti pencarian, artikel berita, dan lain-lain ke lokal (browser) menggunakan web storage seperti :
    * **Cookies**
    
        Data kecil yang dikirim dari situs web dan disimpan di komputer kita oleh web browser saat kita menjelajah. Disebut data kecil karena maksimum data yang dapat disimpan dalam cookies adalah 4096 bytes (4 KB).
    * **Local Storage**

        Disini dapat menyimpan data lebih besar yaitu 5MB per page tanpa mempengaruhi kinerja situs web.
        
        **Karakteristik:**
        * Menyimpan data tanpa tanggal kadaluarsa.
        * Data tidak akan dihapus ketika web browser ditutup dan akan tersedia seterusnya selama kita tidak menghapus data local storage pada web browser.
        * Dapat menyimpan data hingga 5MB.
        * Hanya dapat menyimpan data string.

        Untuk **menyimpan data** pada local storage, kita menggunakan method setItem() yang membutuhkan 2 parameter. Parameter pertama adalah key yang ingin kita simpan dan parameter kedua adalah data (value) dari key yang akan disimpan.
        ```
        localStorage.setItem('key', value);
        ```

        Untuk **mengambil data** yang telah tersimpan pada local storage, kita dapat menggunakan method getItem() yang membutuhkan 1 parameter. Parameter tersebut adalah key dari data yang kita inginkan.
        ```
        localStorage.getItem('key');
        ```
        
        Untuk **menghapus data** yang telah tersimpan pada local storage, kita dapat menggunakan method removeItem() yang membutuhkan 1 parameter. Parameter tersebut adalah key dari data yang ingin kita hapus.
        ```
        // menghapus key tertentu
        localStorage.removeItem("key");

        // menghapus semua key
        localStorage.clear();
        ```
        
    * **Session Storage**

        
        Disini dapat menyimpan data lebih besar yaitu 5MB per page tanpa mempengaruhi kinerja situs web. Bedanya dengan local storage, walaupun masuk ke dalam web storage, data yang tersimpan pada session storage akan hilang ketika session dari sebuah laman berakhir.

        **Karakteristik:**
        * Data yang disimpan pada session storage akan terus tersimpan selama browser terbuka dan tidak hilang jika laman di-reload.
        * Membuka banyak tab/window dengan URL yang sama, akan menciptakan session storage yang berbeda di masing-masing tab/window.
        * Menutup tab/window akan mengakhiri session dan menghapus data yang tersimpan di session storage pada tab/window tersebut.
        * Data yang tersimpan dalam session storage harus berbentuk string.
        * Hanya dapat menyimpan data sebanyak 5MB.

        Untuk **menyimpan data** sintaks nya sama dengan local storage 
        ```
        // menambah session storage
        sessionStorage.setItem('key', value);
        ```

        Untuk **mengambil data** sintaks nya sama dengan local storage
        ```
        // mendapatkan session storage
        sessionStorage.getItem('key');
        ```

        Untuk **menghapus data** dari session storage ada 2:
        ```
        // menghapus session storage satu persatu berdasarkan key
        sessionStorage.removeItem('key');

        // menghapus seluruh session storage sekaligus
        sessionStorage.clear();
        ```
* Penggunaan web storage ditentukan berdasarkan kebutuhan produk dan pengguna dengan mempertimbangkan karakteristik masing-masing pada cookie, local storage dan session storage.
