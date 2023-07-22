# Pengenalan File I/O (Input/Output) di Lua

Pustaka I/O (Input/Output) digunakan untuk membaca dan memanipulasi berkas (file) di dalam bahasa pemrograman Lua. Analoginya, Anda bisa membayangkan pustaka I/O ini sebagai alat yang membantu Anda berinteraksi dengan berkas, seperti membaca data dari berkas atau menulis data ke dalam berkas.

Ada dua jenis operasi berkas di Lua:

1. **Implicit file descriptors**:

Implicit file descriptors / Deskriptor berkas implisit merujuk pada penggunaan standar masukan dan keluaran dalam operasi berkas. Dalam pemrograman, kita sering kali perlu membaca data dari berkas atau menulis data ke dalam berkas. Salah satu cara untuk melakukan ini adalah dengan menggunakan deskriptor berkas.

Sebagai analogi, bayangkan Anda sedang bermain permainan papan. Anda memiliki papan permainan di depan Anda dan beberapa kartu dengan instruksi. Papan permainan itu adalah standar masukan, karena dari papan permainan Anda mendapatkan informasi tentang apa yang harus Anda lakukan selanjutnya. Kartu-kartu instruksi yang Anda ambil dari tumpukan dan letakkan di papan adalah seperti operasi berkas implisit. Anda mengambil instruksi dari kartu dan melakukan aksi yang sesuai berdasarkan instruksi itu.

Dalam pemrograman, standar masukan (input) dan standar keluaran (output) adalah "papan permainan" yang digunakan untuk berkomunikasi dengan program. Deskriptor berkas implisit adalah cara kita menggunakan kartu-kartu instruksi untuk membaca atau menulis data ke dalam berkas. Jadi, ketika kita berbicara tentang deskriptor berkas implisit, kita mengacu pada cara program berinteraksi dengan berkas menggunakan standar masukan dan keluaran.

2. **Explicit file descriptors**:

Explicit file descriptors / Deskriptor berkas eksplisit adalah suatu mekanisme dalam pemrograman di mana operasi berkas menggunakan deskriptor berkas yang diberikan secara eksplisit oleh pengguna. Deskriptor berkas merupakan suatu bilangan bulat yang digunakan oleh sistem operasi untuk mengidentifikasi berkas yang sedang dioperasikan.

Dalam analogi sederhana, kita bisa membayangkan deskriptor berkas sebagai nomor meja di sebuah restoran. Saat Anda memesan makanan atau minuman, Anda diberikan nomor meja sebagai identifikasi unik untuk meja Anda. Ketika makanan atau minuman Anda siap, pelayan dapat mengantarkannya ke meja Anda berdasarkan nomor meja yang Anda miliki. Dengan cara yang serupa, deskriptor berkas membantu sistem operasi menemukan dan mengoperasikan berkas yang sesuai dengan operasi yang diinginkan oleh pengguna.

Pengguna harus secara eksplisit menyediakan deskriptor berkas saat melakukan operasi seperti membuka, menulis, membaca, atau menutup berkas. Hal ini memberikan tingkat kontrol yang lebih tinggi kepada pengguna karena mereka secara langsung menentukan berkas mana yang akan dioperasikan oleh sistem.

Dalam implementasi deskriptor berkas eksplisit, pengguna harus memahami dan mengelola deskriptor berkas dengan cermat. Kesalahan dalam penggunaan deskriptor berkas bisa menyebabkan masalah seperti kebocoran memori atau penggunaan berkas yang tidak tepat. Oleh karena itu, pemrogram perlu berhati-hati dan teliti dalam mengelola deskriptor berkas agar aplikasi berjalan dengan baik dan aman.

Untuk penggunaan sehari-hari, kita mungkin lebih sering berinteraksi dengan implicit file descriptors karena itu lebih sederhana dan umum digunakan. Namun, ada situasi tertentu di mana explicit file descriptors lebih berguna dan memungkinkan Anda untuk melakukan operasi berkas yang lebih kompleks.

## Deskriptor Berkas Implisit

Deskriptor berkas implisit digunakan untuk menggunakan mode standar masukan/keluaran atau hanya satu berkas masukan dan satu berkas keluaran. Ketika program dijalankan, Anda akan mendapatkan keluaran berupa baris pertama dari berkas `test.lua`.

Contoh kode 1:

```lua
file = io.open("test.lua", "r")
print(file:read("*line"))
file:close()
```

Output:

```
-- Ini adalah contoh isi berkas test.lua
```

