# BabyCry Classifier

Web klasifikasi tangisan bayi berbasis TensorFlow.js.

## Penting
Jangan upload file model `.bin` memakai Git LFS. GitHub Pages harus membaca `.bin` sebagai file binary asli. Jika raw file `.bin` menampilkan teks `version https://git-lfs.github.com/spec/v1`, berarti model akan gagal dimuat.

## Struktur Folder

```text
index.html
cek-model.html
models/cnn/model.json
models/cnn/*.bin
models/cnn_lstm/model.json
models/cnn_lstm/*.bin
models/rnn/model.json
models/rnn/*.bin
```

## Cara Tes
Buka `cek-model.html` dari GitHub Pages. Jika semua model berstatus `LOADED`, aplikasi siap digunakan.
