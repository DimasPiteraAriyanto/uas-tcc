## Docker Networking.

Login ke Akun Docker terlebih dahulu jika belum mempunyai akun dapat langsung melakukan [sign up](https://hub.docker.com/) untuk dapat melakukan login.

# Bagian # 1 - Dasar-Dasar Jaringan.

## Langkah 1: Perintah Jaringan Docker.
**docker network** perintah adalah perintah utama untuk mengkonfigurasi dan mengelola jaringan kontainer. Jalankan docker networkperintah dari terminal pertama.
![1](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-02%20untuk%20Docker%20Networking/gambar-01.png)


## Langkah 2: Daftar jaringan.
Jalankan **docker network ls** perintah untuk melihat jaringan kontainer yang ada pada host Docker saat ini.
![2](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-02%20untuk%20Docker%20Networking/gambar-02.png)

## Langkah 3: Periksa jaringan.
**docker network inspect** Perintah ini digunakan untuk melihat rincian konfigurasi jaringan. Rincian ini meliputi; nama, ID, driver, driver IPAM, info subnet, wadah terhubung, dan banyak lagi.

Gunakan docker network inspect <network>untuk melihat detail konfigurasi jaringan kontainer pada host Docker Anda. Perintah di bawah ini menunjukkan perincian jaringan yang disebut bridge.
![3](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-02%20untuk%20Docker%20Networking/gambar-03.png)

## Langkah 4: Daftar plugin driver jaringan
**The docker info** perintah menunjukkan banyak informasi menarik tentang instalasi Docker.

Jalankan docker infoperintah dan temukan daftar plugin jaringan.
![4](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-02%20untuk%20Docker%20Networking/gambar-05.png)

___

# Bagian # 2 - Jembatan Jaringan.
## Langkah 1: Dasar-Dasarnya.
Setiap instalasi Docker yang bersih dilengkapi dengan jaringan yang disebut bridge . Verifikasi ini dengan docker network ls.

//Menampilkan daftar container networks.
**$ docker network ls**

//Mengupdate dan install packages bridge-utils.
**$ apk update**

//Menambahkan packages bridge-utils.
**$ apk add bridge**

//Menampilkan daftar bridges pada Docker host.
**$ brctl show**

//Melihat detail bridge.
**$ ip a**

![5](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-02%20untuk%20Docker%20Networking/gambar-05.png)
![6](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-02%20untuk%20Docker%20Networking/gambar-06.png)
![7](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-02%20untuk%20Docker%20Networking/gambar-07.png)
![7.1](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-02%20untuk%20Docker%20Networking/gambar-07.1.png)
![8](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-02%20untuk%20Docker%20Networking/gambar-08.png)
![9](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-02%20untuk%20Docker%20Networking/gambar-09.png)

## Langkah 2: Hubungkan wadah.

//Membuat container baru.
**$ docker run -dt ubuntu sleep infinity**

//Melihat spek container network.
**$ docker ps**

//Menampilkan daftar bridges pada Docker host.
**$ brctl show**

//Menampilkan lampiran pada container bridge.
**$ docker network inspect bridge**

![10](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-02%20untuk%20Docker%20Networking/gambar-10.png)
![12](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-02%20untuk%20Docker%20Networking/gambar-11.png)
![13](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-02%20untuk%20Docker%20Networking/gambar-12.png)
![14](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-02%20untuk%20Docker%20Networking/gambar-13.png)

## Langkah 3: Uji konektivitas jaringan.

//Mengetes jaringan (ping).
**$ ping -c5 172.17.0.2**

//Melihat spek container network.
**$ docker ps**

//Masuk terminal ubuntu.
**$ docker exec -it yourcontainerid /bin/bash**

//Menginstall program ping.
**$ apt-get update && apt-get install -y iputils-ping**

//Mengetes jaringan (ping).
**$ ping -c5 www.github.com**

//Keluar dari terminal ubuntu.
**$ exit**

//Menghentikan container yang sedang berjalan.
**$ docker stop yourcontainerid**

![15](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-02%20untuk%20Docker%20Networking/gambar-15.png)
![16](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-02%20untuk%20Docker%20Networking/gambar-16.png)
![17](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-02%20untuk%20Docker%20Networking/gambar-17.png)
![18](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-02%20untuk%20Docker%20Networking/gambar-18.png)
![19](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-02%20untuk%20Docker%20Networking/gambar-19.png)
![20](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-02%20untuk%20Docker%20Networking/gambar-20.png)

## Langkah 4: Konfigurasikan NAT untuk konektivitas eksternal.

/Menjalankan container baru dari official NGINX image.
**$ docker run --name web1 -d -p 8080:80 nginx**

//Melihat spek container network.
**$ docker ps**

//Menghubungkan ke docker host.
**$ curl 127.0.0.1:8080**

![21](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-02%20untuk%20Docker%20Networking/gambar-21.png)
![22](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-02%20untuk%20Docker%20Networking/gambar-22.png)
![23](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-02%20untuk%20Docker%20Networking/gambar-23.png)

___

# Bagian # 3 - Overlay Networking.
## Langkah 1: Dasar-Dasarnya.

//Menginisialisasi docker swarm baru.
**$ docker swarm init --advertise-addr $(hostname -i)**

//Menggabungkan node.
**$ docker swarm join token**

![24](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-02%20untuk%20Docker%20Networking/gambar-24.png)

//Melihat daftar node.
**$ docker node ls**

![25](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-02%20untuk%20Docker%20Networking/gambar-25.png)

## Langkah 2: Buat jaringan overlay.

//Membuat sebuah overlay network.
**$ docker network create -d overlay overnet**

//Mengecek/menampilkan network.
**$ docker network ls**

//Melihat lebih detail informasi mengenai overnet network.
**$ docker network inspect overnet**

![26](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-02%20untuk%20Docker%20Networking/gambar-26.png)
![27](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-02%20untuk%20Docker%20Networking/gambar-27.png)
![29](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-02%20untuk%20Docker%20Networking/gambar-28.png)

## Langkah 3: Create Service.

//Membuat layanan baru.
*** $ docker service create --name myservice \ --network overnet \ --replicas 2 \ ***

//Mengecek/menampilkan daftar layanan.
**$ docker service ls**

//Melihat daftar layanan yang sedang berjalan.
**$ docker service ps myservice**

//Mengecek/menampilkan network.
**$ docker network ls**

//Melihat lebih detail informasi mengenai overnet network.
**$ docker network inspect overnet**

![30](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-02%20untuk%20Docker%20Networking/gambar-30.png)
![31](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-02%20untuk%20Docker%20Networking/gambar-31.png)
![32](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-02%20untuk%20Docker%20Networking/gambar-32.png)
![33](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-02%20untuk%20Docker%20Networking/gambar-33.png)
![34](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-02%20untuk%20Docker%20Networking/gambar-34.png)

## Langkah 4: Uji jaringan.

//Melihat lebih detail informasi mengenai overnet network.
**$ docker network inspect overnet**

//Melihat spek container network.
**$ docker ps**

![35](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-02%20untuk%20Docker%20Networking/gambar-35.png)

## Cleaning Up.

//Menghspus layanan.
**$ docker service rm myservice**

//Melihat spek container network.
**$ docker ps**

//Menghapus node.
**$ docker swarm leave --force**

![36](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-02%20untuk%20Docker%20Networking/gambar-36.png)
![37](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-02%20untuk%20Docker%20Networking/gambar-37.png)
![38](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-02%20untuk%20Docker%20Networking/gambar-38.png)


