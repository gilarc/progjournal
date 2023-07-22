# Array

Bayangkan Anda memiliki sebuah wadah penyimpanan telur, seperti wadah penyimpanan telur biasa. Wadah ini diciptakan agar telur dapat disimpan dengan rapi dan teratur tanpa risiko pecah. Wadah tersebut memiliki beberapa bagian terpisah yang memungkinkan Anda menyimpan beberapa telur sekaligus. Jadi, Anda tidak perlu memiliki wadah terpisah untuk setiap telur, melainkan satu wadah yang cukup untuk menyimpan banyak telur.

Hal ini juga berlaku dalam dunia pemrograman. Misalkan Anda memiliki sebuah kelas dengan hampir 40 siswa, dan Anda perlu menyimpan nama-nama mereka dalam komputer menggunakan bahasa pemrograman Lua. Pendekatan awal adalah dengan membuat 40 variabel String seperti nama1, nama2,... hingga nama40 untuk menyimpan nilai nama-nama siswa.

Namun, apakah ada cara yang lebih baik untuk mengatasi masalah ini? Bayangkan jika kita punya wadah mirip wadah telur, yang dapat menyimpan banyak hal dengan jenis yang sama, seperti menyimpan banyak nilai dalam urutan tertentu, mirip dengan cara kita menyusun telur dalam wadah.

Dan itulah mengapa kita memiliki fitur yang disebut "Array" (larik) dalam pemrograman! Ini adalah struktur data yang menarik yang memungkinkan kita menyimpan sejumlah nilai dalam satu wadah. Konsep ini sangat menarik, bukan? Mari kita lanjutkan dan jelajahi lebih dalam tentang Array.

## Pengertian Array

Dalam pemrograman, Array adalah susunan teratur dari objek atau nilai. Anda bisa membayangkan Array sebagai deretan kotak yang dapat berisi nilai-nilai berbeda, seperti bilangan, teks, atau objek lainnya. Anda dapat menyimpan sejumlah nilai dalam satu Array, dan kemudian mengakses nilai-nilai tersebut berdasarkan posisi mereka dalam Array.

Tentu saja, Array ini bisa berupa array satu dimensi yang mirip dengan deretan kotak satu baris, atau array multi-dimensi yang mirip dengan kotak-kotak berbaris dan bertumpuk. Dalam bahasa pemrograman Lua, Array diimplementasikan menggunakan tabel dengan indeks berupa bilangan bulat. Hal menarik tentang Array adalah ukurannya bisa berubah sesuai dengan kebutuhan kita, namun tentu saja tergantung pada ketersediaan memori.

## Array Satu Dimensi

Mari kita mulai dengan mempelajari tentang Array Satu Dimensi. Bayangkan array ini seperti rak penyimpanan yang hanya memiliki satu baris untuk menyimpan beberapa item secara berurutan. Setiap item di dalamnya memiliki nomor urut atau indeks yang membedakannya.

Dalam bahasa pemrograman Lua, kita dapat merepresentasikan array satu dimensi menggunakan struktur tabel sederhana. Pertama, kita perlu menginisialisasi array tersebut, artinya menentukan berapa banyak elemen atau slot yang kita butuhkan. Kemudian, kita bisa membaca nilai-nilai di dalam array tersebut menggunakan loop for sederhana.

Sebagai analogi, bayangkan Anda memiliki sebuah kotak yang memiliki 10 ruang, dan Anda ingin menyimpan 10 buah bola di dalamnya. Setiap bola diberi nomor 1 hingga 10 berdasarkan posisinya di dalam kotak. Kotak ini mirip dengan array satu dimensi, dan nomor di setiap bola adalah indeksnya.

### Contoh Kode 1: Menginisialisasi dan Membaca Array Satu Dimensi

```lua
-- Inisialisasi array satu dimensi dengan 5 elemen
local myArray = {10, 20, 30, 40, 50}

-- Membaca nilai-nilai di dalam array menggunakan loop for
for i = 1, #myArray do
    print(myArray[i]) -- Output: 10 20 30 40 50
end
```

