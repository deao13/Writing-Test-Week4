# Writing-Test-Week4
Writing Test Week 4

**Senin, 10 Oktober 2022**
### JS Intermediate - Asynchronous - Fetch and Async Await

#### Fetch
- API utama di sini adalah Fetch API. Ini memungkinkan JavaScript berjalan di halaman untuk membuat permintaan HTTP ke server untuk mengambil sumber daya tertentu. Saat server menyediakannya, JavaScript dapat menggunakan data tersebut untuk memperbarui halaman, biasanya dengan menggunakan API manipulasi DOM. Data yang diminta seringkali adalah JSON, yang merupakan format yang bagus untuk mentransfer data terstruktur, tetapi bisa juga berupa HTML atau hanya teks.
- Serangkaian file ini akan bertindak sebagai basis data palsu kami; dalam aplikasi nyata, kami akan lebih cenderung menggunakan bahasa sisi server seperti PHP, Python, atau Node untuk meminta data kami dari database. Namun, di sini, kami ingin tetap sederhana dan berkonsentrasi pada bagian sisi klien ini.
- Untuk memulai contoh ini, buat salinan lokal dari fetch-start.html dan empat file teks — verse1.txt, verse2.txt, verse3.txt, dan verse4.txt — di direktori baru di komputer Anda. Dalam contoh ini, kami akan mengambil ayat puisi yang berbeda (yang mungkin Anda kenali dengan baik) saat dipilih di menu tarik-turun.
- Tepat di dalam elemen <script>, tambahkan kode berikut. Ini menyimpan referensi ke elemen <select> dan <pre> dan menambahkan pendengar ke elemen <select>, sehingga saat pengguna memilih nilai baru, nilai baru tersebut diteruskan ke fungsi bernama updateDisplay() sebagai parameter.

1. Pertama, titik masuk ke Fetch API adalah fungsi global bernama fetch(), yang menggunakan URL sebagai parameter (dibutuhkan parameter opsional lain untuk setelan khusus, tetapi kami tidak menggunakannya di sini).
2. Selanjutnya, fetch() adalah API asinkron yang mengembalikan Promise. Jika Anda tidak tahu apa itu, baca modul tentang JavaScript asinkron, dan khususnya artikel tentang promise, lalu kembali ke sini. Anda akan menemukan bahwa artikel tersebut juga membahas tentang API fetch()!

Jadi karena fetch() mengembalikan sebuah promise, kita meneruskan sebuah fungsi ke dalam metode then() dari promise yang dikembalikan. Metode ini akan dipanggil ketika permintaan HTTP telah mendapat respon dari server. Di handler, kami memeriksa apakah permintaan berhasil, dan melontarkan kesalahan jika tidak. Jika tidak, kami memanggil response.text(), untuk mendapatkan isi respons sebagai teks.

Ternyata response.text() juga asinkron, jadi kita mengembalikan promise yang dikembalikannya, dan meneruskan fungsi ke dalam metode then() dari promise baru ini. Fungsi ini akan dipanggil ketika teks respons sudah siap, dan di dalamnya kita akan memperbarui blok kita dengan teks tersebut.

Terakhir, kita merangkai catch() handler di bagian akhir, untuk menangkap kesalahan apa pun yang dilemparkan ke salah satu fungsi asinkron yang kita panggil atau handlernya.

- Anda dapat menguji sendiri kasus kegagalan:
1. Buat salinan lokal dari file contoh.
2. Jalankan kode melalui server web (seperti dijelaskan di atas, dalam Melayani contoh Anda dari server).
3. Ubah jalur ke file yang sedang diambil, menjadi sesuatu seperti 'produce.json' (pastikan salah eja).
4. Sekarang muat file indeks di browser Anda (melalui localhost:8000) dan lihat di konsol pengembang browser Anda. Anda akan melihat pesan yang mirip dengan "Fetch problem: HTTP error: 404".


#### Async Await
- Pemrograman asinkron adalah teknik yang memungkinkan program Anda untuk memulai tugas yang berpotensi berjalan lama dan tetap dapat responsif terhadap kejadian lain saat tugas tersebut berjalan, daripada harus menunggu hingga tugas tersebut selesai. Setelah tugas itu selesai, program Anda disajikan dengan hasilnya.
- Banyak fungsi yang disediakan oleh browser, terutama yang paling menarik, berpotensi memakan waktu lama, dan oleh karena itu tidak sinkron. Sebagai contoh:
a. Membuat permintaan HTTP menggunakan fetch()
b. Mengakses kamera atau mikrofon pengguna menggunakan getUserMedia()
c. Meminta pengguna untuk memilih file menggunakan showOpenFilePicker()

