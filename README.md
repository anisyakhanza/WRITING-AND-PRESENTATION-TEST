# WRITING & PRESENTATION TEST (WEEK-2)
## DAY-1 JAVASCRIPT DASAR
## JavaScript - Scope
* Scope adalah konsep dalam flow data variabel. Dalam menentukan suatu variabel bisa diakses pada scope tertentu atau tidak
* Blocks adalah code yang berada didalam curly braces `{}`

    Sesuatu yang menggunakan blocks:
    * Conditional
    * Function
    * Looping

* Global scope berarti variabel yang kita buat dapat diakses dimanapun dalam suatu file
* Untuk menjadi Global Scope, suatu variabel harus dideklarasikan diluar Blocks
* Local scope berarti kita mendeklarasikan variabel didalam blocks seperti function, conditional, dan looping
* Untuk menjadi local scope, Maka variabel hanya bisa diakses didalam blocks saja. Tidak bisa diakses diluar blocks 

## JavaScript - Function
* Function adalah sebuah blok kode dalam sebuah grup untuk menyelesaikan 1 task/1 fitur
* Membuat function
```
function greeting() {
    return "Hello World";
}
```
* Memanggil function
```
greeting() // memanggil nama fungsi
console.log(greeting()); //output: "Hello World"
```
* Dengan parameter, function dapat menerima sebuah inputan data dan menggunakannya untuk melakukan task/tugas.
* Saat membuat function/fitur, kita harus tahu data-data yang dibutuhkan. (Misalnya saat membuat function penambahan 2 buah nilai. Data yang dibutuhkan adalah 2 buah nilai tersebut)
```
function penambahan(a, b) {
    return a + b;
}
```
* Argumen adalah nilai yang digunakan saat memanggil function.
* Jumlah argumen harus sama dengan jumlah parameternya
* Jadi jika di function penambahan ada 2 parameter nilai saat membuat function. Saat memanggil function kita gunakan 2 buah nilai argumen.
    ```
    function penambahan(a, b) {
        return a + b;
    }

    console.log(penambahan(5, 5)) // Output: 10
    ```
* function sangat dibutuhkan agar kita dapat dengan mudah memanage code dan tracing code jika ada error.
* Default paramaters digunakan untuk memberikan nilai awal/default pada parameter function.
* Default parameters bisa digunakan jika kita ingin menjaga function agar tidak error saat dipanggil tanpa argumen

* Function Helper

    Pada function ini kita bisa menggunakan function yang sudah dibuat pada function lain.

*   Arrow Function

    Merupakan fitur terbaru pada ES6. Kelebihan arrow function adalah penulisan fungsi menjadi lebih singkat dan lebih mudah dibaca.

* Short Syntax Function
    * Zero parameters
        ```
        const functionName = () => {};
        ```
    * One parameter
        ```
        const functionName = paramOne => {};
        ```
    * Two or more parameters
        ```
        const functionName = (paramOne, paramTwo) => {};
        ``` 
    * Single-line block
        ```
        const sumNumbers = number => number + number;
        ```
    * Multi-line block
        ```
        const sumNumbers = number => {
           const sum = number + number;
           return sum;
        ```
---
## DAY-2 JAVASCRIPT DASAR
## Data Type Built in Prototype & Method
* Javascript merupakan bahasa pemograman yang dinamic and weak types (tidak ada peraturan yang ketat buat bahasa ini)

* Menggunakan typeof untuk melihat type data.
```
let hewan = "kAnCIl"
console.log(typeof hewan);
```

