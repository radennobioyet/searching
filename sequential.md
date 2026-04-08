# JOBSHEET SEARCHING

# Percobaan 1

Pertanyaan
1. Jelaskan perbedaan metod tampilDataSearch dan tampilPosisi pada class MahasiswaBerprestasi!
2. Jelaskan fungsi break pada kode program di bawah ini! 
```
if (listMhs[j].ipk==cari){
    posisi=j;
    break;
}
```

3. Apa fungsi variabel pos atau indeks hasil pencarian dalam program sequential search?
4. Jika terdapat lebih dari satu data dengan nilai yang sama, hasil pencarian sequential search yang dibuat di atas akan menampilkan data ke berapa? Jelaskan.
5.	Berkaitan dengan pertanyaan nomor 2 di atas, apa yang terjadi jika perintah break dihapus dari kode di atas?





Jawaban 
1. Perbedaan metode tampilDataSearch dan tampilPosisi
tampilPosisi: Berfungsi hanya untuk menginformasikan lokasi indeks di mana data ditemukan. Outputnya sederhana, hanya memberitahu apakah data ada (beserta indeksnya) atau tidak ada.

tampilDataSearch: Berfungsi untuk menampilkan detail informasi lengkap dari objek yang ditemukan (NIM, Nama, Kelas, dan IPK). Metode ini memberikan visualisasi data yang lebih lengkap kepada pengguna daripada sekadar angka indeks.

2. Fungsi break digunakan untuk menghentikan paksa perulangan (for) segera setelah data yang dicari ditemukan. Hal ini dilakukan demi efisiensi program; jika data sudah ditemukan di awal, program tidak perlu lagi membuang waktu untuk mengecek sisa elemen array di bawahnya.

3. Variabel pos berfungsi sebagai penanda atau alamat hasil pencarian.

Jika bernilai selain -1 (misal: 0, 1, 2...): Menunjukkan lokasi spesifik elemen dalam array sehingga data tersebut bisa diakses kembali untuk ditampilkan atau dimanipulasi.

Jika bernilai -1: Berfungsi sebagai indikator (flag) bahwa proses pencarian telah selesai dilakukan namun data yang dicari tidak ditemukan di dalam array.

4. Jika terdapat lebih dari satu data dengan nilai IPK yang sama, program tersebut akan menampilkan data yang pertama kali ditemukan (indeks terkecil).

Penjelasan: Hal ini terjadi karena adanya perintah break. Begitu perulangan menemukan kecocokan pertama, break akan langsung menghentikan proses pencarian dan mengembalikan indeks tersebut, sehingga data serupa yang terletak setelahnya tidak akan pernah diperiksa.

5. Jika ada data ganda, variabel posisi akan terus diperbarui dan yang akan tersimpan adalah indeks dari data terakhir yang ditemukan (indeks terbesar).

Program menjadi kurang efisien karena melakukan iterasi yang tidak diperlukan setelah tujuan utama (menemukan data) sudah tercapai.