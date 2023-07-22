# Memulai Pemrograman Lua -- Fly me to the lua

`Sebelum melanjutkan, tolong nyalakan wordwrap\softwrap nya terlebih dahulu pada editor anda.`
`Jika membaca langsung di halaman github ini, klik titik 3 diatas lalu centang opsi wrap lines nya.`
`Agar modul tidak berantakan dan mudah untuk dibaca.`

Halo para-pembaca, saya Gilar seorang Self-Programmer dan youtube content creator di channel pribadi saya [muchamadyja](https://www.youtube.com/channel/UC6fmcWOvU__bHXSb6Kyg5cA).

pada modul ini saya akan membahas tentang bahasa pemrograman yang kurang populer jika dibandingkan dengan Javascript namun mudah untuk dipelajari bahkan oleh orang awam sekalipun, bahasa pemrograman tersebut adalah Lua.

Lua adalah bahasa sumber terbuka atau lebih dikenal dengan kata `"open source"`. Lua banyak digunakan di berbagai platform mulai dari sistem server besar hingga aplikasi seluler kecil.
Dalam materi-materi ini dan yang selanjutnya, kita akan membahas berbagai topik fundamental terkait bahasa pemrograman lua.

## Sejarah Singkat Lua
Lua adalah bahasa pemrograman ringan dan dapat diperluas yang dikembangkan oleh Roberto Lerusalimschy, Luiz Henrique de Figueiredo, dan Waldemar Celes pada tahun 1993. Awalnya, Lua adalah sebuah proyek internal yang dibuat untuk memenuhi kebutuhan pemrograman di Petrobras, perusahaan minyak Brasil. Namun, pengembang Lua kemudian memutuskan untuk membuatnya menjadi bahasa pemrograman yang dapat digunakan secara umum.

Pengembangan Lua dimulai pada tahun 1993 oleh tim pengembang yang dipimpin oleh Roberto Lerusalimschy. Mereka menginginkan bahasa pemrograman yang sederhana, ringan, dan dapat diintegrasikan dengan baik dengan bahasa pemrograman lain, terutama bahasa C yang banyak digunakan dalam pengembangan perangkat lunak pada saat itu. Lua bertujuan untuk menawarkan apa yang tidak bisa dilakukan oleh C, yaitu jarak yang baik dari perangkat keras (kemampuan Lua untuk berfungsi dengan baik di berbagai platform dan perangkat keras yang berbeda), struktur dinamis, tidak ada redundansi, kemudahan pengujian dan debugging.

Lua diperkenalkan ke publik pada tahun 1994 dan versi pertamanya, Lua 1.0, dirilis secara resmi pada Juli 1994. Sejak itu, Lua telah mengalami perkembangan dan perluasan yang signifikan. Pada tahun 1996, versi Lua 3.0 dirilis dengan fitur-fitur baru yang lebih kuat dan fleksibel.

Salah satu keberhasilan utama Lua adalah digunakannya dalam industri video game. Lua sangat cocok untuk pengembangan video game karena ukurannya yang terbilang kecil, kecepatannya yang tinggi, dan kemampuannya untuk diintegrasikan dengan game engine yang tersedia saat ini. Banyak perusahaan permainan terkenal seperti [Blizzard Entertainment](https://www.blizzard.com/en-us/) (pengembang Warcraft dan World of Warcraft), [Mojang Studios](https://www.minecraft.net/en-us/article/meet-mojang-studios) (pengembang Minecraft) dan [Roblox Corporation.](https://corp.roblox.com/) (pengembang roblox dan roblox studio engine) menggunakan Lua dalam pengembangan permainan mereka.

Selama perjalanannya, Lua telah menjadi bahasa pemrograman yang populer dalam berbagai bidang seperti pengembangan permainan, pengembangan embedded software, software script, dan lainnya. Saat ini, Lua digunakan secara luas dan terus berkembang dengan adanya komunitas pengembang yang aktif yang berkontribusi dalam pengembangan, dokumentasi, dan penyediaan berbagai pustaka dan kerangka kerja untuk Lua.

Sejarah perjalanan yang sukses dan sifatnya yang ringan, fleksibel, dan mudah diintegrasikan, Lua tetap menjadi pilihan yang populer bagi pengembang untuk diintegrasikan pada software / permainan yang sedang dikembangkannya.

### Note:
Jika anda seorang yang awam / non-IT, pastinya akan banyak kata-kata yang tidak dimengerti, saran saya setiap kata yang anda tidak mengerti itu dicatat lalu cari pengertiannya di internet atau di KBBI (kamus besar bahasa indonesia) supaya memudahkan anda dalam mempelajari materi-materi terkait pemrograman kedepannya (tidak hanya terbatas pada materi di repo ini saja). rata-rata orang yang menyerah untuk belajar pemrograman itu dikarenakan banyak hal terutama dari segi bahasa yang sulit dimengerti yang selalu dipakai ketika menjelaskan materi terkait pemrograman. kekurangan informasi pada `kata` / `frasa` tertentu, membuat otak kita secara otomatis menolak untuk menyimpan informasi tersebut pada long-term memory. hal tersebut terjadi dikarenakan informasi-nya bersifat ambigu / tidak ada penjelasan lebih lanjut di dalam pustaka pada otak kita terkait `kosa kata` yang sedang di baca saat itu. sehingga bacaan tersebut hanya akan disimpan pada short-term memory otak kita dan siap untuk dibuang setelah kita berpindah ke paragraf berikutnya, hal tersebut menyebabkan kita tidak akan pernah mengerti terkait `kosa kata` yang sedang kita baca tersebut. akibat yang ditimbulkan paling banyak adalah menyebabkan tingkat emosi dan ekspresi yang berbeda-beda, biasanya kita akan mengalami stress ringan yg akan menurunkan minat / semangat baca kita dan akan mengalihkan fokus kita kepada sesuatu hal yang dirasa lebih menarik di seketika kita saat itu (seperti beralih dari membaca buku pelajaran menjadi scrolling sosmed atau bermain game).
Semakin banyak kosa-kata yang kita mengerti, akan semakin memudahkan kita dalam mempelajari dunia pemrograman.
untuk awam / pembaca yang baru menginjakan kaki di bulan (lua), silahkan ikuti saja modulnya secara terurut dan jangan khawatir dengan `kosa kata` yang tidak dimengerti, jika hal tersebut adalah pembahasan pokok dalam pembelajaran ini seperti misalkan `string` dan lain-lain, anda pasti akan menemukan penjelasan di modul-modul berikutnya. jika `kosa-kata` tersebut adalah bahasa intelek yang sering digunakan dalam dunia pemrograman, anda bisa mencari penjelasan lengkapnya di internet.

## Lua
Memiliki manajemen memori otomatis, dan cocok untuk menangani string dan jenis data lainnya dengan ukuran yang dinamis. Berikut adalah beberapa fitur Lua:

* Bahasa yang sederhana
* Efisien
* Dapat dijalankan di berbagai platform
* Gratis dan terbuka (open source)

## Bagaimana Lua Diterapkan?
Lua terdiri dari dua bagian - interpreter Lua dan functioning software system. functioning software system adalah aplikasi komputer yang dapat menginterpretasikan program yang ditulis dalam bahasa pemrograman Lua.
Interpreter Lua ditulis dalam bahasa ANSI C, oleh karena itu sangat portabel dan dapat dijalankan di berbagai perangkat. Baik bahasa Lua maupun interpreter-nya telah dinilai sebagai tools yang matang, ringkas, dan cepat.

## Berikut beberapa pengaplikasian Lua:
Di mana digunakan?
* Pemrograman Game
* Scripting dalam Aplikasi
* Scripting di Web
* Ekstensi dan add-on untuk database seperti MySQL Proxy dan MySQL WorkBench
* Sistem keamanan seperti Intrusion Detection System (IDS)

Jika Anda ingin mengatur lingkungan untuk pemrograman Lua, Anda akan membutuhkan hal berikut:
* Editor Teks
* Interpreter Lua, dan
* Compiler Lua

Pada bagian di bawah ini, kita akan melihat panduan singkat untuk menginstal Lua di sistem Anda.

## Editor Teks
Anda membutuhkan editor teks untuk mengetik program Anda. Beberapa editor yang dapat digunakan termasuk Windows Notepad, gedit, Brief, Epsilon, atau Vim. File yang Anda buat dengan editor Anda disebut file sumber / source file. File-file ini berisi kode sumber program. source file untuk program Lua diberi nama dengan ekstensi ".lua" di belakangnya, saya tidak dapat memberikan rekomendasi editor apapun atau IDE apapun, namun saya pribadi menggunakan vscode dengan bantuan beberapa ekstensi seperti Lua by Tencent, Lua Debug by actboy168, dan vscode-lua by trixnz.

## Interpreter Lua
Interpreter Lua adalah sebuah program kecil yang memungkinkan Anda mengetik perintah Lua secara langsung dan menjalankannya segera. Dengan menggunakan interpreter Lua, Anda dapat mengeksekusi perintah-perintah Lua satu per satu. Jika terjadi kesalahan atau error pada perintah kode yang Anda tulis, interpreter Lua akan menghentikan eksekusi file Lua tersebut. Hal ini berbeda dengan kompiler yang mengeksekusi source file secara keseluruhan. sedikit penjelasan terkait Kompiler (Compiler) adalah program yang mengubah source code menjadi bentuk yang dapat dieksekusi oleh komputer atau program yang memiliki sifat berlawanan dengan interpreter.

Interpreter Lua memberikan fleksibilitas bagi pengguna dalam menguji dan menjalankan kode secara interaktif. Anda dapat menguji perintah-perintah Lua secara langsung, melihat hasilnya, dan melakukan perbaikan atau perubahan secara instan. Setiap perintah yang Anda ketik akan dieksekusi segera oleh interpreter Lua.
Dengan demikian, interpreter Lua memberikan fleksibilitas dan kemudahan dalam menguji kode Lua secara interaktif, sementara kompiler memungkinkan Anda untuk menghasilkan file eksekusi yang siap digunakan secara lebih terstruktur dan efisien.

Pasti tersirat di benak anda terkait pertanyaan "apakah lua dapat menggunakan compiler juga?"

Jawabannya adalah :
Ya, Lua juga memiliki kompiler yang disebut "Lua Compiler" atau "luac". Lua Compiler digunakan untuk mengkompilasi file sumber Lua menjadi bytecode yang dapat dieksekusi secara lebih efisien oleh interpreter Lua. Bytecode adalah representasi intermediate code yang lebih dekat dengan bahasa mesin daripada teks sumber Lua.

Proses kompilasi dengan Lua Compiler mengubah source file Lua yang ditulis dalam teks menjadi file bytecode yang dapat dieksekusi langsung oleh interpreter Lua. Bytecode memiliki keuntungan dalam kinerja eksekusi yang lebih cepat karena interpreter Lua dapat menjalankannya tanpa memerlukan proses parsing dan interpretasi teks sumber secara langsung.

Anda dapat menggunakan Lua Compiler untuk mengkompilasi file sumber Lua dengan perintah berikut di command line:

```lua
luac -o outputfile bytecodefile.lua
```

Perintah di atas akan mengkompilasi file sumber `bytecodefile.lua` dan menghasilkan file bytecode dengan nama `outputfile` yang siap dieksekusi oleh interpreter Lua.

Namun, penting untuk dicatat bahwa pemilihan penggunaan interpreter Lua atau kompiler Lua tergantung pada kebutuhan dan tujuan pengembangan. Interpreter Lua memberikan fleksibilitas dalam pengembangan dan eksperimen yang interaktif, sementara kompiler Lua memberikan kinerja eksekusi yang lebih cepat dalam produksi yang lebih besar dan serius.

sedikit intermezzo, untuk pembaca yang awam pasti tidak mengerti terkait dengan apa itu "proses parsing dan interpretasi teks sumber"

Proses parsing dan interpretasi tersebut mirip dengan tugas seorang guru yang membaca dan memahami instruksi tertulis dalam sebuah cerita. Parsing melibatkan membaca dan mengurai setiap kalimat dalam kode sumber, sementara interpretasi adalah mengambil arti dan makna dari instruksi-instruksi tersebut. Interpreter Lua mengenali struktur dan sintaksis yang benar, serta menjalankan instruksi-instruksi sesuai dengan perilaku dan logika yang telah ditentukan dalam bahasa Lua. Dengan demikian, proses parsing dan interpretasi teks sumber adalah langkah-langkah yang dilakukan oleh interpreter Lua untuk membaca, memahami, dan menjalankan kode sumber Lua yang ditulis dalam bentuk teks.

Interpreter Lua melakukan hal yang sama dengan kita terkait perlakuan terhadap source code. Ia akan membaca dan mengenali struktur serta sintaksis yang benar dalam kode sumber, dan kemudian menjalankan instruksi-instruksi tersebut sesuai dengan perilaku dan logika yang telah ditentukan dalam tata bahasa Lua, ibaratnya seperti seorang QC (Quality Control) dalam sebuah rumah / pabrik yang produksi barang untuk dijual.

baik, kita kembali ke topik pembahasan.

## Mendownload dan menginstall lua
Saya pribadi tidak meyarankan untuk menginstall lua menggunakan installernya langsung dari [website_lua](https//lua.org) namun bagi awam installer adalah best practice silahkan ikuti instruksi penginstalannya di [link_ini](https://www.lua.org/download.html), namun jika anda pengguna microsoft windows silahkan ikuti panduan [disini](https://www.oreilly.com/library/view/lua-quick-start/9781789343229/b9f5f696-15a5-4445-9eb7-5fea563e9592.xhtml)

Jika anda setidaknya orang yang faham dengan komputer atau memang pengguna linux distro dan sering menggunakan terminal, boleh silahkan mengikuti langkah-langkah penginstalan lua ini dengan menggunakan version management (credit-to: [DhavalKapil](https://github.com/DhavalKapil/)):

Untuk instruksi dari websitenya langsung silakhan kunjungi https://dhavalkapil.com/luaver/

**Requirements**

Diperlukan `wget`, `git` dan `make`.

Anda mungkin perlu menginstal beberapa dependensi:

```
sudo apt-get install libreadline-dev
```

Juga, jika Anda berencana menginstal versi Lua yang lebih lama (32-bit) pada mesin 64-bit, Anda mungkin perlu menginstal beberapa pustaka 32-bit:

```
sudo apt-get install lib32ncurses5-dev
```

**Instalasi**
**Instalasi melalui Skrip**

Anda dapat menginstal melalui skrip berikut:

```shell
curl https://raw.githubusercontent.com/dhavalkapil/luaver/v1.0.0/install.sh -o install.sh && . ./install.sh
```

Catatan: Ini akan menimpa file install.sh di direktori saat ini. Selain itu, file ini tidak diperlukan setelah instalasi selesai.

**Instalasi dari Repositori Git** (untuk saya pribadi saya menggunakan cara ini, karna lebih saya mengerti prosesnya)

Pertama, clone luaver pada mesin lokal Anda menggunakan git:

```shell
git clone https://github.com/DhavalKapil/luaver
```

Kemudian, jalankan skrip instalasi:

```shell
cd luaver
. ./install.sh
```

**Penggunaan**

Contoh penggunaan:

```shell
luaver install 5.3.1             # Menginstal versi Lua 5.3.1
luaver install 5.3.0             # Menginstal versi Lua 5.3.0
luaver use 5.3.1                 # Beralih ke versi Lua 5.3.1
luaver install-luarocks 2.3.0    # Menginstal versi Luarocks 2.3.0
luaver uninstall 5.3.0           # Menghapus instalasi versi Lua 5.3.0
```
Untuk versi lua terbaru itu di versi 5.4.6 / latest version pada saat modul ini dilengkapi : 19/juli/2023

**Penggunaan lengkap:**

```shell
luaver help

Penggunaan:
   luaver help                              Menampilkan pesan ini
   luaver install <versi>                   Menginstal lua-<versi>
   luaver use <versi>                       Beralih ke lua-<versi>
   luaver set-default <versi>               Menetapkan <versi> sebagai versi default untuk lua
   luaver unset-default                     Membatalkan versi lua default
   luaver uninstall <versi>                 Menghapus instalasi lua-<versi>
   luaver list                              Menampilkan daftar versi Lua yang terinstal
   luaver install-luajit <versi>            Menginstal luajit-<versi>
   luaver use-luajit <versi>                Beralih ke luajit-<versi>
   luaver set-default-luajit <versi>        Menetapkan <versi> sebagai versi default untuk luajit
   luaver unset-default-luajit              Membatalkan versi luajit default
   luaver uninstall-luajit <versi>          Menghapus instalasi luajit-<versi>
   luaver list-luajit                       Menampilkan daftar versi Luajit yang terinstal
   luaver install-luarocks <versi>          Menginstal luarocks<versi>
   luaver use-luarocks <versi>              Beralih ke luarocks-<versi>
   luaver set-default-luarocks <versi>      Menetapkan <versi> sebagai versi default untuk luarocks
   luaver unset-default-luarocks            Membatalkan versi luarocks default
   luaver uninstall-luarocks <versi>        Menghapus instalasi luarocks-<versi>
   luaver list-luarocks                     Menampilkan semua versi luarocks yang terinstal
   luaver current                           Menampilkan versi yang sedang digunakan
   luaver version                           Menampilkan versi luaver
```

# Saatnya membangun program pertama kita di Lua.
Kita akan melihat interpreter lua dalam dua mode yang tersedia:
* Mode Interaktif
* Mode Default

## Mode Interaktif
Lua menyediakan mode yang disebut dengan mode interaktif.
Dalam mode ini, Anda dapat mengetik instruksi satu demi satu dan mendapatkan hasil instan. Ini dapat diakses di `shell` / `terminal` dengan menggunakan perintah `lua -i`.

Setelah Anda mengetiknya, tekan enter, dan mode interaktif akan dimulai.
Anda dapat mencetak sesuatu menggunakan pernyataan:
```lua
print("sesuatu")
```
Setelah Anda menekan enter, Anda akan mendapatkan output:
```lua
sesuatu
```

## Mode Default
Menggunakan interpreter dengan parameter nama file Lua, akan memulai eksekusi file tersebut. Hal Ini akan berlanjut sampai skrip selesai. Ketika skrip selesai, interpreter akan tidak aktif lagi hingga kita mengaktifkannya ulang.
coba anda tulis program Lua sederhana. Semua file Lua akan memiliki ekstensi `.lua`.

Jadi tuliskan kode sumber di dalam file test.lua, apapun atau perintah cetak tadi saja `print("sesuatu")` sebagai contoh. Dengan asumsi, lingkungan Lua tadi sudah diatur dengan benar (lua interpreter sudah ter-instal di komputer anda)
jalankan program menggunakan kode berikut:
```lua
$ lua test.lua
```
hasilnya akan memunculkan :
```lua
test
```
## Sintaksis Lua
Sintaksis adalah aturan atau tata bahasa yang digunakan dalam penulisan kode Lua. Lua memiliki sintaksis yang sederhana dan mudah dipahami. Setiap pernyataan diakhiri dengan tanda newline atau titik koma `(;)` (titik koma hanya di gunakan pada kasus tertentu saja). Komentar dapat ditulis dengan menggunakan tanda dua minus `(-)` ganda `(--)`. Variabel diawali dengan huruf atau garis bawah dan dapat mengandung huruf, angka, atau garis bawah. Struktur kontrol seperti `if-then-else` dan `loops` ditandai dengan kata kunci seperti `if`, `then`, `else`, `while`, dan `for`. Misalnya, pernyataan `if-then-else` dalam Lua ditulis sebagai berikut:

```lua
if kondisi then
   -- pernyataan jika kondisi terpenuhi
else
   -- pernyataan jika kondisi tidak terpenuhi
end
```

Dalam contoh di atas, jika kondisi terpenuhi, maka blok pernyataan di dalam bagian "then" akan dieksekusi. Jika kondisi tidak terpenuhi, maka blok pernyataan di dalam bagian "else" akan dieksekusi. Sintaksis Lua yang sederhana memungkinkan Anda untuk menulis kode dengan mudah dan memahaminya dengan cepat.

**Statement di Lua**

Statement adalah **suatu pernyataan** dalam semua bahasa pemrograman, yang artinya **suatu baris** atau **bahkan beberapa baris kode** yang **melakukan tindakan tertentu** atau **menginstruksikan kepada suatu sistem dalam komputer kita** untuk **melakukan sesuatu**. Statement biasanya **mengubah keadaan program**, **mengontrol aliran eksekusi**, atau **memberikan instruksi kepada komputer**. Sebagai contoh, statement `if-then-else` digunakan untuk **mengambil keputusan berdasarkan kondisi tertentu**, (ikuti saja dulu nanti kita akan bahas pengkondisian pada materinya sendiri) Berikut adalah contoh kodenya:

```lua
if x > 5 then
   print("Nilai x lebih besar dari 5") -- pernyataan (statement) pertama
else
   print("Nilai x kurang dari atau sama dengan 5") -- pernyataan (statement) ke-dua
end
```

Dalam contoh di atas, pernyataan `if-then-else` digunakan untuk memeriksa apakah nilai `x` lebih besar dari 5. Jika kondisi terpenuhi, maka pernyataan pertama akan dieksekusi. Jika tidak, pernyataan dalam bagian `else` akan dieksekusi. Pernyataan dalam Lua sering kali berada dalam blok kode (blok kode akan dibahas setelah materi ini) yang ditandai dengan `do` dan `end`, yang menunjukkan rentang eksekusi dari pernyataan tersebut.

**Expression di Lua**

Expression adalah **bagian dari kode yang menghasilkan nilai**. Expression dapat berupa **pengoperasian aritmatika, operasi perbandingan, pemanggilan fungsi, atau pengambilan nilai variabel**. Expression dapat digunakan dalam berbagai konteks, seperti memberikan nilai pada variabel, argumen dalam pemanggilan fungsi, atau dalam pernyataan pengontrolan aliran program. Berikut adalah contoh kode:

```lua
nilai = 10 + 5
hasil = nilai * 2
print("Hasil perkalian adalah:", hasil)
```

Dalam contoh di atas, `nilai` diinisialisasi dengan hasil penjumlahan 10 dan 5. Kemudian, variabel `hasil` diberikan nilai dari perkalian `nilai` dengan 2. Akhirnya, hasil perkalian ditampilkan menggunakan pernyataan `print`. Dalam kasus ini, ekspresi matematika seperti penjumlahan dan perkalian digunakan untuk menghasilkan nilai yang disimpan dalam variabel (variabel akan di bahasa pada materinya di bawah nanti) atau digunakan dalam pernyataan lain.

## Baris kode
Dalam Lua merujuk pada statement tunggal dalam program. Setiap baris kode diakhiri dengan tanda newline atau titik koma `(;)` dan disebut dengan terminator, namun pada umumnya titik koma `(;)` hanya digunakan untuk memisahkan suatu statement dengan statement yang lain bila ditulis dalam satu baris kode yang sama, biasanya `(;)` tersebut disebut dengan statement separator. dengan kata lain tidak wajib untuk di tuliskan setiap kali menulis satu baris kode.

Setiap pernyataan pada baris kode biasanya menginstruksikan komputer untuk melakukan tindakan tertentu, seperti deklarasi variabel, pemanggilan fungsi, atau perhitungan matematika (tiga hal tersebut akan di bahas di bawah dan di modul lain khusus untuk definisi fungsi).

Contoh sederhana dari baris kode menggunakan terminator:

```lua
nilai = 10;  -- Mendeklarasikan variabel 'nilai' dan memberinya nilai 10
```
Contoh sederhana dari baris kode yang umumnya dituliskan:

```lua
nilai = 10  -- Mendeklarasikan variabel 'nilai' dan memberinya nilai 10
```

Dalam kedua contoh di atas, baris kode `nilai = 10;` mendeklarasikan variabel `nilai` dan memberinya nilai 10.

## Blok kode
Dalam Lua merujuk pada kumpulan statement yang dikelompokan bersama untuk membentuk suatu unit eksekusi yang saling terkait. Blok kode diawali dengan kata kunci seperti `do` dan diakhiri dengan kata kunci `end`. Blok kode biasanya digunakan dalam struktur kontrol seperti loops (perulangan) atau conditional statements (pernyataan kondisional). Contoh sederhana dari blok kode Lua adalah:

```lua
for i = 1, 5 do
   -- Blok kode yang akan dieksekusi berulang kali
   print("Perulangan ke", i)
end
```

Dalam contoh di atas, blok kode di dalam `for` loop akan dieksekusi berulang kali, dari nilai `i` mulai dari 1 hingga 5. Setiap iterasi loop, baris kode `print("Perulangan ke", i)` akan dieksekusi.

## Token dalam Lua

Program Lua terdiri dari berbagai token. Token adalah unit terkecil dalam bahasa pemrograman yang memiliki makna tertentu. Dalam Lua, token dapat berupa kata kunci (keyword), pengenal (identifier), konstanta, string literal, atau simbol. Mari kita bahas lebih detail tentang masing-masing jenis token ini.

### 1. Kata Kunci (Keywords)

Kata kunci adalah kata-kata yang memiliki makna khusus dalam bahasa Lua. Kata kunci ini tidak dapat digunakan sebagai nama variabel atau fungsi oleh pengguna. Lua memiliki sejumlah kata kunci yang telah ditentukan sebelumnya, seperti `if`, `else`, `for`, `while`, dan lain-lain. Kata kunci ini digunakan untuk mengatur alur program dan mengontrol eksekusi kondisional atau perulangan.

Contoh:
```lua
if x > 0 then
  print("Nilai x adalah positif")
else
  print("Nilai x adalah negatif atau nol")
end
```
(tidak usah bingung dulu terkait kode diatas, nanti kita akan bahas satu per satu.)

Pada contoh di atas, kata kunci `if`, `then`, `else`, dan `end` digunakan untuk mengatur struktur percabangan, terkait percabangan akan kita bahas di lain modul.

### 2. Pengenal (Identifiers)

Identifiers digunakan untuk memberikan nama pada variabel, fungsi, atau item lain yang ditentukan oleh pengguna. Pengenal harus diawali dengan huruf `A hingga Z` atau `a hingga z` atau garis bawah `_`, dan dapat diikuti oleh huruf, angka, atau garis bawah. Lua membedakan antara huruf besar dan kecil dalam pengenal (case-sensitive), artinya `nama` dan `Nama` dianggap sebagai dua pengenal yang berbeda.

Contoh:
```lua
local nama = "John"
function sayHello()
  print("Halo, " .. nama)
end
```

Pada contoh di atas, `nama` dan `sayHello` adalah pengenal yang digunakan untuk memberi nama pada variabel dan fungsi.

### 3. Konstanta

Konstanta adalah nilai tetap yang tidak berubah selama program berjalan. Dalam Lua, terdapat beberapa jenis konstanta, seperti bilangan bulat (integer), bilangan desimal (floating-point), boolean (true/false), dan nilai-nilai khusus seperti `nil` (nilai kosong) atau `NaN` (Not a Number).

Contoh:
```lua
local umur = 25 -- bilangan bulat
local tinggi = 1.75 -- bilangan desimal
local benar = true -- boolean
local kosong = nil -- nilai kosong
```

Pada contoh di atas, `umur`, `tinggi`, `benar`, dan `kosong` adalah contoh konstanta dengan jenis yang berbeda.

### 4. String Literal

String literal adalah urutan karakter yang diapit oleh tanda petik tunggal ('...') atau tanda petik ganda ("..."). String literal digunakan untuk merepresentasikan teks atau data dalam program Lua.

Contoh:
```lua
local nama = "John Doe"
local kalimat = "Halo, apa kabar?"
```

Pada contoh di atas, `nama` dan `kalimat` adalah contoh string literal yang berisi teks.

### 5. Simbol

Simbol adalah karakter khusus atau tanda baca yang digunakan dalam program Lua untuk tujuan tertentu. Beberapa simbol yang umum digunakan dalam Lua antara lain: + (penambahan), - (pengurangan), * (perkalian), / (pembagian), % (modulo), = (penugasan), == (persamaan), dan lain-lain. Simbol ini digunakan dalam ekspresi matematika, operasi logika, atau operasi perbandingan.

Contoh:
```lua
local a = 5
local b = 3
local hasil = a + b -- simbol penambahan
```

Pada contoh di atas, `+` adalah contoh simbol yang digunakan untuk melakukan operasi penambahan.

Dengan pemahaman tentang jenis-jenis token ini, Anda dapat mengenali dan menggunakan dengan tepat elemen-elemen dalam program Lua Anda.

## Komentar
Komentar adalah teks bantu dalam program Lua, biasanya digunakan untuk menjelaskan alur kerja dari sebuah baris kode.
Mereka akan diabaikan oleh interpreter jadi tak perlu khawatir source code anda akan menjadi error ketika dijalankan.
Komentar dengan beberapa baris dimulai dengan `--[[` dan diakhiri dengan karakter `]]` seperti yang ditunjukkan di bawah ini −
```lua
--[[
    ini adalah beberapa
    baris komentar
]]
```
Sedangkan komentar satu baris hanya menggunakan `--` seperti ini:
```lua
-- ini adalah komentar satu baris
```

## Pengenal
Pengenal Lua digunakan untuk mengidentifikasi variabel, fungsi, atau item yang ditentukan pengguna lainnya.
Pengenal dimulai dengan huruf `A hingga Z` atau `a hingga z` atau garis bawah `_` diikuti oleh nol atau lebih huruf, garis bawah, dan digit `(0 hingga 9)`.
Lua tidak mengizinkan karakter tanda baca seperti `@, $,` dan `%` dalam pengenal.
Lua adalah bahasa pemrograman yang bersifat case sensitive (membedakan huruf besar dan kecil).
Oleh karena itu

, "Programming", "PROGRAMMING", dan "programming" adalah tiga pengenal yang berbeda dalam Lua.

Itu sudah cukup dengan dasarnya.
Di bab-bab berikutnya, kita akan belajar pemrograman Lua yang lebih kompleks.<br><br>

<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/80x15.png" /></a>
###### <em><span xmlns:dct="http://purl.org/dc/terms/" href="http://purl.org/dc/dcmitype/Text" property="dct:title" rel="dct:type">_01_pengenalan_lua.md</span> by <a xmlns:cc="http://creativecommons.org/ns#" href="https://github.com/muchamadyja" property="cc:attributionName" rel="cc:attributionURL">Gillar Ajie Prasatya</a> is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a>.<br />Based on a work at <a xmlns:dct="http://purl.org/dc/terms/" href="https://github.com/muchamadyja/progstudymaterials/blob/main/lua_study_origin/_01_pengenalan_lua.md" rel="dct:source">github.com/muchamadyja/progstudymaterials</a>.</em>
###### [<em>click here for the license file</em>](https://github.com/muchamadyja/progstudymaterials/blob/main/LICENSE)
