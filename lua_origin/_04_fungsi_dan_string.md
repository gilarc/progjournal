# Functions di Lua

Function atau fungsi dalam bahasa pemrograman Lua adalah blok kode yang digunakan untuk mengelompokkan serangkaian pernyataan yang saling terkait untuk melakukan tugas tertentu. Fungsi memungkinkan kita untuk memecah kode program menjadi bagian-bagian yang lebih kecil dan terorganisir, sehingga memudahkan pemeliharaan dan pemahaman kode pada source file kita. Dengan menggunakan fungsi, kita dapat mengisolasi logika atau tugas tertentu sehingga dapat digunakan kembali dan dipanggil dari berbagai bagian dalam program yang sedang kita buat/kembangkan. Fungsi juga memungkinkan pengiriman argumen sebagai input, pengembalian nilai sebagai output, dan membantu dalam membuat program menjadi lebih efisien dan terstruktur.

Fungsi itu seperti layaknya sekelompok sesuatu yang bekerja sama untuk menyelesaikan sebuah tugas. Bayangkan Anda sedang memasak. Saat Anda memasak, Anda melakukan berbagai langkah seperti memotong bahan, memasak, dan menyajikan makanan. Anda dapat membagi langkah-langkah ini menjadi beberapa tugas yang berbeda seperti memotong bahan, memasak masakan, dan menyajikan. Cara Anda membagi langkah-langkah ini tergantung pada Anda, tetapi penting untuk memastikan setiap tugas memiliki fungsinya tersendiri. Dengan cara ini, pekerjaan dapat dilakukan dengan lebih efisien dan terorganisir.

Atau bisa kita analogikan fungsi sebagai mesin cetak produk botol plastik, yang biasa dikenal sebagai mesin mold.

Bayangkan mesin cetak botol plastik memiliki beberapa komponen, seperti cetakan (mold) dan sistem penggerak. Cetakan berfungsi untuk membentuk botol plastik, sedangkan sistem penggerak mengatur proses pembentukan botol.
Dalam analogi ini, fungsi di Lua serupa dengan mesin cetak. Setiap fungsi dapat dianggap sebagai mesin mold yang menghasilkan produk tertentu. Misalnya, fungsi "buatBotolKecil" akan membuat botol plastik berukuran kecil, sementara fungsi "buatBotolBesar" akan menghasilkan botol berukuran besar.

Ketika memanggil fungsi, seperti menggunakan mesin cetak, kita memberikan argumen atau bahan baku yang dibutuhkan. Misalnya, fungsi "buatBotolKecil" membutuhkan argumen berupa ukuran dan jenis bahan botol.
Fungsi juga dapat mengembalikan nilai, seperti mesin cetak yang menghasilkan produk jadi. Misalnya, fungsi "hitungVolumeBotol" akan mengembalikan nilai volume botol yang dihasilkan.

Selain itu, fungsi dapat digunakan secara berulang, seperti mesin cetak yang dapat mencetak banyak produk dengan menggunakan cetakan yang sama. Dengan fungsi, kita dapat memanggil dan menggunakan kode yang sama berulang kali dalam program, menjadikannya lebih efisien dan modular (terbagi-bagi).

Lua adalah sebuah bahasa pemrograman yang memiliki banyak fungsi bawaan yang siap digunakan. Fungsi-fungsi ini dapat dipanggil dan digunakan di dalam program kita. Contohnya, terdapat sebuah fungsi yang disebut `print()`, yang berguna untuk mencetak nilai yang Anda berikan ke layar komputer kita. Fungsi dalam Lua memiliki banyak nama seperti metode, subrutin, atau prosedur, tetapi pada dasarnya semuanya memiliki tujuan yang sama. Mari kita lihat bagaimana cara kita mendefinisikan dan menggunakan fungsi-fungsi ini.

Kita bisa bayangkan Lua sebagai sebuah lab penelitian di sekolah / workshop di sekolah yang menyediakan berbagai alat, instrumen dan atau perkakas siap pakai untukm melakukan praktikum pada pelajaran praktek mapel tertentu. Salah satu alat yang tersedia di workshop ini adalah mesin cetak, yang dapat digunakan untuk mencetak pesan yang Anda inginkan. Fungsi-fungsi dalam Lua adalah seperti instruksi yang Anda berikan kepada mesin cetak untuk mencetak pesan tertentu.

Definisi metode dalam bahasa pemrograman Lua terdiri dari header metode dan body metode. berikut adalah semua bagian dari metode tersebut:

1. Scope Fungsi Opsional: Anda dapat menggunakan kata kunci "local" untuk membatasi jangkauan fungsi atau mengabaikan bagian jangkauan, yang akan membuatnya dapat diakses secara global. Analoginya seperti membagi pekerjaan di sebuah perusahaan. Jika Anda memberi instruksi khusus kepada sekelompok karyawan lokal, mereka hanya dapat melihat dan menggunakan instruksi tersebut. Namun, jika Anda memberikan instruksi secara global, semua karyawan di perusahaan dapat melihat dan mengikuti instruksi tersebut.

