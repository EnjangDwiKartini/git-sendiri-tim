# GIT dan Cara Kerjanya 

## Apa itu GIT ? 

Git adalah Version Control System (VCS) untuk melacak perubahan pada sebuah file dan mengkoordinasikan file tersebut diantara banyak orang, umumnya digunakan untuk manajemen source code pada pengembangan perangkat lunak (software development). Git diciptakan oleh Linus Torvalds yang juga merupakan pencipta Kernel Linux. 
Git tidaklah sama dengan GitHub, namun GitHub merupakan bagian dari Git. Git adalah sebuah metode, sedangkan GitHub adalah alat untuk mengoperasikan metode itu. Github adalah situs hosting perangkat lunak VCS yang kebanyakan digunakan untuk menyimpan kodepemrograman. Tidak hanya itu saja, Github juga memberikan layanan pengelolaan source code yang juga diturunkan dari fitur Git.

## Kelebihan menggunakan GIT 

* Memudahkan dalam bekerja sama 
    Dalam pembuatan software tentu lebih mudah jika kita membuatnya bersama dengan orang lain. Seperti tujuan dibuatnya Git, kita akan lebih mudah mengolah kode dari para programmer. Dengan adanya fitur "branch" yang memungkinkan setiap programmer dapat membuat cabang sebagai wilayah kerjanya dan masing-masing dapat mengambil file dari branch yang lain lalu mengeditnya dan menyimpannya di branch-nya sendiri. Juga terdapat fitur "message" yang dapat memberi keterangan bagian mana yang direvisi. Jika mengabungkan kedua fitur tersebut kita bisa memperoleh informasi kapan waktu direvisi, siapa yang merevisi dan bagian mana yang direvisi.
* Mempermudah mencari dan memperbaiki error
    Berkat kedua fitur diatas, kita bisa lebih mudah menemukan letak error dan memperbaikinya karena bukan hanya kita saja yang berfikir tetapi juga dibantu orang lain. Setelah letak error ditemukan, kita dapat memberikan keterangan bahwa terdapat error dibagian ini sehingga semua anggota mengetahui. Jika setelah kita melakukan perubahan lalu terjadi error padahal sebelumnya normal, kita bisa mengembalikan ke versi sebelumnya, inilah yang disebut restore point
* Lebih cepat dan efisien
    Hal ini karena hampir semua operasinya dilakukan secara lokal. Umumnya operasi yang dilakukan hanya membutuhkan berkas dan resource lokal sehingga tidak perlu informasi dari komputer yang lain. Misalnya jika ingin melihat history dari proyek yang sedang dikerjakan, Git tidak perlu mengakses data history dari server melainkan Git membaca history langsung dari database lokal. Contoh lain yaitu jika ingin membandingkan perbedaan atau perubahan dengan versi sebelumnya misal sebulan yang lalu, Git akan mencari berkas tersebut pada history lokal sebulan kebelakang lalu melakukan pembandingan dengan yang sekarang secara lokal, tidak dengan cara meminta server untuk mengirimkan berkas sebulan yang lalu kemudian membandingkannya.
* Memiliki integritas SHA-1
    Segala perubahan pada berkas Git akan melewati proses checksum terlebih dahulu sebelum disimpan dan hasil checksum tersebut digunakan untuk mereferensikan perubahan yang dilakukan. Hal ini mengakibatkan tidak mungkin melakukan perubahan terhadap berkas tanpa diketahui oleh sistem Git. Mekanisme checksum yang digunakan oleh Git yaitu SHA-1 hash. 

## Perintah Dasae GIT 

- git init untuk membuat repo lokal baru pada perintah ini akan dibuat sebuah folder baru yang bernama ".git"
- *git status* untuk melihat status dari repo lokal
- *git add* untuk menambahkan file ke dalam repo yang sebelumnya sudah dibuat
- *git commit* untuk menyimpan seluruh perubahan yang terjadi
- *git pull / push* untuk menyimpan dan mengambil data dari remote repo
- *git checkout* untuk pindah branch
- *git diff* untuk membandingkan perubahan file
- *git merge* untuk melakukan penggabungan antar branch
- *git remote* untuk menambahkan remote repo baru
- *git reset* untuk membatalkan perubahan pada repo lokal

## Cara Kerja GIT

* *Modified* adalah kondisi dimana revisi atau perubahan sudah anda lakukan tetapi belum ditandai dan belum disimpan di version control.
* *Staged* adalah kondisi dimana revisi sudah ditandai tetapi belum disimpan di version control.
* *Committed*  adalah kondisi dimana revisi sudah disimpan di version control.

