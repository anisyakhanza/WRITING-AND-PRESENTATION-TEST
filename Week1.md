# WRITING & PRESENTATION TEST (WEEK-1)
## DAY-1 UNIX COMMAND LINE
* Shell : Progam yang digunakan untuk berkomunikasi atau memerintah sistem operasi.
* Command Line Interface : Jenis shell yang berbasis teks.  Contoh : sh, bash (shell yang ada di linux), zsh, smd.exe
* Grapic User Interface (GUI) : Jenis shell berbasis grafik atau tampilan. Contoh : google drive, Microsoft Windows, macOS, dan Ubuntu.
* Terminal Emulator : Aplikasi untuk mengakses CLI.
* Cara mengakses CLI menggunakan bash:
    * Mendownload aplikasi git
    * Lalu menginstalnya
    * Kemudian klik start, search git bash lalu klik dua kali.
* Filesystem adalah bentuk struktur dari direktori atau file-file dari komputer kita.  Filesystem berfungsi untuk mengatur bagaimana data disimpan di dalam sebuah system. 
* Sistem operasi Windows & Unix-like menyusun file dan direktori menggunakan struktur yang bentuknya mirip tree

### Command untuk navigasi
* pwd (print working directory) : command untuk melihat current working directory
* ls (lists) : 
Command untuk melihat isi file yang ada di sebuah direktori
* cd (change directory) : Command untuk pindah ke direktori lain

### Membuat files & direktori
* touch : Command untuk membuat sebuah file
* mkdir : Command untuk membuat sebuah direktori

### Melihat isi files
* head : Command untuk melihat beberapa line awal dari sebuah file text
* tail : Command untuk melihat beberapa line akhir dari sebuah file text
* cat : Command untuk melihat isi sebuah file

### Menyalin
* cp : Command untuk mengcopy files atau directory
### Memindahkan 
* mv (move) :
Command untuk memindahkan files atau directory. Bisa digunakan untuk rename
### Menghapus 
* rm (remove) : 
Command untuk menghapus file atau directory
---
## GIT DAN GITHUB DASAR
* Version control : sebuah sistem yang merekam perubahan terhadap sebuah file dalam waktu tertentu. Berfungsi mencatat setiap perubahan pada File (termasuk code yang kita buat) pada suatu proyek baik dikerjakan secara individu maupun tim.
* Git :  Tools untuk programmer. Git adalah aplikasi yang dapat melacak setiap perubahan yang terjadi pada suatu folder atau file.
* GitHub : website yang digunakan untuk menyimpan dan mengelola kode suatu project
* Konfigurasi Git
```
// Mengatur username
git config --global user.name "anisyakhanza"
// Mengatur email
git config --global user.email "anisyakhanza22@gmail.com"
```
* Cek apakah instalasi berhasil
```
git --version
```
* Cek apakah setup berhasil
```
git config --list
```
* Tahapan bekerja dengan Git 
  * Working directory : membuat file, memodifikasi file, menghapus file
  * Staging : file yang siap disimpan
  * Commit : perubahan file disimpan sebagai commit
* Repositori git : direktori proyek yang kita buat
```
// Membuat direktori dengan perintah 'git init nama-dir'
git init proyek-01
```
```
// Membuat repositori pada direktori saat ini (working directory)
git init .
```
* Terdapat 3 kondisi file dalam git
    * Modified adalah kondisi dimana revisi atau perubahan sudah dilakukan, tetapi belum ditandai (untracked) dan belum disimpan dalam version control.
    * Staged adalah kondisi dimana revisi sudah ditandai (modified) namun belum disimpan di version control.
    * Commit/committed adalah kondisi dimana revisi sudah disimpan pada version control.

* Check repositori status
```
git status
```
* Menambahkan files ke "staging"
```
git add
```
* Menyimpan files di “staging” sebagai commit
```
git commit
```
* Melihat histori perubahan
```
git log
```

* Melihat detail perubahan
```
git diff
```
* Untuk kembali ke commit tertentu
```
git checkout
```
* Untuk reset files ke sebuah commit, perubahan di branch yang dihapus menjadi ‘untracked files’
```
git reset
```
* Untuk undo commit, perubahan disimpan dalam commit
```
git revert
```
* Files yang perubahannya diabaikan didaftarkan pada .gitignore

