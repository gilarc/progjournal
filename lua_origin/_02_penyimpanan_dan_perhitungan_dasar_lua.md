## Penyimpanan dan perhitungan dasar lua

Pada topik sebelumnya, kita telah melihat bagaimana mencetak sesuatu dalam Lua dan beberapa konsep dasar pemrograman Lua. Sekarang mari kita melangkah lebih jauh.

### Variabel

Variabel sebenarnya hanya merupakan nama yang diberikan pada area penyimpanan. Variabel dapat menyimpan berbagai jenis nilai termasuk fungsi dan tabel. Nama variabel dapat terdiri dari huruf, angka, dan karakter garis bawah. Variabel harus dimulai dengan huruf atau garis bawah. Huruf besar dan huruf kecil dibedakan karena Lua bersifat *case-sensitive*. Kita dapat menganggap variabel seperti kotak penyimpanan dengan label. Setiap kotak memiliki nama unik yang dapat digunakan untuk mengakses barang berupa **nilai** (nanti kita bahas apa itu nilai) yang disimpan di dalamnya. Sebuah kotak variabel dapat menyimpan berbagai jenis nilai, seperti angka, teks, fungsi, atau bahkan struktur data kompleks seperti tabel. Nama variabel harus mengikuti aturan tertentu, seperti dimulai dengan huruf atau underscore `(_)`, dan karakter setelahnya dapat terdiri dari huruf, angka, dan karakter garis bawah kembali. Penting untuk memperhatikan perbedaan antara huruf besar dan huruf kecil karena Lua memperlakukan keduanya secara berbeda, sehingga "namaVariabel" dan "namavariabel" dianggap sebagai dua variabel yang berbeda.

**Nilai** dalam Lua adalah informasi atau data yang dapat disimpan, dimanipulasi, dan digunakan dalam program. Setiap nilai memiliki jenis atau tipe yang menentukan cara nilai tersebut diinterpretasikan dan dioperasikan. Kita bisa membayangkan nilai sebagai benda atau objek dalam kehidupan sehari-hari. Misalnya, sebuah nilai angka dapat dianggap sebagai suatu jumlah uang yang kita miliki, sedangkan nilai teks dapat dianggap sebagai sebuah buku dengan kata-kata yang tercetak di dalamnya. Seperti halnya kita dapat melakukan operasi matematika pada nilai-nilai angka atau membaca dan memanipulasi teks dalam buku, dalam Lua, kita dapat melakukan operasi dan manipulasi pada nilai-nilai sesuai dengan jenisnya, seperti melakukan perhitungan matematika atau manipulasi teks.

**Deklarasi** dalam Lua mengacu pada proses mendefinisikan dan memberikan nama pada variabel, fungsi, atau tipe data tertentu. Saat melakukan deklarasi, kita memberikan identitas atau label pada elemen yang akan digunakan dalam program. kita dapat membayangkan deklarasi seperti memberi nama pada kotak penyimpanan tadi (variabel). Ketika kita memberikan nama pada kotak, kita dapat dengan mudah mengidentifikasi dan menggunakan isinya saat kita membutuhkannya. Dalam Lua, deklarasi memungkinkan kita untuk merujuk dan menggunakan variabel atau fungsi dengan nama yang telah ditentukan, sehingga mempermudah dalam penggunaan dan manipulasi data dalam suatu program.

#### Contoh Deklarasi Variabel

```lua
local i, j
local i
local a, c
```

Variabel dapat diinisialisasi (diberikan nilai awal) dalam deklarasinya. Inisialisasi terdiri dari tanda sama dengan `(=)` diikuti oleh ekspresi konstan (Nilai tetap).

#### Contoh Inisialisasi Variabel

```lua
local d, f = 5, 10   -- deklarasi d dan f sebagai variabel lokal.
d, f = 5, 10;       -- deklarasi d dan f sebagai variabel global.
d, f = 10           --[[deklarasi d dan f sebagai variabel global.]]
```

