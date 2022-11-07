# WRITING & PRESENTATION TEST WEEK 7

## Proptypes 

### Apa itu PropTypes?

PropTypes merupakan library untuk menvalidasi props. Ini sangat membantu dalam meminimalkan bugs saat mengembangkan App besar. Jika props tidak benar type nya maka akan muncul warning.

Cara Penggunaan :

- Install Proptypes

- npm install prop-types

- Import kedalam file component :

- import PropTypes from "prop-types"

Panggil proptype seperti gambar yang ada dibawah

![image](https://user-images.githubusercontent.com/80618060/200304095-48d88d10-297f-44b0-a524-171928a25c9d.png)

## React Router 

React Router merupakan standar library untuk routing pada React.

standar routing berfungsi untuk membuat suatu website menjadi dynamic.

Pada React, Router membantu untuk mengarahka page satu ke page yg lainnya berdasarkan path url yg ditentukan.

### Cara menginstall/menggunakan React Router :

- npm install react-router-dom@6
- Menambahkan import { BrowserRouter } from "react-router-dom"; pada bagian index.js
- Menambahkan code :

        <BrowserRouter>
        <App />
        </BrowserRouter>
    
- Browser Router merupakan interface pada umumnya yg digunakan untuk menjalankan react di browser atau untuk membuat router-router sederhana.
- HashRouter penulisannya menggunakan #, yg digunakan pada sebuah website yang menggunakan satu page saja.
- Code pada Bagian App.js

        import React from 'react'
        import { BrowserRouter, Route, Switch } from 'react-router-dom'

        import Notfound from './pages/NotFound'
        import Home from './pages/Home'
        import Profil from './pages/Profil'
        import ProfilDetail from './pages/ProfilDetail'

        function App() {
          return (
            <BrowserRouter>
              <Switch>
                <Route path="/" exact component={Home} />
                <Route path="/profil" exact component={Profil} />
                <Route path="/profil/:name" exact component={ProfilDetail} />
                <Route component={Notfound} />
              </Switch>
            </BrowserRouter>
          )
        }

        export default App

- Code pada Bagian Page Home

        import React from 'react'
        import { Link } from 'react-router-dom'

        function Home(props) {
          return (
            <>
              <h2>
                Home page
              </h2>

              <Link to="/profil">Menuju profil</Link>
            </>
          )
        }

### Dynamic Route & Nested Route

- Dynamic Route 

        import { useState } from 'react'
        import reactLogo from './assets/react.svg'
        import './App.css'
        import { Link, Route, Routes } from 'react-router-dom'
        import HomePage from './pages/HomePage'
        import AboutPage from './pages/AboutPage'
        import DetailPage from './pages/DetailPage'
        function App() {
          return(
            <>
              <nav>
                <Link to={"/"}>Home |</Link>
                <Link to={"/about"}>About</Link>
              </nav>
              <Routes>
                <Route path='/' element={<HomePage/>}/>
                <Route path='/about' element={<AboutPage/>}/>
                <Route path='/detail/:id' element={<DetailPage/>}/>
              </Routes>
            </>
          )

        }

        export default App
        
- Nested Route 

        import User from './user/User';
        import Setting from './user/setting/Setting';
        import Profile from './user/profile/Profile';
        import Favorite from './favorite/Favorite';

        function App() {
          return (
            <>
          <ul className='user'>

          <li><Link to="/">Home</Link></li>
          <li><Link to="/user">User</Link></li>
          <li><Link to="/favorite">FavoriteKu</Link></li>
          <li> <Link to="/galeri">Galeri</Link></li>
          </ul>

          <Routes>
                <Route path='/' element={<Home/>}/>
                <Route path='/User' element={<User/>}/>
                <Route path='/Gallery' element={<Gallery/>}/>
                <Route path='/Favorite' element={<Favorite/>}/>

                {/* Nested router */}
                <Route path='/Favorite/Music' element={<Music/>}/>
                <Route path='/User/Profile' element={<Profile/>}/>
                <Route path='/User/Settings' element={<Settings/>}/>
          </Routes>
           </>
          );
        }
        
## React Redux 

### Apa itu React Redux ?

Redux adalah salah satu library state management yang biasa disandingkan dengan react.

Idenya sederhana…

Yaitu dengan menyimpan state di satu tempat, sehingga lebih mudah untuk di manage.

Biasanya tanpa state management library, kita akan menyimpan state di setiap komponen.

Kalau butuh komunikasi data antar komponen, kita bisa menggunakan props.

Namun akan menjadi tantangan bila aplikasi yang kita bangun semakin kompleks.

Akan sedikit sulit untuk mengatur state di komponennya, belum lagi jika ada komunikasi data antar komponen.

Salah satu solusi dari masalah tersebut adalah dengan menggunakan library state management seperti redux.

### Instalasi React Redux 

- mulai dengan menginstall:

        npm install redux react-redux
        
- Siapkan folder redux di dalam src/

![image](https://user-images.githubusercontent.com/80618060/200308548-6becdf09-f70c-48f0-bfaf-c46881ccb61a.png)

- File Store

Buat file store.js pada folder redux [/src/redux/store.js] dan tulis kode seperti di bawah : 

![image](https://user-images.githubusercontent.com/80618060/200308713-ea5a6566-1269-41de-ae00-426825b0a214.png)

- buat 1 folder types pada redux [/src/redux/types] dan sebuah file baru dengan nama counter.js dengan kode berikut:

![image](https://user-images.githubusercontent.com/80618060/200308849-41dd5636-059f-4824-9146-a5de3b1c3e01.png)

- Buat folder baru actions di dalam folder redux [/src/redux/actions/] dan buat sebuah file dengan nama counter.js:

![image](https://user-images.githubusercontent.com/80618060/200308979-3dd66932-34d5-4b28-9757-f9c53b371783.png)

- Kita perlu membuat folder reducer [/src/redux/reducers/] dan file pertama yaitu index.js yang akan kita gunakan untuk indexing setiap reducer 

![image](https://user-images.githubusercontent.com/80618060/200309142-5703b0bb-8eca-4f05-ac10-9c15165d6264.png)

- sekarang kita buat reducer pertama kita dengan nama counter.js pada folder reducers [/src/redux/reducers/counter.js]

![image](https://user-images.githubusercontent.com/80618060/200309456-03af4c5a-4538-4202-9e2f-aa0bad8d4691.png)

- Kini reducer counter kita siap digunakan, kita bisa implementasi store kita dengan cara berikut:

![image](https://user-images.githubusercontent.com/80618060/200309529-8290d691-a139-4c70-af02-68e1689546ab.png)

## Redux Thunk

- Redux digunakan untuk mengolah state management

- State management pada dasarnya adalah cara untuk memfasilitasi komunikasi dan berbagi data di seluruh komponen.

Redux Memudahkan User dalam :

    - menyimpan status aplikasi Anda.
    - mengelola status aplikasi Anda.
    - memberi tahu pihak yang berkepentingan ketika status aplikasi berubah.

- Redux memungkinkan untuk mengelola status aplikasi Anda di satu tempat dan membuat perubahan di aplikasi mudah untuk diprediksi dan dilacak

- Redux thunk adalah middleware yang memungkinkan untuk memanggil pembuat aksi yang mengembalikan fungsi sebagai ganti objek aksi.

- Fungsi itu menerima metode pengiriman penyimpanan, yang kemudian digunakan untuk mengirim aksi sinkron di dalam isi fungsi setelah operasi asinkron selesai.

- Untuk penggunaan redux thunk dengan npm install redux-thunk@2.3.0