-contoh coding untuk async await 
`let getAnime = async function() { try { let res= await fetch( "https://gegonime.herokuapp.com/popular" result.map((item) => { console.log(nama anime : ${animeTitle}`) }) ) catch (error) { console.log(error) } } }`







**Selasa, 11 Oktober 2022**
### Git & Github Lanjutan

#### Git
- Git adalah tools untuk programmer
- Git sebagai version control system
- Tugas dari version control system adalah mencatat setiap perubahan pada file (termasuk code yang kita buat) pada suatu proyek baik dikerjakan secara individu maupun tim
- Git adalah aplikasi yang dapat melacak setiap perubahan yang terjadi pada suatu folder atau file
- Git biasanya digunakan oleh programmer sebagai tempat menyimpan file pemrograman yang mereka buat, karna lebih efektif


#### Repository GIT
- Repository adalah direktori yang kita buat
`1 Repo = 1 Proyek = 1 Direktori`

- Membuat Repository
`git init proyek-01`

#### Conflict pada github
- Conflict terjadi jika ada 2 orang atau lebih yang melakukan perubahan pada file yang sama atau pada baris yang sama maka akan terjadi conflict pada saat pul request atau menggabungkan antar branch,adapun cara mengatasi conflict sebagai berikut :
1. Git pull dev terlebih dahulu untuk mendapatkan update terbaru
2. Setelah itu git merge dev pada project kita
3. Dan membenarkan code yang salah atau memilih code yang benar (diantara code yang conflict)
4. Setelah itu git add dan commit
5. Setelah itu lakukan git push origin -u origin “nama branch”
 

**Rabu, 12 Oktober 2022**
### Responsive Web Design

- Responsive Web Design adalah bertujuan membuat desain website kita dapat diakses dalam device apapun
- Device yang digunakan umumnya adalah laptop/PC, smartphone, dan tablet
- Setiap developer website wajib menggunakan tools bawaan dari setiap browser yang memudahkan proses development website
- Pada browser chrome biasa disebut dengan Chrome Dev Tools
- Kita dapat menggunakan Media Query untuk membuat web responsive adapun jenis media query adalah min-width dan max-widthh Co : @media Scree and (min-width:ur pixel) {} Adapun ada 2 cara atau pattern dalam menggunakan media query :
1. Membuat file css berbeda untuk masing-masing device
2. Menggabungkan file SCC untuk setting styling berbagai device

- Jenis media query
1. Media query untuk responsive web design umumnya hanya menggunakan 2 jenis media query
2. Keduanya yaitu min-width dan max-width

- Ada 2 cara/pattern dalam menggunakan media query
1. Membuat file css berbeda untuk masing-masing device
2. Menggabungkan 1 file css untuk setting styling berbagai device




#### Bootstrap 5
- Bootstrap 5 adalah versi terbaru dari salah satu front-end framework terbaik yang  cepat dan ringan. untuk membantu proses pengembangan website. Dengan Bootstrap, Anda tidak perlu menulis kode CSS yang panjang, karena Anda bisa langsung menggunakan semua elemen yang disediakan Bootstrap.
- Bootstrap adalah framework HTML, CSS, dan JavaScript yang berfungsi untuk mendesain website responsive dengan cepat dan mudah. 
- Kemudahan yang ditawarkan oleh Bootstrap adalah Anda tak perlu coding komponen website dari nol. Framework ini tersusun dari kumpulan file CSS dan JavaScript berbentuk class yang tinggal pakai. 

KEGUNAAN BOOTSTRAP
1. Menciptakan website Mobile Friendly —Berkat sistem grid, proses membuat website mobile friendly tak akan membutuhkan waktu lama.
2. Memudahkan resize gambar — Cukup dengan menambahkan class .img-responsive ke gambar, maka gambar tersebut akan otomatis di-resize sesuai ukuran layar pengguna.
3. Menambahkan elemen website tanpa ribet — Bootstrap menyediakan berbagai elemen yang bisa langsung Anda gunakan di website. Misalnya, navigasi, menu dropdown, thumbnail, dan sebagainya.
4. Membuat website lebih interaktif — Bootstrap juga memungkinkan Anda menggunakan plugin custom JQuery. Jadi, Anda bisa menambahkan berbagai elemen interaktif ke website dengan mudah. Misalnya, popup, transisi, image carousel, dan sebagainya.
 
Fungsi class pada bootstrap adalah sebagai berikut ini
1. class table berfungsi membuat tabel pada bootstrap
2. class .img-rounded untuk mengatur tampilan image menjadi rounded
3. class alert berfungsi untuk membuat panel yang berisi pesan pada bootstrap
4. class btn berfungsi untuk membuat sebuah button
 


