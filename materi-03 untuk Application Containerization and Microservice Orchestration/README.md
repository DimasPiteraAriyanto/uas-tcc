Application Containerization and Microservice Orchestration

Stage Setup
Step 0: Basic Link Extractor Script
Step 1: Containerized Link Extractor Script
Step 2: Link Extractor Module with Full URI and Anchor Text
Step 3: Link Extractor API Service
Step 4: Link Extractor API and Web Front End Services
Step 5: Redis Service for Caching
Step 6: Swap Python API Service with Ruby
Conclusions

# Setup

//Mengclone repository dari url github
**$ git clone https://github.com/ibnesayeed/linkextractor.git**

//Berpindah ke direktori linkextractor
**$ cd linkextractor**

//Berpindah ke branch demo
**$ git checkout demo**

![1](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-03/gambar-01.png)

## Langkah 0: Skrip Extractor Tautan Dasar

//Berpindah ke branch step0
**$ git checkout step0**

//Menampilkan struktur folder
**$ tree**

//Menampilkan isi file linkextractor.py
**$ cat linkextractor.py**

//Menjalankan file linkextractor.py
**$ ./linkextractor.py http://example.com/**

//Melihat hak/izin akses file linkextractor.py
**$ ls -l linkextractor.py**

//Menjalankan file linkextractor.py
**$ python linkextractor.py**

![2](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-03/gambar-02.png)
![3](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-03/gambar-03.png)
![4](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-03/gambar-04.png)
![5](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-03/gambar-05.png)
![6](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-03/gambar-06.png)

## Langkah 1: Script Extractor Tautan Kontainer

//Berpindah ke branch step1
**$ git checkout step1**

//Menampilkan struktur folder
**$ tree**

//Menampilkan isi file Dockerfile
**$ cat Dockerfile**

//Membuat image
**$ docker image build -t linkextractor:step1 .**

//Menampilkan daftar image
**$ docker image ls**

//Menjalankan container
**$ docker container run -it --rm linkextractor:step1 http://example.com/**

//Menjalankan container
**$ docker container run -it --rm linkextractor:step1 https://training.play-with-docker.com/**

![7](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-03/gambar-07.png)
![8](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-03/gambar-08.png)
![9](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-03/gambar-09.png)
![10](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-03/gambar-10.png)
![11](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-03/gambar-11.png)

## Langkah 2: Tautkan Modul Extractor dengan URI Lengkap dan Anchor Text
//Berpindah ke branch step2
**$ git checkout step2**

//Menampilkan struktur folder
**$ tree**

//Menampilkan isi file linkextractor.py
**$ cat linkextractor.py**

//Membuat image
**$ docker image build -t linkextractor:step2 .**

//Menampilkan daftar image
**$ docker image ls**

//Menjalankan container
**$ docker container run -it --rm linkextractor:step2 https://training.play-with-docker.com/**

//Menjalankan container
**$ docker container run -it --rm linkextractor:step1 https://training.play-with-docker.com/**

![12](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-03/gambar-12.png)
![13](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-03/gambar-13.png)
![14](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-03/gambar-14.png)
![15](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-03/gambar-15.png)
![16](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-03/gambar-16.png)
![17](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-03/gambar-17.png)
![18](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-03/gambar-18.png)

## Langkah 3: Layanan Link Extractor API

//Berpindah ke branch step3
**$ git checkout step3**

//Menampilkan struktur folder
**$ tree**

//Menampilkan isi file Dockerfile
**$ cat Dockerfile**

//Menampilkan isi file main.py
**$ cat main.py**

//Membuat image
**$ docker image build -t linkextractor:step3 .**

//Menjalankan container
**$ docker container run -d -p 5000:5000 --name=linkextractor linkextractor:step3**

//Menampilkan daftar container
**$ docker container ls**

//Membuat permintaan HTTP
**$ curl -i http://localhost:5000/api/http://example.com/**

//Melihat catatan container
**$ docker container logs linkextractor**

//Menghapus container
**$ docker container rm -f linkextractor**

