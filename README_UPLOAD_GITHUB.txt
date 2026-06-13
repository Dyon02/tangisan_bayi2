CARA UPLOAD AGAR MODEL BISA LOAD DI GITHUB PAGES

PENTING:
1. HAPUS file .gitattributes di repository GitHub.
2. JANGAN pakai Git LFS untuk file .bin, karena file .bin model ini kecil-kecil sekitar 4 MB per shard.
3. HAPUS folder models lama di GitHub, lalu upload folder models dari ZIP ini.
4. HAPUS index.html lama, lalu upload index.html dari ZIP ini.
5. Setelah upload, tunggu 1-3 menit, buka GitHub Pages, lalu tekan Ctrl + Shift + R.

Struktur wajib di root repository:
index.html
cek-model.html
models/cnn/model.json
models/cnn/group1-shard1of14.bin ... group1-shard14of14.bin
models/cnn_lstm/model.json
models/cnn_lstm/group1-shard1of3.bin ... group1-shard3of3.bin
models/rnn/model.json
models/rnn/group1-shard1of1.bin

CARA CEK:
Buka halaman:
https://USERNAME.github.io/NAMA_REPO/cek-model.html

Kalau tertulis LOADED, model sudah terbaca.
Kalau tertulis LFS POINTER, artinya .bin masih ke-upload sebagai Git LFS dan harus dihapus lalu upload ulang tanpa .gitattributes.
