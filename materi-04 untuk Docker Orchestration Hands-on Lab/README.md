# Docker Orchestration Hands-on Lab.

* Section #1 - What is Orchestration.
* Section #2 - Configure Swarm Mode.
* Section #3 - Deploy applications across multiple hosts.
* Section #4 - Scale the application.
* Section #5 - Drain a node and reschedule the containers.
* Cleaning Up.

___

1. Membuat container baru pada terminal node1.
![1](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-04%20untuk%20Docker%20Orchestration%20Hands-on%20Lab/gambar-01.png)
![1.1](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-04%20untuk%20Docker%20Orchestration%20Hands-on%20Lab/gambar-01.1.png)

2. Melihat daftar container untuk memastikan bahwa container telah berhasil dibuat.

3. Menginisialisasi docker swarm.

4. Melihat informasi docker swarm pada node1.

5. Menggabungkan node2 dan node3 kedalam swarm node1 dengan menggunakan token yang telah didapatkan sebelumnya.

![2](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-04%20untuk%20Docker%20Orchestration%20Hands-on%20Lab/gambar-02.png)

6. Melihat daftar node yang ada beserta keterangannya.

![3](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-04%20untuk%20Docker%20Orchestration%20Hands-on%20Lab/gambar-03.png)

7. Mendeploy container.
![4](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-04%20untuk%20Docker%20Orchestration%20Hands-on%20Lab/gambar-04.png)

8. Memastikan bahwa container telah berhasil di deploy.
![5](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-04%20untuk%20Docker%20Orchestration%20Hands-on%20Lab/gambar-05.png)

9. Menjalankan layanan yang sama dengan skala 7.
![6](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-04%20untuk%20Docker%20Orchestration%20Hands-on%20Lab/gambar-06.png)

10. Melihat layanan yang sedang berjalan.
![7](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-04%20untuk%20Docker%20Orchestration%20Hands-on%20Lab/gambar-07.png)

11. Menjalankan kembali layanan yang sama namun dengan skala 4.
![8](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-04%20untuk%20Docker%20Orchestration%20Hands-on%20Lab/gambar-08.png)

12. Melihat kembali layanan yang sedang berjalan.
![9](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-04%20untuk%20Docker%20Orchestration%20Hands-on%20Lab/gambar-09.png)

13. Melihat daftar node yang ada.
![10](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-04%20untuk%20Docker%20Orchestration%20Hands-on%20Lab/gambar-10.png)

14. Melihat daftar container.
![11](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-04%20untuk%20Docker%20Orchestration%20Hands-on%20Lab/gambar-11.png)

15. Melihat kembali daftar node yang ada.
![12.1](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-04%20untuk%20Docker%20Orchestration%20Hands-on%20Lab/gambar-12.png)
![12](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-04%20untuk%20Docker%20Orchestration%20Hands-on%20Lab/gambar-12.1.png)

16. Mengubah availability node 2 menjadi drain.
![13](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-04%20untuk%20Docker%20Orchestration%20Hands-on%20Lab/gambar-13.png)

17. Mengecek hasilnya.
![14](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-04%20untuk%20Docker%20Orchestration%20Hands-on%20Lab/gambar-14.png)

18. Melihat container yang sedang berjalan pada node2.
![15](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-04%20untuk%20Docker%20Orchestration%20Hands-on%20Lab/gambar-15.png)

19.Melihat layanan yang sedang berjalan.
![16](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-04%20untuk%20Docker%20Orchestration%20Hands-on%20Lab/gambar-16.png)

20. Menghapus layanan.
![17](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-04%20untuk%20Docker%20Orchestration%20Hands-on%20Lab/gambar-17.png)

21. Melihat daftar container yang ada.
![18](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-04%20untuk%20Docker%20Orchestration%20Hands-on%20Lab/gambar-18.png)

22. Menghapus container.
![19](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-04%20untuk%20Docker%20Orchestration%20Hands-on%20Lab/gambar-19.png)

23. Mengapus swarm pada node1, 2 dan 3.
![20](https://github.com/XabaraNeanthal/uas-tcc/blob/master/materi-04%20untuk%20Docker%20Orchestration%20Hands-on%20Lab/gambar-20.png)



