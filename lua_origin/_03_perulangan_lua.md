# Perulangan dalam lua

### Apa itu Mengulangi Sebuah Tugas?
Mengulangi sebuah tugas berarti melakukan tugas yang sama berulang-ulang sampai mencapai tujuan yang diinginkan. 
Misalkan guru Anda memberikan Anda pekerjaan rumah untuk menulis 'Saya suka Lua' sebanyak 100 kali. Jika Anda melakukannya secara manual, mungkin Anda akan menulisnya seperti ini:
```
Saya suka Lua Saya suka Lua . . Saya suka Lua
```
Namun, tentu saja, tugas ini terasa melelahkan dan membosankan jika harus dilakukan secara manual. Dalam dunia komputer, kita bisa menggunakan konsep loop (pengulangan/perulangan) dalam pemrograman untuk melakukan tugas yang sama secara otomatis.

### Loop dalam Pemrograman

#### Pengenalan Loop
Loop adalah seperti sebuah siklus yang terus berulang sampai mencapai tujuan yang ditentukan. Bayangkan ketika Anda sedang mengaduk adonan kue menggunakan mixer. Anda akan terus mengaduk adonan tersebut sampai mencapai tekstur yang diinginkan. Dalam pemrograman, loop juga bekerja dengan cara yang sama. Anda memiliki `blok instruksi` yang akan diulang-ulang sampai kondisi tertentu terpenuhi. Misalnya, Anda ingin mencetak angka dari 1 hingga 10. Anda dapat menggunakan loop untuk mencetak angka tersebut secara berurutan sampai mencapai angka 10. Ada beberapa elemen penting dalam loop:

- **Loop**: Ini adalah kata kunci yang memberi tahu komputer bahwa kita ingin melakukan tugas yang diulang.
- **Kapan berhenti**: Ini adalah kondisi yang menentukan kapan loop harus berhenti.
- **Blok loop**: Ini berisi instruksi yang ingin kita ulangi.

Dalam Lua, terdapat tiga jenis loop yang umum digunakan:

1. **While loop**
2. **Repeat...until loop**
3. **For loop**

Mari kita jelajahi masing-masing loop.

### While Loop dalam Lua

#### Apa itu While Loop?
While loop digunakan ketika kita tidak tahu berapa kali loop harus diulang, namun kita tahu kondisi kapan loop harus berhenti. Loop ini akan terus dijalankan selama kondisi terpenuhi. seperti permisalan ketika kita sedang menunggu bus datang di halte. Kita tidak tahu pasti berapa lama kita harus menunggu, tetapi kita tahu bahwa kita harus berhenti menunggu ketika bus tiba. Jadi, kita akan terus menunggu (melakukan loop) selama kondisi belum terpenuhi (bus belum tiba). Begitu bus tiba dan kondisi terpenuhi, kita berhenti menunggu (menghentikan loop).

#### Contoh Kode dan Penjelasan Cara Membacanya
Berikut adalah contoh kode while loop dalam Lua:

```lua
local a = 10

while a < 20 do
    print("nilai a:", a)
    a = a + 1
end
```

Penjelasan:
- Pertama, kita mendefinisikan variabel `a` dengan nilai awal 10.
- Selama nilai `a` kurang dari 20, blok instruksi di dalam while loop akan dijalankan.
- Pada setiap iterasi, nilai `a` akan dicetak menggunakan pernyataan `print`.
- Setelah itu, nilai `a` akan ditambah 1 dengan `a = a + 1`.
- Loop akan terus berlanjut sampai nilai `a` mencapai 20.

Output dari kode di atas adalah:

```
nilai a: 10
nilai a: 11
nilai a: 12
nilai a: 13
nilai a: 14
nilai a: 15
nilai a: 16
nilai a: 17
nilai a: 18
nilai a: 19
```

#### Contoh Kode Lainnya

```lua
local x = 1

while x <= 5 do
    print(x * 2)
    x = x + 1
end
```

Penjelasan:
- Pada contoh ini, kita memiliki variabel `x` yang diinisialisasi dengan nilai 1.
- Blok instruksi di dalam while loop akan dijalankan selama nilai `x` kurang dari atau sama dengan 5.
- Pada setiap iterasi, nilai `x` akan dikalikan dengan 2 dan dicetak menggunakan pernyataan `print`.
- Nilai `x` akan ditambah 1 setiap kali iterasi dengan `x = x + 1`.
- Loop akan berhenti ketika nilai `x` mencapai 6.

Output dari kode di atas adalah:

```
2
4
6
8
10
```

### Repeat...until Loop dalam Lua

#### Apa itu Repeat...until Loop?
Repeat...until loop dalam Lua adalah jenis loop yang melakukan pengulangan instruksi hingga kondisi tertentu terpenuhi. Perbedaannya dengan while loop adalah kondisi diperiksa setelah `blok instruksi` dieksekusi.

Analoginya, kita bisa membayangkan Repeat...until loop seperti mengecek kondisi setelah kita melakukan suatu tindakan. Misalkan kita ingin mencoba makanan baru. Kita akan mencicipi makanan tersebut terlebih dahulu (melakukan blok instruksi), dan setelah itu kita mengecek apakah kita menyukainya atau tidak (mengecek kondisi). Jika kita belum menyukainya, kita akan mencoba makanan baru lagi (mengulangi blok instruksi) dan kemudian mengecek kembali. Pengulangan ini akan terus dilakukan sampai kita menemukan makanan yang kita sukai atau kondisi tertentu terpenuhi.