Penjelasan contoh kode 1:
- Pada contoh kode ini, kita membuka berkas `test.lua` dalam mode baca `"r"`.
- Fungsi `file:read("*line")` digunakan untuk membaca satu baris dari berkas tersebut.
- Hasil pembacaan baris pertama berkas akan dicetak menggunakan fungsi `print`.
- Terakhir, kita menutup berkas menggunakan `file:close()`.

Contoh kode 2:

```lua
file = io.open("data.txt", "w")
file:write("Halo, dunia!\n")
file:write("Ini adalah contoh isi berkas.")
file:close()
```

Output (data.txt):

```
Halo, dunia!
Ini adalah contoh isi berkas.
```

Penjelasan contoh kode 2:
- Pada contoh ini, kita membuka berkas `data.txt` dalam mode tulis `"w"`.
- Menggunakan fungsi `file:write()`, kita menuliskan dua baris teks ke dalam berkas.
- Setelah selesai menulis, kita menutup berkas menggunakan `file:close()`.

Contoh kode 3:

```lua
file = io.open("data.txt", "a")
file:write("\nTambahan isi berkas.")
file:close()
```

Output (data.txt setelah kode 3 dijalankan):

```
Halo, dunia!
Ini adalah contoh isi berkas.
Tambahan isi berkas.
```

Penjelasan contoh kode 3:
- Pada contoh ini, kita membuka berkas `data.txt` dalam mode tambah `"a"`.
- Menggunakan fungsi `file:write()`, kita menambahkan satu baris teks ke dalam berkas.
- Setelah selesai menulis, kita menutup berkas menggunakan `file:close()`.

Selain itu, semua mode pembukaan berkas dan parameter baca untuk deskriptor eksternal sama dengan deskriptor berkas implisit. Dengan kata lain, cara membuka, membaca, menulis, dan menutup berkas dalam contoh kode di atas juga dapat diterapkan pada berkas-berkas lainnya.

## Deskriptor Berkas Eksplisit

Deskriptor berkas eksplisit adalah ketika kita secara eksplisit menyatakan dan mengendalikan deskriptor berkas menggunakan variabel terpisah. Dalam hal ini, kita harus menyatakan deskriptor berkas secara eksplisit dan mengatur operasi pada deskriptor tersebut.

Contoh kode 1:

```lua
local file = io.open("test.lua", "r")
local content = file:read("*line")
print(content)
file:close()
```

Output:

```
-- Ini adalah contoh isi berkas test.lua
```

Penjelasan contoh kode 1:
- Pada contoh kode ini, kita mendeklarasikan variabel `file` sebagai deskriptor berkas `io.open("test.lua", "r")` untuk membuka berkas `test.lua` dalam mode baca.
- Kemudian, kita membaca satu baris dari berkas tersebut menggunakan `file:read("*line")` dan menyimpannya di variabel `content`.
- Hasil pembacaan baris pertama berkas akan dicetak menggunakan fungsi `print`.
- Terakhir, kita menutup berkas menggunakan `file:close()`.

Contoh kode 2:

```lua
local file = io.open("data.txt", "w")
file:write("Halo, dunia!\n")
file:write("Ini adalah contoh isi berkas.")
file:close()
```

Output (data.txt):

```
Halo, dunia!
Ini adalah contoh isi berkas.
```

Penjelasan contoh kode 2:
- Pada contoh ini, kita mendeklarasikan variabel `file` sebagai deskriptor berkas `io.open("data.txt", "w")` untuk membuka berkas `data.txt` dalam mode tulis.
- Menggunakan fungsi `file:write()`, kita menuliskan dua baris teks ke dalam berkas.
- Setelah selesai menulis, kita menutup berkas menggunakan `file:close()`.

Contoh kode 3:

```lua
local file = io.open("data.txt", "a")
file:write("\nTambahan isi berkas.")
file:close()
```

Output (data.txt setelah kode 3 dijalankan):

```
Halo, dunia!
Ini adalah contoh isi berkas.
Tambahan isi berkas.
```

Penjelasan contoh kode 3:
- Pada contoh ini, kita mendeklarasikan variabel `file` sebagai deskriptor berkas `io.open("data.txt", "a")` untuk membuka berkas `data.txt` dalam mode tambah.
- Menggunakan fungsi `file:write()`, kita menambahkan satu baris teks ke dalam berkas.
- Setelah selesai menulis, kita menutup berkas menggunakan `file:close()`.