2. Nama Fungsi: Ini adalah nama yang sebenarnya dari fungsi. Analoginya seperti memberikan nama pada sebuah alat atau peralatan di rumah Anda. Misalnya, Anda memberi nama "Blender" pada peralatan dapur yang digunakan untuk membuat jus. Ketika Anda membutuhkan fungsi blender, Anda hanya perlu memanggilnya dengan nama "Blender".

3. Argumen: Argumen berperan sebagai pengganti dalam fungsi. Ketika Anda memanggil sebuah fungsi, Anda memberikan nilai ke argumen tersebut. Analoginya seperti memberikan instruksi kepada seorang asisten pribadi. Anda memberikan asisten pribadi Anda beberapa informasi atau petunjuk yang diperlukan untuk menyelesaikan tugas tertentu.

4. Tubuh Fungsi: Tubuh fungsi berisi serangkaian pernyataan yang menentukan apa yang harus dilakukan oleh fungsi. Analoginya seperti langkah-langkah atau instruksi yang harus diikuti oleh seseorang untuk menyelesaikan sebuah tugas. Misalnya, jika Anda memberi instruksi kepada seseorang tentang cara membuat kue, tubuh fungsi akan berisi langkah-langkah yang harus diikuti, seperti mencampur bahan, memanggang, dan menghias kue.

5. Return: Di Lua, Anda dapat menggunakan pernyataan "return" untuk mengembalikan satu atau beberapa nilai dari sebuah fungsi. Analoginya seperti memberikan hasil atau output dari suatu pekerjaan yang dilakukan. Misalnya, jika Anda meminta seseorang untuk melakukan perhitungan matematika, mereka dapat memberikan jawaban hasil perhitungan tersebut kepada Anda.

Dengan analogi ini, dapat dikatakan bahwa metode dalam bahasa pemrograman Lua seperti mengatur tugas-tugas dalam perusahaan, memberikan nama pada peralatan di rumah, memberikan petunjuk kepada asisten pribadi, mengikuti langkah-langkah dalam menyelesaikan tugas, dan mendapatkan hasil atau output dari pekerjaan yang dilakukan.

Fungsi dalam pemrograman mirip dengan kerja sama antara tim dalam menyelesaikan tugas tertentu. Bayangkan Anda memiliki tugas besar yang perlu diselesaikan. Anda dapat memecah tugas tersebut menjadi beberapa bagian kecil dan menugaskan setiap bagian kepada anggota tim yang berbeda. Setiap anggota tim akan menyelesaikan bagian tugas yang diberikan sesuai dengan keahliannya. Setelah semua anggota tim menyelesaikan tugas masing-masing, hasil kerja mereka akan digabungkan untuk mencapai tujuan akhir.

Dalam pemrograman, fungsi berperan seperti anggota tim. Fungsi memungkinkan kita untuk memecah kode menjadi bagian-bagian kecil yang masing-masing melakukan tugas tertentu. Fungsi-fungsi ini dapat dipanggil dalam program kita, mirip dengan cara kita memanggil anggota tim untuk menyelesaikan tugas mereka. Bahasa pemrograman Lua memiliki banyak fungsi bawaan yang sudah siap digunakan. Kita dapat memanggil fungsi-fungsi ini dalam program kita untuk melakukan tugas-tugas tertentu, seperti mencetak teks ke layar atau memanipulasi string.

Analoginya adalah:
Bayangkan Anda ingin membangun sebuah rumah. Anda tidak akan melakukannya sendirian, tetapi akan bekerja dengan tim yang terdiri dari tukang, pengecat, dan tukang ledeng. Setiap anggota tim ini mewakili sebuah fungsi. Tukang akan membangun struktur rumah, pengecat akan melukis dinding, dan tukang ledeng akan mengurus instalasi pipa air. Setiap anggota tim melakukan tugasnya sendiri-sendiri, tetapi pada akhirnya, hasil kerja mereka digabungkan untuk membentuk sebuah rumah yang utuh. Dalam hal ini, fungsi dalam pemrograman bekerja serupa dengan anggota tim yang bekerja sama untuk menyelesaikan proyek rumah.

Kita telah berurusan dengan fungsi pada materi di atas. 
```lua
-- Definisi fungsi max
function max(num1, num2)
    if num1 > num2 then
        return num1
    else
        return num2
    end
end

-- Pemanggilan fungsi max
local result = max(10, 6)
print("Nilai maksimum adalah: " .. result)
```
lihat contoh fungsi di atas. Kode di atas adalah kode sumber untuk sebuah fungsi yang disebut `max()`. 

Dalam contoh diatas, kita memiliki fungsi bernama `max` yang mengambil dua argumen `num1` dan `num2`. Fungsi ini membandingkan kedua angka dan mengembalikan nilai maksimum di antara keduanya. Pertama, kita membandingkan `num1` dengan `num2` menggunakan pernyataan `if`. Jika `num1` lebih besar dari `num2`, maka nilai `num1` dikembalikan sebagai hasilnya. Jika tidak, nilai `num2` dikembalikan. Kemudian, kita memanggil fungsi `max` dengan argumen 10 dan 6, dan hasilnya disimpan dalam variabel `result`. Terakhir, kita mencetak nilai maksimum ke konsol.

