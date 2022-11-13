# Writing and Presentation Test Week 8

## React Context 

### Apa itu React Context ? 

Context itu seperti variable global yang bisa kamu akses dimana saja tanpa kamu harus memparsing props ke setiap komponen.

### Kapan Harus Menggunakan Context? 

Jika kamu mempunyai aplikasi yang besar, kamu tidak disarankan untuk menggunkan context ini. Karena jika kamu mempunyai aplikasi yang besar, mungkin kamu harus segera menggunakan redux. Tapi jangan khawatir saya tidak akan membahas tentang redux di sini, mungkin saya akan menjelaskan redux di artikel selanjutnya.

Jadi maksudnya adalah, kamu di rekomendasikan menggunakan context ini jika kamu mempunyai aplikasi dengan skala kecil ke menengah untuk membuat aplikasimu mudah di kembangkan dan mudah di mengerti oleh orang-orang.

## React Testing

- Testing berarti memeriksa bahwa kode kami memenuhi beberapa harapan
- Testing dibagi menjadi 2 main kategori yaitu :
    - Unit Testing
    - integration testing
    - UI texting
    
- Unit Texting menggunakan Jest adalah a JavaScript test runner, yaitu library JavaScript untuk membuat, menjalankan, dan menyusun pengujian.
- Unit testing ini, unit individu atau komponen perangkat lunak diuji. Sebuah unit dapat berupa fungsi individu, metode, prosedur, modul, atau objek. Tes unit mengisolasi bagian kode dan memverifikasi kebenarannya, untuk memvalidasi bahwa setiap unit kode perangkat lunak berfungsi seperti yang diharapkan.

### Terdapat 2 scenario yang dilakukan dalam melakukan unit testing yaitu:
- mewarisi kode warisan yang datang tanpa tes
- menerapkan fungsi baru secara tiba-tiba

### Alur testing:
- import fungsi untuk menguji
- Memberikan masukan ke fungsi
- Menentukan apa yang diharapkan sebagai output
- Memeriksa apakah fungsi menghasilkan output yang diharapkan

### Mengapa perlu dilakukan testing:
- Tujuan pertama dari testing adalah untuk mencegah regresi. Regresi adalah kemunculan kembali bug yang sebelumnya telah diperbaiki. Itu membuat fitur berhenti berfungsi sebagaimana dimaksud setelah peristiwa tertentu terjadi
- Testing digunakan memastikan fungsionalitas komponen kompleks dan aplikasi modular.
- Testing diperlukan untuk kinerja yang efektif dari aplikasi perangkat lunak atau produk.
- React Testing Library dibangun di atas DOM Testing Library dengan menambahkan API untuk bekerja dengan komponen React.
- Menginstall library testing npm install --save-dev @testing-library/react
