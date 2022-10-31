# Writing and Presentation Test Week 6

## React JS Intro 

### Why using React JS?

- Declarative
React makes it painless to create interactive UIs. Design simple views for each state in your application, 
and React will efficiently update and render just the right components when your data changes.

- Component-Based
Build encapsulated components that manage their own state, then compose them to make complex UIs.

- Learn Once, Write Anywhere
We don’t make assumptions about the rest of your technology stack, so you can develop new features in React without rewriting existing code.

### Cara membuat react project

- Cari folder yang diinginkan
- Buka folder tersebut menggunakan CMD
- Ketik pada CMD "npm create vite@latest my-Test-react" tanpa quote
- Pilih Framework (React)
- Pilih Variant (JS)
- Lalu ikuti seperti gambar dibawah

![image](https://user-images.githubusercontent.com/80618060/198893989-3b0925ad-2fb1-46d5-a623-581b9a2f909c.png)


### Cara membuat component pada React 

Ada 2 cara membuat component pada react JS, yaitu dengan :

- Menggunakan Fucntion 
- Menggunakan Class

### Perbedaan Class dan Fucntion Component

- Functional component hanya bisa menggunakan props itu sebabnya function component disebut stateless component atau biasa digunakan juga sebagai UI Component (komponen yang menangani tampilan).
- Sedangkan Class component dapat menggunakan state dan props.

### Cara membuat component menggunakan Function 

- Membuat, lalu buka react app yang sudah dibuat menggunakan code editor
- Membuat folder baru dengan nama components di dalam folder src

![image](https://user-images.githubusercontent.com/80618060/198893286-f5465a54-c9c1-4b5e-b857-eb813c95d455.png)

- Lalu buat file jsx, dengan diawali huruf besar diawal

![image](https://user-images.githubusercontent.com/80618060/198893316-da769c2b-d534-4cb5-848c-ecc21b2395f9.png)

- Contoh function component 

![image](https://user-images.githubusercontent.com/80618060/198893345-719caf27-d5dc-4893-a425-863a4c62daed.png)

- Lalu export, dan import pada App.jsx lalu panggil didalam return

![image](https://user-images.githubusercontent.com/80618060/198893379-9800fe62-1202-49e0-b1fa-6bee98deac70.png)

### Cara Styling pada react

- Beri className pada label

![image](https://user-images.githubusercontent.com/80618060/198893636-ceba82a3-662a-444f-8214-5b96326a48e2.png)

- Masuk ke file App.css
- Lalu seperti membuat css pada umumnya 

![image](https://user-images.githubusercontent.com/80618060/198893655-4573b2ad-cff7-4dec-8920-a9228be5f325.png)

### State and Props

- State, sebuah object untuk menyimpan data pada React dan akan di render atau muat ulang ketika data mengalami perubahan
- Props, Props adalah suatu cara untuk mengirim dan mengakses data dari komponent lain secara langsung.

Contoh : 

![image](https://user-images.githubusercontent.com/80618060/198895534-e2edf99a-c3a6-4e50-9f57-58c9325aae58.png)

### React Lifecycle

Component — component di react js akan melewati tiga fase hidup, yaitu :

- Mounting
- Updating
- Unmounting

![image](https://user-images.githubusercontent.com/80618060/198962277-6e7313db-2479-4fb6-9e47-32f9a342c4b8.png)

- Fase Mounting 

adalah fase ketika components di buat atau pertama kali di render ke DOM Coba perhatikan pada fase Mounting di atas ! Pada fase ini ada tiga methods yang akan di eksekusi yaitu componentWillMount, render, dan componentDidMount. Urutannya eksekusi setiap methodsnya di mulai dari atas ke bawah seperti pada gambar di atas.

Dalam hal ini componentWillMount adalah method yang akan di eksekusi pertama kali, kemudian akan mengeksekusi method render. Di dalam method render inilah kita menyimpan file jsx yang nantinya akan di render ke DOM.

- Fase updating 

adalah fase ketika sebuah component akan di render ulang, biasanya ini terjadi ketika ada perubahan pada state atau props yang mengakibatkan perubahan DOM.

Di fase ini adalah 5 methods yang akan di eksekusi :

  - componentWillReceiveProps : fungsi ini akan di eksekusi bila state yang ada di component akan di update atau di ubah dengan nilai props yang baru.
  - shouldComponentUpdate : tugasnya adalah untuk menentukan apakah sebuah component akan di render ulang atau tidak.Method ini akan mengembalikan nilai boolean true & false, jika true maka component akan di render ulang atau sebaliknya.
  - componentWillUpdate : fungsi ini akan di eksekusi jika fungsi shouldComponentUpdate mengembalikan nilai true.
  Kemudian kembali method render akan di jalankan
  - componentDidUpdate : fungsinya sama dengan componentDidMount yaitu untuk manipulasi DOM dan request data.

- Fase unmounting 

adalah fase ketika component di hapus dari DOM.Pada fase ini hanya ada satu method yang akan di eksekusi yaitu componentWillUnmount, yang di jalankan sebelum sebuah component di hapus dari DOM

## React JS Lanjutan

### React Hooks

Apa itu itu react hooks ?

Sebenarnya react hooks hanya kumpulan fungsi — fungsi khusus. Dengan fungsi — fungsi ini, memungkinkan kita menggunakan fitur — fitur react tampah harus menggunakan class komponen.

- useState 

Fungsi useState akan mereturn pasangan nilai dari state dan fungsi untuk mengubah state tersebut dalam bentuk sebuah array.

    import React, {useState} from "react"

    const Example = () => {
      const [name, setName] = useState("")
      const changeName = e => setName(e.target.value)
      return(
        <input
          type="text"
          value={name}
          onChange={changeName}
        />
      )
    }    
    
- Item pertama adalah statenya
- Item keduanya adalah fungsi untuk mengubah state tersebut

- useEffect
- 
React hooks useEffect digunakan untuk menambahkan side effect ke function komponen.

Penggunaan useEffect mirip dengan lifecycle method seperti componentDidMount, componentDidUpdate, dan componentWillMount di class component.

useEffect hooks akan menerima dua parameter, yaitu sebuah callback dan sebuah array.

    useEffect(fn, [])
    
Contoh code menggunakan useEffect : 

    import React from "react"
    import axios from "axios"

    const Example = () => {
      const [lists, setLists] = useState([])
      useEffect(() => {
        axios.get(endPoint)
          .then(res => setLists(res.data)
      },[])
      return(
        <div>
          <h1>my component</h1>
        <div/>
      )
    }
    export default Example

### PropTypes

Apa itu PropTypes?

PropTypes merupakan library untuk menvalidasi props. Ini sangat membantu dalam meminimalkan bugs saat mengembangkan App besar. Jika props tidak benar type nya maka akan muncul warning.

Cara Penggunaan : 

- Install Proptypes 
  
    npm install prop-types
    
- Import kedalam file component : 

    import PropTypes from "prop-types"

- Panggil proptype seperti gambar yang ada dibawah 

![image](https://user-images.githubusercontent.com/80618060/198964326-800eb2fb-8f7f-448b-a88c-bdf396214d6a.png)
