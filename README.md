## Commit 1 Reflection

Fungsi `handle_connection` menerima sebuah request sebagai parameter. `BufReader` akan melakukan split untuk dilakukan iterasi
dan setiap line nya akan dimasukkan ke dalam vektor. Setiap item pada vektor kemudian akan dicetak.


## Commit 2 Reflection
![](commit2.png)
fungsi `handle_connection` sekarang akan mengirimkan HTTP Response dengan status 200 Ok. Response juga akan mengirimkan 
file html yang akan ditampilkan pada web browser beserta panjang dari konten file html.