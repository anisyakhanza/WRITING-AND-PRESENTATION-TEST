# WRITING (WEEK-6)
## DAY 1 REACT JS LANJUTAN - PROPTYPES
* Prop Types merupakan lib yang dapat membantu untuk memeriksa data props yang dikirim, dengan kata lain nantinya kita akan mengecek type dari sebuah prop agar sesuai dengan ekspetasi. Jika tidak sesuai maka akan muncul pesan error. 
* Install Proptypes:
    ```
    npm install prop-types
    ```
* Props yang akan dikirim harus sesuai dengan tipe data yang diinginkan
* Nanti akan muncul pesan error pada console log jika tidak sesuai ekspetasi
---
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
* Beberapa hal yang membantu untuk memasang routingan-nya
    ```
    import { Routes, Route, Link } from "react-router-dom";
    ```
    * Routes berguna untuk menampung atau membungkus dari anak-anak routing an yang akan dibuat. Caranya import di app
* Jika memberi tag Link,harus disertai atau pengganti href dengan `to`
    ```
    <Link to={"/"}>Home</Link>
    ```
* 
---
## DAY 3 STATE MANAGEMENT REACT REDUX
* Redux adalah wadah keadaan yang dapat diprediksi untuk aplikasi JavaScript, dan alat untuk mengatur keadaan aplikasi. Ini merupakan library yang popular untuk manage state di react apps
* Props drilling: props nya di oper-oper (dari parent ke child kemudian di oper lagi). Problemnya harus mengubah nama dari awal
* Solusi dari props drilling adalah State management, contoh : redux, context, jotai, zustand 
* cara menginstall redux core, ada 2 packages yang harus diinstall yaitu redux dan react redux 
    ```
    npm install redux react-redux
    ```
* Langkah berikutnya harus menyediakan store
    * Membuat file redux di src
    * Di dalam file redux membuat file store
    * Di dalam store membuat sebuah file index.js 
        ```
        import { createStore } from "redux"

        const store = createStore(() => {})

        export default store;
        ```
* Membuat reducer, reducer ada didalam store. Reducer diibaratkan sebagai rak barang. Reducer berupa sebuah function
    * Membuat file di dalam redux bernama reducer
    * Di dalam reducer membuat file misal keranjangReducer
    * Membuat function
        ```
        //membuat initial state atau nilai awal
        const initialState = {
            totalKeranjang: 0
        }

        function keranjangReducer(state = initialState, action) {
            switch (action.type) {
                default: state //default akan mengembalikan state itu sendiri
                break;
            }
        }

        export default keranjangReducer;
        ```
* Tinggal kita panggil reducer nya ke dalam store
    ```
    import { createStore } from "redux"
    import keranjangReducer from "../reducer/keranjangReducer"

    const store = createStore(keranjangReducer)

    export default store;
    ```
* action adalah kegiatan yang dilakukan untuk merubah sebuah data
* langkah yang berikutnya membuat provider. provider dibuat menggunakan react redux
    * Pada main.jsx
        ```
        import { provider } from "react-redux"
        import store from "./redux/store"

        ReactDOM.createRoot(document.getElementById('root')).render(
            <Provider store={store}>
                <App />
            </Provider>
        )
        ```
* Tahap selanjutnya ambil data dari store dengan menggunakan useSelector
* Action : sebuah function yang mereturn sebuah objek, objek tersebut memiliki sebuah property wajib yaitu type. Type inilah yang menentukan bagaimana statenya akan diubah
* Reducer : sebuah fungsi yang tugasnya untuk mengolah state yang ada di store. Misal menambah data, menghapus data, mengambil data, dsb. Reducer harus bersifat pure, yang berarti tidak boleh ada sebuah logic yang digunakan di dalamnya. Ada 2 parameter wajib dari reducer, yaitu state dan action.
* Store: tempat untuk menampung state. Store memiliki beberapa fungsi:
    * Izinkan akses ke status melalui getState().
    * Izinkan status diperbarui melalui dispatch(action).
    * Daftar listeners menggunakan subscribe(listener).
    * Memegang seluruh status aplikasi.

    ```
    import { createStore } from 'redux';
    import todoReducer from './reducers';

    const store = createStore(todoReducer);
    ```
* Combining Reducers: Redux memberi kita fungsi yang disebut combineReducers yang melakukan dua tugas:
    * Menghasilkan fungsi yang memanggil reducer dengan state yang dipilih sesuai dengan key/kuncinya.
    * Menggabungkan hasil menjadi satu objek sekali lagi.
---
## DAY 4 ASYNC ACTIONS WITH MIDDLEWARE AND THUNK
* Middleware : sebuah alat yang digunakan untuk merubah hasil dari request sebelum masuk menjadi response. Middleware Redux dapat melakukan apa saja saat melihat tindakan yang dikirim: mencatat sesuatu, memodifikasi tindakan, menunda tindakan, melakukan panggilan asinkron, dan banyak lagi. Middleware juga memiliki akses ke dispatch dan getState. Itu berarti kita dapat menulis beberapa logika asinkron di middleware, dan masih memiliki kemampuan untuk berinteraksi dengan toko Redux dengan mengirimkan actions.
    ```
    import { client } from '../api/client'

    const delayedActionMiddleware = storeAPI => next => action => {
    if (action.type === 'todos/todoAdded') {
            setTimeout(() => {
    // Delay this action by one second
    next(action)
    }, 1000)
    return
    }

    return next(action)
    }

    const fetchTodosMiddleware = storeAPI => next => action => {
    if (action.type === 'todos/fetchTodos') {
    // Make an API call to fetch todos from the server
    client.get('todos').then(todos => {
    // Dispatch an action with the todos we received
    storeAPI.dispatch({ type: 'todos/todosLoaded', payload: todos })
    })
    }

    return next(action)
    }
    ```
* Thunk : konsep pemrograman yang menggunakan fungsi untuk menunda evaluasi/kalkulasi suatu operasi. Redux Thunk adalah middleware yang memungkinkan Anda memanggil pembuat aksi yang mengembalikan fungsi sebagai ganti objek aksi. Fungsi itu menerima metode pengiriman penyimpanan, yang kemudian digunakan untuk mengirim aksi sinkron di dalam isi fungsi setelah operasi asinkron selesai.
    ```
    npm install redux-thunk
    ```

* Contoh Penggunaan redux-thunk
    ```
        import { connect } from 'react-redux';
    import { addTodo } from '../actions';
    import NewTodo from '../components/NewTodo';

    const mapDispatchToProps = dispatch => {
     return {
            onAddTodo: todo => {
            dispatch(addTodo(todo));
         }
       };
    };

    export default connect(
    null,
    mapDispatchToProps
    )(NewTodo);
    ```

    Aksi ini akan menggunakan Axios untuk mengirim permintaan POST. Selain menerima metode pengiriman dari status, fungsi yang dikembalikan oleh aksi asinkron bersama Redux Thunk juga menerima metode getState dari penyimpanan.

    ```
                export const addTodo = ({ title, userId }) => {
             return (dispatch, getState) => {
                    dispatch(addTodoStarted());

                    console.log('current state:', getState());

                    };
            };
            ```