Dengan menggunakan deskriptor berkas eksplisit, kita lebih mengontrol dan menyatakan variabel-variabel untuk mengelola berkas secara terpisah. Ini memberi fleksibilitas lebih dalam operasi berkas dan memudahkan dalam manipulasi data dari berkas yang berbeda.

## Metode Berkas Umum Lainnya

Selain dari metode-metode yang sudah dijelaskan sebelumnya, ada beberapa metode umum lainnya yang digunakan dalam manipulasi berkas, yaitu:

1. `file:seek(pilihan whence, opsi offset)`: Metode ini digunakan untuk mengatur posisi penunjuk berkas. Parameter `whence` bisa berisi nilai "set", "cur", atau "end". Jika `whence` adalah "set", maka `offset` menentukan posisi baru berkas dari awal berkas. Jika `whence` adalah "cur", maka `offset` menentukan perpindahan relatif dari posisi saat ini dalam berkas. Dan jika `whence` adalah "end", maka `offset` menentukan perpindahan relatif dari akhir berkas. Jika tidak ada nilai yang diberikan untuk kedua argumen ini, maka posisi berkas saat ini akan diperoleh. Misalnya:
   
   ```lua
   -- Mengatur posisi berkas ke 10 byte dari awal berkas
   file:seek("set", 10)
   ```

2. `file:flush()`: Metode ini digunakan untuk mengosongkan buffer keluaran berkas. Buffer adalah area temporary yang digunakan untuk menampung data sebelum ditulis ke berkas secara fisik. Dengan menggunakan `file:flush()`, data dalam buffer akan ditulis ke berkas secara paksa sehingga data dalam berkas menjadi konsisten dengan data dalam buffer. Misalnya:

   ```lua
   file:write("Hello, World!") -- Data akan tersimpan dalam buffer
   file:flush() -- Data akan ditulis ke berkas secara fisik
   ```

3. `io.lines(opsional nama berkas)`: Metode ini menyediakan iterator loop generik yang memungkinkan kita untuk mengakses berkas baris per baris. Iterator ini akan menutup berkas secara otomatis setelah seluruh berkas telah dijelajahi. Misalnya:

   ```lua
   for line in io.lines("data.txt") do
       print(line) -- Mencetak setiap baris pada berkas "data.txt"
   end
   ```

Tentu, berikut adalah beberapa metode umum lainnya yang digunakan dalam manipulasi berkas di Lua:

4. `file:write(...)`: Metode ini digunakan untuk menulis data ke dalam berkas. Kita dapat menyediakan satu atau lebih argumen data yang akan ditulis ke berkas. Misalnya:

   ```lua
   file:write("Hello, ", "World!") -- Menulis "Hello, World!" ke dalam berkas
   ```

5. `file:read(opsional format, ...)`: Metode ini digunakan untuk membaca data dari berkas. Parameter `format` berfungsi untuk menentukan format bacaan, seperti "*n" untuk membaca angka, "*a" untuk membaca seluruh isi berkas, atau "*l" untuk membaca baris per baris. Jika tidak ada `format` yang diberikan, metode ini akan membaca seluruh isi berkas. Misalnya:

   ```lua
   local number = file:read("*n") -- Membaca angka dari berkas
   local line = file:read("*l") -- Membaca baris pertama dari berkas
   ```

6. `file:close()`: Metode ini digunakan untuk menutup berkas setelah selesai melakukan operasi pembacaan atau penulisan. Menutup berkas sangat penting untuk memastikan bahwa sumber daya sistem tidak terbuang sia-sia. Misalnya:

   ```lua
   file:close() -- Menutup berkas setelah selesai membaca atau menulis
   ```

7. `file:lines(opsional format)`: Metode ini mengembalikan iterator untuk membaca berkas baris per baris. Jika `format` diberikan (misalnya, "*n" atau "*a"), maka metode ini akan membaca berkas dengan format tertentu. Misalnya:

   ```lua
   for line in file:lines("*l") do
       print(line) -- Mencetak setiap baris pada berkas menggunakan iterator
   end
   ```

8. `io.open(nama berkas, mode)`: Fungsi ini digunakan untuk membuka berkas dalam mode tertentu. Mode dapat berisi kombinasi huruf "r" (baca), "w" (tulis), "a" (tulis dengan mode tambahan), "b" (mode biner), dan "+" (untuk membaca dan menulis). Misalnya:

   ```lua
   local file = io.open("data.txt", "r") -- Membuka berkas "data.txt" dalam mode baca
   ```

