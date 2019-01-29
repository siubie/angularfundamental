# Struktur File Pada Project Angular

Untuk memulai membuat project angular dapat dilakukan dengan membuat sebuah project baru menggunakan angular cli, untuk membuat project dengan angular cli ikutilah langkah langkah percobaan dibawah ini

## Langkah percobaan

Ketikkan perintah berikut ini pada terminal anda

```
ng new tutorial
```

![ngnew](diagrams/ngnew.png)

Setelah ng new tutorial dijalankan angular cli akan meminta anda memilih untuk menambahkan routing module atau tidak, untuk saat ini pilih Y untuk menambahkan routing module

![ngnewrouting](diagrams/ngnew-route-y.png)

Selanjutnya angular cli akan meminta anda untuk memilih format stylesheet yang akan digunakan pilihlah css sebagai stylesheetnya.

![ngnewcss](diagrams/ngnew-css.png)

Proses selanjutnya angular cli akan mendownload dan menginstall dependency yang dibutuhkan. Tunggulah proses ini sampai selesai

![installProgres](diagrams/ngnew-install.png)

Berikut ini tampilan terminal ketika proses install sudah selesai

![installdone](diagrams/ngnew-install-done.png)

Untuk langkah selanjutnya silahkan buka folder tutorial yang sudah dibuat dengan menggunakan visual studio code atau editor yang anda kuasai.

![installvscode](diagrams/ngnew-finished-vs.png)

Di editor ini anda dapat melihat struktur file yang dimiliki oleh angular v.7 pada dasarnya struktur file ini masih sama dengan yang dimiliki oleh angular v6.

Didalam folder src terdapat folder app yang berisi module dan component, nanti pada pembelajaran selanjutnya kita akan mengubah dan menambah component serta module di dalam folder ini. Untuk tahap awal pembelajaran angular kita akan lebih sering bekerja di folder app.
