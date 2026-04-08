# JOBSHEET SEARCHING

# Percobaan 2

Pertanyaan
1.	Tunjukkan pada kode program yang mana proses divide dijalankan!
2.	Tunjukkan pada kode program yang mana proses conquer dijalankan!
3.	Apa fungsi left, right, dan mid?
4.	Jika data IPK yang dimasukkan tidak urut. Apakah program masih dapat berjalan? Mengapa demikian?
5.	Jika IPK yang dimasukkan dari IPK terbesar ke terkecil (misal: 3.8, 3.7, 3.5, 3.4, 3.2) dan elemen yang dicari adalah 3.2. Bagaimana hasil dari binary search? Apakah sesuai? Jika tidak sesuai maka ubahlah kode program binary seach agar hasilnya sesuai
6.	Jelaskan bagaimana binary search menentukan bahwa data yang dicari tidak ditemukan di dalam array.
7.	Modifikasi program di atas yang mana jumlah mahasiswa yang diinputkan sesuai dengan masukan dari keyboard.





Jawaban
1. Terjadi pada baris: mid = (left + right) / 2;
Program membagi rentang pencarian menjadi dua bagian tepat di tengah.

2. Terjadi pada pemanggilan rekursif:
return findBinarySearch(cari, left, mid - 1); atau return findBinarySearch(cari, mid + 1, right);
Program memilih salah satu bagian untuk dicari lebih lanjut hingga ketemu.

3. left: Indeks batas bawah (awal) pencarian.
right: Indeks batas atas (akhir) pencarian.
mid: Indeks titik tengah sebagai acuan pembanding.

4. Tidak Akurat. Program tetap jalan, tapi hasil salah karena logika Binary Search membuang setengah data berdasarkan asumsi urutan. Jika tidak urut, data yang dicari bisa saja berada di bagian yang "dibuang".

5. Hasil: Data kemungkinan besar tidak ditemukan (-1) karena logika kode asli mencari ke arah yang salah.
Modifikasi Kode: Tukar operator perbandingannya.
```
// Ubah bagian else if pada findBinarySearch
else if (listMhs[mid].ipk < cari) { // Jika mid lebih kecil, cari ke kiri
    return findBinarySearch(cari, left, mid - 1);
} else { // Jika mid lebih besar, cari ke kanan
    return findBinarySearch(cari, mid + 1, right);
}
```

6. Binary search berhenti dan menyatakan data tidak ada melalui kondisi if (right >= left). Jika area pencarian terus mengecil hingga nilai left lebih besar dari right, artinya seluruh area sudah diperiksa dan fungsi akan mengeksekusi return -1.

7. 
```
System.out.print("Masukkan jumlah mahasiswa: ");
int jumMhs = sc.nextInt();
sc.nextLine(); // Membersihkan buffer

// Inisialisasi ulang array di class MahasiswaBerprestasi9
list.listMhs = new Mahasiswa19[jumMhs];

for (int i = 0; i < jumMhs; i++) {
    // ... proses input data seperti biasa
}
```