Pada contoh kode di atas, kita membuat sebuah array dengan 5 elemen (10, 20, 30, 40, dan 50). Kemudian, kita menggunakan loop for untuk membaca nilai-nilai di dalam array tersebut dan mencetaknya ke layar.

### Contoh Kode 2: Mengakses Elemen di Luar Ukuran Array

```lua
-- Inisialisasi array satu dimensi dengan 3 elemen
local myArray = {100, 200, 300}

-- Mencoba mengakses elemen di luar ukuran array
local value = myArray[4]

-- Cetak nilai yang diperoleh
print(value) -- Output: nil
```

Dalam contoh kode ini, kita membuat sebuah array dengan 3 elemen (100, 200, dan 300). Kemudian, kita mencoba mengakses elemen ke-4 yang sebenarnya tidak ada di dalam array. Ketika kita mencoba mengakses elemen yang tidak ada, Lua akan mengembalikan nilai nil.

### Contoh Kode 3: Membuat Objek pada Indeks 0 dan di Bawah 0

```lua
-- Inisialisasi array dengan objek pada indeks 0 dan -1
local myArray = {[0] = "A", [-1] = "B", "C", "D"}

-- Mencetak nilai pada indeks 0 dan -1
print(myArray[0]) -- Output: A
print(myArray[-1]) -- Output: B

-- Mencetak nilai pada indeks 1 dan 2
print(myArray[1]) -- Output: C
print(myArray[2]) -- Output: D
```

Dalam contoh ini, kita membuat array dengan objek pada indeks 0 dan -1, serta dua objek lainnya pada indeks 1 dan 2. Meskipun indeks umumnya dimulai dari 1 di Lua, kita dapat dengan mudah membuat objek pada indeks 0 dan di bawah 0 jika diperlukan.

## Array Multi-Dimensi

Array Multi-Dimensi adalah susunan data yang lebih kompleks dibandingkan dengan array satu dimensi. Array ini dapat diimplementasikan dengan dua cara berbeda:

1. Array dari Array: Adalah struktur data di mana sebuah array dapat menyimpan elemen-elemen berupa array lain sebagai elemen-elemennya. Dalam hal ini, kita memiliki array utama yang berperan sebagai wadah,

 dan setiap elemen array utama dapat berupa array kecil yang masing-masing menyimpan beberapa elemen. Dengan pendekatan ini, kita dapat mengorganisir data dalam dua tingkat indeks, yaitu indeks array utama untuk mengakses array kecil, dan indeks array kecil untuk mengakses elemen-elemen di dalamnya. Penggunaan array dari array memungkinkan representasi struktur data yang lebih kompleks dan lebih efisien dalam menyimpan dan mengakses data dengan lebih terorganisir. Analoginya, bayangkan Anda memiliki sebuah buku besar yang berisi banyak bab. Setiap bab itu sendiri adalah array berisi beberapa elemen. Dengan cara ini, kita memiliki dua tingkat indeks, satu untuk buku besar (array utama) dan satu lagi untuk bab (array dalam).

2. Array Satu Dimensi dengan Memanipulasi Indeks: Array satu dimensi dengan memanipulasi indeks adalah bentuk struktur data di mana elemen-elemen data disusun dalam satu dimensi linier, dan setiap elemen dapat diakses melalui indeks yang ditentukan secara manual. Biasanya, indeks dimulai dari angka 1 dan berlanjut secara berurutan, namun dalam pendekatan ini, kita dapat mengatur indeks sesuai kebutuhan tanpa harus mengikuti urutan angka. Misalnya, kita dapat membuat sebuah array dengan indeks 100, 200, dan 300, lalu menyimpan nilai-nilai di posisi indeks yang tepat. Pendekatan ini memungkinkan fleksibilitas dalam mengelompokkan dan mengatur data tanpa harus mengikuti konvensi indeks standar. Dengan cara ini, kita dapat memanfaatkan struktur array satu dimensi untuk berbagai keperluan, seperti menyimpan data dalam kelompok-kelompok khusus, mengatasi data yang jarang muncul, atau melakukan representasi data dalam format tertentu. Analoginya, bayangkan Anda memiliki sebidang tanah dengan petak-petak tertentu. Meskipun Anda hanya memiliki satu dimensi untuk menandai petak-petak tersebut, Anda dapat mengatur dan mengelompokkan data berdasarkan indeks yang sesuai dengan kebutuhan.