* Melihat branch yang ada. Branch aktif ditandai dengan `*`
```
git branch
```
* Melihat branch baru
```
git branch nama_branch
```
* Menggabungkan perubahan atau histori dari branch_target ke branch saat ini
```
git merge branch_target
```

* Remote repository, tempat untuk menyimpan git repo di internet
* Melihat daftar remote di repository
```
git remote
```
* Menambahkan remote
```
git remote add
```
* Mengirim perubahan ke remote repository
```
git push
```
* Mengambil metadata dari remote
```
git fetch
```
* Mengambil perubahan dari remote ke local
```
git pull
```
* Proses review merge yang dibuat
```
Pull Request
```

* Menyalin remote repository ke komputer kita
```
git clone
```
* Github fork untuk membuat copy dari repository orang lain ke akun kita
---
## DAY-2 HTML
* HTML adalah singkatan dari Hypertext Markup Language. HTML digunakan untuk menampilkan konten pada browser.
* HTML bersifat statis
* HTML bukanlah sebuah bahasa pemrograman, artinya HTML tidak bisa dinamis mengolah data.
* Tools utama yang digunakan untuk membuat HTML
    * Browser
    * Code editor
* Visual Studio Code adalah code editor yang dikembangkan oleh tim engineer Microsoft.
* Struktur HTML
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <h1>Hellow World!</h1>
</body>
</html>
```
* HTML tersusun sebagai kesatuan dari sebuah tingkatan (family tree relationship)
* Saat sebuah element berada di dalam element lain, maka disebut child element
* Element yang berada diatas element lain disebut parent element


HTML Anatomy
```
<p>Hello World!</p>
```
* Opening tag : `<p>`
* Content :  `Hello World!`
* Closing tag : `</p>`
* Element : mencakup opening tag, content, dan closing tag

HTML Attributes
```
<body>
    <div>
    // element heading dengan attribut id 
    <h1 id="header">Content</h1>

    // element image dengan attribut src
    <img src="image.png">

    // element link dengan attribut href
    <a href="https://google.com">Menuju google.com</a>
    </div>
</body>
```
* Attribute adalah properties dari sebuah HTML Element.
* Semua HTML Element memiliki attribute.

* Fungsi HTML Comment `<!-- blablabla -->`
    * Memberikan penjelasan maksud dari line code
    * Menonaktifkan code
    * comment hanya dibaca oleh sesama progammer
* Tidak semua HTML Element memiliki content. Element ini disebut empty element. Empty element tidak memiliki closing tag. misal : `<br>`
* Tag IMG
```
<img src="images/my_profile.jpg" alt="Profile"> 
```

*  tag img untuk menampilkan gambar
* src atau source adalah  attribute untuk memberitahukan sumber gambar
* alt adalah alternative
* Tag Video
```
<video controls>
    <source src="movie.mp4" type="video/mp4">
</video>
```
* Video merupakan double closing tag sehingga kita menaruh konten di antara opening dan closing
* controls berguna untuk kita bisa mengatur videonya di play / pause dan indikator menit
* Tag untuk tabel
```
<table>
  <tr>
    <th>Nama</th>
    <th>Nomor Telpon</th>
    <th>Negara</th>
  </tr>
  <tr>
    <td>Nisa</td>
    <td>0811111111</td>
    <td>Indonesia</td>
  </tr>
  <tr>
    <td>Khanza</td>
    <td>0822222222</td>
    <td>Indonesia</td>
  </tr>
