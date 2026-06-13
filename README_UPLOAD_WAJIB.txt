WAJIB BACA - CARA UPLOAD AGAR MODEL TIDAK GAGAL

Masalah utama jika muncul error:
- tensor should have 128 values but has 78 / 33
- Failed to load model

Penyebabnya: file .bin di GitHub masih berupa Git LFS POINTER, bukan file binary model asli.
Ciri file salah jika dibuka raw muncul teks:
version https://git-lfs.github.com/spec/v1

SOLUSI WAJIB:
1. Di GitHub repo, hapus folder models yang lama.
2. Hapus file .gitattributes jika ada.
3. Upload ulang folder models dari ZIP ini.
4. Jangan gunakan Git LFS untuk file .bin.
5. Jangan jalankan perintah: git lfs track "*.bin".
6. Upload file .bin asli dari ZIP ini. Ukuran setiap shard .bin sekitar 1 MB - 4 MB, jadi aman diupload ke GitHub biasa.
7. Setelah upload, buka raw salah satu file .bin. Kalau masih muncul teks "version https://git-lfs.github.com/spec/v1", berarti upload masih salah.

Struktur root repo harus begini:
index.html
cek-model.html
models/cnn/model.json
models/cnn/group1-shard1of14.bin
models/cnn_lstm/model.json
models/cnn_lstm/group1-shard1of3.bin
models/rnn/model.json
models/rnn/group1-shard1of1.bin

Tes setelah upload:
https://USERNAME.github.io/NAMA_REPO/cek-model.html

Kalau semua model LOADED, baru buka index.html.
