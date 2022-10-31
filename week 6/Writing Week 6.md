# **Writing and Presentation Test Week 6**
## **React JS Dasar**
#### **Introduction JS**
- **React.js**
React.js adalah framework view library javascript yang dibuat oleh Facebook untuk membuat user interface. React.js memanfaatkan konsep komponen untuk membangun user interface.
- Kenapa menggunakan React Js? <br>
React Js is Fast.<br>
React Js membuat aplikasi front-end menjadi lebih cepat walaupun harus menghandle berbagai data.
React Js is Modular.<br>
Kita dapat menerapkan konsep Modular javascript pada React Js. React Js membagi 1 tampilan pada website menjadi komponen - komponen kecil.
React JS is Scalable.<br>
React JS dapat digunakan pada aplikasi berskala kecil hingga bear dan kompleks.
React is Popular.<br>
Komunitas React JS dieluruh dunia sangat besar. Kebanyakan peruahaan teknologi pun sudah menggunakan React JS.
- **Instalasi React.js**
  1. Install Node JS
  2. Use library create-react-app
      - npx (npx create-react-app my-app)
      - npm (npm init react-app my-app)
      - yarn (yarn create react-app my-app)
- **JSX**
  - JSX adalah sintaks yang digunakan untuk menuliskan kode React. JSX adalah gabungan dari HTML dan JavaScript. JSX memungkinkan kita untuk menuliskan kode React dengan lebih mudah dan cepat.
  - Contoh JSX
    ```js
    import React from "react";

    const App = () => {
      return (
       <div>
         <h1>Hello World</h1>
       </div>
      );
    };
    export default App;
    ```
- **Virtual DOM**
  - Dengan DOM kita dapat berinteraksi seperti mengupdate data di web page, Virtual DOM aadalah duplikasi dari real DOM yang sebenarnya.
#### **Component**
- **React Component**
  - React Component adalah sebuah fungsi atau kelas yang mengembalikan kode JSX. React Component memungkinkan kita untuk memisahkan kode JSX menjadi beberapa bagian yang lebih kecil. React Component memungkinkan kita untuk membuat komponen-komponen yang dapat digunakan kembali.
  - React Component ada 2 yaitu :
    1. Function Component
      ```js
       // Cara 1
      import React from "react";
    
      function App() {
        return (
          <div>
            <h1> Function Component </h1> 
          </div>
        );
      };
    
      export default App;
      ```
      ```js
      // Cara 2
      import React from "react";
    
      const App = () => {
        return (
          <div>
            <h1> Function Component </h1>
          </div>
        );
      };
    
      export default App;
      ```
    2. Class Component
    ```js
     import React from "react";

      class App extends React.Component {
        render() {
          return (
            <div>
               <h1> Class Component </h1>
            </div>
          )
        };
      };
    
      export default App;
    ```
- **State & Props**
  -  State & Props adalah hal yang berhubungan dengan Stateless & Stateful Component. Stateless hanya memiliki props, stateful memiliki state. Jadi state adalah data local. Props digunakan agar component memiliki data yang dinamis dari component lain.
- **lifecycle**
  - Lifecycle method pada React.js adalah method yang akan dijalankan pada saat tertentu. Life cycle method pada React.js adalah method yang akan dijalankan pada saat mounting, unmounting dan updating. Lifecycle method pada React.js adalah method yang akan dijalankan pada saat mounting yaitu constructor, getDerivedStateFromProps, render, componentDidMount, dan getSnapshotBeforeUpdate. Lifecycle method pada React.js adalah method yang akan dijalankan pada saat unmounting yaitu componentWillUnmount. Lifecycle method pada React.js adalah method yang akan dijalankan pada saat updating yaitu getDerivedStateFromProps, shouldComponentUpdate, render, getSnapshotBeforeUpdate, dan componentDidUpdate. 
- **Styling**
  - Styling pada React.js dapat dilakukan dengan menggunakan beberapa cara yakni: Inline styling, CSS file, CSS Module dan Styled Components.<br>
  - Contoh Inline Styling:
  ```js
  import React from 'react';

    const App = () => {
      return (
        <>
          <h1 style={{backgroundColor: "lightblue"}}>Hello World!</h1>
          <p style={{color: "grey"}}>My Name is Farauq<p>
        </>
      );
    }
  ```
## **React JS Lanjutan**
#### **Hooks**
- Hooks pada React.js adalah function yang dapat digunakan pada functional component untuk menggantikan class component. Hooks pada React.js adalah function yang dapat digunakan pada functional component untuk menggantikan class component yaitu useState, useEffect, useContext, dll.
- Contoh Hooks
  - pada usestate
    ```js
    import React, { useState } from "react";

    const App = () => {
      const [name, setName] = useState("Aqilla");
    
      return (
        <div>
          <h1>Hello, {name}</h1>
        </div>
      );
    };
    
    export default App;
    ```