</table>
```
* `<table>` sebagai element utama.
* `<tr>` atau dikenal sebagai table row tag, digunakan untuk membuat baris baru di dalam `<table>`.
* `<td>` atau dikenal sebagai table data tag, digunakan sebagai container (wadah) dari data yang kita mau isi di dalam `<tr>`.
* Terkadang tag `<th> `sebagai pengganti `<td>` untuk membuat header cell (biasanya digunakan untuk menampilkan judul kolom). `<th>` membuat tulisan di dalamnya menjadi tebal.
* Semantic artinya kita menggunakan element html yang sesuai dengan kebutuhan konten.
* Kegunaan semantic html:
    *  Membantu developer supaya lebih “Easy to read and understand”
    * Meningkatkan Accessibility 
    * Meningkatkan SEO 
    * Lebih mudah di maintain 
* Contoh dari semantic element:
    * `<section>` menandakan bagian dalam sebuah halaman web.
    * `<header>` merupakan bagian tajuk dari sebuah halaman web.
    * `<footer>` merupakan bagian halaman web yang terletak di bagian bawah konten utama.
    * `<article>` menandakan sebuah blok teks yang isinya independen terhadap element lain dalam halaman web.
    * `<nav>` adalah bagian yang berisi tautan navigasi utama. Kalian mungkin sering melihat menu navigasi yang berisi tautan ke halaman "Beranda", "Kontak kami", "Galeri", dan lain-lain.
    * `<aside>` adalah bagian di samping konten utama. Kontennya sebaiknya berhubungan dengan element di sebelahnya.

* Deploy adalah sebuah proses untuk menyebarkan aplikasi yang sudah kita kerjakan supaya bisa digunakan oleh orang-orang
* Jika aplikasi kita HTML atau Web App kita perlu mendeploy ke server.
* Cara mendeploy HTML:
    * Masuk ke netlify.com lalu register seperti biasa menggunakan email atau github
    * Setelah itu masuk ke tab Sites lalu drag and drop seluruh folder html
---
## DAY-3 CSS
* Cascading Style Sheets atau CSS adalah bahasa komputer yang digunakan untuk menambahkan design ke suatu halaman website di internet.
* CSS comment dapat diberika di external css dan internal css /* */
* 3 cara untuk menyisipkan CSS ke dalam HTML:
    * Inline CSS : menggunakan attribute style untuk menyisipkan kode CSS langsung di dalam HTML element.
    * Internal CSS :  menggunakan element `<style>` untuk menyisipkan kode CSS. Element `<style>` tersebut diletakkan di dalam element .
    * External CSS : sebuah file CSS terpisah yang disambungkan dengan file HTML dengan menggunakan element `<link>`
* Syntax CSS : CSS Syntax adalah syntax yang digunakan untuk menunjuk atau memilih HTML element mana yang ingin diberi style (dihias). CSS syntax terdiri dari selector, property, dan value.
```
selector {
    property : value;
}
```
* Selector adalah vas bunga, yaitu benda (HTML element, misal paragraf) mana yang akan dihias.
* Property adalah bagian mana dari vas bunga (dalam HTML misal, setiap huruf dari paragraf) yang akan dihias, dalam kasus ini berarti warna dari vas tersebut.
* Value adalah warna merah, yaitu nilai atau hiasan 'berupa apa' yang akan diberikan ke vas bunga.
* Property dalam CSS contohnya background-color, color, font-size, margin, direction, letter-spacing, line-height, Text-align dll
*  pseudo-class digunakan untuk mendefinisikan keadaan khusus pada suatu element. misal:
    * Memberikan style pada link pada saat di-hover (memberikan style pada element ketika kursor kalian melewati suatu element)
    * Memberikan style pada link setelah di-klik (dikunjungi)
    * Memberikan style pada checkbox setelah dicentang
    ```
    selector:pseudo-class {
    property: nilai;
    }
    ```
* pseudo-element CSS digunakan untuk memberikan style pada bagian tertentu dari suatu element. misal:
    * Memberikan style pada huruf pertama pada suatu kalimat
    * Memberikan style pada baris pertama dari dari suatu paragraf
    * Menyisipkan konten sebelum atau sesudah suatu element
    ```
    selector::pseudo-element {
    property: nilai;
    }
    ```
* Box model bisa  dianggap sebagai kotak yang membungkus setiap HTML element
* Box model terdiri dari:
    * margin yaitu area terluar yang kosong setelah border. Margin bersifat transparan.
    * border yaitu garis tepi yang membungkus padding dan konten.
    * padding yaitu area kosong di antara konten dan border. Padding bersifat transparan.
    * content yaitu konten (value/nilai) dari HTML element. Bisa berupa teks, gambar, video, ataupun suara.
* CSS - Tag Name
    
    Jika menggunakan Tag element HTML maka akan bersifat global yg artinya akan mengubah seluruh html
    ```
    h1 {
      color: red; 
    }
    ```
* CSS - Class Name

    HTML yang memiliki class yang sama, akan mempunyai styling yang sama saat digunakan pada CSS
    ```
    .text-color-red{
	        color: blue; 
    }
    ```
* CSS - Multiple Class

    Disini dapat menggunakan lebih dari 1 class yang berbeda untuk 1 element HTML
    ```
    .title {
        color : brown;
    }
    .uppercase {
        text-transform : uppercase;
    }
    .lowercase {
        text-transform : lowercase;
    }
    ```
* CSS - ID Name 
    
    ID Name bersifat unik artinya hanya ada 1 nama ID pada 1 element HTML, contoh navigation dan footer. Gunakan (#namaID) saat memanggil element ID HTML pada CSS

* Nested Element yaitu setiap element terdiri dari parent dan child, sama seperti html
* !important CSS yaitu styling CSS yang memiliki level paling atas dari ID dan Class. Dengan kata lain ika pada styling CSS kita menggunakan !important, maka styling sebelumnya baik itu ID Name atau Class Name akan di override.
* Flexbox berguna memudahkan para programmer untuk mengatur layout, posisi, dan ukuran dari tiap element di dalamnya
* Dua istilah penting pada saat belajar flexbox: 
    * container adalah element yang membungkus dan mengatur tampilan dari element di dalamnya,
    * item adalah element dalam container yang diatur tampilannya.
* Ordering & Orientation
    * flex-direction

        properti flex-direction digunakan untuk mengatur letak item child. 
    * flex-wrap

        flex secara default akan membuat tata letak item children dalam 1 line saja. flex akan menyesuaikan space yang ada. 
    * flex-flow

        properti flex-flow digunakan sebagai shortcut untuk set up flex-direction dan flex-wrap bersamaan.
    * order

        properti order pada flex adalah berfungsi untuk ordering item mana yang ingin kita atur posisinya berdasarkan urutan order.
* Alignment
    * justify-content : digunakan untuk mengatur tata letak dan space antar item child secara horizontal atau main axis.
    * align-items :  digunakan untuk mengatur align dari item child secara vertikal atau cross axis.
    * align-self : digunakan untuk mengatur align item pada masing-masing item.
    * align-content : digunakan untuk mengatur tata letak dan space antar item child secara vertikal atau cross axis

* Flexibility
    * flex-grow : properti flex-grow dapat mengatur size suatu item child pada flexbox. value dari properti flex-grow adalah number dan tidak boleh negatif.
    * flex-shrink : properti yang membuat size suatu item child mengecil secara relatif terhadap item child yang lainnya.
    * flex-basis :  mengatur width dari setiap item child. jika kita telah menggunakan width, maka flex-basis akan melakukan override properti width.
---
## DAY-4 ALGORITMA 
* Algoritma adalah deskripsi berupa step-step yang dibutuhkan untuk menyelesaikan suatu masalah
* Data struktur digunakan untuk menyatakan
cara tertentu mengatur data untuk jenis operasi tertentu
* Perbedaan data struktur dan algoritma adalah Data struktur digunakan untuk mengelola/manajemen sebuah data. Sedangkan Algoritma yang akan menyelesaikan suatu permasalahan menggunakan data tersebut.  
* Ciri-ciri algoritma:
    * Input : Memiliki 0 atau lebih inputan
    * Output : Memiliki min 1 buah output
    * Definiteness (pasti) : Instruksi jelas tidak ambigu
    * Finiteness (ada batas) : Memiliki titik berhenti (stop)
    * Effectiveness (tepat dan efisien) : Sebisa mungkin tepat sasaran dan efisien
* Jenis proses algoritma 
    * Sequence :  Instruksi yg dijalankan secara berurutan
    * Selection : Instruksi yg dijalankan jika memenuhi suatu kondisi
    * Iteration : Instruksi yg berulang kali dijalankan selama memenuhi suatu kondisi
    * Concurrent : Instruksi yg dijalankan secara bersamaan
* Manfaat algoritma:
    * Membantu memecahkan suatu permasalahan dengan logika, terstruktur dan sistematis
    * Membantu menyederhanakan atau mempersingkat proses suatu program yang rumit dan besar
    * Meminimalisir sehingga mengurangi penulisan program secara berulang-ulang
* Manfaat data struktur:
    * Memudahkan dalam menggunakan konsep algoritma pemrograman
    * Memudahkan dalam pengaturan data
    * Memudahkan dalam menyusun bahasa pemrograman
* Penyajian algoritma:
    * Deskriptif : Penulisan algoritma dengan cara deskriptif seperti kita menulis tutorial (tata cara) dengan bahasa sehari-hari
    * Flow Chart : penyajian algoritmanya lebih mudah dibaca karena memiliki tampilan visual.
    * Pseudo Code : Penulisan algoritma yg hampir menyerupai penulisan pada kode pemrograman. 
    
        Pseudocode memiliki 3 bagian:
        * Judul : Penjelasan dari algoritma yg dibuat
        * Deklarasi : Mendefinisikan/menyiapkan semua nama (variabel) yg akan digunakan
        * Deskripsi : langkah-langkah penyelesaian masalah

        Pseudocode harus ditulis jelas, simple, konsisten dan mudah dibaca orang lain.

        Jenis pseudocode:
        * Procedural : cara berpikir runtun (serangkaian perintah yang berurutan)
        * Conditional: jika dibutuhkan suatu percabangan masalah (if else)
        * Looping : sebuah perintah yg diulang-ulang
        * Recursive : sebuah perintah yang memanggil method/function didalam sebuah function

        contoh pseudocode
        ```
        program hitung_luas_segitiga

        deklarasi
        var luas,alas,tinggi:integer;

        algoritma:
        alas <-- 5;
        tinggi <-- 10;

        luas <-- (alas * tinggi)/2

        display(luas)
        ```
contoh algoritma dengan javascript:
```
let a = 5;
let b = 10;
let c = 0;