### Tipe Data

Lua adalah bahasa yang tipe datanya dinamis tidak harus memiliki tipe ketika proses deklarasi variabel, hanya nilai yang diinisialisasikan ke dalam variabel yang memiliki tipe. Nilai tersebut dapat disimpan dalam variabel, dikirim sebagai parameter, dan dikembalikan sebagai hasil. Dalam Lua, meskipun kita tidak memiliki tipe data variabel, kita memiliki tipe data untuk nilai-nilainya, itulah yang disebut dengang tipe data dinamis, konsep ini juga digunakan pada beberapa scripting language lainnya seperti javascript dan python. 

Berikut adalah beberapa tipe data yang tersedia di Lua:

- **nil**: Digunakan untuk membedakan nilai yang memiliki data atau tidak (nil). Analoginya adalah jika kita membawa sebuah tas, kita bisa melihat apakah tas itu kosong (tidak ada isinya) atau berisi sesuatu.
- **boolean**: Mencakup nilai *true* dan *false*. Biasanya digunakan untuk pemeriksaan kondisi. Analoginya adalah seperti tombol saklar yang bisa berada dalam keadaan "hidup" (true) atau "mati" (false).
- **number**: Mewakili angka riil (titik mengambang presisi ganda). Analoginya adalah seperti angka pada pengukur suhu yang dapat memiliki nilai desimal.
- **string**: Mewakili urutan karakter. Analoginya adalah seperti tali yang terdiri dari kumpulan huruf, angka, atau karakter lainnya.
- **function**: Mewakili metode yang ditulis dalam C atau Lua. Analoginya adalah seperti alat yang melakukan tugas tertentu. Misalnya, sebuah blender adalah fungsi yang dapat digunakan untuk mencampur bahan-bahan makanan.
- **userdata**: Mewakili data C sembarang. Analoginya adalah seperti kotak misterius yang berisi informasi yang hanya bisa dipahami oleh program lain atau bahasa pemrograman lain.
- **thread**: Mewakili alur eksekusi independen dan digunakan untuk mengimplementasikan coroutines. Analoginya adalah seperti memiliki beberapa pekerja yang bekerja secara bersamaan dan bisa berkomunikasi satu sama lain.
- **table**: Mewakili array biasa, tabel simbol, himpunan, catatan, graph, tree, dll., dan mengimplementasikan tabel asosiatif. Tabel dapat menyimpan nilai apa pun (kecuali nil). Analoginya adalah seperti sebuah buku catatan yang dapat berisi berbagai jenis informasi seperti daftar belanja, daftar kontak, atau grafik data.

Contoh kode:

```lua
local value = nil
local isTrue = true
local number = 10.5
local text = "Hello, Lua!"
local function addNumbers(a, b)
  return a + b
end
local userdata = io.open("file.txt", "r")
local thread = coroutine.create(function() print("Hello from coroutine!") end)
local tableData = {1, 2, 3, name = "John", age = 25}

print(value) -- Output: nil
print(isTrue) -- Output: true
print(number) -- Output: 10.5
print(text) -- Output: Hello, Lua!
print(addNumbers(5, 3)) -- Output: 8
print(userdata) -- Output: userdata: 0xXXXXXXXX
print(thread) -- Output: thread: 0xXXXXXXXX
print(tableData[1]) -- Output: 1
print(tableData.name) -- Output: John
```

Dalam contoh kode di atas, kita mendeklarasikan variabel dengan tipe data yang berbeda-beda. kemudian kita mencetak nilai-nilai variabel tersebut menggunakan fungsi print(). Cara membaca contoh kode ini adalah dengan menjalankan program Lua, yang akan mencetak nilai-nilai variabel ke konsol atau output yang sesuai.

### Type Function

