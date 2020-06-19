[Kurbenetes Untuk Pemula atau Newbie](https://github.com/XabaraNeanthal/uas-tcc/blob/master/Newbie.md)



Untuk menjalankan virtual Kurbenetes For Beginner dapat dilakukan login terlebih dahulu, salah satu akun untuk login yaitu akun Docker. Jika belum mempunyai akun docker dapat mendaftar ![di sini](https://github.com/XabaraNeanthal/uas-tcc/blob/master/gambar-01.png)

___

## Memulai Cluster.
Pertama gunakan perintah berikut *ls* (list directory content) adalah salah satu perintah untuk melihat daftar sebuah direktori atau (pwd) direktori aktif.

![](https://github.com/XabaraNeanthal/uas-tcc/blob/master/gambar-02.png)

# Mulai cluster.
Langkah pertama adalah menginisialisasi gugus di terminal pertama.

![](https://github.com/XabaraNeanthal/uas-tcc/blob/master/gambar-03.png)

Itu akan memakan waktu beberapa menit, selama waktu itu Anda akan melihat banyak aktivitas di terminal.
Lalu akan mendapatkan sebuah token dan salin seluruh baris yang dimulai kubeadm join dari terminal pertama.
Urutannya sebagai berikut : kubeadm join --token a146c9.9421a0d62a0611f4 172.26.0.2:6443 --discovery-token-ca-cert-hash sha256:9a4dc07bd8ac596336ecee6ce0928b3500174037c07a38a03bebef25e97c4db5.

![](https://github.com/XabaraNeanthal/uas-tcc/blob/master/gambar-04.png)

Dan akan menampilkan hasil seperti ini.

![](https://github.com/XabaraNeanthal/uas-tcc/blob/master/gambar-4.1.png)

Terakhir, Anda hanya perlu menginisialisasi jaringan cluster di terminal pertama.

![](https://github.com/XabaraNeanthal/uas-tcc/blob/master/gambar-05.png)

Sebelumnya clone repo pada github **https://github.com/dockersamples/dockercoins**.

![](https://github.com/XabaraNeanthal/uas-tcc/blob/master/gambar-06.png)

___

## Menjalankan aplikasi.
1. Buka direktori dockercoins, di repo hasil kloning.

2. Gunakan Tulisan untuk membuat dan menjalankan semua wadah.

![](https://github.com/XabaraNeanthal/uas-tcc/blob/master/gambar-07.png)

___

# Menghubungkan ke UI web.

1. webui wadah mengekspos dashboard web.

2. Dengan browser web, sambungkan ke node1 (dibuat saat Anda menjalankan aplikasi).

![](https://github.com/XabaraNeanthal/uas-tcc/blob/master/gambar-08.png)

Untuk menghentikannya dapat menggunkan perintah **ctrl - c**.

![](https://github.com/XabaraNeanthal/uas-tcc/blob/master/gambar-09.png)

___

## Kontak pertama dengan kubectl

Komposisi cluster.

![](https://github.com/XabaraNeanthal/uas-tcc/blob/master/gambar-10.png)

atau.

![](https://github.com/XabaraNeanthal/uas-tcc/blob/master/gambar-11.png)

# Memperoleh hasil yang bisa dibaca mesin

kubectl get dapat menampilkan JSON, YAML, atau langsung diformat.

![](https://github.com/XabaraNeanthal/uas-tcc/blob/master/gambar-12.png)

Untuk YAML.

![](https://github.com/XabaraNeanthal/uas-tcc/blob/master/gambar-13.png)

Menampilkan kapasitas semua node sebagai aliran objek JSON.

![](https://github.com/XabaraNeanthal/uas-tcc/blob/master/gambar-14.png)

Daftar Layanan Service Cluster.

![](https://github.com/XabaraNeanthal/uas-tcc/blob/master/gambar-15.png)

atau.

![](https://github.com/XabaraNeanthal/uas-tcc/blob/master/gambar-15.1.png)

Lalu menjalankan kubect1 get all.

![](https://github.com/XabaraNeanthal/uas-tcc/blob/master/gambar-20.png)
* deploy/pingpong( penyebaran yang baru saja kami buat).
* rs/pingpong-xxxx( set replika yang dibuat oleh penyebaran).
* po/pingpong-yyyy( pod yang dibuat oleh set replika).




