# ⚔️ Glory Battleground

Game **roguelike arena 1 lawan 1** yang berjalan sepenuhnya di browser, dalam **satu file HTML** tanpa dependensi, tanpa instalasi, dan tanpa server.

Kamu melawan boss yang muncul terus-menerus tanpa istirahat. Setiap kali kalah, kamu kembali ke menu untuk membeli dan meng-upgrade senjata, menaikkan statistik, atau membeli item sekali pakai, lalu mengulang dari awal dengan tujuan menembus ronde sejauh mungkin.

---

## Daftar isi
- [Fitur utama](#fitur-utama)
- [Cara menjalankan](#cara-menjalankan)
- [Mode permainan](#mode-permainan)
- [Kontrol](#kontrol)
- [Cara kerja permainan](#cara-kerja-permainan)
- [Senjata](#senjata)
- [Statistik](#statistik)
- [Item](#item)
- [Kartu buff dan tingkat warna](#kartu-buff-dan-tingkat-warna)
- [Boss](#boss)
- [Dash dan super dash](#dash-dan-super-dash)
- [Pengaturan](#pengaturan)
- [Performa dan grafis](#performa-dan-grafis)
- [Penyimpanan data](#penyimpanan-data)
- [Detail teknis](#detail-teknis)
- [Kontribusi](#kontribusi)
- [Lisensi](#lisensi)

---

## Fitur utama
- 🎮 **3 mode**: Campaign (1000 ronde), Endless, dan Custom Sandbox.
- 🔫 **26 senjata** dengan gaya main berbeda, masing-masing bisa di-upgrade sampai **Lv 100**.
- 📈 **7 statistik** yang juga bisa dinaikkan sampai Lv 100.
- 🧪 **9 item aktif** dan **9 item spesial otomatis** (beberapa menambah risiko demi gold lebih banyak).
- 🎴 **Kartu buff** setelah tiap ronde, dengan sistem **tingkat warna Putih sampai Hitam**.
- 👹 **15 gaya serangan boss**, boss berbeda tiap ronde, dan peluru boss yang naik tingkat (Putih sampai Hitam) seiring ronde.
- 💨 **Dash** dan **super dash** dengan risiko benturan.
- ⚙️ **Pengaturan lengkap**: ubah shortkey, tembak otomatis, bidik otomatis, dan 4 tingkat grafis (termasuk **Ultra Potato**).
- 💾 Semua progres tersimpan otomatis di browser.

## Cara menjalankan
**Cara termudah:** unduh file `glory-battleground.html` (atau `index.html`), lalu buka dengan browser modern (Chrome, Edge, Firefox, atau Safari desktop). Selesai.

**Lewat GitHub Pages:**
1. Taruh file HTML di repositori ini (ganti namanya menjadi `index.html` supaya langsung terbuka).
2. Buka **Settings → Pages**, pilih branch yang berisi file tersebut, lalu simpan.
3. Mainkan di alamat `https://<username>.github.io/<nama-repo>/`.

> Tips: bermain dari file lokal biasanya lebih ringan daripada lewat halaman yang menyematkannya di dalam situs lain.

## Mode permainan
| Mode | Deskripsi |
|---|---|
| **Campaign** | Kalahkan boss di **1000 ronde** untuk menang. Boss dan serangannya **tetap sama** tiap kali main (tidak acak). |
| **Endless** | Tanpa akhir. Boss, nama, dan kombinasi serangannya **diacak tiap run**, dan serangan tiap ronde **dijamin berbeda** dari ronde sebelumnya. Rekor ronde tertinggi disimpan. |
| **Custom Sandbox** | Panggil boss apa saja (per gaya serangan, boss besar, boneka latihan), pakai senjata di level berapa pun, dan pakai item tanpa batas. **Tidak mengubah data simpananmu.** |

## Kontrol
Semua tombol keyboard di bawah adalah **default** dan bisa diubah di tab **⚙️ Pengaturan → Shortkey** (tiap aksi punya 3 slot tombol).

| Aksi | Default |
|---|---|
| Bergerak | `W` `A` `S` `D` atau panah |
| Membidik | Mouse |
| Menyerang | Klik kiri (tahan), atau tombol `J` |
| Dash (kebal sesaat) | Klik kanan, `Spasi`, atau `Shift` |
| Super dash | `F` |
| Ganti senjata | `Q`, `E`, `Ctrl`, atau scroll mouse |
| Toggle tembak otomatis | `G` |
| Item 1 sampai 9 | `1` sampai `9` |
| Jeda | `Esc` atau `P` |
| Memilih kartu | Klik kanan = balik kartu, klik kiri = pilih |

**Layar sentuh:** geser di sisi kiri untuk bergerak, sentuh di sisi kanan untuk membidik dan menembak, plus tombol di strip bawah (ganti senjata, dash, super dash, item, jeda).

**Pengguna touchpad laptop:** banyak laptop mengabaikan touchpad saat tombol keyboard ditekan, sehingga sulit menembak sambil bergerak. Aktifkan **Tembak otomatis** dan **Arah bidik: Musuh terdekat** di Pengaturan, jadi kamu cukup bergerak.

## Cara kerja permainan
1. **Pilih mode** dan senjata di loadout (maksimal 2 senjata, ganti saat bermain).
2. **Lawan boss.** Begitu boss kalah, kamu memilih satu kartu buff dan boss berikutnya langsung muncul.
3. **Kalah?** Kamu kembali ke menu. Gold yang didapat tetap milikmu. Upgrade senjata dan statistik yang sudah dibeli **tetap ada**, tetapi **item sekali pakai yang belum dipakai hangus**.
4. **Belanja dan ulangi.** Beli senjata baru, upgrade, naikkan statistik, lalu coba tembus ronde lebih jauh.

**Ekonomi:**
- Gold per ronde kira-kira `(14 + 2,6 × ronde)`, dikali 3 untuk boss besar (tiap 10 ronde) dan 3 lagi untuk mega boss (tiap 100 ronde), lalu dipengaruhi statistik Pemburu Harta dan item spesial. Kalah memberi sedikit gold hiburan.
- **Jual** senjata atau satu level upgrade (senjata maupun statistik) mengembalikan **50%** harga, jadi kamu bebas bongkar-pasang kombo.
- Level maksimal senjata dan statistik adalah 100.

## Senjata
Senjata starter adalah **Gun** (seimbang di semua sisi). Kolom DPS adalah perkiraan damage per detik ke satu target di Lv 0 (tanpa statistik), supaya bisa dibandingkan.

| Senjata | Tipe | Harga | DPS | Deskripsi |
|---|---|---|---|---|
| Gun | Proyektil | Gratis | ~36 | Seimbang di semua sisi. Senjata awal. |
| Pedang | Jarak dekat | 300 | ~48 | Tebasan lebar jarak dekat. Bisa menangkis peluru. |
| Shotgun | Proyektil | 350 | ~43 | 7 peluru sekali tembak. Mematikan dari dekat. |
| Busur | Proyektil | 400 | ~40 | Panah menembus 2 musuh. Pelan tapi tajam. |
| SMG | Proyektil | 450 | ~40 | Hujan peluru cepat, agak liar. |
| Tombak | Jarak dekat | 500 | ~42 | Tusukan panjang dan sempit. Jarak aman lebih jauh. |
| Boomerang | Lemparan | 600 | ~40 | Pergi lalu kembali: kena dua kali. |
| Sniper | Proyektil | 650 | ~44 | Satu tembakan besar, menembus 4 musuh. |
| Flamethrower | Api | 800 | ~42 | Semburan api pendek yang membakar. |
| Tongkat Tesla | Petir | 850 | ~40 | Petir melompat ke 3 target. Cocok lawan minion. |
| Roket | Ledakan | 900 | ~38 | Ledakan area. Lambat tapi menggelegar. |
| Railgun | Sinar | 1.100 | ~40 | Sinar instan menembus semuanya dalam garis. |
| Sabit | Jarak dekat | 750 | ~45 | Tebasan hampir 360°. Mencuri 5% damage jadi HP. |
| Gergaji Pantul | Gergaji | 700 | ~40 | Gergaji memantul di dinding dan menggerus berulang. Maks 3 aktif. |
| Peluncur Ranjau | Jebakan | 800 | ~55 | Lempar ranjau ke kursor. Meledak saat musuh dekat. Maks 5. |
| Menara Otomatis | Menara | 950 | ~36 | Pasang menara yang menembak musuh terdekat selama 9 detik. Maks 2. |
| Tongkat Meteor | Area | 1.000 | ~40 | Tandai area di kursor, meteor jatuh 0,85 detik kemudian. |
| Bilah Orbit | Orbit | 850 | ~38 | Bilah berputar di sekitarmu 2,6 detik dan menangkis peluru. Jumlah bilah naik seiring level. |
| Pistol Ganda | Proyektil | 600 | ~41 | Menembak dari 2 laras sekaligus. Laras bertambah di level tinggi. |
| Pistol Pantul | Proyektil | 650 | ~33 | Peluru memantul di dinding arena. Cocok untuk menembak dari sudut. |
| Belati Kembar | Jarak dekat | 400 | ~41 | Tebasan super cepat jarak sangat dekat. |
| Granat Lontar | Granat | 900 | ~40 | Lempar granat ke kursor, meledak setengah detik setelah mendarat. |
| Rudal Pelacak | Proyektil | 1.000 | ~33 | Peluru mengejar musuh terdekat. Jumlah rudal naik seiring level. |
| Laser Terus | Sinar | 1.000 | ~23 | Sinar tipis nonstop berjangkauan sedang (menembus semua musuh dalam garis). |
| Palu Gempa | Gempa | 1.100 | ~46 | Hantaman area di depanmu. Juga menghapus peluru musuh. |
| Lubang Hitam | Zona | 1.300 | ~33 | Lubang di kursor: melukai, memperlambat musuh, dan memakan peluru. |

Tiap level menaikkan damage dan kecepatan serang, dan beberapa senjata juga menambah jumlah/batasnya (misalnya jumlah peluru, tembusan, menara, ranjau, atau bilah). Warna senjata berubah mengikuti level: **Putih → Biru → Hijau → Kuning → Oranye → Merah → Ungu → Hitam**, dan Hitam (dengan outline putih) hanya di level maksimal.

## Statistik
| Statistik | Lv 0 | Lv 100 |
|---|---|---|
| Vitalitas | Max HP 100 | Max HP 1300 |
| Kekuatan | Damage +0% | Damage +300% |
| Kelincahan | Kecepatan +0.0% | Kecepatan +80.0% |
| Fokus Kritis | Peluang kritis 5.0% (x2 damage) | Peluang kritis 75.0% (x2 damage) |
| Regenerasi | Regen 0.0 HP/detik | Regen 15.0 HP/detik |
| Pemburu Harta | Gold +0% | Gold +300% |
| Dash Gesit | Cooldown dash 1.50 detik | Cooldown dash 0.60 detik |

## Item
### Item aktif (dipakai manual, tombol 1 sampai 9)
| Tombol | Item | Harga | Efek |
|---|---|---|---|
| 1 | Ramuan Heal | 120 | Pulihkan 50% HP. |
| 2 | Bom | 180 | Ledakan besar: melukai musuh sekitar dan menghapus peluru. |
| 3 | Perisai | 200 | Kebal selama 6 detik. |
| 4 | Elixir Rage | 220 | Damage x2 selama 10 detik. |
| 5 | Bekukan | 170 | Bekukan semua musuh 4 detik. |
| 6 | Bulu Phoenix | 450 | Pasif: bangkit sekali dengan 60% HP saat mati. |
| 7 | Jam Pasir | 260 | Musuh, peluru, dan serangan melambat 60% selama 6 detik. |
| 8 | Kristal Fokus | 240 | Semua seranganmu kritis selama 8 detik. |
| 9 | Adrenalin | 230 | Kecepatan +50% dan dash tanpa cooldown selama 8 detik. |

### Item spesial (otomatis sepanjang run)
Tidak perlu ditekan. Seperti item lain, semuanya hangus saat run berakhir.

| Item | Harga | Maks | Efek |
|---|---|---|---|
| Round Skipper | 150 | 10 | Otomatis di awal run: lompati 1 ronde per item (dapat 50% gold ronde yang dilewati). |
| Buff Stacker | 300 | 10 | Otomatis: tiap 1 item menahan 1 kartu buff sebelumnya, jadi buff menumpuk sampai ronde berikutnya. |
| Darah Raksasa | 200 | 10 | Otomatis: HP boss +25% per tumpuk, tapi gold +20% per tumpuk. |
| Peluru Terkutuk | 260 | 7 | Otomatis: peluru dan minion boss naik 1 level warna per tumpuk (damage naik), gold +25% per tumpuk. |
| Perisai Awal | 220 | 10 | Otomatis: tiap ronde dimulai dengan menyerap 1 serangan per tumpuk. |
| Koin Rejeki | 180 | 10 | Otomatis: gold tiap ronde +10% per tumpuk. |
| Berkah Ronde | 180 | 10 | Otomatis: pulih 8% HP per tumpuk di awal tiap ronde. |
| Shortening Round | 500 | 9 | Khusus Campaign: tiap 1 item memangkas 100 ronde (maks 900, jadi tinggal 100 ronde). Musuh makin kuat per tumpuk (HP +200%, damage +150%), tapi kamu juga dapat buff (HP maks +60%, damage +80%, kecepatan +2%) yang lebih kecil dari buff musuh. Gold +50% per tumpuk. |
| Weakened Self | 200 | 10 | Dirimu melemah: HP maks dan damage -7%, kecepatan -4% per tumpuk. Sebagai gantinya gold +20% per tumpuk. |

## Kartu buff dan tingkat warna
Setelah tiap ronde kamu menerima **3 kartu acak** (tidak bisa di-refresh). Kartu tampil dengan sisi belakang berisi ikon; **klik kanan** untuk membalik dan membaca efeknya, lalu **klik kiri** untuk memilih. Efek kartu hanya berlaku di **ronde berikutnya** lalu hilang (kartu lama diganti kartu baru), kecuali kamu punya item **Buff Stacker**.

Tiap kartu punya **tingkat warna**. Putih paling sering muncul dan tanpa penguatan, Hitam paling langka dan paling kuat.

| Tingkat | Peluang kartu | Kekuatan efek | Peluru boss mulai ronde | Pengali damage peluru boss |
|---|---|---|---|---|
| Putih | 40% | ×1 | 1 | ×1 |
| Biru | 25% | ×1.25 | 35 | ×1.2 |
| Hijau | 15% | ×1.5 | 90 | ×1.45 |
| Kuning | 9% | ×1.8 | 170 | ×1.75 |
| Oranye | 5.5% | ×2.2 | 280 | ×2.1 |
| Merah | 3.5% | ×2.7 | 430 | ×2.5 |
| Ungu | 1.5% | ×3.3 | 640 | ×3 |
| Hitam | 0.5% | ×4 | 880 | ×3.6 |

Kartu yang tersedia (nilai di bawah adalah efek dasar tingkat Putih):

| Kartu | Efek dasar |
|---|---|
| Pemulihan | Pulihkan 30% HP sekarang. |
| Amarah | +30% damage di ronde berikutnya. |
| Angin Badai | +30% kecepatan gerak, dash 30% lebih cepat pulih. |
| Tembakan Cepat | +35% kecepatan serang. |
| Mata Elang | +25% peluang kritis. |
| Kulit Baja | Damage yang diterima -30%. |
| Haus Darah | Curi 6% damage jadi HP. |
| Perisai Arcane | Menyerap 3 serangan berikutnya. |
| Tembus | Peluru menembus +2 musuh, tebasan lebih lebar. |
| Serakah | Gold ronde berikutnya x2. |
| Waktu Melambat | Boss bergerak dan menyerang 25% lebih lambat. |
| Berkat Alam | Regenerasi +4 HP/detik. |
| Berkat Kembar | Heal 15% sekarang dan +15% damage. |
| Taruhan Berani | +60% damage, tapi damage diterima +30%. |

## Boss
- Setiap ronde punya boss berbeda (warna, bentuk, nama, kecepatan, dan kombinasi serangan).
- Boss besar muncul tiap **10 ronde**, mega boss tiap **100 ronde**, dan boss terakhir Campaign adalah **THE GLORY KING**.
- **15 gaya serangan:** Tembak, Kipas, Cincin, Spiral, Dash, Minion, Bom, Laser, Teleport, Gelombang, Hujan, Salib, Pemburu, Tembok, Sapuan.
- **Peluru dan minion boss mengikuti tingkat warna.** Semakin jauh ronde, semakin tinggi tingkatnya (damage naik per tingkat). Di ronde-ronde akhir semua peluru berwarna **Hitam** dengan outline putih.
- HP boss kira-kira `180 × (1 + 0,09 × (ronde − 1))^1,1`, dikali 2,2 untuk boss besar dan 2,5 lagi untuk mega boss.

## Dash dan super dash
| | Dash | Super dash |
|---|---|---|
| Tombol | Klik kanan / Spasi / Shift | `F` |
| Cooldown | 1,5 detik (turun lewat statistik) | 3× cooldown dash |
| Efek | Meluncur singkat, kebal sesaat | Meluncur jauh dan cepat, menangkis peluru, memberi damage dan dorongan ke boss dan minion, plus gempa saat mendarat |
| Menabrak musuh | −5% HP saat ini | −10% HP saat ini |
| Menabrak dinding | −10% HP saat ini | −20% HP saat ini |

- Penalti benturan tidak pernah membunuhmu (HP minimal 1) dan hanya terjadi sekali per dash.
- Selama super dash cooldown, dash biasa juga terkunci.
- Damage super dash dihitung dari rata-rata DPS senjata di slot 1 dan 2, lalu dikali buff statistikmu.

## Pengaturan
Tab **⚙️ Pengaturan** di menu berisi:
- **Grafis**: Ultra Potato / Hemat / Sedang / Tinggi.
- **Turunkan grafis otomatis** saat FPS terus rendah.
- **Tampilkan FPS** (penghitung kecil di pojok arena).
- **Tembak otomatis** dan **Arah bidik** (kursor atau musuh terdekat).
- **Shortkey**: ubah semua tombol, 3 slot per aksi, dengan penanganan bentrok tombol otomatis.

## Performa dan grafis
| Tingkat | Resolusi render | Catatan |
|---|---|---|
| **Ultra Potato** | 40% | Tanpa partikel dan angka damage, gambar paling minimal, 30 FPS gambar. Dibuat untuk **membuktikan game bisa berjalan lancar bahkan di perangkat sangat lemah, termasuk ponsel**. Ini bukan tampilan khusus HP (layout tetap untuk desktop). |
| Hemat | 60% | Efek dikurangi, 30 FPS gambar. |
| Sedang | 80% | Sebagian efek. |
| Tinggi | 100% | Semua efek. |

Beberapa optimasi yang dipakai: latar arena digambar sekali lalu dipakai ulang, peluru digambar per kelompok warna, batas jumlah partikel/peluru/teks per tingkat grafis, dan penurunan grafis otomatis.

Default grafis dipilih otomatis berdasarkan jumlah core CPU dan memori perangkat yang dilaporkan browser.

## Penyimpanan data
Semua data disimpan di **localStorage** browser kamu (tidak ada server, tidak ada akun):
- `glory_battleground_v1`: gold, senjata, statistik, item, rekor.
- `gb_settings`: grafis, kontrol tembak, dan shortkey.

Tombol **Hapus semua data save** di bagian bawah menu mereset progres. Menghapus data situs di browser juga mereset semuanya. Data tidak ikut berpindah antar browser atau perangkat.

## Detail teknis
- Satu file HTML berisi HTML, CSS, dan JavaScript (tanpa framework dan tanpa library eksternal).
- Rendering memakai **Canvas 2D** (resolusi logis 960×600, di-skala sesuai tingkat grafis). HUD berupa elemen DOM di luar arena supaya tidak menutupi permainan.
- Logika game berjalan dengan `requestAnimationFrame`, langkah waktu dibatasi (maks 50 ms) agar stabil.
- Boss dibuat secara prosedural dari seed per ronde (deterministik di Campaign, acak per run di Endless).

## Kontribusi
Saran dan perbaikan dipersilakan lewat issue atau pull request. Beberapa area yang menarik untuk dikembangkan: senjata dan boss baru, kartu buff baru, tata letak khusus layar sentuh, dan efek suara.

## Lisensi
Belum ditentukan. Tambahkan berkas `LICENSE` (misalnya MIT) sesuai keinginanmu sebelum dipublikasikan.
