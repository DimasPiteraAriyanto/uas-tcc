## [Docker for Beginners - Linux](https://training.play-with-docker.com/beginner-linux/)

___

Login ke Akun Docker terlebih dahulu jika belum mempunyai akun dapat langsung melakukan [sign up](https://hub.docker.com/) untuk dapat melakukan login

___

# Melakukan Cloning Repo Github.
![2](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-01/gambar-02.png)

# Task 1: Run some simple Docker containers.
Run a single task in an Alpine Linux container.

1. Memulai container baru dengan image alpine.
![3](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-01/gambar-03.png)

2. Melihat container yang tersedia.
![4](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-01/gambar-04.png)

Run an interactive Ubuntu container.

1. Menjalankan Docker container dan mengakses terminal ubuntu.
![5](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-01/gambar-05.png)

2. Menjalankan perintah berikut.
![6](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-01/gambar-06.png)
ls /akan mencantumkan isi direktur root dalam wadah, ps auxakan menunjukkan proses yang berjalan dalam wadah, cat /etc/issueakan menunjukkan distro Linux mana wadah berjalan, dalam hal ini Ubuntu 18.04.3 LTS.

3. Lalu keluar untuk mengakhirinya dan Cek versi host VM.
![7](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-01/gambar-07.png)

## Run a background MySQL container.

1. Menjalankan MySQL container.
![8](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-01/gambar-08.png)

2. Melihat daftar container.
![9](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-01/gambar-09.png)

3. Cek log dan proses yang berjalan didalam container.
![10](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-01/gambar-10.png)
![11](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-01/gambar-11.png)

4. Menampilkan daftar versi MySQL menggunakan **docker container exec**.
![12](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-01/gambar-12.png)

___

# Tugas 2: Paket dan menjalankan aplikasi khusus menggunakan Docker.

## Bangun image situs web sederhana.
1. Berpindah ke direktori repo yang telah di-clone sebelumnya. **$cat** digunakan untuk melihat isi dari dockerfile.
![14])(https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-01/gambar-14.png)

2. Mengexport variabel dockerid dengan isian id docker kita. **$echo** digunakan untuk menampilkan dockerid 
![15](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-01/gambar-15.png)

3. Membuat docker image.
![16](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-01/gambar-16.png)

4. Menjalankan container untuk menghosting image yang telah dibuat.
![17](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-01/gambar-17.png)

5. Mengecek hasilnya dengan menekan link yang telah disediakan.
![18](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-01/gambar-18.png)

6. Menghentikan dan menghapus container lalu mengeceknya.
![19](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-01/gambar-19.png)
![20](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-01/gambar-20.png)

____

# Tugas 3: Memodifikasi situs web yang sedang berjalan.

1. Menjalankan container untuk menghosting image yang telah dibuat.
![21](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-01/gambar-21.png)

2. Mengecek bahwasanya image berhasil di hosting dengan menekan link yang telah disediakan.
![22](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-01/gambar-22.png)

3. Mengcopy index.html container dan merefresh web sebelumnya untuk melihat hasilnya.
![23](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-01/gambar-23.png)
![24](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-01/gambar-24.png)

4. Menghentikan dan menghapus container dan mengeceknya.
![25](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-01/gambar-25.png)
![26](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-01/gambar-26.png)
![27](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-01/gambar-27.png)

# Update the image.

1. Membuat image baru.
![29](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-01/gambar-28.png)

2. Melihat daftar image yang ada.
![30](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-01/gambar-29.png)

# Test the new version.

1. Menjalankan container dan melihat hasilnya.
![31](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-01/gambar-31.png)
![32](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-01/gambar-32.png)

2. Menjalankan container lainnya dan melihat hasilnya.
![33](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-01/gambar-33.png)
![34](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-01/gambar-34.png)

# Push your images to Docker Hub.

1. Melihat daftar image yang telah di hosting.
![35](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-01/gambar-35.png)

2. Sebelumnya login menggunakan akun docker kita agar tepat dan lancar di push atau upload pada akun docker kita.
![36](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-01/gambar-36.png)

3. Push image versi 1.0 dan 2.0.
![37](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-01/gambar-37.png)
![39](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-01/gambar-39.png)

Hasilnya saat di cek di docker kita.
![38](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-01/gambar-38.png)
![40](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-01/gambar-40.png)