* **Tipe data primitif** : Tipe data yang masih standart. Semua jenis kecuali objek mendefinisikan nilai yang tidak dapat diubah (yaitu, nilai yang tidak dapat diubah).
    * Boolean : Boolean mewakili entitas logis dan dapat memiliki dua nilai: benar dan salah.
    * Undefined : Variabel yang belum diberi nilai memiliki nilai yang tidak terdefinisi
    * Null : Memiliki tepat satu nilai null.
    * BigInt : Primitif numerik dalam JavaScript yang dapat mewakili bilangan bulat dengan presisi arbitrer. BigInts dapat dengan aman menyimpan dan mengoperasikan bilangan bulat besar bahkan di luar batas bilangan bulat aman untuk Numbers.
    * Symbol : Nilai primitif yang unik dan tidak dapat diubah dan dapat digunakan sebagai kunci dari properti Objek (lihat di bawah).
    * String : String berguna untuk menyimpan data yang dapat direpresentasikan dalam bentuk teks.  

        String memiliki 1 properties (ciri-ciri) berupa length berguna untuk mengecek ada beberapa banyak karakter.

            ```
            console.log(hewan.length);
            ```

        String mempunyai banyak method (keahlian). Method adalah sebuah function. contoh:
        *   ```
            console.log(hewan.toUpperCase()); // mengubah teks menjadi huruf kapital semua
            ```
        *   ```
            console.log(hewan.toLowerCase()); // mengubah teks menjadi huruf kecil semua
            ```
        *   ```
            console.log(hewan.chartAt(1)); // output: A
            akan menampilkan karakter nomer 1 mirip dengan array
            ```
        *   ```
            console.log(hewan.includes("n")); // output: true
            akan menegecek apakah ada nilai "n" pada "kAnCIl" jika benar akan menampilkan true, jika salah false.
            ```

    * Number : Digunakan untuk mewakili dan memanipulasi angka 
        Method number
         * Math.abs(x) : Digunakan untuk mengubah angka x yang bernilai negatif menjadi positif
         * Math.pow(x, y) : Digunakan untuk menghitung hasil dari x pangkat y
         * Math.sqrt(x) : Digunakan untuk menghitung akar kuadrat dari x
         * Math.cbrt(x) : Digunakan untuk menghitung akar pangkat 3 dari x
         * Math.round(x) : Digunakan untuk membulatkan angka desimal x menjadi bilangan bulat.
         * Math.floor(x) : Digunakan untuk membulatkan angka desimal x ke bawah
         * Math.ceil(x) : Digunakan untuk membulatkan angka desimal x ke atas
         * Math.random() : Digunakan untuk menampilkan angka secara acak antara 0 hingga 1 (0 termasuk. 1 tidak)
         * Math.max(x, y, z, ..., n) : Mencari angka terbesar
         * Math.min(x, y, z, ..., n) : Mencari angka terkecil


* **Tipe data non-primitif** : Merupakan tipe data kembangan dari tipe- tipe data tersebut
    * Array 
    * Object
---
## DAY-3 JAVASCRIPT DASAR
## DOM
* **DOM** (Document Object Model) adalah jembatan supaya bahasa pemograman dapat berinteraksi dengan dokumen HTML, dengan DOM, JS dapat memanipulasi struktur HTML. DOM merupakan progaming interface.

    File HTML -> load -> DOM (dalam bentuk tree structure)
* Dengan DOM, JavaScript diberi akses untuk membuat HTML menjadi dinamis, seperti:
    * Mengubah element HTML pada halaman website.
    * Mengubah attribute HTML pada halaman website.
    * Mengubah CSS style pada halaman website.
    * Menambah dan/atau menghapus element maupun attribute HTML.
    * Menambah HTML event (contoh: efek klik pada mouse, hover pada mouse, dan lain-lain) pada halaman website.
    * Berinteraksi dengan semua HTML event di website
* Pada HTML DOM, semua element HTML dari sebuah website dianggap sebagai objek
* DOM Property : untuk mengubah nilai properti dari element HTML
* DOM Method : untuk memanggil fungsi dari suatu element HTML
* ketika kita mengakses DOM kita akan mendapatkan element dan node
    * Element: cuma HTML element, contoh: `<span>`, `<div>`
    * Node : setiap bagian-bagian terkecil di HTML. contoh: text, comment, `<span>`

* **Traversing**(menjelajahi) ada 3 bagian. akses sesuai dengan kebutuhan
    * Ke bawah
        * getElementByID
        * getElementByClassName
        * getElementByTagName
        * querySelectorFamily
        * children
    * Ke atas
        * parentElement
        * closest()
    * Ke samping
        * nextElementSibling
        * previousElementSibling