9. `io.input(opsional nama berkas)`: Fungsi ini digunakan untuk mengubah aliran masukan saat membaca berkas. Jika tidak ada `nama berkas` yang diberikan, maka fungsi ini akan menggunakan masukan standar (stdin). Misalnya:

   ```lua
   io.input("input.txt") -- Mengubah aliran masukan ke berkas "input.txt"
   ```

10. `io.output(opsional nama berkas)`: Fungsi ini digunakan untuk mengubah aliran keluaran saat menulis ke berkas. Jika tidak ada `nama berkas` yang diberikan, maka fungsi ini akan menggunakan keluaran standar (stdout). Misalnya:

    ```lua
    io.output("output.txt") -- Mengubah aliran keluaran ke berkas "output.txt"
    ```

Semakin banyak metode yang Kita kuasai, semakin luas pula kemampuan Anda dalam memanipulasi berkas dalam bahasa pemrograman Lua.


# Penanganan Kesalahan (Error Handling) di Lua

Penanganan kesalahan (error handling) adalah cara program menghadapi situasi yang tidak normal atau anomali saat program dijalankan. Analoginya, kita bisa membayangkan penanganan kesalahan seperti cara kita menghadapi situasi tak terduga dalam kehidupan sehari-hari. Misalnya, saat kita sedang mengendarai mobil menuju suatu tempat, tiba-tiba ban mobil kita bocor. Itu adalah sebuah kesalahan atau kondisi yang tidak normal dalam perjalanan kita. Sebagai pengemudi yang bijak, kita perlu tahu bagaimana menangani situasi tersebut dengan aman dan mengambil tindakan yang tepat.

Di dalam pemrograman Lua, ada dua jenis kesalahan:

1. **Sinkron**: Kesalahan sinkron terjadi di dalam jalannya program secara langsung. Misalnya, jika program mencoba untuk membagi sebuah angka dengan nol, ini akan menyebabkan kesalahan sinkron karena pembagian dengan nol tidak diperbolehkan dalam matematika.
2. **Asinkron**: Kesalahan asinkron terjadi di luar kendali program dan seringkali disebabkan oleh faktor eksternal seperti kegagalan perangkat keras atau masalah jaringan.

Contoh kesalahan yang sederhana adalah ketika Anda mencoba membaca file dari disk, tetapi file tersebut tidak ada atau tidak dapat diakses karena beberapa alasan. Ketika program menghadapi situasi seperti itu, maka kita memerlukan mekanisme untuk menangani kesalahan tersebut agar program bisa tetap berjalan dengan baik dan tidak berhenti begitu saja.

Penanganan kesalahan sangat penting dalam pemrograman di dunia nyata. Ketika kita berurusan dengan operasi-operasi kompleks seperti membaca atau menulis berkas, melakukan transaksi pada database, atau melakukan panggilan ke layanan web, selalu ada kemungkinan terjadi kesalahan. Oleh karena itu, kita perlu memahami bagaimana menangani kesalahan ini dengan cara yang baik dan aman, sehingga program kita tetap dapat berjalan dengan lancar meskipun terjadi situasi tak terduga.

Kesalahan dalam pemrograman dapat terjadi dalam dua jenis:

1. **Kesalahan Sintaksis**:

Jenis kesalahan ini terjadi karena penggunaan komponen program yang salah, seperti operator dan ekspresi. Analoginya, bayangkan Anda berbicara dengan teman menggunakan bahasa yang tidak benar atau tidak dimengerti oleh teman Anda. Contohnya, salah menggunakan tanda "sama dengan" tunggal atau ganda dapat menyebabkan kesalahan. Sebagai contoh kode:

   ```lua
   -- Kesalahan sintaksis, menggunakan tanda "sama dengan" ganda secara salah
   local x = 5
   if x == 5 then
     print("Nilai x adalah 5")
   end
   ```

   Output:
   ```
   [tidak ada output]
   ```
   Penjelasan: Kode di atas mengalami kesalahan sintaksis karena operator perbandingan "==" digunakan secara ganda. Padahal, dalam Lua, untuk perbandingan, kita harus menggunakan operator "==" hanya satu kali.

Contoh Kode ke 2:
```lua
-- Kesalahan sinkron, mencoba membagi angka dengan nol
local a = 10
local b = 0
local result = a / b
print(result)
```

Output:
```
lua: example.lua:3: attempt to perform arithmetic on a nil value (global 'b')
```