Cara Membaca Contoh Kode:
1. Pertama, kita mendefinisikan fungsi `max` dengan dua argumen `num1` dan `num2`.
2. Dalam tubuh fungsi, kita menggunakan pernyataan `if` untuk membandingkan `num1` dengan `num2`.
3. Jika `num1` lebih besar dari `num2`, kita mengembalikan `num1` sebagai nilai maksimum menggunakan pernyataan `return`.
4. Jika `num1` tidak lebih besar dari `num2`, kita mengembalikan `num2` sebagai nilai maksimum.
5. Ketika kita memanggil fungsi `max` dengan argumen 10 dan 6, nilai 10 akan dikembalikan karena 10 lebih besar dari 6.
6. Nilai maksimum tersebut kemudian disimpan dalam variabel `result`.
7. Selanjutnya, kita mencetak nilai maksimum ke konsol menggunakan fungsi `print` dan menggabungkannya dengan string menggunakan operator `..`.

## Argumen Fungsi

Ketika kita menggunakan fungsi dengan argumen, kita perlu memberikan nilai ke fungsi tersebut. Nilai ini disebut argumen, dan fungsi akan menggunakan variabel khusus yang disebut dengan parameter untuk menerima nilai ini. Analoginya seperti memesan makanan di restoran. Ketika kita memesan makanan, kita memberikan instruksi dan preferensi kita kepada pelayan (argumen), dan kemudian pelayan meneruskannya ke dapur (fungsi) melalui pesanan. Dapur menggunakan instruksi dan preferensi yang diberikan oleh pelayan untuk mempersiapkan makanan sesuai permintaan kita.

Berikut adalah beberapa poin penting yang perlu diingat saat menggunakan argumen dalam fungsi:

1. Deklarasi Variabel: Fungsi harus mendeklarasikan variabel-variabel khusus yang akan menerima nilai dari argumen. Variabel-variabel ini disebut parameter formal dan berperilaku seperti variabel lokal di dalam fungsi.
2. Nilai Masuk dan Keluar: Saat fungsi dipanggil, argumen yang diberikan akan ditampung oleh parameter dalam fungsi. Parameter akan mengambil nilai dari argumen dan menggunakan nilainya dalam operasi di dalam fungsi. Ketika fungsi selesai dieksekusi, parameter tidak lagi berlaku dan nilainya tidak dapat diakses.
3. Menggunakan Argumen: Argumen digunakan untuk memberikan data atau instruksi yang dibutuhkan oleh fungsi untuk melakukan tugasnya. Analoginya seperti memberikan instruksi kepada pelayan di restoran tentang preferensi makanan yang kita inginkan.
4. Fleksibilitas dan Kustomisasi: Dengan menggunakan argumen dalam fungsi, kita dapat memanggil fungsi yang sama dengan argumen yang berbeda, sehingga menghasilkan hasil yang berbeda pula. Analoginya seperti memesan makanan dengan preferensi yang berbeda di restoran yang sama, menghasilkan hidangan yang berbeda pula.

Contoh Kode 1: Fungsi dengan Argumen
```lua
-- Definisi fungsi dengan argumen
function greet(name)
    print("Halo, " .. name .. "! Selamat datang!")
end

-- Pemanggilan fungsi dengan argumen
greet("John")
greet("Jane")
```
Penjelasan: Dalam contoh ini, kita memiliki fungsi `greet` yang menerima satu argumen `name`. Ketika fungsi dipanggil dan argumen seperti "John" atau "Jane" diberikan, fungsi akan mencetak pesan selamat datang yang disesuaikan dengan nama yang diberikan.

Contoh Kode 2: Fungsi dengan Argumen dan Nilai Kembali
```lua
-- Definisi fungsi untuk menghitung luas persegi
function calculateArea(sideLength)
    local area = sideLength * sideLength
    return area
end

-- Pemanggilan fungsi dengan argumen dan nilai kembali
local squareArea = calculateArea(5)
print("Luas persegi dengan sisi 5 adalah " .. squareArea)

local rectangleArea = calculateArea(4, 6)  -- Hanya sisi pertama yang digunakan
print("Luas persegi panjang dengan panjang 4 dan lebar 6 adalah " .. rectangleArea)
```
Penjelasan: Dalam contoh ini, kita memiliki fungsi `calculateArea` yang menerima satu argumen `sideLength`. Fungsi ini menghitung luas persegi berdasarkan panjang sisi yang diberikan dan mengembalikan nilai luas tersebut. Ketika fungsi dipanggil dengan argumen seperti 5, fungsi akan mengembalikan luas persegi dengan sisi 5. Nilai kembalian ini kemudian dapat disimpan dalam variabel dan digunakan sesuai kebutuhan. Pada pemanggilan fungsi dengan dua argumen, hanya sisi pertama yang digunakan untuk menghitung luas persegi, sedangkan sisi kedua diabaikan.