#### Contoh Kode dan Penjelasan Cara Membacanya
Berikut adalah contoh kode repeat...until loop dalam Lua:

```lua
local b = 1

repeat
    print("nilai b:", b)
    b = b + 1
until b > 5
```

Penjelasan:
- Pertama, kita mendefinisikan variabel `b` dengan nilai awal 1.
- Blok instruksi di dalam repeat...until loop akan dijalankan.
- Pada setiap iterasi, nilai `b` akan dicetak menggunakan pernyataan `print`.
- Setelah itu, nilai `b` akan ditambah 1 dengan `b = b + 1`.
- Setelah itu, kondisi `b > 5` diperiksa. Jika kondisi terpenuhi, loop berhenti.
- Jika kondisi tidak terpenuhi, loop akan terus berlanjut.

Output dari kode di atas adalah:

```
nilai b: 1
nilai b: 2
nilai b: 3
nilai b: 4
nilai b: 5
```

#### Contoh Kode Lainnya

```lua
local c = 10

repeat
    print(c)
    c = c - 2
until c < 0
```

Penjelasan:
- Pada contoh ini, kita memiliki variabel `c` yang diinisialisasi dengan nilai 10.
- Blok instruksi di dalam repeat...until loop akan dijalankan.
- Pada setiap iterasi, nilai `c` akan dicetak menggunakan pernyataan `print`.
- Nilai `c` akan dikurangi 2 setiap kali iterasi dengan `c = c - 2`.
- Loop akan berhenti ketika nilai `c` menjadi negatif.

Output dari kode di atas adalah:

```
10
8
6
4
2
0
```

### For Loop dalam Lua

#### Apa itu For Loop?
For loop digunakan ketika kita sudah tahu berapa kali loop harus diulang. Kita dapat mengatur nilai awal, kondisi berhenti, dan langkah perubahan dalam loop ini. ibaratnya seperti saat kita memberikan instruksi pada seseorang untuk melakukan tugas tertentu berulang kali dalam urutan yang telah kita tentukan sebelumnya.

Bayangkan Anda berada di sebuah taman bermain seperti ghibli park / disneyland dengan lima tempat bermain yang berbeda. Anda diberi tugas untuk bermain di setiap tempat bermain sebanyak satu kali per tempatnya. Anda ingin memastikan Anda bermain di setiap tempat dengan urutan yang tepat sesuai tingkat keasikannya.

Dalam hal ini, Anda dapat menggunakan for loop untuk mengulangi tugas ini `5` kali. Anda memulai di tempat bermain pertama, kemudian berpindah ke tempat bermain berikutnya setiap kali Anda selesai bermain di tempat sebelumnya dan harus mengulang tugas tersebut pada tempat bermain berikutnya. Anda akan terus bergerak maju dari satu tempat ke tempat lain hingga Anda telah bermain di semua tempat.

Jadi, for loop memungkinkan kita untuk melakukan tugas berulang dengan mengikuti urutan yang telah ditentukan, mirip dengan cara kita bermain di setiap tempat bermain dengan urutan yang tepat di sebuah taman bermain.

#### Contoh Kode dan Penjelasan Cara Membacanya
Berikut adalah contoh kode for loop dalam Lua:

```lua
for i = 1, 5 do
    print(i)
end
```

Penjelasan:
- Kode di atas menghasilkan loop yang melakukan pengulangan dari 1 hingga 5.
- Variabel `i` diinisialisasi dengan nilai awal 1.
- Loop akan terus berjalan selama nilai `i` kurang

 dari atau sama dengan 5.
- Pada setiap iterasi, nilai `i` akan dicetak menggunakan pernyataan `print`.
- Loop akan berhenti ketika nilai `i` mencapai 6.

Output dari kode di atas adalah:

```
1
2
3
4
5
```

#### Contoh Kode Lainnya

```lua
for j = 10, 1, -2 do
    print(j)
end
```

Penjelasan:
- Pada contoh ini, kita memiliki variabel `j` yang diinisialisasi dengan nilai awal 10.
- Loop akan terus berjalan selama nilai `j` lebih besar dari atau sama dengan 1.
- Pada setiap iterasi, nilai `j` akan dicetak menggunakan pernyataan `print`.
- Nilai `j` akan dikurangi 2 setiap kali iterasi dengan `j = j - 2`.
- Loop akan berhenti ketika nilai `j` mencapai 0.

Output dari kode di atas adalah:

```
10
8
6
4
2
```

Dengan menggunakan loop, kita dapat mengulangi tugas dengan cara yang lebih efisien dan menghindari penulisan manual yang membosankan.

###### [<em>“” by Gillar Ajie Prasatya is licensed under CC-BY-SA-4.0</em>](https://github.com/muchamadyja/progstudymaterials/blob/main/LICENSE)

<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/80x15.png" /></a>
###### <em><span xmlns:dct="http://purl.org/dc/terms/" href="http://purl.org/dc/dcmitype/Text" property="dct:title" rel="dct:type">_03_perulangan_lua.md</span> by <a xmlns:cc="http://creativecommons.org/ns#" href="https://github.com/muchamadyja" property="cc:attributionName" rel="cc:attributionURL">Gillar Ajie Prasatya</a> is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a>.<br />Based on a work at <a xmlns:dct="http://purl.org/dc/terms/" href="https://github.com/muchamadyja/progjournal/tree/main/lua_origin" rel="dct:source">github.com/muchamadyja/progjournal</a>.</em>
###### [<em>click here for the license file</em>](https://github.com/muchamadyja/progjournal/blob/main/LICENSE)