Cara kerja git ini memanfaatkan repositori online dan offline, contohnya kita punya folder/directory project di lokal (offline), folder tersebut bisa kita upload ke repositori online yang sudah disediakan banyak pihak, setelah di upload kita bisa meng-clone(istilahnya copas) lalu setelah di clone maka orang  lain bisa mengubah isi file pada project tersebut secara lokal. Jika kita ingin menambah atau mengurangi code yang ada pada file, mereka harus upload ke repository terlebih dahulu, kemudian tim atau teman kita yang  lain  jika ingin mendapatkan update harus mendownload lagi repositorinya, namun file yang di download ini sesuai dengan perubahan yang dilakukan oleh kita.

![alt text](https://github.com/EnjangDwiKartini/git-sendiri-tim/blob/master/struktur-git.png "struktur-git")

Secara umum caha kerja GIT adalah sebagai berikut :
* Membuat repository menggunakan Git hosting.
* Menyalin repository ke lokal.
* Menambahkan file ke dalam lokal repository.
* “Push” perubahan pada lokal repository ke master branch.
* Melakukan perubahan pada file dan melakukan commit.
* “Pull” perubahan ke komputer lokal.
* Membuat “branch”.
* Membuka “pull request”.
* “Merge” branch ke master branch.

## Fitur - fitur unggulan GIT 

1. Version control system yang terdistribusi, GIT menggunakan pendekatan peer to peer, tidak seperti yang lainnya seperti Subversion (SVN) yang menggunakan model client-server.
2. GIT memungkinkan developer untuk memiliki branch kode yang independent dan massive. Membuat, menghapus dan menggabungkan branch tersebut menjadi lebih cepat, lancar dan tidak butuh waktu yang lama.
3. dalam GIT, semua operasinya bersifat atomic, artinya sebuah tindakan akan benar-benar diselesaikan dengan lengkap atau sama sekali gagal. Ini sangat penting, karena di beberapa version control system seperti CVS, operasinya bersifat non-atomic. Jika ada operasi yang ‘gantung’ dan terkait dengan repository, kondisi repository menjadi tidak stabil.
4. Dalam GIT, semuanya disimpan dalam folder .git. Berbeda dengan VCS lain seperti SVN atau CVS, dimana metadata file disimpan dalam folder tersembunyi seperti .cvs, .svn, .etc.
5. GIT menggunakan data model yang membanti memastikan integritas cryptographic apapun ada dalam repository. Setiap kali sebuah file ditambahkan atau di-commit, checksum-nya akan diciptakan; sama hal nya, juga di-retrieve lewat checksum-nya juga.
6. Fitur menarik lainnya yang ada di GIT adalah staging area atau index. Dengan stagin area, developer bisa memformat commit dan membuatnya bisa di-review sebelum benar-benar diterapkan.

## Collaborative Development Models 
Proyek di GitHub Enterprise dapat menggunakan dua jenis model pengembangan kolaboratif yang disebut fork & pull dan shared repository model .
### Fork & Pull
Model fork & pull memungkinkan siapa pun menggunakan repositori yang ada dan mendorong perubahan ke github pribadi mereka tanpa memerlukan akses  ke repositori sumber. Perubahan kemudian harus ditarik ke dalam repositori sumber oleh pengelola proyek. Model ini  populer dengan proyek sumber terbuka karena memungkinkan orang untuk bekerja secara mandiri tanpa koordinasi di awal.

### Shared Repository Models / Model Repositori Bersama 
Model repositori bersama dapat digunakan untuk  berkolaborasi dalam proyek-proyek pribadi. Setiap orang diberikan akses push ke satu repositori bersama dan cabang topik digunakan untuk mengisolasi perubahan.
Pada proyek pengembangan software yang melibatkan banyak orang (tim), kita tidak hanya akan menyimpan sendiri repository proyeknya.
Semua tim yang terlibat dalam pengkodean (coding) akan menyimpan repository lokal di komputernya masing-masing.
Setelah itu, akan dilakukan penggabungan ke repository inti atau remote.
Biasanya akan ada repository pusat atau untuk menyimpan source code yang sudah digabungkan (merge) dari beberapa orang.

![alt text](https://github.com/EnjangDwiKartini/git-sendiri-tim/blob/master/git-tim.png "git-tim")