![19](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-03/gambar-19.png)
![20](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-03/gambar-20.png)
![21](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-03/gambar-21.png)
![22](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-03/gambar-22.png)
![23](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-03/gambar-23.png)
![24](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-03/gambar-24.png)
![25](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-03/gambar-25.png)
![27](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-03/gambar-27.png)

## Langkah 4: Link Extractor API dan Layanan Front Web

//Berpindah ke branch step4
**$ git checkout step4**

//Menampilkan struktur folder
**$ tree**

//Menampilkan isi file docker-compose.yml
**$ cat docker-compose.yml**

//Menampilkan isi file www/index.php
**$ cat www/index.php**

//Menjalankan layanan docker compose
**$ docker-compose up -d --build**

//Menampilkan daftar container
**$ docker container ls**

//Menghubungakan dengan layanan API
**$ curl -i http://localhost:5000/api/http://example.com/**

![28](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-03/gambar-28.png)
![29](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-03/gambar-29.png)
![30](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-03/gambar-30.png)
![31](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-03/gambar-31.png)
![32](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-03/gambar-32.png)
![33](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-03/gambar-33.png)


Mengakses web Link Extractor

![35](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-03/gambar-35.png)

//Memodifikasi index file link extractor
**$ sed -i 's/Link Extractor/Super Link Extractor/g' www/index.php**

![34](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-03/gambar-34.png)

Mengakses web Link Extractor yang telah di ubah

![35](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-03/gambar-35.png)

//Mereset atau mengembalikan perubahan
**$ git reset --hard**



//Menghentikan layanan
**$ docker-compose down**

![36](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-03/gambar-36.png)
![37](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-03/gambar-37.png)

## Langkah 5: Layanan Redis untuk Caching

//Berpindah ke branch step5
**$ git checkout step5**

//Menampilkan struktur folder
**$ tree**

//Menampilkan isi file www/Dockerfile
**$ cat www/Dockerfile**

//Menampilkan isi file api/main.py
**$ cat api/main.py**

//Menampilkan isi file docker-compose.yml
**$ cat docker-compose.yml**

//Menjalankan layanan
**$ docker-compose up -d --build**

![38](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-03/gambar-38.png)
![39](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-03/gambar-39.png)
![40](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-03/gambar-40.png)
![41](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-03/gambar-41.png)
![42](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-03/gambar-42.png)

Mengakses web Link Extractor
![43](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-03/gambar-43.png)

//Membuaka client redis
**$ docker-compose exec redis redis-cli monitor**

//Memodifikasi index file link extractor
**$ sed -i 's/Link Extractor/Super Link Extractor/g' www/index.php**

//Mereset atau mengembalikan perubahan
**$ git reset --hard**

//Menghentikan layanan
**$ docker-compose down**

![44](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-03/gambar-44.png)
![45](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-03/gambar-45.png)

Langkah 6: Tukar Layanan API Python dengan Ruby

//Berpindah ke branch step6
**$ git checkout step6**

//Menampilkan struktur folder
**$ tree**

//Menampilkan isi file api/linkextractor.rb
**$ cat api/linkextractor.rb**

//Menampilkan isi file api/Dockerfile
**$ cat api/Dockerfile**

//Menampilkan isi file docker-compose.yml
**$ cat docker-compose.yml**

//Menjalankan layanana
**$ docker-compose up -d --build**

//Menghubungkan layananan
**$ curl -i http://localhost:4567/api/http://example.com/**

Mengakses web link extractor
![52](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-03/gambar-52.png)

//Menghentikan layanan
**$ docker-compose down**

//Melihat catatan sebuah web yang telah di extract
**$ cat logs/extraction.log**

![46](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-03/gambar-46.png)
![47](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-03/gambar-47.png)
![48](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-03/gambar-48.png)
![49](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-03/gambar-49.png)
![50](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-03/gambar-50.png)
![51](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-03/gambar-51.png)
![52](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-03/gambar-52.png)
![53](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-03/gambar-53.png)
![54](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-03/gambar-54.png)








