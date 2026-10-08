1. Layar Menu (MenuScreen)
Masalah: Tampilan menu terpotong/error (overflow) saat layar HP terlalu pendek atau daftar menu terlalu panjang.

Penyebab: Tampilan dibuat statis tanpa menyesuaikan ukuran layar dan langsung memuat seluruh menu sekaligus.

Solusi: Menggunakan batas ukuran layar (600 dp). Jika di HP, menu tampil sebagai daftar (list). Jika di tablet, menu otomatis berubah menjadi petak (grid). Keduanya kini menggunakan sistem scroll yang lebih hemat memori (lazy loading).

2. Header Toko (StoreHeader)
Masalah: Nama toko dan bagian ulasan/rating bertabrakan di layar HP yang sempit.

Penyebab: Teks dan elemen di dalam baris tidak diberi batasan lebar.

Solusi: Memberikan ruang tersisa untuk informasi toko menggunakan Expanded, serta membatasi teks yang terlalu panjang dengan tanda titik-titik (...) di akhirnya.

3. Kategori Pilihan (CategoryBar)
Masalah: Tombol-tombol filter kategori melebihi batas kanan layar.

Penyebab: Baris tombol dibuat kaku ke samping tanpa fitur usap (scroll).

Solusi: Mengubah baris filter agar bisa diusap/digeser ke samping (horizontally scrollable).

4. Kartu Promo (PromoStrip / PromoCard)
Masalah: Kartu promo terpotong, dan aplikasi crash (rusak) jika promo kurang dari dua.

Penyebab: Ukuran kartu tidak menyesuaikan layar, dan sistem menganggap promo selalu ada minimal dua.

Solusi: Ukuran kartu kini fleksibel mengikuti lebar layar. Jika tidak ada promo, bagian ini disembunyikan. Teks promo yang panjang juga dibatasi agar tidak meluap.

5. Baris Item Menu (MenuTile)
Masalah: Nama makanan/minuman yang panjang mendorong harga dan tombol "Tambah" keluar dari layar.

Penyebab: Teks tidak fleksibel dan tidak punya batas lebar.

Solusi: Mengatur kolom teks agar menggunakan ruang yang tersedia saja, dan memotong teks yang kepanjangan dengan tanda titik-titik (...).

6. Kartu Menu Tablet (MenuCard)
Masalah: Gambar dan teks menu terpotong pada tampilan grid tablet.

Penyebab: Ukuran gambar dikunci (fixed size) dan teks tidak dibatasi.

Solusi: Mengatur proporsi gambar menggunakan rasio layar (AspectRatio) dan membatasi jumlah baris teks.

7. Bar Keranjang Belanja (CartBar)
Masalah: Tombol dan rincian keranjang di bagian bawah terpotong di HP kecil, atau tertutup oleh bar navigasi bawaan HP.

Penyebab: Tinggi dan lebar bar dikunci secara manual tanpa memperhitungkan area aman layar.

Solusi: Menghapus ukuran kaku, membatasi panjang teks ringkasan, dan membungkusnya dengan SafeArea agar tidak tertutup tombol navigasi HP.

8. Tampilan Menu Kosong (Empty menu)
Masalah: Saat tidak ada menu, aplikasi malah bingung mencari promo dan akhirnya error.

Penyebab: Belum ada tampilan khusus ketika data kosong.

Solusi: Menambahkan layar empty state khusus yang menampilkan ikon, pesan informasi, serta tombol untuk menghapus filter.