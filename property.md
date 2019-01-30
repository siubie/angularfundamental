# Property Binding

Property binding adalah cara angular untuk menghubungkan antara tag attribute pada template html dan variabel class component. Untuk mempermudah pemahaman terhadap property binding ada beberapa konsep yang harus dipahami yaitu :

1. Semua tag html memiliki attribut.
2. Semua attribut pada tag html tersebut dapat di akses melalui Document Object Model (Dom).
3. Semua Dom memiliki properties yang sesuai dengan attribut pada tag html tersebut.

> Untuk yang sudah berpengalaman dengan akses DOM menggunakan jquery atau javascript mungkin dapat lebih mudah memahami konsep ini

Contoh :

```html
<!-- kode program html biasa: -->
<input type="text" value="hello world" />
<!-- kode program property binding pada atribut html: -->
<input type="text" [value]="namaVariabelDiComponent" />
<!-- kode program property binding pada interpolasi pada html: -->
<input type="text" value="{{namaVariabelDiComponent}}" />
```

Dengan potongan kode program di atas kita melakukan property binding ke attribut value dari input text. Dengan cara ini kita dapat menghubungkan nilai variabel dengan nama "namaVariabelDiComponent" ke isi dari input text.

Selain dengan menggunakan `[]` (square bracket) property binding juga bisa dilakukan dengan menggunakan interpolasi seperti pada kode program di atas, namun cara yang umum dan sering digunakan adalah cara pada kode program baris ke dua.

Property binding dengan cara ini merupakan model "one way data binding" dimana data mengalir satu arah dari component ke template, artinya data hanya akan berubah jika component mengubah nilai dari data tersebut template html hanya menjadi presenter atau alat untuk menampilkan data.

## Langkah Percobaan
