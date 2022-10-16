# Writing and Presentation Test Week 4

## GIT & GITHUB Lanjutan

### Pendahuluan

- Git adalah aplikasi yang dapat melacak setiap perubahan yang terjadi pada suatu folder atau file.
- Git biasanya digunakan oleh para programmer sebagai tempat penyimpanan file pemrograman mereka, karena lebih efektif.
- File-file yg disimpan menggunakan git akan terlacak seluruh perubahannya, termasuk siapa yang mengubah.

### ‘WHY’ should use GIT and Github?
- Dengan menggunakan GIT dan Github, kamu akan bisa bekerja dalam sebuat tim.
- Tujuan besarnya adalah kamu bisa berkolaborasi mengerjakan proyek yang sama tanpa harus repot copy paste folder aplikasi yang terupdate.
- Kamu juga tidak perlu menunggu rekan dalam satu tim kamu menyelesaikan suatu program dahulu untuk berkolaborasi.
- Kamu bisa membuat file didalam projek yang sama atau membuat code di file yang sama dan menyatukannya saat sudah selesai.

### Cara membuat repository 

- Login akun github, lalu klik icon (+) dan pilih new repository seperti gambar dibawah

![image](https://user-images.githubusercontent.com/80618060/196036194-e99f30df-d549-4e55-84eb-806909977fba.png)

- Isi form 

![image](https://user-images.githubusercontent.com/80618060/196036460-ab573ad2-8df9-44cc-945a-e15852959999.png)

- Lalu kita bisa melakukan configurasi untuk bisa commit dan push pada repository

![image](https://user-images.githubusercontent.com/80618060/196036597-c9361b01-22b2-41b4-8308-6153dc79954e.png)

### Cara Clone repository

- Pilih Repository yang ingin di Clone lalu copy link

![image](https://user-images.githubusercontent.com/80618060/196036655-f7fc8122-f585-48a6-af84-131e69f481d5.png)

- Pilih folder lalu, panggil command git clone

![image](https://user-images.githubusercontent.com/80618060/196036702-08bd8699-d4f5-4070-b661-933f87bde81a.png)

- Berhasil deh 

![image](https://user-images.githubusercontent.com/80618060/196036757-56346b27-6bea-426b-8fea-e4c34bace0fe.png)

### Cara Merge 

- Setelah cloning repo kita langsung buka code editor dan membuat branch baru

![image](https://user-images.githubusercontent.com/80618060/196036944-4a497308-ac7a-47ae-bf15-da403d566da1.png)

- Setelah membuat branch baru kita lanjut dengan mengedit file/membuat file baru

- Lalu menggunakan git add dan git commit

![image](https://user-images.githubusercontent.com/80618060/196037052-3bf5cbf0-03c0-4e6e-bdc3-645a1299e8b3.png)

- dan juga terakhir kita push

![image](https://user-images.githubusercontent.com/80618060/196037119-9f5ecdb3-9673-4269-bee4-dcd6e3e07345.png)

### Cara Merge

- Setelah kita push branch baru kita akan merge branch "coba-writing" ke branch master
- Perhatikan base dan compare, dan jika aman langsung saja kita PR\

![image](https://user-images.githubusercontent.com/80618060/196037178-6594397a-e098-4f52-8196-379c61b159c4.png)

- Lalu merge pull request 

![image](https://user-images.githubusercontent.com/80618060/196037221-c83cbae1-ead3-47b8-80d5-5d9f4cff4166.png)

- Berhasil Merged 

![image](https://user-images.githubusercontent.com/80618060/196037237-40f802e1-929a-471d-9110-e81362e868fe.png)

### Cara Github Collaboration 

- Pilih atau buah repository
- Lalu pilih setting
- Pilih collaborattors dan add people 

![image](https://user-images.githubusercontent.com/80618060/196037989-0d254c97-f31d-4246-82f1-8b52e80c7a14.png)

## Responsive Web Design

### Pendahuluan 

- Responsive Web Desin yaitu suatu tampilan website yang dapat menyesuikan dengan perangkat yang digunakan

### Chrome Dev Tools 
- merupakan tools pada google chrome yang digunakan sebagai tools Responsive Web Design
- Untuk mengakses Chrome Dev Tools yaitu
    - ctrl + shift + j ctrl + shift + m digunakan untuk melihat toggle bar
    
### Viewport

- Dalam menggunakan Responsive Web Design pada bagian HTML perlu ditambahkan viewport pada bagian head agar tampilan website dapat menyesuaikan dengan berbagai device
- Untuk membuat suatu gambar pada halaman website agar menjadi responsive dapat dilakukan dengan menambahkan atribut Max - width = 100% pada bagian gambar
- Media Query salah satu cara untuk mengatur suatu website agar bisa terdiri dari beberapa jenis
    - Penggunaan media query yang umum digunakan adalah min-width dan max-width
    - Contoh penerapan media query @media screen and (max-width: 500px)
- Cara mengkondisikan Media Query ada 2 cara yaitu:
    - Memisahkan beberapa file css sesuai dengan tampilan device yang ingin dibuat
    - Menggabungkan semua styling css device menjadi 1
- Breakpoint yaitu istilah saat terjadi perubahan ukuran pada suatu website ketika berganti device
- Terdapat 3 jenis breakpoint yaitu desktop, tablet, dan mobile phone
- Penggunaan breakpoint pada media query dapat dilakukan dengan membuat range ukuran sesuai dengan tampilan device yang ingin dibuat

## Flexbox

### Pendahuluan 

- Flexbox bertujuan untuk membuat website yang lebih efisien dalam mengatur, menata dan item pada dalam sebuah wadah bahkan ketika ukurannya tidak diketahui dan/atau dinamis (dengan menggunakan kata "flex").

###  Terdapat beberapa nilai yang dapat diatur pada flex container, diantaranya :

- display
    - Pengaturan display flex dilakukan pada container. Terdapat dua value display, yaitu flex (block) dan inline-flex (inline).
- flex-direction
    - Digunakan untuk mengatur arah alur dari items yang ada pada container flex. Default valuenya row. Terdapat empat nilai :
        - Row : Kiri ke kanan
        - Row-Reverse : Kanan ke kiri
        - Column : Atas ke bawah
        - Column-Reverse : Bawah ke atas        
- flex-wrap
    - Secara default, semua item pada flexbox akan mencoba berada dalam satu baris. Maka dengan flex wrap kita dapat mengubah hal tersebut.
        - nowrap : semua item flex akan berada dalam satu baris
        - wrap : item fkex akan membungkus ke beberapa baris, dari atas ke bawah.
        - wrap-reverse :item flex akan membungkus beberapa baris dari bawah ke atas.
        
## Bootstrap 

### Pendahuluan 

- Bootstrap adalah framework web development berbasis HTML, CSS, dan JavaScript yang dirancang untuk mempercepat proses pengembangan web responsive dan mobile-first (memprioritaskan perangkat seluler).

### Grid Class pada bootstrap

![image](https://user-images.githubusercontent.com/80618060/196039215-a797220d-3c95-408f-925d-610128b28ecd.png)

### Responsive Container

- .container-sm
- .container-md
- .container-lg
- .container-xl
- .container-xxl

### Gutters

- Gutter berfungsi untuk memberikan jarak antar item di dalamnya. Contohnya sebagai berikut:

    <div class="container">
      <div class="row g-2">
        <div class="col-6">
          <div class="p-3 border bg-light">Custom column padding</div>
        </div>
        <div class="col-6">
          <div class="p-3 border bg-light">Custom column padding</div>
        </div>
        <div class="col-6">
          <div class="p-3 border bg-light">Custom column padding</div>
        </div>
        <div class="col-6">
          <div class="p-3 border bg-light">Custom column padding</div>
        </div>
      </div>
    </div>
