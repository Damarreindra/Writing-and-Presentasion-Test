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

### Tools Pendukung HTML 

Ada 2 tools utama yang harus dipersiapkan untuk membuat HTML

- Browser
    - Chrome (Paling direkomendasikan), OperaGX, dan Firefox.
- Code Editor
    - VSCode (Paling direkomendasikan), dan SublimeText.