### Contoh 1: Array dari Array

```lua
-- Array utama (array besar) berisi array-array kecil (bab)
local arrayUtama = {
    {1, 2, 3},
    {2, 4, 6},
    {3, 6, 9}
}

-- Mengakses elemen array menggunakan indeks
print(arrayUtama[1][1]) -- Output: 1
print(arrayUtama[2][3]) -- Output: 6
print(arrayUtama[3][2]) -- Output: 6
```

Pada contoh pertama, kita memiliki array utama yang berisi tiga array kecil (bab) di dalamnya. Setiap array kecil memiliki tiga elemen. Untuk mengakses elemen-elemen ini, kita menggunakan dua tingkat indeks: indeks pertama untuk array utama dan indeks kedua untuk array kecil (bab) di dalamnya.

### Contoh 2: Array Satu Dimensi dengan Memanipulasi Indeks

```lua
-- Array satu dimensi dengan indeks termanipulasi
local arraySatuDimensi = {}
arraySatuDimensi[1] = 1
arraySatuDimensi[2] = 2
arraySatuDimensi[3] = 3
arraySatuDimensi[4] = 2
arraySatuDimensi[5] = 4
arraySatuDimensi[6] = 6
arraySatuDimensi[7] = 3
arraySatuDimensi[8] = 6
arraySatuDimensi[9] = 9

-- Mengakses elemen array menggunakan indeks
print(arraySatuDimensi[1]) -- Output: 1
print(arraySatuDimensi[5]) -- Output: 4
print(arraySatuDimensi[9]) -- Output: 9
```

Pada contoh kedua, kita memiliki array satu dimensi yang berisi sembilan elemen. Kita menggunakan indeks untuk menentukan posisi setiap elemen dalam array tersebut. Meskipun indeks ini berjalan secara berurutan dari 1 hingga 9, kita dapat dengan mudah mengatur dan mengelompokkan data sesuai kebutuhan.

### Contoh 3: Array Multi-Dimensi untuk Representasi Matriks

```lua
-- Array multi-dimensi untuk matriks 2x3
local matriks = {
    {1, 2, 3},
    {4, 5, 6}
}

-- Mengakses elemen array menggunakan indeks
print(matriks[1][2]) -- Output: 2
print(matriks[2][3]) -- Output: 6
```

Pada contoh ketiga, kita menggunakan array multi-dimensi untuk mewakili matriks 2x3. Matriks ini memiliki dua baris dan tiga kolom. Dengan menggunakan indeks, kita dapat dengan mudah mengakses elemen-elemen di dalam matriks sesuai dengan posisinya.

## Iterator

Iterator adalah sebuah konstruksi yang memungkinkan kita untuk melakukan penjelajahan terhadap elemen-elemen dalam suatu koleksi atau wadah data. Untuk memberikan gambaran, kita bisa membayangkan koleksi sebagai sejenis tempat penyimpanan yang berisi banyak objek. Kita ingin dapat mengunjungi setiap objek dalam koleksi tersebut satu per satu untuk melakukan operasi atau manipulasi data yang diperlukan.

Di dalam bahasa pemrograman Lua, koleksi tersebut sering kali diwakili oleh tabel (table), yang merupakan struktur data yang serbaguna untuk menyimpan kumpulan nilai-nilai. Analoginya, kita bisa membayangkan tabel sebagai sebuah laci dengan banyak laci-laci kecil tambahan / sekat-sekat pemisah membentuk kota-kota kecil untuk menyimpan sesuatu di dalamnya, di mana setiap laci kecil / ruas sekat tersebut berisi sebuah nilai.

Sebagai contoh sederhana, kita akan menggunakan fungsi iterator bawaan Lua yang bernama `ipairs`. Fungsi ini memberikan pasangan kunci (indeks) dan nilai (elemen) dari setiap elemen dalam tabel. Kita bisa membayangkan bahwa iterator ini berfungsi seperti seorang penunjuk yang mengarahkan kita pada setiap laci kecil dalam tabel untuk melihat isinya.