c = a + b;
console.log(c);
```

## JAVASCRIPT - INTRODUCTION
* Javascript adalah bahasa pemograman yang sangat powerful yang digunakan untuk logic pada sebuah website. Javascript membuat website menjadi interaktif dan dinamis
* Javascript dijalankan melalui browser pada device setiap user. Contoh: browser Chrome dan Mozilla yang sudah support untuk semua fitur Javascript.
* syntax digunakan untuk membuat statement program, instruksi untuk djalankan/dieksekusi oleh web browser, compiler, ataupun intrepreter
    * contoh syntax Javascript:
        * Alert()
        * Prompt()
        * Confirm()
* Console log adalah tempat kita untuk cek logic pemograman web yang kita kembangkan. Console log juga tempat kita untuk melakukan debugging (mengetahui error pada code) pada pemograman web
* Comments 

    Comments adalah sintaks yang digunakan untuk memberi keterangan tentang suatu statement. Menggunakan bahasa inggris atau bahasa indonesia.
    * Single Comments
        ```
        console.log(5); Prints 5
        ```
    * Multiline Comments
        ```
        /* 
        This is all commented
        console.log(10);
        None of this is going to run!
        console.log(99);
        */
        ```
* Tipe Data

   Tipe data adalah klasifikasi yang kita berikan untuk berbagai macam data yang digunakan dalam programming.
 
    6 tipe data fundamental pada Javascript:
    * number : tipe data yang mengandung semua angka termasuk angka desimal
        ```
        let number1 = 12;
        let number2 = 24;
        let number3 = 1000;
        let number4 = 24.12;
        ```
    * string :  grup karakter yang ada pada keyboard laptop/PC kita yaitu letters (huruf), number (angka), spaces (spasi), symbol, dan lainnya. 
    Tipe data string memiliki ciri khas yaitu nilai data dibungkus dengan tanda ' atau "
        ```
        let nama = "Stefanus";
        ```
    * boolean : nilai benar dari sebuah pernyataan yang dituliskan sebagai true atau false
        ```
        let benar = true;
        let salah = false;
        ```
    * null : sebuah nilai yang berarti kosong atau menunjuk pada nilai yang tidak ada
        ```
        let dataPertama = null;
        ```
    * undefined : menandakan kondisi variabel yang belum diberi sebuah nilai. 
        ```
        let a = "informatika";
        let b = "manajemen";
        let peserta = ["anisya", "mila", "riska"];

        console.log(c); // undefined
        console.log(a); // "informatika"
        console.log(peserta.length); // 3
        console.log(peserta.panjangkarakter); // undefined
        ```
    * object : sebuah kumpulan pasangan properti dan nilai
        ```
        let orang = {
        nama: 'sarah',
        umur: 24,
        pekerjaan: 'programmer'
        };