Contoh Kode 3: Fungsi dengan Argumen Default
```lua
-- Definisi fungsi dengan argumen default
function greet(name, greeting)
    if greeting == nil then
        greeting = "Halo"
    end
    print(greeting .. ", " .. name .. "!")
end

-- Pemanggilan fungsi dengan dan tanpa argumen
greet("John", "Selamat pagi")
greet("Jane")
```
Penjelasan: Dalam contoh ini, kita memiliki fungsi `greet` yang menerima dua argumen, yaitu `name` (nama) dan `greeting` (sapaan). Jika argumen `greeting` tidak diberikan saat memanggil fungsi, maka fungsi akan menggunakan nilai default "Halo". Jika argumen `greeting` diberikan, maka fungsi akan menggunakan nilai yang diberikan. Dalam pemanggilan fungsi pertama, sapaan "Selamat pagi" diberikan, sedangkan dalam pemanggilan fungsi kedua, argumen `greeting` tidak diberikan sehingga sapaan default "Halo" digunakan.

## Memanggil Fungsi

Ketika Anda membuat fungsi dalam bahasa pemrograman Lua, Anda memberikan petunjuk tentang tugas apa yang harus dilakukan oleh fungsi tersebut. Analoginya, ini mirip dengan memberikan instruksi kepada seseorang untuk melakukan pekerjaan tertentu. Setelah fungsi didefinisikan, Anda dapat memanggilnya saat Anda membutuhkan fungsi tersebut untuk melakukan tugas yang telah ditentukan. Anda bisa membayangkan hal ini seperti memanggil seseorang untuk melakukan tugas tertentu.

Ketika program memanggil fungsi, kontrol program akan berpindah ke dalam fungsi yang dipanggil. Fungsi tersebut kemudian menjalankan tugas sesuai dengan instruksi yang diberikan. Ketika fungsi mencapai pernyataan `return`, nilai yang dihasilkan akan dikembalikan ke program utama. Dalam analogi ini, setelah seseorang menyelesaikan tugas yang diberikan, mereka memberikan hasil pekerjaan tersebut.

Untuk memanggil fungsi, Anda perlu menggunakan nama fungsi diikuti oleh tanda kurung. Jika fungsi membutuhkan argumen atau nilai masukan, Anda harus memberikan nilai-nilai tersebut saat memanggil fungsi. Analoginya, ini seperti memberikan informasi atau data yang dibutuhkan oleh seseorang untuk menyelesaikan tugas yang diberikan.

Jika fungsi mengembalikan nilai, Anda dapat menyimpan nilai yang dikembalikan dalam variabel. Analoginya, ketika seseorang memberikan hasil pekerjaan, Anda dapat menyimpan hasil tersebut untuk digunakan nanti. Ketika Anda menjalankan kode yang menggunakan fungsi-fungsi ini, Anda akan melihat hasil yang dihasilkan oleh fungsi tersebut.

Berikut adalah contoh kode yang menggambarkan konsep ini:

```lua
-- Fungsi untuk menentukan nilai maksimum dari dua angka
function max(a, b)
    if a > b then
        return a
    else
        return b
    end
end

-- Memanggil fungsi dan menyimpan hasilnya
local result1 = max(8, 5)
local result2 = max(3, 7)

-- Menampilkan hasil
print("Nilai maksimum dari dua angka adalah " .. result1)
print("Nilai maksimum dari dua angka adalah " .. result2)
```

Penjelasan: Dalam contoh ini, kita mendefinisikan fungsi `max` yang mengambil dua argumen `a` dan `b`. Fungsi ini membandingkan kedua argumen dan mengembalikan nilai maksimum di antara keduanya. Ketika kita memanggil fungsi `max` dengan argumen seperti 8 dan 5, fungsi tersebut mengembalikan nilai 8. Kemudian, kita menyimpan hasilnya dalam variabel `result1`. Hal yang sama dilakukan untuk pemanggilan kedua dengan argumen 3 dan 7. Hasilnya, 7, disimpan dalam variabel `result2`. Akhirnya, kita mencetak hasilnya ke konsol.

Dalam contoh ini, Anda dapat melihat bagaimana fungsi `max` didefinisikan dan kemudian dipanggil dengan argumen yang sesuai. Hasil yang dikembalikan oleh fungsi tersebut disimpan dalam variabel dan kemudian ditampilkan sebagai output.

## Giving and Passing Functions (Memberikan dan Melewati Fungsi)

Memberikan dan melewati fungsi adalah kemampuan bahasa Lua dimana kita dapat menganggap fungsi sebagai nilai dan menggunakannya dalam berbagai cara. Anda dapat membayangkan fungsi sebagai kotak alat yang berisi instruksi untuk melakukan tugas tertentu. Anda dapat memberikan kotak alat ini kepada orang lain agar mereka dapat menggunakannya, atau Anda dapat memasukkan kotak alat ini ke dalam kotak alat lain sebagai bagian dari tugas yang lebih besar.

