# WRITING (WEEK-6)
## DAY 1 REACT JS LANJUTAN - PROPTYPES
* Prop Types merupakan lib yang dapat membantu untuk memeriksa data props yang dikirim, dengan kata lain nantinya kita akan mengecek type dari sebuah prop agar sesuai dengan ekspetasi. Jika tidak sesuai maka akan muncul pesan error. 
* Install Proptypes:
    ```
    npm install prop-types
    ```
* Props yang akan dikirim harus sesuai dengan tipe data yang diinginkan
* Nanti akan muncul pesan error pada console log jika tidak sesuai ekspetasi

## DAY 2 REACT ROUTER
* Router dipakai buat pindah-pindah halaman
* Perbedaan dengan waktu yang di html itu menggunakan tag `<a>` kalau di react menggunakan tag `<link>` dengan fungsi yang sama untuk memindah halaman 
* React router akan dipakai untuk berpindah-pindah halaman
* Cara memakai react router versi 6
    * Install Router menggunakan npm
        ```
        npm install react-router-dom@6
        ```
    * import BrowserRouter pada index.js
        ```
        import { BrowserRouter } from "react-router-dom";
        ```
    * Tambahkan pada React.strickMode
        ```
        <BrowserRouter>
            <App />
        </BrowserRouter>
        ```
* BrowserRouter merupakan pembungkus agar react router bisa berjalan. Jika lupa membungkus menggunakan BrowserRouter maka tidak akan berjalan routingan-nya kita
* Setiap membikin project baru, kita haru menginstal react app nya, mengcreate dari awal. React router nya juga diinstalldari awal.