# WRITING & PRESENTATION TEST (WEEK-5)
## DAY-1 REACT JS - INTRO
* React JS : framework vies library javascript untuk membuat tampilan user interface pada website.
* Alasan menggunakan React JS:
    * Membuat aplikasi front-end menjadi lebil cepat walaupun harus menghandle banyak data
    * Dapat menerapkan konsep modular javascript pada React JS membagi 1 tampilan pada website menjadi komponen-komponen kecil
     * Dapat digunakan pada aplikasi berskala kecil hingga besar dan kompleks (scalable)
     * Banyak digunakan oleh perusahaan teknologi. dengan kata lain lebih mudah mendapatkan pekerjaan jika menguasai React JS
* Cara instalasi React JS:
    * Install Node JS
    * Use Libraty (create-react-app)
* 2 cara membuat user interface menggunakan Vanilla JS dan DOM
* Vanilla JS : menggunakan native javascript (default)
* JSX : syntax extension for javascript. JSX dikembangkan untuk digunakan pada React JS. Sebelum ditampilkan ke browser, JSX ini perlu dicompile untuk menjadi javascript dulu. Dengan JSX dapat menggunakan HTML didalam file extension javascript (.js)
* Setiap JSX hanya bisa menggunakan 1 parent element, jika tidak begitu akan error. maka solusinya menggunakan tag `<div>` atau tag fragment `<>`
* DOM Manipulation ada core dari javascript. Dengan DOM kita dapat mengupdate data di web page.
* React JS mempunyai fitur Virtual DOM. Virtual DOM adalah duplikasi dari real DOM yang sebenarnya. Misalnya kita mempunyai 2 komponen UI dalam 1 page. Kita dapat mengupdate data yang 1 komponen, maka React JS hanya melakukan render ulang pada komponen tersebut.
* Pada JSX attribut class di tag element html harus menggunakan className
* Dengan menggunakan curlt braces kita dapat menggunakan syntax javascript di dalam element html
* Menggunakan curly braces untuk mengakses variable pada JSX
* Menggunakan curly braces untuk data attribut
* Mendeklarasikan event dengan menggunakan curly braces

## REACT JS - COMPONENT