Contoh Kode 1: Memberikan Fungsi ke Variabel
```lua
-- Definisi fungsi
function greet()
    print("Halo, selamat datang!")
end

-- Memberikan fungsi ke variabel
local myFunction = greet

-- Memanggil fungsi melalui variabel
myFunction()
```
Penjelasan: Dalam contoh ini, kita mendefinisikan fungsi `greet` yang mencetak pesan "Halo, selamat datang!" ke konsol. Kemudian, kita memberikan fungsi tersebut ke variabel `myFunction` dengan hanya menyebutkan nama fungsi tanpa tanda kurung. Sekarang, kita dapat memanggil fungsi tersebut melalui variabel `myFunction`, dan outputnya akan sama seperti memanggil fungsi `greet` langsung.

Contoh Kode 2: Melewati Fungsi sebagai Parameter
```lua
-- Definisi fungsi yang menerima fungsi lain sebagai parameter
function printMessage(messageFunction)
    messageFunction()
end

-- Fungsi yang akan dilewatkan sebagai parameter
function greet()
    print("Halo, selamat datang!")
end

-- Memanggil fungsi dan melewati fungsi greet sebagai parameter
printMessage(greet)
```
Penjelasan: Dalam contoh ini, kita mendefinisikan fungsi `printMessage` yang menerima satu parameter bernama `messageFunction`. Fungsi ini memanggil parameter `messageFunction` tanpa argumen. Kemudian, kita mendefinisikan fungsi `greet` yang mencetak pesan selamat datang. Selanjutnya, kita memanggil fungsi `printMessage` dan melewati fungsi `greet` sebagai parameter. Ini mengakibatkan fungsi `printMessage` memanggil fungsi `greet` di dalamnya, sehingga pesan selamat datang akan dicetak.

Contoh Kode 3: Menggunakan Fungsi sebagai Nilai Kembali
```lua
-- Definisi fungsi yang mengembalikan fungsi lain
function createMultiplier(multiplier)
    return function(number)
        return number * multiplier
    end
end

-- Membuat fungsi baru dengan nilai kembali
local double = createMultiplier(2)

-- Menggunakan fungsi baru
print(double(5)) -- Output: 10
print(double(7)) -- Output: 14
```
Penjelasan: Dalam contoh ini, kita mendefinisikan fungsi `createMultiplier` yang mengambil satu argumen `multiplier`. Fungsi ini mengembalikan fungsi baru yang mengalikan angka dengan `multiplier` yang diberikan. Kemudian, kita menggunakan fungsi `createMultiplier` untuk membuat fungsi baru dengan nilai kembali. Variabel `double` sekarang berisi fungsi yang mengalikan angka dengan 2. Ketika kita memanggil `double(5)`, itu akan mengembalikan hasil perkalian 5 dengan 2, yaitu 10.

Cara Membaca Contoh Kode:
1. Dalam contoh 1, kita mendefinisikan fungsi `greet` yang mencetak pesan selamat datang. Kemudian, kita memberikan fungsi tersebut ke variabel `myFunction`. Pada akhirnya, memanggil `myFunction()` akan mencetak pesan selamat datang.
2. Dalam contoh 2, kita mendefinisikan fungsi `printMessage` yang menerima parameter `messageFunction`. Fungsi ini memanggil parameter `messageFunction` tanpa argumen. Kemudian, kita mendefinisikan fungsi `greet` yang mencetak pesan selamat datang. Saat memanggil `printMessage(greet)`, itu akan memanggil fungsi `greet` di dalamnya dan mencetak pesan selamat datang.
3. Dalam contoh 3, kita mendefinisikan fungsi `createMultiplier` yang mengembalikan fungsi baru. Fungsi baru tersebut mengalikan angka dengan `multiplier`. Kemudian, kita menggunakan `createMultiplier` untuk membuat fungsi `double` dengan nilai kembali. Saat memanggil `double(5)`, itu akan mengalikan 5 dengan 2 dan mengembalikan hasilnya, yaitu 10.

Dalam semua contoh, kita menggunakan fungsi sebagai nilai dan dapat mengoperasikannya seperti variabel lainnya. Ini memungkinkan kita untuk memanfaatkan fleksibilitas Lua dalam memanipulasi fungsi dan memungkinkan adanya komposisi fungsi dan penggunaan fungsi sebagai argumen dalam skenario yang lebih kompleks.

## Apa Itu String?

String adalah serangkaian huruf atau karakter. Dalam pemrograman, string digunakan untuk menyimpan dan memanipulasi teks. string bisa kita bandingkan dengan sebuah tali yang ditempeli stiker huruf-huruf yang disusun bersama.

Contoh Kode 1: Inisialisasi String dengan Tanda Kutip Tunggal
```lua
local name = 'John'
print('Halo, ' .. name)
```
Penjelasan: Dalam contoh ini, kita menginisialisasi variabel `name` dengan string menggunakan tanda kutip tunggal. Kemudian, kita mencetak pesan "Halo, " diikuti oleh isi dari variabel `name`.