```lua
--

 Contoh penggunaan iterator ipairs pada tabel
local fruits = {"apel", "pisang", "jeruk"}

for index, value in ipairs(fruits) do
    print(index, value)
end
```

Hasil dari program di atas akan menjadi:

```
1	apel
2	pisang
3	jeruk
```

Kita bisa melihat bahwa iterator `ipairs` membantu kita untuk mengunjungi setiap elemen dalam tabel `fruits` secara berurutan, mengembalikan indeks dan nilainya.

Dalam Lua, ada dua jenis utama iterator berdasarkan cara mereka mengelola status saat melakukan iterasi:

1. Stateless Iterators (Iterator Tanpa Status): Iterator ini tidak menyimpan informasi tentang posisi saat melakukan iterasi. Setiap kali fungsi iterator dipanggil, ia hanya mengembalikan elemen berikutnya tanpa menyimpan riwayatnya. Analoginya, kita bisa membayangkan bahwa ketika kita mengunjungi sekumpulan buah dalam keranjang dan melihat satu per satu, kita tidak tahu apakah buah yang telah kita lihat sebelumnya atau belum.

```lua
-- Contoh penggunaan stateless iterator
function statelessIterator(collection)
    local index = 1

    return function()
        local value = collection[index]
        index = index + 1
        return value
    end
end

local fruits = {"apel", "pisang", "jeruk"}

for fruit in statelessIterator(fruits) do
    print(fruit)
end
```

Hasil dari program di atas akan menjadi:

```
apel
pisang
jeruk
```

Pada contoh di atas, fungsi `statelessIterator` mengembalikan sebuah fungsi (closure) yang bertanggung jawab untuk mengatur indeks dan mengembalikan elemen dari tabel `fruits` satu per satu.

2. Stateful Iterators (Iterator dengan Status): Iterator ini menyimpan status saat melakukan iterasi, sehingga bisa mengingat posisi terakhir yang telah dilewati dan melanjutkan dari posisi tersebut saat dipanggil kembali. Analoginya, kita bisa membayangkan seorang pemandu wisata yang mengingat tempat terakhir yang telah dikunjungi oleh grup wisatawan dan mengarahkan mereka ke tempat berikutnya.

```lua
-- Contoh penggunaan stateful iterator
function statefulIterator(collection)
    local index = 1

    return function()
        if index <= #collection then
            local value = collection[index]
            index = index + 1
            return value
        end
    end
end

local fruits = {"apel", "pisang", "jeruk"}

local iterator = statefulIterator(fruits)
print(iterator())  -- Output: apel
print(iterator())  -- Output: pisang
print(iterator())  -- Output: jeruk
```

Pada contoh di atas, fungsi `statefulIterator` juga mengembalikan sebuah fungsi (closure) yang mengelola indeks dan mengembalikan elemen dari tabel `fruits`, namun fungsi ini mengingat indeks terakhir yang telah diproses dan melanjutkan dari indeks tersebut ketika dipanggil kembali.

Dengan pemahaman tentang iterator dan beberapa jenisnya, kita dapat membuat iterasi atau penjelajahan yang lebih fleksibel dan sesuai dengan kebutuhan dalam pemrograman Lua.

<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/80x15.png" /></a>
###### <em><span xmlns:dct="http://purl.org/dc/terms/" href="http://purl.org/dc/dcmitype/Text" property="dct:title" rel="dct:type">_05_array_dan_iterators.md</span> by <a xmlns:cc="http://creativecommons.org/ns#" href="https://github.com/muchamadyja" property="cc:attributionName" rel="cc:attributionURL">Gillar Ajie Prasatya</a> is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a>.<br />Based on a work at <a xmlns:dct="http://purl.org/dc/terms/" href="https://github.com/muchamadyja/progjournal/tree/main/lua_origin" rel="dct:source">github.com/muchamadyja/progjournal</a>.</em>
###### [<em>click here for the license file</em>](https://github.com/muchamadyja/progjournal/blob/main/LICENSE)