Dalam Lua, ada fungsi yang disebut dengan 'type' yang memungkinkan kita mengetahui tipe variabel. Fungsi ini berguna untuk memeriksa tipe data suatu variabel.
(terkait apa itu fungsi, nanti kita jelaskan pada modulnya tersendiri)

Contoh penggunaan fungsi 'type':

```lua
local a = "Hello"
local b = 123
local c = true

print(type(a))   -- Output: string
print(type(b))   -- Output: number
print(type(c))   -- Output: boolean
```

### Pengambilan Keputusan dengan Pernyataan Kondisional

Pengambilan keputusan dengan pernyataan kondisional merupakan bagian penting dalam pemrograman di mana kita perlu membuat keputusan berdasarkan kondisi tertentu. Di Lua, kita dapat menggunakan pernyataan kondisional untuk melakukan hal ini. Pernyataan kondisional memungkinkan program untuk mengevaluasi ekspresi logika, seperti perbandingan antara nilai atau keadaan variabel, dan menjalankan blok kode tertentu jika kondisi tersebut terpenuhi.

Mari kita bayangkan sebuah toko online yang menjual berbagai macam produk. Ketika seorang pelanggan melakukan pembelian, toko perlu memeriksa apakah produk yang diinginkan oleh pelanggan tersedia atau tidak. Jika produk tersebut tersedia, toko akan mengirimkan produk tersebut kepada pelanggan. Namun, jika produk tersebut tidak tersedia, toko akan memberitahu pelanggan bahwa produk tersebut sedang habis. Dalam hal ini, toko melakukan pengambilan keputusan berdasarkan kondisi ketersediaan produk, dan pernyataan kondisional dapat digunakan untuk mengimplementasikan logika ini dalam kode program.

Dengan menggunakan pernyataan kondisional, program dapat membuat keputusan secara dinamis berdasarkan kondisi-kondisi yang diberikan, memungkinkan kontrol alur eksekusi program untuk bervariasi sesuai dengan situasi yang terjadi.

#### Pernyataan If-Else

Pernyataan if-else merupakan salah satu bentuk pernyataan kondisional yang sering digunakan dalam bahasa pemrograman Lua. Pernyataan ini memungkinkan kita untuk membagi alur program menjadi dua cabang berbeda berdasarkan kondisi yang diberikan. Pada dasarnya, pernyataan if-else akan mengevaluasi suatu kondisi, dan jika kondisi tersebut bernilai benar (true), maka blok kode yang terkait dengan pernyataan if akan dieksekusi. Namun, jika kondisi tersebut bernilai salah (false), maka blok kode yang terkait dengan pernyataan else akan dieksekusi.

Misalnya, kita bisa menggunakan analogi sebuah pintu dengan kunci. Jika kita memiliki kunci yang sesuai (kondisi benar), maka kita dapat membuka pintu (eksekusi blok kode if). Namun, jika kunci tidak sesuai (kondisi salah), maka pintu tetap tertutup dan kita harus mencari jalur alternatif (eksekusi blok kode else).

Berikut adalah contoh kode menggunakan pernyataan if-else:

```lua
local x = 10

if x > 0 then
    print("Nilai x adalah positif")
else
    print("Nilai x adalah negatif atau nol")
end
```

Penjelasan:
- Baris pertama mendeklarasikan variabel `x` dengan nilai 10.
- Pada baris kedua, terdapat pernyataan if dengan kondisi `x > 0`, yang berarti kita akan mengecek apakah `x` lebih besar dari 0.
- Jika kondisi tersebut bernilai benar, maka pernyataan if dieksekusi, dan baris ketiga ("Nilai x adalah positif") akan dicetak.
- Namun, jika kondisi tersebut bernilai salah, maka pernyataan else dieksekusi, dan baris kelima ("Nilai x adalah negatif atau nol") akan dicetak.
- Akhir blok pernyataan if-else ditandai dengan kata kunci `end`, yang menandakan akhir dari blok kode yang terkait dengan pernyataan if-else.

