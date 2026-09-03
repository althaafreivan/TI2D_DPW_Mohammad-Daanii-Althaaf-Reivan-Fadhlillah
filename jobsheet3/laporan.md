# Jobsheet 3
Nama: Mohammad Daanii Althaaf Reivan Fadhlillah <br>
Kelas: TI 2D <br>
NIM: 254107020123 <br>


## Tugas Mandiri
1. Penerapan desain responsif pada seluruh halaman termasuk halaman Anggota (viewport meta, navbar hamburger dengan checkbox hack, scroll horizontal tabel data, dan kartu statistik multi-breakpoint):

## Latihan Reflektif

1. `<meta name="viewport">` wajib dipasang di setiap file HTML agar browser mobile tidak mengasumsikan lebar layar 980px (zoom-out otomatis), sehingga media query dapat mengenali ukuran layar fisik perangkat secara akurat.
2. Teknik *checkbox hack* memanfaatkan checkbox tersembunyi sebagai penyimpan status (*state*) yang dikendalikan oleh `<label>`, kemudian menggunakan selector `.nav-toggle:checked ~ nav` untuk memunculkan menu tanpa memerlukan JavaScript.
3. Tabel data dibungkus dengan `<div class="table-responsive">` yang diberi `overflow-x: auto` karena elemen `<table>` sulit membatasi lebarnya sendiri, sehingga pembungkus tersebut membatasi lebar sesuai kontainer layar dan menyediakan scrollbar horizontal lokal.


---
### Self Question
1. Kenapa di jobsheet ini memakai pendekatan *desktop-first* (`max-width`) daripada *mobile-first* (`min-width`), dan kapan situasi yang tepat untuk memilih salah satunya?
2. Apakah penggunaan *checkbox hack* untuk menu hamburger ramah terhadap aksesibilitas (*screen reader* dan navigasi keyboard) dibandingkan kontrol tombol berbasis JavaScript?

### Notes
1. `<meta name="viewport" content="width=device-width, initial-scale=1">` adalah syarat mutlak agar styling responsif dan breakpoint media query bekerja di perangkat mobile.
2. Sibling combinator (`~`) hanya dapat memilih elemen saudara yang berada di level yang sama dan terletak setelah elemen pemicu pada struktur HTML.
3. Media query pada strategi *desktop-first* harus ditulis di baris paling bawah file CSS agar aturan override dapat menimpa gaya dasar secara tepat.
4. `overflow-x: auto` hanya menampilkan scrollbar ketika konten melebar melebihi kontainer pembungkusnya, berbeda dengan `scroll` yang selalu memunculkan scrollbar.
5. Grid kartu statistik diatur bertahap melalui media query: 3 kolom (desktop), 2 kolom (tablet ≤768px), dan 1 kolom bertumpuk (mobile ≤480px).
6. Mengubah `flex-direction` menjadi `column` pada navbar saat layar mobile membuat susunan tautan menu tersusun vertikal dan lebih ramah sentuhan di layar ponsel.
