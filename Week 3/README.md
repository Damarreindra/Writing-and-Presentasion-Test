# Writing and Presentation Week 3

## Module 1 : Javascript Array and Multidimension Array

### Pendahuluan Array :

- Array adalah Mengorganisasi data dan menyimpan data adalah core concept dari programming.
- Array adalah tipe data list order yang dapat menyimpan tipe data apapun di dalamnya.
- Array dapat menyimpan tipe data String, Number, Boolean, dan lainnya.
- Array dapat dibuat / didefinisikan menggunakan square bracket

### Contoh Array : 

![image](https://user-images.githubusercontent.com/80618060/194893857-afeea1b7-9ca0-4f57-a501-b460150a1b4f.png)

### Cara Memanggil Array : 

- Array pada javascript dihitung dari index data ke-0.
- Data pertama adalah index ke-0.

![image](https://user-images.githubusercontent.com/80618060/194894204-c1436c56-7ea0-446f-a000-e258b226a633.png)

### Array Properties :

- Array memiliki 5 properti yang sering digunakan yaitu constructor, length, index, input, dan prototype.
- Properties adalah fitur yang sudah disediakan oleh Javascript untuk memudahkan developer.

### Array Method : 

- Array memiliki method atau biasa disebut built-in methods. 
- Javascript sudah memudahkan kita dengan menyediakan function/method umum yang bisa kita gunakan. Diantaranya :
    - .push() adalah method untuk menambahkan item  array pada urutan yang paling akhir.
    - .pop() adalah method yang menghapus item array index terakhir.
    - .shift() adalah method untuk menghapus item Array pada index pertama
    - .unshift() adalah method untuk menambahkan item Array pada index pertama
    - .sort() adalah method untuk mengurutkan secara Ascending atau Descending Alphanumeric

### Looping Array :

- .forEach() adalah method untuk melakukan looping pada setiap elemen array.
- .map() melakukan perulangan/looping dengan membuat array baru.

## Module 2 : Javascript Object :

### Pendahuluan Object

- object adalah sebuah tipe data pada variabel yang menyimpan properti dan fungsi (method)
- Properti adalah data lengkap dari sebuah object.
- Method adalah action dari sebuah object. Apa saja yang dapat dilakukan dari suatu object.

### Membuat sebuah object 

- Sama seperti tipe data sebelumnya. Object dapat diassign kedalam sebuah variabel.
- Sama seperti array, didalam object kita dapat menyimpan properti dengan tipe data apapun.

![image](https://user-images.githubusercontent.com/80618060/194895921-c173b142-f2db-4f48-95b5-217af581a575.png)

### Mengakses Object dan Property Object

![image](https://user-images.githubusercontent.com/80618060/194896055-f76895d8-e7b5-4305-b6ed-9e28c8817a5e.png)

Pada gambar tersebut akan menampilkan semua properti pada object, nah bagaimana jika kita hanya ingin mengambil salah satu properti?

        let person = {
        nama : "rei",
        umur : 18
        }
        
Misal disini saya hanya akan mengambil properti nama maka saya menjalankan console.log(person.nama) dan hasilnya seperti ini

![image](https://user-images.githubusercontent.com/80618060/194897683-1b81f36c-877d-42b9-ab98-ec4ed9f2b409.png)

### Update Object 

- Object dapat mengupdate value dari key yang sudah tersedia
- Object dapat menambahkan key dan value baru

![image](https://user-images.githubusercontent.com/80618060/194897888-f5ad6d06-2108-4733-9b62-f616b43ecc00.png)

### Delete Object 

- Kita dapat menghapus properti dari object menggunakan delete operator.

![image](https://user-images.githubusercontent.com/80618060/194898085-f1380a6c-39b7-4cd9-b0cc-87a0999e9c28.png)


## Module 3 : Javascript Recursive 

### Pendahuluan Recursive 

- Recursive adalah function yang memanggil dirinya sendiri sampai kondisi tertentu.

### Ciri Recursive 

- Fungsi rekursif selalu memiliki kondisi yang menyatakan kapan fungsi tersebut berhenti. Kondisi ini harus dapat dibuktikan akan tercapai, karena jika tidak tercapai maka kita tidak dapat membuktikan bahwa fungsi akan berhenti, yang berarti algoritma kita tidak benar.

- Fungsi rekursif selalu memanggil dirinya sendiri sambil mengurangi atau memecahkan data masukan setiap panggilannya. Hal ini penting diingat, karena tujuan utama dari rekursif ialah memecahkan masalah dengan mengurangi masalah tersebut menjadi masalah-masalah kecil.

### Contoh Kasus Recursive

![image](https://user-images.githubusercontent.com/80618060/194898702-edf8bd2e-86b3-4529-8ff7-3452f4cca9ae.png)

## Module 4 : Asynchronous 

### Pendahuluan
- Asynchronous sebuah teknik yang menyelesaikan fungsi secara paralel
- Penggunaan asynchronous dapat dilakukan jika kita ingin mengambil data dari database
- Mengapa perlu menggunakan asynchronous? Asynchronous dibutuhkan ketika ada proses yangg membutuhkan waktu lama. Jadi kita bisa mengerjakan proses yg lain secara paralel.
- Callbacks adalah suatu function namun cara pengeksekusiannya yang berbeda yaitu hanya mengeksekusi pada point tertentu.
- Salah satu function yang digunakan untuk mengatur penjadwalan asynchronous adalah setTimeout function

### Contoh 

        function p1() {
          console.log('p1 done')
        }
          function p2() {
          setTimeout(
            function() {
              console.log('p2 done')
            },2000
          )
        }
        function p3() {
        console.log('p3 done')
        }
        p1()
        p2()
        p3()
        
### Asynchronous - Promise 

- merupakan suatu object dan digunakan hanya untuk satu event dengan menyimpan hasil dari sebuah operasi asynchronous baik itu hasil yang diinginkan (resolved value) atau alasan kenapa operasi itu gagal (failure reason)

### Contoh Promise 

        function GetUser(id) {
        return new Promise((resolve, reject) => {
        if (id !== "" && id !== undefined) {
          reesolve (id);
        } else {
          reject ("ID Harus di Isi");
            }
        });
        }

        GetUser( ) 
        .then((response) => {
        console.log(response);
         })
         .catch((error) => {
        console.log(error);
        });

## Module 5 : Web Storage 

### Pendahuluan Web Storage

- adalah wadah untuk sebuah data yang digunakan untuk penyimpanan data yang terikat di browsernya
- Jenis Web Storage yang umum digunakan yaitu :
    - Local Storage
    - Session storage
    - IndexDB
    - Cookies
    
### Cara Menyimpan Pada Web Storage 

- Cara menyimpan data pada local storage

        let token = "asdfghjkl" //key
        localStorage.setItem("token", token);
    
- Cara mengambil token

        localstorage.getItem("token", token);
        console.log(localStorage.getItem('token");
    
- Cara menghapus data

        localStorage.removeItem("token")