---
## DAY-4 JAVASCRIPT DASAR
## DOM
* **Mengubah konten element**
    * createElement() : membuat element baru
    * appendChild() : menambahkan node ke daftar child nodes dari parent node yang telah ditentukan
    * textContent : mendapatkan dan mengatur content teks dari sebuah node
    * innerHTML : mendapatkan dan mengatur content teks dari sebuah element. innerHtml ini merubah isi contentnya bisa menyisipkan html. pada innerHtml tidak bisa memasukkan variable
    * innerText : hampir mirip dengan innerHtml. innerTeks ini merubah isi content dengan string saja
    * after() : menambahkan node setelah element
    * apppend() : menambahkan node setelah child node terakhir dari  parent node
    * prepend() : menambahkan node sebelum child node terakhir dari  parent node
    * insertAdjacentHTML() : parsing text sebagai HTML dan memasukkan node yang dihasilkan ke dalam document pada posisi yang telah ditentukan
    * replaceChild() : mengganti child element dengan new element
    * cloneNode() : mengkloning element dan semua keturunannya
    * removeChild() : menghapus element anak dari sebuah node
    * insertBefore() : menambahkan node baru sebelum node yang ada sebagai child node dari parent node yang telah ditentukan
    * insertAfter() helper function : menambahkan node baru setelah node yang ada sebagai child node dari parent node yang telah ditentukan  

* **Mengubah style element**
    * style property : mendapatkan atau mengatur style inline dari element
    * getComputedStyle() : mengembalikan style yang dihitung dari suatu element
    * className property : mengembalikan list space-separated CSS class
    * classList property :memanipulasi CSS class dari suatu element
    * Element’s width & height : mendapatkan width dan height dari element
---
## DAY-5 JAVASCRIPT DASAR
## DOM
* Interaksi User **(Events)** : User experience itu bersifat dua arah: 
    * menampilkan element HTML
    * halaman web juga harus bisa menangkap interaksi user
* HTML DOM event:
    * Focus
    * Change
    * Click
    * Hover
    * Blur
    * Scroll
    * Submit
* Mecam-macam event pada javascript:
    * onclick : event jika sebuah element html di klik
    * onchange : event jika sebuah element html berubah
    * onmouseover : event jika sebuah element html diletakkan cursor mouse
    * onekeydown: event jika saat terjadi pengetikan pada element html
    * onload : event jika saat element atau halaman dibuka 
* Menangkap Interaksi User 
    * Element.onevent
    * Dengan cara Element.addEventListener(“event”)
        * Bisa dihilangkan
        * Bisa ada beberapa event listener yang sama untuk 1 element
        * Memiliki argument tambahan { options }
    
* EventListener - Click

    Misalkan kita mempunyai element `<input id=”user-input” />`  dan `<button id=”alert-button”>show</button>`. 
    Jika ingin menampilkan pop up box yang berisi teks di dalam input tadi, yang harus dilakukan adalah 
    ```
    // cari dulu kedua element tersebut berdasarkan id-nya

    const input = document.getElementById(“user-input”)
    const button = document.getElementById(“alert-button”)

    // baru tambahkan event listener
    button.addEventListener(“click”, function() {
        alert(input.value)
    })

    // atau
    button.onclick = function() { alert(input.value) }
    ```

* EventListener - Blur 

    lawan dari “focus”, adalah event di mana sebuah element kehilangan fokus dari user (misal user klk mouse di luar element tersebut atau user klik tab untuk berpindah element)

    Jika ingin memvalidasi isi dari `<input id=”username” />` agar panjangnya minimal 6 karakter..
    ```
    // cari dulu element tersebut berdasarkan id-nya

    const input = document.getElementById(“username”)

    // tambahkan event listener
    input.addEventListener(“blur”, () => {
        if(input.value.length < 6) alert(“Panjang username minimal 6”)
    })
    ```

* EventListener - Form Submission

    Misalkan kita mempunyai element beberapa input dalam sebuah form `<input name=”email />` dan `<input type=”password” name=”password” />`

    ada 2 cara untuk memdapatkan isi dari kedua input saat submit form:
    * Pasang event listener di kedua input dan tombol submit, lalu saat tombol diklik, baca value dari kedua input tersebut. 
    * Pasang event listener di form, lalu gunakan FormData untuk mengambil data dari masing-masing input

    Caranya:
    Pasang event listener di form, lalu gunakan FormData untuk mengambil data dari masing-masing input
    ```
    const form = document.getElementById(“form”)

    form.addEventListener(“submit”, function(event) {
        // cegah page refresh
        event.preventDefault()

        const formData = new FormData(form)
        const values = Object.fromEntries(formData) // { email: ... }
    })
    ```
