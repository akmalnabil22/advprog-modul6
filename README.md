## Commit 1 Reflection

Fungsi `handle_connection` menerima sebuah request sebagai parameter. `BufReader` akan melakukan split untuk dilakukan iterasi
dan setiap line nya akan dimasukkan ke dalam vektor. Setiap item pada vektor kemudian akan dicetak.


## Commit 2 Reflection
![](commit2.png)
fungsi `handle_connection` sekarang akan mengirimkan HTTP Response dengan status 200 Ok. Response juga akan mengirimkan 
file html yang akan ditampilkan pada web browser beserta panjang dari konten file html.


## Commit 3 Reflection
![](commit3.png)
fungsi `handle_connection` sekarang akan menyesuaikan file html yang dikirim sesuai dengan status yang didapatkan dari request.
Jika status yang didapat `200 Ok`, akan mengirimkan `hello.html`. Jika status yang didapat `404 NOT FOUND`, maka file html yang
dikirim akan mengirimkan `404.html`. Refactoring dilakukan agar tidak ada duplikasi kode pada `main.rs`.


## Commit 4 Reflection
Pada endpoint `sleep`, kita akan melakukan sleep pada thread kita yang sedang berjalan. Karena kita hanya memakai satu thread,
saat kita mengakses browser dari windows baru, maka harus menunggu proses dari endpoint `/sleep` selesai terlebih dahulu
karena kedua proses tersebut berjalan di thread yang sama.


## Commit 5 Reflection
Sekarang kita menyiapkan 4 thread yang bisa digunakan untuk menjalankan proses. Setiap ada request yang masuk, request akan 
dijalankan pada salah satu thread. Pada `lib.rs`, kita membuat struktur ThreadPool yang mengelola kumpulan worker thread.
Setiap ada tugas baru yang dikirim, worker thread akan mengambil dan mengeksekusi tugas tersebut. Jadi, kita bisa menjalankan 
berbagai tugas secara konkuren.