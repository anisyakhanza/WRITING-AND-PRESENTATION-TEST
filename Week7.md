# WRITING (WEEK-7)
## DAY 1 REACT CONTEXT 
* Di context ini nantinya akan membuat sebuah component yang akan memprovide aplikasinya. sehingga nanti kalau component nya butuh state, tinggal di ambil dari component context nya.
* Context menyediakan cara untuk meneruskan data melalui pohon component tanpa harus meneruskan prop secara manual di setiap level.
* Context bisa ngeshare data (global), misal autentifikasi user, sebuah tema, language


---
## DAY 2 REACT CONTEXT 
* passing props: cara yang bagus untuk secara eksplisit menyalurkan data melalui hierarki UI Anda ke component yang menggunakannya.
* Context adalah state management built in React.
* **Membuat context**
    ```
    const Context = createContext(MockData);
    ```
* **Membuat Provider pada context**
    ```
    const Parent = () => {
     return (
        <Context.Provider value={initialValue}>
        <Children/>
        </Context.Provider>
        )
    }
    ```
* **Mengimpor context**
    ```
    import { createContext } from "react"
    ```

* Perbedaan Redux dan Context

   Untuk state management dalam react, dalam arti secara keseluruhan, tidak ada hal yang benar benar berbeda antara Redux dengan Context. Satu hal yang mungkin berbeda adalah Context merupakan state management built in React, sedangkan Redux adalah third party library yang dapat digunakan dengan React. Akan tetapi, kedua hal tersebut (Context dan Redux) mempunyai tujuan yang sama, yaitu untuk mengatur state management
---
## DAY 3 REACT TESTING
* React Testing : Seperangkat helpers yang memungkinkan Anda mengetes komponen pada React tanpa bergantung pada detail implementasinya. Ada banyak jenis testing yang terbagi dalam tiga kategori utama yaitu :
    * unit testing
    * integration testing
    * UI testing
* Tampilan alur pengujian/testing :
    * impor fungsi untuk menguji
    * berikan masukan ke fungsi
    * tentukan apa yang diharapkan sebagai output
    * periksa apakah fungsi menghasilkan output yang diharapkan
* Alasan pentingnya unit testing:
    * Membantu memperbaiki bug di awal pada siklus software development dan menghemat biaya
    * Membantu developer untuk memahami basis kode dan memungkinkan mereka membuat perubahan dengan cepat
    * Berfungsi sebagai dokumentasi proyek
    * Membantu reusability code pada projek baru

* Unit testing memiliki tiga teknik:
    * **Black Box Testing**
        
        Sebuah pengujian yang tidak perlu melihat dan memahami suatu software lebih dalam, pengujiannya melalui user interface, input dan output
    * **White Box Testing**

        White box testing bersifat transparan jadi kita bisa melihat suatu sistem dari awal sampai akhir untuk dilakukan testing. Untuk testingnya dilakukan untuk menguji struktur internal, desain, fungsi dan detail implementasi dari sebuah aplikasi
    * **Grey Box Testing**

        Grey box testing ini merupakan sebuah perpaduan antara black box testing dan white box testing. Pengujiannya ini digunakan untuk eksekusi test, resiko dan metode penilaian

* Jest adalah test runner pada JavaScript yang memungkinkan untuk mengakses DOM melalui jsdom. Untuk setiap pengujian, Umumnya kita me-render ke sebuah elemen DOM yang terhubung dengan document, agar pengujian dapat menerima event DOM. Setelah pengujian selesai, kita harus melakukan "pembersihan". Cara yang umum dilakukan adalah menggunakan pasangan blok beforeEach dan afterEach agar mereka terus berjalan dan memisahkan efek-efek dari sebuah pengujian hanya kepada pengujian tersebut. Cara Install Jest:
    ```
    npm i jest --save-dev
    ```

    Untuk menjalankan tes, tambahkan ini ke package.json:

    ```
    "scripts": {
        "test": "jest"
    }
    ```

* Test Coverage: berfungsi untuk melihat komponen mana saja yang sudah memiliki test dan komponen yang belum memiliki test. Untuk menjalankan test ini kita hanya perlu mengetikan perintah npm test — -coverage pada terminal, dan akan muncul daftar komponen mana saja yang sudah dan belum memiliki test. Berikut contoh hasil dari perintah npm test — -coverage.

* Fungsi Mock Dengan Menggunakan Jest

    Seperti artinya kita akan membuat tiruan/mock dari suatu fungsi dan membuat balikannya secara manual, sehingga tidak peduli apakah fungsi tersebut bekerja, fungsi akan mengembalikan nilai sesuai yang kita definisikan. Kita akan mencoba membuat mock dari fungsi fungsiTambah yang kita buat sebelumnya.

* Snapshot testing : fitur pada Jest yang memungkinkan kita membandingkan hasil render dari suatu komponen. Hasil render ini akan dibaca dalam bentuk JSON kedalam suatu file tersendiri yang secara otomatis akan terbentuk saat kita menjalankan snapshot testing.