* Variabel : variable adalah container/tempat untuk menyimpan sebuah nilai

    3 cara mendefinisikan variabel:
    * var : variabel yang dinamis/dapat diubah
    * let : variabel yang dinamis/dapat diubah
    * const : biasanya digunakan ketika variabel tidak dapat diubah nilainya

* Operator
    * Assignment Operator (=)
    * Mathematical Assignment Operator : operator yang digunakan untuk memberikan tugas kepada variabel. Biasanya digunakan untuk mengisi variabel. contoh: `=` , `+=` , `-=` , `*=` , `**=` , `/=` , `%=`
    * Increment dan Decrement : untuk menambah atau mengurangi sebesar 1 nilai. contoh: `++` , `--`
    * Arithmetic Operator, contoh: `+` , `-` , `*` , `/` , `%`
    * Comparison Operator : operator yang membandingkan satu nilai dengan nilai lainnya. contoh: `<` ,`>` , `<=` , `=>`, `===` , `!==`

    * Logical Operator : digunakan untuk semua conditional. menghasilkan nilai boolean. contoh: `&&` , `||` , `!`
---
## DAY-5 JAVASCRIPT DASAR
### JavaScript Dasar - Conditional
* Conditional merupakan statement percabangan yang menggambarkan suatu kondisi
* Conditional statement akan mengecek kondisi spesifik dan menjalankan perintah berdasarkan kondisi tersebut
* Contoh Conditional: 
    * if statement
    ````
    let lapar = true;
    if (lapar) {
        console.log("Yuk makan");
    };
    ````
    * if ... else statement
    ```
    let lapar = true;
    if (lapar) {
        console.log("Yuk makan");
    } else {
        console.log("Tidak makan");
    };
    ````
    * if ... else if statement
    ```
    let stopLight = "yellow";

    if (stopLight === "red") {
        console.log("Stop!");
    } else if (stopLight === "yellow") {
        console.log("Slow down!");
    } else if (stopLight === "green") {
        console.log("Go");
    } else {
        console.log("Caution, unknown!");
    }
    ```
* Truthy and falsy digunakan untuk mengecek apakah variabel telah terisi namun tidak mementingkan nilainya.
* Switch Case Conditional

    Switch case ini digunakan jika kondisi dan percabangan terlalu banyak
    ```
    var warna = "merah";
 
		switch (warna){
			case "hitam":
				teks = "warna hitam";
				break;
			case "merah":
				teks = "Warna merah";
				break;
			case "hijau":
				teks = "Warna hijau";
				break;
			default:
			    teks = "Warna tidak terdeteksi";
		}		
     ```
* Tenary operator

    Ternary operator merupakan short-syntax dari statement if … else.

### JavaScript - Looping
* Looping adalah statement yang mengulang sebuah instruksi hingga kondisi terpenuhi atau jika kondisi stop/berhenti tercapai.
* Manual Looping
    ```
    //akan menampilkan nilai 1-5
    console.log(1);
    console.log(2);
    console.log(3);
    console.log(4);
    console.log(5);
    ```
* For Loop

    For Loop merupakan instruksi pengulangan yang dapat kita berikan pada program yang kita kembangkan
    ```
    let angka = 1;
    for (angka; angka <= 5; angka++) {
        console.log(angka);
    }
    ```
* While Loop

    While Loop digunakan jika kita tidak mengetahui jumlah pasti pengulangan.
    ```
    let angka = 1;
    while (angka <= 5) {
        console.log(angka);
        angka++
    }
    ```

* Do While
    ```
    var bensin = 9;

    do{
        console.log("Nyalakan mesin!");
        bensin--;
    } while(bensin > 0)
    ```

* Nested Loop
    ```
    for (let i = 1; 1<= 10; i++) {
        for (let j = 1; j <= 1; j++) {
            document.write("<br />")
            document.write("baris", +i);
            document.write("<br />")
            document.write("kolom", +j);
        }
    }