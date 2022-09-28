# Writing and Presentation Test Week 1
## Module 1 : Unix Command Line
- Shell ini adalah program yang menerima perintah, kemudian meneruskan perintah tersebut ke system untuk dieksekusi, atau bisa dibilang sebagai perantara yang digunakan user dan sistem operasi dalam berkomunikasi.
- sedangkan CLI merupakan jenis shell yang berbasis teks.

Contoh CLI :
 - sh
 - bash
 - zsh
 - cmd.exe
 
### Cara mengakses CLI

 dikarenakan disini saya menggunakan Windows jadi saya bisa mengakses CLI menggunakan terminal bawaan windows, yaitu CMD.exe
 
 ![image](https://user-images.githubusercontent.com/80618060/192426310-53f88dd0-17e5-4b6d-bfb9-9b8738d51779.png)

### File System

Sebelum melanjutkan ke navigation file kita harus mengetahui file system, Sistem operasi Windows & Unix-like menyusun file dan direktori menggunakan struktur yang bentuknya mirip tree

![image](https://user-images.githubusercontent.com/80618060/192427169-c3b1a28c-ad65-496d-a846-fe36dc208d9e.png)

### Navigation files dan directory

- Command “pwd” (print working directory) untuk melihat nama direktori kita berada saat ini.
- Command “ls” (lists) untuk melihat isi dari direktori.
- Command “cd”  (change directory) untuk pindah ke direktori lain.

### File Manipulation

#### Create File & Directory

- Command “touch” untuk membuat sebuah file.
- Command “mkdir” untuk membuat sebuah direktori.

#### View File Contents

- Command “head” untuk melihat beberapa line awal dari sebuah file text.
- Command "tail" untuk melihat beberapa line akhir dari sebuah file text
- Command "cat" untuk melihat isi sebuah file.

#### Copy, Move, and Delete Files & Directory

- Command "cp" untuk menyalin sebuah file/direktori.
- Command "mv" untuk memindahkan file/direktori, sekaligus bisa untuk mengganti nama file/direktori.
- Command "rm" untuk menghapus sebuah file/direktori.

## Module 2 : Git & Github

- Git merupakan tools dalam memversikan program
- Git digunakan sebagai version control system serta dapat digunakan untuk melacak segala perubahan pada suatu file atau folder maupun source code
Vendor Git yaitu Github, Gitlab, Bitbucket Github merupakan vendor git yang paling umum digunakan dan sebagai tempat penyimpanan Git Repository

### Instalasi dan Konfigurasi Git & Github
- git config global user.name "Damarreindra"
- git config global user.email damarihya08@gmail.com
- Melihat hasil konfigurasi dengan git config --list Config list

![image](https://user-images.githubusercontent.com/80618060/192455526-f29a321f-2d19-467a-a8a3-ebf7ea89d1fc.png)

- Membuat Repository

![image](https://user-images.githubusercontent.com/80618060/192456027-85c0bf0a-d36d-4b18-874c-65cc4ac7a747.png)

- git init (dilakukan didalam folder yang dibuat)

![image](https://user-images.githubusercontent.com/80618060/192456274-61d27b17-2ab3-400c-bdef-493a28bf8d27.png)

- git Status digunakan untuk melihat apakah terjadi perubahan atau tidak pada Git
(files masih untracked jadi kita harus menggunakan git add)

![image](https://user-images.githubusercontent.com/80618060/192456363-69b7da3a-4400-4d9c-982d-f7ca62020de5.png)

- git add untuk menambah file baru/file yang telah diubah pada Git

![image](https://user-images.githubusercontent.com/80618060/192456556-6b86ee55-052d-4ef2-a094-bd0f1cb58914.png)

- git remote menghubungkan remote repository dengan project local yang telah kita buat direktorinya

![image](https://user-images.githubusercontent.com/80618060/192457181-80854383-4a35-4b3e-8b54-91a8e45e791d.png)

- git commit -m "commit message" digunakan untuk menyimpan perubahan pada Git

![image](https://user-images.githubusercontent.com/80618060/192456864-8690ac51-1faa-496f-a166-33eac100d77b.png)

- git push -u origin master digunakan untuk mengirimkan/perubahan file ke remote repository

![image](https://user-images.githubusercontent.com/80618060/192457417-3d896c4d-d36c-4ddc-82c7-53b4052a5460.png)


- git branch -b [nama branch] digunakan untuk membuat branch baru

![image](https://user-images.githubusercontent.com/80618060/192457232-1a99ed2c-c471-468e-b965-cca0550d45ca.png)

- git checkout digunakan untuk berpindah branch
- git merge digunakan untuk menggabungkan branch cabang ke branch master ( git merge origin/(nama branch))

## Module 3 : HTML

### Pendahuluan HTML

- HTML adalah singkatan dari Hypertext Markup Language.
- HTML digunakan untuk menampilkan konten pada browser. 
- HTML bukanlah sebuah bahasa pemrograman, artinya HTML tidak bisa dinamis mengolah data.
- HTML bisa dijalankan dengan melakukan klik kanan dan pilih default browser atau menggunakan live server extension.

### Tools Pendukung HTML 

Ada 2 tools utama yang harus dipersiapkan untuk membuat HTML

- Browser
    - Chrome (Paling direkomendasikan), OperaGX, dan Firefox.
- Code Editor
    - VSCode (Paling direkomendasikan), dan SublimeText.
    
### HTML Structure

    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta http-equiv="X-UA-Compatible" content="IE=edge">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Writing and Presentation Test</title>
    </head>
    <body>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsum impedit totam quis necessitatibus, suscipit molestiae ipsam amet doloremque eius nobis?</p>
    </body>
    </html>

### Jenis Tag

- Single Tag

      - <br/>
      - <hr/>
      - <img>
      
- Paired Tag

      - <h1></h1>
      - <p>
      - <head>
 
### Anatomy Tag
 
     <p> : Opening Tag
      Lorem bla bla : Content
     </p> : Closing Tag

### Semantic HTML

Dibandingkan menggunakan tag div dengan class header lebih baik kita menggunakan tag header yang sudah semantic, hal ini juga berlaku seperti footer, section, aside.

    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta http-equiv="X-UA-Compatible" content="IE=edge">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Writing and Presentation Test</title>
    </head>
    <body>
        <header>
            <nav>
                <a href="">Blog gg manja</a>
            </nav>
        </header>

        <article>
            <p>Lorem ipsum dolor sit amet cecessitatibus, suscipit molestiae ipsam amet doloremque eius nobis?  </p>
        </article>

        <footer>
            Made by Damar with love
        </footer>
    </body>
    </html>

### Contoh Membuat Tag Popular
     <table border="1">
            <thead>
                <tr>
                    <td>Nama</td>
                    <td>Umur</td>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>Damar</td>
                    <td>20</td>
                </tr>
            </tbody>
        </table>
 
### Deploy Web Dengan Netlify

- Login dengan akun Git Provider

![image](https://user-images.githubusercontent.com/80618060/192659057-5c17a6c3-841d-4eaa-baa3-2900936677f7.png)

- Pilih repo yang ingin dideploy

![image](https://user-images.githubusercontent.com/80618060/192659602-a85ad58d-acf3-432d-a951-ea077802d22a.png)

- Pilih Branch, lalu klik deploy

![image](https://user-images.githubusercontent.com/80618060/192659683-58969efd-9594-4e51-a179-43f918e52f8b.png)

- Tunggu proses dan selesai (Belum menggunakan custom domain)

![image](https://user-images.githubusercontent.com/80618060/192659798-467a3ca2-c8c0-4441-b537-4509526dd070.png)

- Link : https://singular-melba-77bed3.netlify.app

![image](https://user-images.githubusercontent.com/80618060/192660195-231b0b2d-2892-4c1c-aebc-559eca34315e.png)

## Module 4 : CSS

### Pendahuluan CSS

Apa itu CSS? CSS adalah bahasa yang digunakan untuk mendesain halaman website.

Dengan CSS, kita bisa mengubah warna, menggunakan font custom, editing text format, mengatur tata letak, dan lainnya.

### Struktur CSS

    .elementHTML{  
         property : value } 
         
### Comment CSS

Digunakan untuk memberi keterangan terutama jika bekerja bersama tim, karena akan lebih memudahkan dalam proses developing

### Selector CSS

- Class Selector ( . ) untuk menyeleksi class yang ingin stylenya kita ubah
- Id Selector ( # ) untuk menyeleksi id yang ingin stylenya kita ubah
- Tag Selector ( head, body, h1) untuk menyeleksi tag element yang ingin stylenya kita ubah. tag element HTML maka akan bersifat global yg artinya akan mengubah seluruh html

### Memanggil CSS

- Inline Tag : menggunakan css langsung di atribute element html
- Internal Tag : menggunakan tag style di bagian head
- External Tag : menggunakan file css terpisah dengan html

### Flexbox 

- Flexbox adalah suatu cara untuk mengatur layout atau tata letak
- Flexbox terdiri 1 parent (container) dan bisa beberapa child
- Flex direction digunakan untuk mengatur letak child
- Flex wrap mengatur tata letak child pada 1 line
- Flex flow yaitu digunakan sebagai shortcut untuk set up flex-direction dan flex-wrap secara bersamaan
- Order digunakan untuk ordering item yang ingin diatur posisinya
- Justify - content digunakan untuk mengatur tata letak antar item child secara horizontal
- Align - content digunakan untuk mengatur tata letak antar item child secara vertikal atau cross axis
- Flex-grow digunakan untuk mengatur size suatu item child pada flexbox
- Flex-shrink digunakan untuk memperkecil size suatu item child secara relatif terhadap item child lainnya
- flex-basis digunakan untuk mengatur width setiap item child

### Responsive 

Responsive digunakan supaya tampilan web terlihat baik pada semua ukuran device.

- Fluid Grid
Maksud dari fluid grid adalah sebuah grid atau garis-garis batas yang menentukan letak suatu komponen dalam desain, namun dapat berubah-ubah sesuai dengan ukuran tampilannya.

Hal ini karena satuan yang digunakan adalah satuan yang relatif seperti persen, atau em (satuan dipakai dalam tipografi).

- Media queries
Adanya media query memungkinkan desainmu lebih sesuai dengan berbagai ukuran layar.

Media query memungkinkan website untuk dapat mengambil data mengenai ukuran layar yang digunakan untuk menampilkan konten.

- Responsive media
Prinsip selanjutnya yang harus diperhatikan dalam membuat responsive web design adalah media yang responsif.

Seperti pada poin pertama, yaitu kamu harus memastikan bahwa media seperti foto dan video dapat ditampilkan dengan baik di berbagai ukuran layar.

Oleh karenanya, dibandingkan dengan menggunakan ukuran tampilan berupa pixel, maka pastikan ukuran dari media yang ditampilkan dalam bentuk persentase.

Sangat disarankan untuk memberikan pengukuran dari media sebesar 100%, agar media yang ditampilkan dalam tampilan yang maksimal. 

    @media screen and (min-width: 800px) {
      .container {
        margin: 1em 2em;
      }
    }

## Module 5 : Algoritma 

### Pendahuluan Algoritma dan Data Struktur

- Algoritma adalah deskripsi berupa step-step yang dibutuhkan untuk menyelesaikan suatu masalah.
- Struktur data adalah cara penyimpanan , pengorganisasian , dan pengaturan data di dalam media penyimpanan komputer sehingga data tersebut dapat digunakan secara efisien.
- Dengan struktur data yang baik, maka konsep algoritma yang digunakan pun akan baik. Begitu juga dengan sebaliknya, jika struktur data tidak baik, maka konsep algoritma pada proses pemrograman pun juga tidak akan baik. Dengan memahami algoritma, suatu program akan mudah dilakukan.

### Kualitas wajib dari Algoritma

- Input dan output harus didefinisikan terlebih dahulu dengan tepat
- Setiap step harus benar-benar clear dan tidak ambigu
- Algoritma seharusnya tidak mengandung suatu code pada bahasa pemograman tertentu. Algoritma harus dibuat agar dapat digunakan dalam bahasa pemograman apapun.

### Contoh Algoritma

- Step 1 : Start
- Step 2 : Declare Variabe a,b, and sum.
- Step 3 : Read Variable a and b.
- Step 4 : add a and b values to sum to assign a+b
- Step 5 : display sum
- Step 6 : Stop

### Pseudocode

Pseudocode adalah menuliskan algoritma dengan umumnya bahasa inggris sebelum kita implementasikan ke bahasa pemograman tertentu.

### Contoh Pseudocode

    STORE "Num1" from input form
    STORE "Num2" from input form
    STORE "Sum" without value
    
    CALCULATE "Num1" + "Num2" and SET value to "Sum"
    DISPLAY "Sum"
    
 ### Contoh Penerapan Dengan Javascript
 
    var a,b,num1,num2,sum;
    a= prompt("Input first Number");
    b= prompt("Input second Number");
    num1 = parseFloat(a);
    num2 = parseFloat(b);
    sum = num1+num2;

    alert(sum);