Penjelasan: Pada contoh kode di atas, program mencoba untuk membagi nilai a dengan b, di mana b adalah nol. Hal ini menyebabkan kesalahan sinkron karena pembagian dengan nol tidak diperbolehkan dalam matematika. Kode tersebut akan menghasilkan pesan kesalahan yang menyatakan bahwa operasi aritmatika dilakukan pada nilai nil (b), karena variabel b belum diinisialisasi.

2. **Kesalahan Waktu Eksekusi**:

Jenis kesalahan ini terjadi ketika program berhasil dijalankan, tetapi kesalahan muncul saat eksekusi karena masalah dalam input atau penggunaan fungsi yang salah. Analoginya, Anda sedang mengikuti resep masakan dan tanpa disadari salah menggunakan bahan tertentu, sehingga masakan tersebut tidak berhasil sesuai harapan. Contohnya, kesalahan dapat terjadi jika kita mencoba mengakses elemen yang tidak ada di dalam sebuah array. Sebagai contoh kode:

   ```lua
   -- Kesalahan waktu eksekusi, mengakses elemen di luar batas array
   local fruits = {"apel", "pisang", "jeruk"}
   print(fruits[4])
   ```

   Output:
   ```
   nil
   ```
   Penjelasan: Kode di atas mengalami kesalahan waktu eksekusi karena mencoba mengakses elemen keempat dari array fruits, padahal hanya ada tiga elemen dalam array tersebut. Sehingga, nil (kosong) dikembalikan sebagai hasilnya.

Contoh Kode ke 2:

```lua
-- Kesalahan waktu eksekusi, menggunakan fungsi tanpa mengimpor modul terlebih dahulu
local result = os.date("%Y-%m-%d")
print(result)
```

Output:
```
lua: example.lua:2: attempt to call a nil value (global 'os')
```

Penjelasan: Pada contoh kode di atas, program mencoba untuk menggunakan fungsi os.date untuk mendapatkan tanggal dalam format tertentu. Namun, kesalahan waktu eksekusi terjadi karena fungsi os.date membutuhkan modul os untuk diimpor terlebih dahulu sebelum penggunaannya. Karena modul os tidak diimpor, fungsi os.date tidak dapat diakses, sehingga menghasilkan pesan kesalahan "attempt to call a nil value (global 'os')".

Kode tersebut dapat diperbaiki dengan mengimpor modul os sebelum penggunaan fungsi os.date. Contoh kode yang benar adalah sebagai berikut:

```lua
-- Memperbaiki kesalahan waktu eksekusi dengan mengimpor modul os
local os = require("os")
local result = os.date("%Y-%m-%d")
print(result)
```

Output:
```
2023-07-20
```

Penjelasan: Kode di atas telah diperbaiki dengan mengimpor modul os menggunakan sintaks require("os"). Sekarang fungsi os.date dapat diakses dan mengembalikan tanggal dalam format yang diharapkan.

3. **Kesalahan Logika**:

Jenis kesalahan ini terjadi ketika program berhasil dijalankan dan tidak ada kesalahan sintaksis, tetapi output yang diberikan tidak sesuai dengan yang diharapkan karena alur logika yang salah. Analoginya, bayangkan Anda mengikuti petunjuk jalan yang salah dan akhirnya sampai di tempat yang tidak diinginkan. Contohnya, kesalahan logika dapat terjadi jika kita menggunakan kondisi yang salah dalam sebuah pernyataan if. Sebagai contoh kode:

   ```lua
   -- Kesalahan logika, kondisi dalam pernyataan if tidak sesuai
   local x = 10
   if x > 20 then
     print("Nilai x lebih besar dari 20")
   else
     print("Nilai x kurang dari atau sama dengan 20")
   end
   ```

   Output:
   ```
   Nilai x kurang dari atau sama dengan 20
   ```
   Penjelasan: Kode di atas mengalami kesalahan logika karena kita menggunakan kondisi yang salah. Kondisi "x > 20" tidak benar karena nilai x adalah 10, sehingga pernyataan else yang dieksekusi.

Contoh Kesalahan Logika lainnya:

Contoh Kode:
```lua
-- Kesalahan logika, penggunaan operator logika yang salah
local a = true
local b = false
if a and b or not a then
    print("Kondisi terpenuhi")
else
    print("Kondisi tidak terpenuhi")
end
```

Output:
```
Kondisi tidak terpenuhi
```

