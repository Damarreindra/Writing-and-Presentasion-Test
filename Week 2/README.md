# Writing and Presentation Week 2

## Module 1 : Javascript Scope

### Pendahuluan Scope

Scope adalah konsep dalam flow data variabel. 

Menentukan suatu variabel bisa diakses pada scope tertentu atau tidak.

Analoginya seperti ini:

Kita semua bisa melihat bintang-bintang dilangit karena bumi bersifat global.

Namun jika kamu tinggal di Bandung, kamu tidak akan bisa melihat monas yang berada di jakarta. Monas bersifat local yaitu hanya berada di Jakarta.

### Blocks

Blocks adalah code yang berada didalam curly braces {}.

Conditional, function, dan  looping menggunakan blocks.

### Global Scope

Global scope berarti variabel yang kita buat dapat diakses dimanapun dalam suatu file.

Agar menjadi Global Scope, suatu variabel harus dideklarasikan diluar Blocks.

Contoh : 

![image](https://user-images.githubusercontent.com/80618060/193535541-4720be8b-1f5b-4273-831a-c004e09ac3b5.png)


### Local Scope 

Local scope berarti kita mendeklarasikan variabel didalam blocks seperti function, conditional, dan looping.

Maka variabel hanya bisa diakses didalam blocks saja. Tidak bisa diakses diluar blocks.

Contoh : 

![image](https://user-images.githubusercontent.com/80618060/193535670-2838d1fa-6a09-4ab9-acf8-6b62491a9d7a.png)

## Module 2 : Function 

### Pendahuluan Function

Function adalah sebuah blok kode dalam sebuah grup untuk menyelesaikan 1 task/1 fitur.

Saat kita membutuhkan fitur tersebut nantinya, kita bisa kembali menggunakannya.

Dibandingkan kita membuat code 1 per 1 yang pastinya membuat kode tidak rapih, 

apalagi task/fitur yang ingin kita buat membutuhkan nilai yang dinamis.

### Contoh Function dan Anatomy Function

![image](https://user-images.githubusercontent.com/80618060/193536421-0c705c5c-c7ec-46b4-aa78-737f998c6278.png)

![image](https://user-images.githubusercontent.com/80618060/193536422-42f3e9b1-66da-4589-bacb-c8a3ae4ea2e8.png)

### Cara memanggil Function 

![image](https://user-images.githubusercontent.com/80618060/193536599-d768c1f8-e4f9-4728-a1c3-ec02206d5133.png)

### Parameter dan Argumen

Dengan parameter, function dapat menerima sebuah inputan data dan menggunakannya untuk melakukan task/tugas.

Saat membuat function/fitur, kita harus tahu data-data yang dibutuhkan. 

Misalnya saat membuat function penambahan 2 buah nilai. Data yang dibutuhkan adalah 2 buah nilai tersebut.

### Contoh Parameter dan Anatomy Parameter

![image](https://user-images.githubusercontent.com/80618060/193537488-30f090b6-8f52-40af-9cf6-b21b4eeb9858.png)

### Argumen Function

Argumen adalah nilai yang digunakan saat memanggil function.

Jumlah argumen harus sama dengan jumlah parameternya. Jadi jika di function penambahan ada 2 parameter nilai saat membuat function. 

Saat memanggil function kita gunakan 2 buah nilai argumen.

### Contoh dan Anatomy Argumen

![image](https://user-images.githubusercontent.com/80618060/193537715-e8f50882-f330-4f58-9383-edf7f4ca9e78.png)

### Arrow Function 

Arrow function adalah cara lain menuliskan function. Ini adalah fitur terbaru yang ada pada ES6 (Javascript Version)


## Error Type

### Contoh-contoh Error

- EvalError

Terjadi kesalahan dalam fungsi eval ()

- RangeError

Telah terjadi angka “di luar jangkauan”

- ReferenceError

Referensi ilegal telah terjadi

- SyntaxError

Terjadi kesalahan sintaks

- TypeError

Telah terjadi kesalahan tipe

- URIError

Terjadi kesalahan dalam encodeURI()

## Module 3: DOM

### Pendahuluan DOM

Document Object Model (DOM) adalah antarmuka pemrograman aplikasi (API) untuk memanipulasi dokumen HTML.

DOM mewakili dokumen HTML sebagai pohon simpul. DOM menyediakan fungsi yang memungkinkan Anda untuk menambah, menghapus, dan memodifikasi bagian dokumen secara efektif.

Perhatikan bahwa DOM adalah cara lintas platform dan bahasa-independen untuk memanipulasi dokumen HTML dan XML.

### Memanipulasi Element HTML

- Mencari Element HTML : 

![image](https://user-images.githubusercontent.com/80618060/193581386-a9478509-5844-479b-ae29-a1878b062c3c.png)

- Mengubah Konten Element :

    - Element.textContent : Element.textContent dapat kita gunakan untuk mengubah teks di dalam sebuah element

![image](https://user-images.githubusercontent.com/80618060/193582120-1690a585-8701-4f4b-940b-75ec28365143.png)

   - Element.innerHTML : Element.innerHTML dapat kita gunakan untuk mengubah konten HTML di dalam sebuah element.
  
getElementsByClassName itu bakal ngereturn bentuk array. walaupun cuma ada 1 element dengan class itu

Kalau bisa diulangin lagi penggunaan id dan class (id cuma boleh 1 element per page, class bisa beberapa sekaligus dan per element bisa beberapa class)

- Membuat Element HTML :

![image](https://user-images.githubusercontent.com/80618060/193582968-a3bfe660-37df-4e0c-b82f-3c660b7580d8.png)

### Event

- Menangkap Interaksi User

    - Element.addEventListener(“event”) : 
        - Bisa dihilangkan
        - Bisa ada beberapa event listener yang sama untuk 1 element
        - Memiliki argument tambahan { options }

    - Element.onevent

- Macam-macam Event Listener :

    - EventListener - Click :

    ![image](https://user-images.githubusercontent.com/80618060/193584454-76b14bbf-7be4-4408-a186-223814bb8030.png)

    - EventListener - Blur :
    
    “Blur”, lawan dari “focus”, adalah event di mana sebuah element kehilangan fokus dari user 
    
    (misal user klk mouse di luar element tersebut atau user klik tab untuk berpindah element)
    
    ![image](https://user-images.githubusercontent.com/80618060/193584760-c63169a7-51d2-4039-9ce1-1921a228c305.png)

     - EventListener - Form Submission :

    Misalkan kita mempunyai element beberapa input dalam sebuah form <input name=”email /> dan <input type=”password” name=”password” />. 
    
    Bagaimana caranya  kita mendapatkan isi dari kedua input tersebut saat submit form?
    
    Ada 2 cara:
    
    - Pasang event listener di kedua input dan tombol submit, lalu saat tombol diklik, baca value dari kedua input tersebut.
       
    - Pasang event listener di form, lalu gunakan FormData untuk mengambil data dari masing-masing input