Contoh Kode 2: Inisialisasi String dengan Tanda Kutip Ganda
```lua
local message = "Ini adalah pesan."
print(message)
```
Penjelasan: Dalam contoh ini, kita menginisialisasi variabel `message` dengan string menggunakan tanda kutip ganda. Kemudian, kita mencetak isi dari variabel `message`.

Contoh Kode 3: Inisialisasi String dengan `[[` dan `]]`
```lua
local multiline = [[Ini adalah
sebuah
string
multiline.]]
print(multiline)
```
Penjelasan: Dalam contoh ini, kita menginisialisasi variabel `multiline` dengan string menggunakan tanda `[[` dan `]]`. Dalam tipe ini, kita dapat membuat string multiline dengan memasukkan baris baru dan menjaga format teks yang asli. Kemudian, kita mencetak isi dari variabel `multiline`.

Cara Membaca Contoh Kode:
1. Dalam contoh pertama, variabel `name` diinisialisasi dengan string menggunakan tanda kutip tunggal. Kita menggunakan operator `..` untuk menggabungkan string, yaitu pesan "Halo, " dengan isi variabel `name`.
2. Dalam contoh kedua, variabel `message` diinisialisasi dengan string menggunakan tanda kutip ganda. Pesan yang ada dalam string tersebut dicetak langsung ke konsol.
3. Dalam contoh ketiga, variabel `multiline` diinisialisasi dengan string menggunakan tanda `[[` dan `]]`. String ini memungkinkan kita untuk membuat string multiline yang melibatkan beberapa baris teks. Saat mencetak isi variabel `multiline`, teks akan dicetak sesuai dengan format yang telah ditentukan dalam string.

Analogi String:
Anda dapat membayangkan string seperti layaknya stiker huruf-huruf yang ditempelkan pada seutas tali. Jika Anda ingin menyimpan nama seseorang, Anda bisa menggunakan string "John" atau "Jane" untuk melambangkan nama tersebut. Anda juga dapat menggunakan string untuk membuat pesan atau paragraf yang lebih panjang. Seperti halnya Anda dapat mengikat beberapa helai tali bersama-sama untuk membentuk tali yang lebih panjang. dalam pemrograman, Anda dapat menggabungkan beberapa string menjadi satu string yang lebih panjang menggunakan operator konkatenasi (operator penggabungan).

Karakter escape Sequence (urutan escape) adalah karakter khusus yang digunakan dalam string untuk mengubah interpretasi normal karakter yang mungkin memiliki arti khusus. Ketika karakter urutan escape digunakan dalam sebuah string, karakter tersebut tidak dianggap sebagai karakter normal, tetapi memberikan arti khusus atau perilaku tertentu.

Contoh Kode: Menggunakan Karakter Urutan Escape
```lua
local message = "Ini adalah tanda kutip ganda: \"\""
print(message)
```
Penjelasan: Dalam contoh ini, kita menggunakan karakter urutan escape `\"` di dalam string. Hal ini memungkinkan kita untuk mencetak tanda kutip ganda secara harfiah ke dalam string tanpa mengakhiri string tersebut. Sebagai hasilnya, ketika pesan dicetak, tanda kutip ganda akan tercetak di antara teks.

Cara Membaca Contoh Kode:
1. Dalam contoh kode, kita menggunakan karakter urutan escape `\"` di dalam string.
2. Karakter urutan escape `\"` digunakan untuk menunjukkan bahwa tanda kutip ganda yang ada di dalam string adalah karakter yang ingin dicetak, bukan sebagai penanda akhir string.
3. Dengan menggunakan karakter urutan escape, kita dapat mencetak karakter tanda kutip ganda secara harfiah ke dalam string tanpa menganggapnya sebagai akhir string.

Ada banyak cara untuk mengubah atau memanipulasi string dalam pemrograman. Berikut ini beberapa cara yang umum digunakan:

1. Mengubah huruf menjadi huruf besar atau huruf kecil: Analoginya, jika kita memiliki kata "rumah" dan ingin mengubahnya menjadi "RUMAH", kita dapat menggunakan fungsi `string.upper()` untuk mengembalikan representasi kata tersebut dalam huruf besar. Sebaliknya, jika kita ingin mengubahnya menjadi "rumah" dengan huruf kecil, kita dapat menggunakan fungsi `string.lower()`.

Contoh Kode:
```lua
local word = "rumah"

local uppercaseWord = string.upper(word)
print(uppercaseWord) -- Output: RUMAH

local lowercaseWord = string.lower(word)
print(lowercaseWord) -- Output: rumah
```

2. Mengganti substring dalam string: Analoginya, bayangkan kita memiliki kalimat "Saya suka makan nasi" dan ingin mengganti kata "nasi" dengan "mie". Dalam hal ini, kita dapat menggunakan fungsi `string.gsub()` untuk mengganti kemunculan kata "nasi" dengan "mie".

Contoh Kode:
```lua
local sentence = "Saya suka makan nasi"

local newSentence = string.gsub(sentence, "nasi", "mie")
print(newSentence) -- Output: Saya suka makan mie
```

