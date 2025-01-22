**NAMA: SRI GUSTINAH FAUZIAH**

**NIM: 20220801012**

**Fakultas/Prodi: Ilmu Komputer/ Teknik Informatika**

Soal

Buatlah Topologi dan Konfigurasi ruang lab praktikum Universitas Esa Unggul untuk masing masing kampus (CR, KHI, KJ) bagaimana agar mereka bisa terhubung dan terkoneksi dengan memanfaatkan routing statik, routing dinamik (BGP, RIP, OSPF), Kumpulkan semua ke github masing-masing.

**JAWABAN:**

Berikut adalah parafrase dari teks yang telah diberikan:

---

**Setiap kampus memerlukan IP publik yang disediakan oleh ISP untuk saling terhubung melalui jaringan internet.**  
Internet Service Provider (ISP) adalah layanan yang menyediakan akses internet kepada pengguna untuk terhubung secara daring. Di Indonesia, ISP lebih dikenal sebagai penyedia atau provider internet. Dalam kasus ini, ISP berfungsi sebagai jalur utama yang menghubungkan tiga kampus melalui jaringan publik. Untuk menjamin keamanan koneksi antar-kampus, digunakan VPN tunnel, yaitu teknologi yang menciptakan jalur aman di jaringan publik. VPN tunnel melindungi data dari penyadapan dan manipulasi dengan mengenkripsi data yang dikirimkan melalui jaringan tersebut.  

---

### **Penerapan Tunnel dan ISP untuk Koneksi Tiga Kampus**

1. **Konfigurasi Dasar pada Setiap Router**  
Setiap router yang ditempatkan di kampus KJ, CR, dan KHI dikonfigurasi dengan pengaturan dasar. Router ini menggunakan dua jenis alamat IP: IP lokal untuk jaringan internal kampus, dan IP publik yang disediakan ISP untuk mengakses internet dan koneksi antar-kampus melalui tunnel. DHCP server diaktifkan agar router dapat memperoleh IP secara otomatis. Selain itu, NAT (Network Address Translation) diaktifkan untuk mengubah IP lokal menjadi IP publik, memungkinkan perangkat internal mengakses internet secara aman dan efisien.

2. **Pengaturan Tunnel Antar-Lokasi**  
Setiap router di ketiga kampus (KJ, CR, dan KHI) dikonfigurasi untuk membuat tunnel ke IP publik dari router di kampus lain melalui jaringan ISP. Contohnya, router di KJ membuat tunnel ke IP publik dari router CR dan KHI, demikian juga sebaliknya. Dengan konfigurasi ini, jalur komunikasi langsung antar-kampus dapat dibuat menggunakan ISP sebagai media transportasi. Enkripsi pada tunnel memastikan data tetap aman selama perjalanan.

3. **Routing Statis untuk Mengatur Jalur Data**  
Routing statis digunakan untuk menentukan jalur yang diambil oleh data untuk mencapai tujuan. Sebagai contoh, router di KJ akan diarahkan ke tunnel menuju IP publik dari router di CR atau KHI sesuai kebutuhan. Dengan pengaturan ini, perangkat di ketiga kampus dapat saling berkomunikasi tanpa memerlukan konfigurasi tambahan pada perangkat lain di jaringan lokal.

---

**Kesimpulan**  
Dalam konfigurasi ini, ISP menyediakan IP publik yang menjadi penghubung antar-kampus. Sementara itu, VPN tunnel berperan menjaga privasi dan keamanan jalur komunikasi antar-kampus meskipun menggunakan jaringan publik.