Penjelasan: Pada contoh kode di atas, kita mencoba untuk mengevaluasi suatu kondisi menggunakan operator logika. Namun, kita melakukan kesalahan dalam menempatkan tanda kurung sehingga evaluasi logika menjadi salah. Operator "and" memiliki prioritas lebih tinggi daripada operator "or", jadi jika tidak ada tanda kurung, evaluasi akan dilakukan dari kiri ke kanan. Dalam kasus ini, nilai a adalah true dan nilai b adalah false, sehingga kondisi "(a and b) or not a" menghasilkan false. Seharusnya, kita ingin menempatkan tanda kurung seperti "(a and b) or (not a)" untuk mendapatkan hasil yang benar.

**Kesimpulan:**

Dari penjelasan di atas, kita dapat menyimpulkan beberapa hal terkait kesalahan dalam pemrograman:

1. **Kesalahan Sintaksis** terjadi karena salah penggunaan komponen program, seperti operator dan ekspresi. Hal ini dapat dicegah dengan lebih berhati-hati dalam menulis kode dan memahami aturan sintaksis dari bahasa pemrograman yang digunakan.

2. **Kesalahan Waktu Eksekusi** terjadi ketika program berhasil dijalankan, tetapi kesalahan muncul saat eksekusi karena masalah dalam input atau penggunaan fungsi yang salah. Untuk mencegah kesalahan waktu eksekusi, pastikan input yang diberikan sesuai dengan yang diharapkan dan periksa penggunaan fungsi secara cermat.

3. **Kesalahan Logika** terjadi ketika program tidak menghasilkan output yang diharapkan karena alur logika yang salah. Hal ini sering terjadi akibat kesalahan dalam perumusan kondisi atau algoritma yang digunakan. Agar menghindari kesalahan logika, perlu dipastikan bahwa algoritma dan kondisi yang digunakan sesuai dengan kebutuhan program.

Dalam mengatasi kesalahan dalam pemrograman, beberapa langkah yang dapat diambil antara lain:

- **Debugging**: Proses mencari dan memperbaiki kesalahan dalam kode. Penggunaan breakpoint, pencetakan (print), atau tools debugging lainnya bisa membantu mengidentifikasi kesalahan dengan lebih baik.

- **Validasi Input**: Memastikan bahwa data yang dimasukkan ke dalam program sesuai dengan harapan dan menghindari kesalahan akibat input yang tidak valid.

- **Pengujian**: Melakukan pengujian dengan kasus-kasus yang berbeda untuk memastikan program berjalan dengan benar dalam berbagai skenario.

- **Pemahaman Bahasa Pemrograman**: Memahami aturan sintaksis dan struktur bahasa pemrograman yang digunakan untuk menghindari kesalahan sintaksis.

- **Perencanaan Algoritma**: Merencanakan algoritma dengan baik sebelum menulis kode, untuk memastikan bahwa logika program berjalan dengan benar.

Jika kita dapat menghindari kesalahan-kesalahan di atas dan meningkatkan pemahaman dan keterampilan dalam pemrograman, maka program yang kita buat akan lebih handal dan bekerja sesuai dengan yang diharapkan.


###### Penutupan Pembelajaran :
###### <em>Modul ini adalah modul terakhir dan penutup untuk pembelajaran bahasa pemrograman lua pada tingkat fundamental, terima kasih telah membaca materi-materi pembelajaran lua ini. semoga membantu dalam proses pembelajaran untuk menjadi programmer yang professional, jika ingin melanjutkan pembelajaran ke tingkat intermediate, silahkan berpindah ke modul berikutnya yaitu pada modul ke 07.</em>

<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/80x15.png" /></a>
###### <em><span xmlns:dct="http://purl.org/dc/terms/" href="http://purl.org/dc/dcmitype/Text" property="dct:title" rel="dct:type">_06_Penanganan_File_dan_Kesalahan_lua.md</span> by <a xmlns:cc="http://creativecommons.org/ns#" href="https://github.com/muchamadyja" property="cc:attributionName" rel="cc:attributionURL">Gillar Ajie Prasatya</a> is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a>.<br />Based on a work at <a xmlns:dct="http://purl.org/dc/terms/" href="https://github.com/muchamadyja/progstudymaterials/blob/main/lua_study_origin/_06_Penanganan_File_dan_Kesalahan_lua.md" rel="dct:source">github.com/muchamadyja/progstudymaterials</a>.</em>
###### [<em>click here for the license file</em>](https://github.com/muchamadyja/progstudymaterials/blob/main/LICENSE)