3. Mencari posisi substring dalam string: Analoginya, jika kita memiliki kalimat "Hari ini cuaca sangat cerah" dan ingin mencari posisi kata "cuaca", kita dapat menggunakan fungsi `string.find()` untuk menemukan indeks awal dan indeks akhir dari kata tersebut dalam kalimat.

Contoh Kode:
```lua
local sentence = "Hari ini cuaca sangat cerah"

local startPos, endPos = string.find(sentence, "cuaca")
print("Posisi awal: " .. startPos) -- Output: Posisi awal: 10
print("Posisi akhir: " .. endPos) -- Output: Posisi akhir: 15
```

Ini hanya beberapa contoh manipulasi string yang umum digunakan. Terdapat juga fungsi lain seperti `string.reverse()` untuk membalikkan karakter dalam string, `string.format()` untuk memformat string, `string.len()` untuk mendapatkan panjang string, `string.rep()` untuk mengulangi string sebanyak n kali, dan operator `..` untuk menggabungkan dua string.

contohnya sebagai berikut :

1. `string.reverse()`: Fungsi ini digunakan untuk membalikkan urutan karakter dalam sebuah string.

Contoh Kode:
```lua
local word = "Hello"
local reversedWord = string.reverse(word)
print(reversedWord) -- Output: olleH
```

Penjelasan: Dalam contoh di atas, kita memiliki string "Hello". Dengan menggunakan `string.reverse()`, kita membalikkan urutan karakter dalam string tersebut menjadi "olleH".

2. `string.format()`: Fungsi ini digunakan untuk memformat string dengan menggunakan format yang ditentukan.

Contoh Kode:
```lua
local name = "John"
local age = 25
local formattedString = string.format("Nama: %s, Usia: %d tahun", name, age)
print(formattedString) -- Output: Nama: John, Usia: 25 tahun
```

Penjelasan: Dalam contoh di atas, kita menggunakan `string.format()` untuk memformat string dengan memasukkan nilai variabel `name` dan `age` ke dalam format yang ditentukan. Hasilnya adalah "Nama: John, Usia: 25 tahun".

3. `string.len()`: Fungsi ini digunakan untuk mendapatkan panjang sebuah string.

Contoh Kode:
```lua
local word = "Hello"
local length = string.len(word)
print(length) -- Output: 5
```

Penjelasan: Dalam contoh di atas, kita menggunakan `string.len()` untuk mendapatkan panjang string "Hello". Panjangnya adalah 5 karakter.

4. `string.rep()`: Fungsi ini digunakan untuk mengulangi sebuah string sebanyak n kali.

Contoh Kode:
```lua
local word = "Hello"
local repeatedWord = string.rep(word, 3)
print(repeatedWord) -- Output: HelloHelloHello
```

Penjelasan: Dalam contoh di atas, kita menggunakan `string.rep()` untuk mengulangi string "Hello" sebanyak 3 kali. Hasilnya adalah "HelloHelloHello".

5. Operator `..`: Operator ini digunakan untuk menggabungkan dua string (konkatenasi string).

Contoh Kode:
```lua
local firstName = "John"
local lastName = "Doe"
local fullName = firstName .. " " .. lastName
print(fullName) -- Output: John Doe
```

Penjelasan: Dalam contoh di atas, kita menggunakan operator `..` untuk menggabungkan string `firstName`, spasi, dan string `lastName`. Hasilnya adalah "John Doe".

Dengan menggunakan fungsi-fungsi tersebut, Anda dapat memanipulasi string sesuai kebutuhan Anda. Misalnya, mengubah urutan karakter, memformat string, mendapatkan panjang string, mengulangi string, atau menggabungkan string.

Sebelumnya pada pembahasan tentang fungsi diatas, sempat menyinggung terkait `Metode`, `Subrutin`, dan `Prosedur`, kita akan tambahkan penjelasan 3 hal tersebut  
sebagai materi tambahan.

**Metode, Subrutin, dan Prosedur pada Lua**

Metode, subrutin, dan prosedur adalah istilah yang sering digunakan untuk merujuk pada fungsi di Lua. Dalam konteks Lua, ketiganya memiliki arti yang sama yaitu sekelompok pernyataan yang dieksekusi secara bersama-sama untuk melakukan tugas tertentu.

**1. Metode**

Metode adalah fungsi yang terkait dengan sebuah objek atau tabel dalam paradigma `Object Oriented Programming` atau sering dikenal dengan kata `OOP` (_kita akan bahas OOP pada modul lain dengan tingkatan pemahaman yang lebih tinggi_).
Metode berfungsi untuk menggambarkan tingkah laku atau tindakan yang dapat dilakukan oleh objek tersebut. Analoginya, kita bisa membayangkan objek sebagai sebuah perangkat elektronik seperti ponsel, sementara metode adalah berbagai fungsi yang dapat dilakukan oleh ponsel tersebut, seperti mengirim pesan, menjalankan aplikasi, atau menerima panggilan.

Contoh kode:
```lua
-- Definisikan sebuah tabel
tabel = {}

-- Definisikan metode untuk tabel
function tabel:metode1()
   -- Pernyataan-pernyataan di dalam metode
end

-- Panggil metode pada tabel
tabel:metode1()
```

