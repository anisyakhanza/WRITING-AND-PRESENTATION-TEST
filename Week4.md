# WRITING & PRESENTATION TEST (WEEK-4)
## DAY-1 JAVASCRIPT INTERMEDIATE
## JavaScript Asynchronous - Fetch
* Dalam JavaScript kita bisa mengirimkan network request dan juga bisa mengambil informasi data terbaru dari server jika dibutuhkan.
* Contoh network request yang biasa kita lakukan:
    * Mengirimkan data dari sebuah form.
    * Mengambil data untuk ditampilkan dalam list/table.
    * Mendapatkan notifikasi.
* Untuk melakukan network request, JavaScript memiliki metode bernama fetch()
* Proses melakukan fetch() adalah salah satu proses asynchronous di JavaScript sehingga kita perlu menggunakan salah satu diantara promise atau async/await.
    * Fetch dengan Promise

        Mengambil data end-point dari API JSONPlaceholder 
        ```
        fetch("https://jsonplaceholder.typicode.com/posts")
        .then(function (response) {
            return response.json();
        })
        .then(function (post) {
            console.log(post);
        });
        ```
    * Fetch dengan async/await

        ```
        const tesFetchAsync = async () => {
        let response = await fetch("https://jsonplaceholder.typicode.com/posts");
        response = await response.json();
        console.log(response);
        };
        tesFetchAsync();
        ```

* Keduanya menghasilkan inputan yang sama, penggunaan promise ataupun async/await tetapi kita lihat jika menggunakan async/await, kode kita terlihat lebih clean dan mudah dibaca.

## JavaScript Asynchronous - Async Await
* Async/await dan promise itu sama saja, namun hanya berbeda dari syntax dan cara penggunaannya
* async, mengubah function synchronous menjadi asynchronous.
* await, menunda eksekusi hingga proses asynchronous selesai.
* Sebuah async function bisa tidak berisi await sama sekali atau lebih dari satu await. Keyword await hanya bisa digunakan didalam async function, jika digunakan di luar async function maka akan terjadi error.
* contoh penggunaan async
    ```
    // async menggunakan keyword function 
    async function tesAsyncAwait() {
    return "Fulfilled";
    }

    console.log(tesAsyncAwait());
    // async menggunakan arrow function
    const tesAsyncAwait = async () => {
    return "Fulfilled";
    };

    console.log(tesAsyncAwait());
    ```
* contoh penggunaan async/await
    ```
    async function tesAsyncAwait() {
    await 'Fulfilled';
    }
    ```
    await hanya bisa digunakan dalam async function dan await adalah keyword dalam async yang digunakan untuk menunda hingga proses asynchronous selesai.

---
## DAY-2 GIT & GITHUB LANJUTAN
* Berkolaborasi di git bersama tim atau lebih dari satu orang. Pentingnya tim ini karena di dalam web akan ada banyak fitur. sehingga adanya tim akan lebih ringan karena pengerjaan nya bisa dibagi.
* Cara berkolaborasi
    * Siapkan repositori terlebih dahulu, baik itu repositori pribadi (harus dikasih akses ke anggota tim-nya) atau organization 
    * Lebih baik menggunakan organization, caranya:
        * Klik `+` yang ada dipojok kanan (new organization)
        * Pilih free (create a free organization)
        * Mengisi data untuk penamaan organization. kemudian next
    * Setelah membuat organization, invite semua teman-teman yang berada dalam tim, kemudian ubah hak aksesnya menjadi owner
    * Setelah organization nya sudah ada, selanjutnya membuat repositori
    * Kemudian membuat branch bernama `dev`

* Mengecek pull request
    * Setiap ada pull request, team lead akan mengeceknya
    * Jika pull request belum sesuai, dapat diberi komen atau diberi kaar anggota yang melakukan pull request tersebut
    * Jika sudah sesuai lakukan merge

---
## DAY-3 RESPONSIVE WEB DESIGN
* Responsive Web Design (RWD) bertujuan untuk membuat desain website dapat diakses dalam device apapun, misal laptop/PC, smartphone, tablet
* Responsive :
    * meta viewport
    * max-width
    * relative unit
    * media query
    * flex
    * grid
* Setiap developer web wajib menggunakan tool bawaan dari setiap browser yang memudahkan proses dalam development
* Pada browser chrome biasanya disebut juga chrome dev tools
* Media query digunakan untuk membuat beberapa styles tergantung pada jenis device
* Ada dua cara/pattern dalam menggunakan media query:
    * Membuat file css berbeda untuk masing-masing device
    * Menggabungkan 1 file css untuk setting styling berbagai device
* Breakpoint adalah perubahan yang terjadi pada tampilan saat berganti device atau ukuran width. Ada 3 breakpoint
* Complex breakpoint media query
    
     Dapat digunakan jika kita menginginkan tampilan yang ingin diteraokan pada arnge ukuran device tertentu, kita bisa membuatnya menjadi range media query
* Tidak ada aturan baku dalam besaran width dan berapa banyak breakpoint yang harus dilakukan.
* Responsive web design dilakukan sesuai kebutuhan konten 
* Jika sebuah konten yang ditampilkan sudah tidak bisa diakses atau sulit dilihat pada width tertentu, saatnya menggunakan media query

## BOOTSTRAP 5
* Bootstrap merupakan sebuah framework css untuk melakukan styling yang membuat lebih cepat dan responsif
* Disarankan satu website satu framework biar memorinya tidak besar
* Cara custom bootstrap,tinggal bikin class, tambahin class baru di element nya terus tinggal dicustom
* ada 2 cara untuk mecustom
    * lansung ke element bootstrap
    * menimpa bootsrap yang sudah ada dengan styling yang baru, tinggal bikin class baru