Dalam contoh ini, karena `x` memiliki nilai 10, yang lebih besar dari 0, maka kondisi pada pernyataan if (`x > 0`) bernilai benar. Oleh karena itu, output yang akan dicetak adalah "Nilai x adalah positif".

#### Pernyataan If Bersarang

Pernyataan if bersarang adalah konstruksi dalam bahasa pemrograman Lua yang memungkinkan kita untuk menyusun beberapa pernyataan if di dalam pernyataan if lainnya. Ini memungkinkan kita untuk membuat pengecekan kondisi yang lebih kompleks dan mengambil keputusan berdasarkan kombinasi dari beberapa kondisi yang berbeda.

Bayangkan kita sedang membuat program untuk memeriksa kelayakan seseorang untuk mendapatkan pinjaman. Pertama, kita ingin memeriksa apakah seseorang memiliki pendapatan yang memadai. Jika ya, kita akan lanjutkan ke langkah berikutnya dan memeriksa kembali apakah mereka memiliki catatan kredit yang baik atau tidak. Jika kedua kondisi ini terpenuhi, kita akan memberikan persetujuan pinjaman. Namun, jika salah satu atau kedua kondisi tidak terpenuhi, maka pinjaman akan ditolak.

meskipun saya sarankan jangan terbiasa pinjam-meminjam, lebih baik menabung agar tidak meminjam kepada orang lain, hatipun lebih tenang karna tidak merasa dikejar-kejar penagih hutang. (sekedar intermezo, tolong jangan dimasukan ke hati)

Berikut adalah contoh kode yang mengilustrasikan penggunaan pernyataan if bersarang dalam Lua:

```lua
local pendapatan = 5000
local catatan_kredit = "baik"

if pendapatan >= 4000 then
  if catatan_kredit == "baik" then
    print("Pinjaman disetujui")
  else
    print("Catatan kredit tidak memadai")
  end
else
  print("Pendapatan tidak mencukupi")
end
```

Cara membaca kode di atas adalah sebagai berikut: Jika pendapatan lebih besar atau sama dengan 4000, maka kita akan memeriksa kondisi berikutnya. Jika catatan kredit adalah "baik", maka pesan "Pinjaman disetujui" akan dicetak. Jika catatan kredit tidak memenuhi syarat, maka pesan "Catatan kredit tidak memadai" akan dicetak. Jika pendapatan kurang dari 4000, maka pesan "Pendapatan tidak mencukupi" akan dicetak.

Penggunaan pernyataan if bersarang memungkinkan kita untuk membuat alur logika yang lebih kompleks dan membuat keputusan berdasarkan kombinasi dari beberapa kondisi.
Ini adalah beberapa konsep dasar pemrograman Lua yang perlu kita ketahui. Dengan pemahaman ini, kita dapat memulai membangun program Lua yang lebih kompleks dan fungsional.
_02_penyimpanan_dan_perhitungan_dasar_lua.md

<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/80x15.png" /></a>
###### <em><span xmlns:dct="http://purl.org/dc/terms/" href="http://purl.org/dc/dcmitype/Text" property="dct:title" rel="dct:type">_02_penyimpanan_dan_perhitungan_dasar_lua.md</span> by <a xmlns:cc="http://creativecommons.org/ns#" href="https://github.com/muchamadyja" property="cc:attributionName" rel="cc:attributionURL">Gillar Ajie Prasatya</a> is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a>.<br />Based on a work at <a xmlns:dct="http://purl.org/dc/terms/" href="https://github.com/muchamadyja/progstudymaterials/blob/main/lua_study_origin/_02_penyimpanan_dan_perhitungan_dasar_lua.md" rel="dct:source">github.com/muchamadyja/progstudymaterials</a>.</em>
###### [<em>click here for the license file</em>](https://github.com/muchamadyja/progstudymaterials/blob/main/LICENSE)