**Cara membaca contoh kode:** 
Pada contoh di atas, kita membuat sebuah tabel kosong `tabel` dan mendefinisikan metode `metode1()` yang terkait dengan tabel tersebut. Untuk memanggil metode pada tabel, kita menggunakan sintaksis `tabel:metode1()`.

**2. Subroutine**

Subrutin atau Subroutine adalah fungsi yang dapat dipanggil dan dieksekusi dalam program Lua. Subroutine berfungsi untuk menjalankan serangkaian pernyataan dan dapat dipanggil dari berbagai bagian dalam program. Analoginya, kita bisa membayangkan Subroutine sebagai seorang karyawan yang memiliki tugas tertentu dalam suatu perusahaan. Karyawan tersebut dapat dipanggil dari departemen mana pun untuk menjalankan tugas yang telah ditentukan tersebut. atau bisa kita analogikan sebagai alat yang dapat dipanggil dari berbagai tempat dalam suatu proses, mirip dengan alat kunci pas yang dapat digunakan untuk memperbaiki atau memasang baut pada berbagai mesin. Seperti halnya subroutine, alat kunci pas memiliki tugas khusus yang dapat digunakan secara berulang, independen dari mesin yang diperbaiki. Ketika mesin membutuhkan perbaikan pada bagian tertentu, alat kunci pas dapat dipanggil dan digunakan untuk menyelesaikan tugas tersebut, kemudian dapat dipanggil kembali di tempat lain untuk tugas yang serupa.

Contoh kode:
```lua
-- Definisikan Subroutine
function subrutin1()
   -- Pernyataan-pernyataan di dalam subrutin
end

-- Panggil Subroutine
subrutin1()
```

**Cara membaca contoh kode:** 
Pada contoh di atas, kita mendefinisikan subroutine `subrutin1()` yang terdiri dari serangkaian pernyataan. Untuk memanggil subroutine, kita cukup menggunakan nama subroutine tersebut diikuti dengan tanda kurung `subrutin1()`.

**3. Prosedur**

Prosedur adalah fungsi yang memiliki tugas khusus dan tidak mengembalikan nilai. Prosedur berfungsi untuk menjalankan serangkaian pernyataan tanpa menghasilkan nilai yang dikembalikan. Analoginya, kita bisa membayangkan prosedur sebagai instruksi yang harus diikuti dalam suatu proses. Misalnya, secarik kertas berisi prosedur untuk membuat secangkir teh dengan langkah-langkah yang harus diikuti tanpa menghasilkan output. atau misalnya, bayangkan Anda bermain game petualangan di mana Anda harus melewati berbagai rintangan dan mencapai tujuan akhir. Di dalam game tersebut, Anda akan mengikuti serangkaian tindakan dan keputusan yang harus diambil untuk maju ke level berikutnya. Setiap tindakan atau keputusan tersebut dapat dianggap sebagai prosedur dalam game tersebut. Misalnya, Anda harus mengalahkan monster, memecahkan teka-teki, dan mengumpulkan item tertentu untuk melanjutkan ke level selanjutnya. Prosedur dalam Lua berperan serupa, di mana setiap langkah atau tindakan yang Anda jalankan memiliki peran penting dalam mencapai tujuan dalam program Anda, seperti memanipulasi data, menghitung hasil, atau menjalankan serangkaian operasi yang diperlukan.

Contoh kode:
```lua
-- Definisikan prosedur
function prosedur1()
   -- Pernyataan-pernyataan di dalam prosedur
end

-- Panggil prosedur
prosedur1()
```

**Cara membaca contoh kode:** 
Pada contoh di atas, kita mendefinisikan prosedur `prosedur1()` yang terdiri dari serangkaian pernyataan. Untuk memanggil prosedur, kita cukup menggunakan nama prosedur diikuti dengan tanda kurung `prosedur1()`.

Dengan menggunakan metode, subrutin, dan prosedur, kita dapat memecah program menjadi bagian-bagian yang terpisah dan lebih mudah dikelola. Kita dapat memanggil dan menggunakan kode tersebut sesuai kebutuhan dalam program kita.

<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/80x15.png" /></a>
###### <em><span xmlns:dct="http://purl.org/dc/terms/" href="http://purl.org/dc/dcmitype/Text" property="dct:title" rel="dct:type">_04_fungsi_dan_string.md</span> by <a xmlns:cc="http://creativecommons.org/ns#" href="https://github.com/muchamadyja" property="cc:attributionName" rel="cc:attributionURL">Gillar Ajie Prasatya</a> is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a>.<br />Based on a work at <a xmlns:dct="http://purl.org/dc/terms/" href="https://github.com/muchamadyja/progstudymaterials/blob/main/lua_study_origin/_04_fungsi_dan_string.md" rel="dct:source">github.com/muchamadyja/progstudymaterials</a>.</em>
###### [<em>click here for the license file</em>](https://github.com/muchamadyja/progstudymaterials/blob/main/LICENSE)
