# **Writing and Presentation Test Week 7**
## **React JS Lanjutan**
#### **Prop Types**
- Prop Types merupakan sebuah lib yang dapat membantu kamu untuk memeriksa data props yang kamu kirim agar sesuai dengan ekspektasi, jika tidak sesua maka akan muncul error.
- Instalasi PropTypes
  `npm install prop-types`
- contoh penggunaan proptypes
  ```js
    import PropTypes from ' prop - type ' ;  function Header ( props ) { 
      return ( 
        <>
            <h2>Name: {props.char} </h2>
            <h2>Age: {props.age} </h2>
        </> 
      )
    }
    Header.propTypes = { 
      char: PropTypes.string , 
      umur: PropTypes.number
    }
  ```
#### **React Router**
- React Router merupakan standar library untuk routing pada React. standar routing berfungsi untuk membuat suatu website menjadi dynamic. Pada React, Router membantu untuk mengarahka page satu ke page yg lainnya berdasarkan path url yg ditentukan.
- Cara menginstall React Router :
  1. npm (`$ npm install react-router-dom@6`)
  2. Yarn (`$ yarn add react-router-dom@6`)
  3. pnpm (`$ pnpm add react-router-dom@6`)
- Browser Router merupakan interface pada umumnya yg digunakan untuk menjalankan react di browser atau untuk membuat router-router sederhana.
#### **Pemanggilan React-router**
```js
    import * as React from "react";
    import * as ReactDOM from "react-dom";
    import { BrowserRouter } from "react-router-dom";

    ReactDOM.render(
    <BrowserRouter>
      {/* The rest of your app goes here */}
    </BrowserRouter>,
    root
    );


      import { Link } from "react-router-dom";

      function Home() {
      return (
        <div>
          <h1>Home</h1>
          <nav>
            <Link to="/">Home</Link> |{" "}
            <Link to="about">About</Link>
          </nav>
        </div>
        );
        }
```
_Note :_

- > `<Link>` merupakan double tag yang bertujuan untuk mengarahkan suatu menu ke menu lain sifatnya seperti seperti tag `<a></a>`

- > _to_ merupakan atribut untuk mengarahkan ke suatu path / nilai untuk ke suatu page

- > _`"/"`_ artinya adalah mengarahkan ke page utama 

#### **React Redux**
- Redux digunakan untuk mengolah state management Yaitu dengan menyimpan state di satu tempat, sehingga lebih mudah untuk di manage.
- cara kerja Redux :
  - Action : Adalah sebuah function yang mereturn sebuah objek.
  - Reducer : sebuah fungsi yang tugasnya untuk mengolah state yang ada di store.
  - Store : tempat untuk menampung state
- Cara kerjanya
  - Action merupakan suatu event, di mana ia adalah satu-satunya cara Anda dapat mengirim data dari aplikasi Anda ke Redux Store. Data tersebut pun dapat berasal dari interaksi pengguna, panggilan API (API request), atau bisa juga pengiriman formulir. Action ini pun dikirim menggunakan metode ‘store.dispatch ()’.Action merupakan objek JavaScript biasa dan harus memiliki tipe properti (property type).
    ```javascript
    export const INCREMENT = "INCREMENT"
    export const DECREMENT = "DECREMENT"
    
    export function increment (){
        return{
    
            type: INCREMENT
        }
    }
    
    export function decrement(){
    
        return{
            type: DECREMENT
        }
    }
    ```
  - Reducer adalah fungsi murni yang mengambil status aplikasi saat ini. Reducer juga berfungsi untuk melakukan tindakan,dan mengembalikan status baru (new state). Status ini disimpan sebagai objek, dan menentukan bagaimana status aplikasi berubah sebagai respons terhadap tindakan yang dikirim.
    ```javascript
    import { INCREMENT,DECREMENT } from "../action/KeranjangAction"
    
    const inisitialState ={
        count:0,
    }
    
    const ReducerKeranjang = (state = inisitialState, action)=>{
        switch (action.type) {
            case INCREMENT:
                return{
                    count: state.count+1
                }
                case DECREMENT:
                    return{
                        count: state.count-1
                    }
            default: return state
        }
    }
    
    export default ReducerKeranjang;
    ```
  - Store berfungsi untuk menyimpan status aplikasi. Sangat disarankan untuk hanya menyimpan satu store di aplikasi Redux apa pun. Anda dapat mengakses status yang disimpan, mengupdate status, dan mendaftarkan atau membatalkan pendaftaran listener melalui metode helper.
    ```javascript
    import {combineReducers, createStore} from "redux"
    import ReducerKeranjang from "../reducer/ReducerKeranjang";
    import todoReducer from "../reducer/TodoReducer";
    
    
    const allReducer = combineReducers({
    
        counter: ReducerKeranjang,
        todo: todoReducer
    })
    const store = createStore(allReducer)
    
    export default store;
    ```
#### **Async Actions with Middleware and Thunk**
- Redux Thunk adalah middleware yang memungkinkan memanggil pembuat aksi yang mengembalikan fungsi sebagai ganti objek aksi. Fungsi itu menerima metode pengiriman penyimpanan, yang kemudian digunakan untuk mengirim aksi sinkron di dalam isi fungsi setelah operasi asinkron selesai.
- Cara Penggunaan :
  - Instal (`npm install redux-thunk`)
  - Update Redux store agar dapat menggunakan middleware (`import thunk from 'redux-thunk'`)
  - import applyMiddleware (`import { createStore, applyMiddleware } from 'redux';`)
- memulai menggunakan redux-thunk
```js
store.dispatch(dispatch => {
  dispatch({ type: "FETCH_LOADING"});

  fetch("link json")
  .then (res => res.json())
  .then (data => dispatch({ type : "FETCH_SUCCESS", payload:data }))
  .catch (error => dispatch({ type : "FETCH_ERROR",payload:error }));

})
```

- membuat reducer
```js
function reducer(state = {loading:false, data:null, error:null}, action){
switch(action.type){
  case 'FETCH_SUCCESS':
    return {loading:false, data:action.payload};
  case 'FETCH_ERROR':
    return {loading:false, erorr:action.payload};
  case 'FETCH_LOADING':
    return {loading:true};
default: return state;
}
}
```
