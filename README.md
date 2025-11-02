Haloo ini Zakhi Algifari 122140198 

file explanation adalah file yang ada penjelasan setiap step dan file yang satunya adalah hasil training dikaggle.

Langkah yang dilakukan : 
1. Pra-pemrosesan Data : Menambahkan start dan end untuk awal dan akhir kalimat, membersihkan tesk dari tanda baca (kecuali kurang siku) dan mengubah ke huruf kecil, membagi data 80 % training, validasi 10 %, dan pengujian 10 %
2. Vektorisasi Teks : Menggunakan teksvektor untuk untuk konversi teks menjadi urutan bilangan bulat, membatasi vocabulari 15.000 agar tidak overfitting, panjang urutan ditetapkan 20 token.
3. Pembangunan Arsitektur Transformer : PositionalEmbedding: menggabungkan embedding token dan posisi, TransformerEncoder: lapisan encoder berbasis multi-head self-attention, TransformerDecoder: lapisan decoder dengan masked self-attention dan cross-attention terhadap encoder.
4. Pelatihan model : model dilatih dengan 15 epoch dengan batch size 64, Menggunakan optimizer RMSprop dan fungsi kerugian sparse categorical crossentropy
5. Inferensi : model menghasilkan satu token pada satu waktu hingga mencapai token


Performa pelatihan :
Akurasi pelatihan: ~91.6%
Akurasi validasi: ~90.6%
Loss validasi: ~0.51

