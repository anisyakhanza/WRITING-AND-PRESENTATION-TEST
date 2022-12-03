# WRITING TEST (WEEK-5)
## DAY-1 REACT JS - INTRO
* NodeJS didalamnya ada V8 sehingga JS bisa berjalan di luar web browser 
* nodeJS untuk install react dan beberapa lib
* React JS : library javascript untuk membuat tampilan user interface pada website. React JS dibuat oleh dikembangkan oleh engineer facebook.
* alternative: 
    * angular
    * vue
    * svelte
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
* React Js 
    * declarative
    * component-based
    * learn once, write anywhere
* Component: salah satu core dari React JS. Component membagi UI dalam satuan-satuan kecil, yang berarti dalam 1 page ada beberapa componen yang bisa dibuat
---
## DAY 2 REACT JS - COMPONENT
* Component dibuat jika component tersebut bersifat reusable code
* Ada 2 cara pembuatan component yaitu dengan menggunakan funtion dan menggunakan class
* Penulisan nama folder, file, dan function component harus menggunakan huruf besar diawal dan kata selanjutnya 
* untuk react hanya bisa untuk 1 parent utama (pembungkus utama/tag). Bisa menggunakan tag `<div>` atau tag fragment `<>`
* Jika di html ada properti class, maka di react adanya className
* State : sebuah object untuk menyimpan data di react, baru nanti dirender ketika kita melakukan sebuah perubahan data.
* Props (properties) : untuk komunikasi dari component parent ke component child. Komunikasi adalah pengiriman data. 
* Datanya akan ditampung di state lalu kemudian akan dikirim melalui props
* Props biasanya dipasang di function, seperti paramater dari di function
* State adalah data lokal
* Props digunkan agar component memiliki data yang dinamis yang dikirim dari component lain
* useState: untuk menyimpan data (variable) yang berubah-ubah di react. Data yang berubah-ubah leboh baik disimpan di dalam useState. UseState berbentuk Array
* React sifatnya immutable yang berarti value atau state yang tidak bisa diubah
* Stateless: Tidak memiliki state dan hanya punya props (datanya dari props aja)
* Stateful: Mempunyai state dan bisa mengirim state tersebut ke component
* Kalau mau memasukkan code bootstrap lewat main.jsx (bukan di app.jsx)
---
## DAY 3 REACT JS - COMPONENT
* State : Data yang ditinggal di dalam component tersebut
* Props : Data yang dikasih. Props mirip dengan atribut
* Pada react tidak bisa menggunakan variable biasa (karena bersifat immutable) dan harus menggunakan useState 

    **Penulisan state**
    ```
    const [count, setCount] = useState(0) //benar

    let count = 0 //salah
    ```
    set : untuk mengubah

    get : untuk mendapatkan

* Menambahkan event sesuai kebutuhan, tidak harus ada state
* Memakai state kalau butuh data, datanya ada kemungkinan bisa berubah
* Kalau di **component** itu namanya **props**. sedangkan, di **function biasa** namanya **parameter**
* Kalau mau menambahkan argumen pada function yang ada didalam event, kita jadikan callback dulu kemudian diberi argumen
* Jika kita mau menampilkan list card, diminta untuk dipasangkan key (didalam key nilai yang bersifat unik/beda-beda). misal
    ```
    <Card key={index} nama={item.name} umur={item.umur} />
    ```
* Dapat dikatakan stateless jika tidak ada state
* Dikatakan stateful jika punya state
---
## DAY 4 REACT JS HOOKS
* Component mempunyai lifecycles (siklus hidup), dibagi menjadi 3
    * Mounting (menempel/muncul)
    * Update (memperbarui)
    * UnMount (mencopot/menghilang)
* Hooks untuk memudahkan penggunaan functonal components agar bisa menggunakan state, dan lifecycle lainnya.
* Sebelumnya, state(setState) dan lifecycle (componentDidMount, componentDidUpdate) hanya bisa digunakan di class component, namun dengan hooks bisa digunakan di functional component
* Hooks yang sering digunakan adalah useState dan useEffect. Keduanya sama dengan state, dan lifecycle di class yang biasa kita sering gunakan
* Kelebihan menggunakan hooks agar code terlihat lebih clean, pendek dan mudah dimengerti

* **Syntax useState**
    ```
    const [ selectedRoom, setselectedRoom] = useState (intial value)
    ```

    Penggunaan useState Hooks
    * Import useState dari react
        ```
        import { useState } from "react";
        ```
    * Menuliskan useState hooks
        ```
        const [nama, setNama] = useState("luthfi");
    * Pemanggilan data
        ```
        <p> Halo, saya {nama} </p> 
    * Update state
        ```
        <button onClick={ setNama("david")}> Ubah </button>

* **Array dalam useState Hooks**
    
    Disini kita dapat menggunakan array untuk menyimpan data dalam state. Kita tinggal memasukkan tanda `[]` dalam useState untuk menandakan bahwa state tersebuat adalah array
* UseState akan digunakan saat menyimpan data suatu form yang nantinya akan dipost ke api untuk diproses. Case lain, pada saat melakukkan call api, kita bisa menyimpan data hasil get dari api tersebut ke dalam state menggunakan **useState**
* **useEffect Hooks** : hooks yang bisa digunakan untuk menggunakan lifecycle pada functional component dengan mudah
    
    Penggunaan useEffect bisa dimasukkan **sebelum** melakukan render, useEffect sendiri biasanya ditempatkan di bawah useState. Nanti yang dituliskan ke dalam useEffect akan dijalankan setaip component baru di mount (componentDidMount), terjadi perubahan (componentDidUpdate), dan pada saat component akan ditinggalkan (componentWillUnmount).

    **Cara Penggunaan useEffect**
    * Import useEffect
        ```
        import { useEffect } from "react"
        ```
    * Tuliskan penggunaan useEffect hooks sebelum dirender
        ```
        useEffect(() => {
            console.log("Telah jadi perubahan")
        }, [nama])

* Re-render yang berlebihan atau infinite render bisa saja terjadi, kita bisa menambahkan `[]` atau `[variableYangBerubah]` untuk menentukan bahwa useEffect hanya akan berjalan saat terjadi update pada variablle yang di bagian akhir
* useEffect akan digunakan saat membuat suatu call api, karena api akan selalu dipanggil saat komponen terbentuk, maka call api bisa dilakukan di dalam useEffect
* Ada hooks lain yang jarang digunakan misalnya useContext dan useReducer
* Hooks, **harus selalu** dipanggil dibagian atas component, yaitu biasanya setelah pembuatan function component, begitu juga untuk useState dan useeffect
---
## DAY 5 REACT JS - COMPONENT
Dalam membuat form pada function 
* Membuat tag form
    ```
    <form action="">
    </form>
    ```
* Di label, yang dahulu dihtml nya `for` . di react menjadi `htmlFor`
    ```
    <label htmlFor="name">Name</label>
    ```
* Kalau membuat formulir, jangan lupa button nya diberi type submit
    ```
    <button type="submit">Submit</button>
    ```
