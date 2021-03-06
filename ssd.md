**SOFTWARE DESIGN DOCUMENT (SDD)**
<br>
<br>
**1.** **Pendahuluan**<br>
	&emsp;**1.1.** **Tujuan**<br>
	&emsp;**1.2.** **Lingkup**<br>
	&emsp;**1.3.** **Definisi, akronim, dan singkatan**<br>
**2.** **Referensi**<br>
**3.** **Penjelasan Dekomposisi**<br>
	&emsp;**3.1.** **Dekomposisi modul**<br>
	&emsp;**3.2.** **Dekomposisi prosis konkuren**<br>
	&emsp;**3.3.** **Dekomposisi data**<br>
**4.** **Deskripsi Ketergantungan/Keterkaitan**<br>
	&emsp;**4.1.** **Keterkaitan inter modul**<br>
	&emsp;**4.2.** **Keterkaitan inter proses**<br>
	&emsp;**4.3.** **Keterkaitan data**<br>
**5.** **Deskripsi Antarmuka**<br>
	&emsp;**5.1.** **Antarmuka modul**<br>
		&emsp;&emsp;**5.1.1.** **Deskripsi modul 1**<br>
		&emsp;&emsp;**5.1.2.** **Deskripsi modul 2**<br>
	&emsp;**5.2.** **Antarmuka proses**<br>
		&emsp;&emsp;**5.2.1.** **Deskripsi proses 1**<br>
		&emsp;&emsp;**5.2.2.** **Deskripsi proses 2**<br>
**6.** **Desain Detail/Rinci**<br>
	&emsp;**6.1.** **Rinci modul**<br>
		&emsp;&emsp;**6.1.1.** **Rinci modul 1**<br>
		&emsp;&emsp;**6.1.2.** **Rinci modul 2**<br>
	&emsp;**6.2.** **Desain data secara rinci**<br>
		&emsp;&emsp;**6.2.1.** **Rinci entiti data 1**<br>
		&emsp;&emsp;**6.2.2.** **Rinci entiti data 2**<br>
<br>
<br>
<br>
<br>
**1.** **Pendahuluan**<br>
	&emsp;**1.1.** **Tujuan**<br>
		&emsp;&emsp; Tujuan dalam membuat dokumen SDD (Software Design Description) ini adalah untuk menjelaskan langkah-langkah desain dan proses-proses dalam pembuatan sistem aplikasi yang akan di terapkan pada aplikasi simulasi management proyek RPL dan juga memberi definisi kebutuhan untuk sistem spesifikasi kebutuhan fungsional.<br>
	&emsp;**1.2.** **Lingkup**<br>
		 &emsp;&emsp;Ruang lingkup SDD ini adalah penjelasan mengenai aplikasi simulasi management proyek RPL berbasis website, ruang lingkup system ini mencangkup informasi mengenai antarmuka dari system tersebut.<br>
	&emsp;**1.3.** **Definisi, akronim, dan singkatan**<br>
		 &emsp;&emsp;Dalam penulisan dokumen pembuatan projek ini yang mungkin akan sulit dipahami berikut ini:<br>
		 	&emsp;&emsp;&emsp;SSD:	Software Design Description<br>
		 	&emsp;&emsp;&emsp;OOP:	Object Oriented Programing<br>
		 	&emsp;&emsp;&emsp;User: 	Untuk pengguna system<br>
**2.** **Referensi**<br>
   &emsp;a. Modul KULIAH RPL 7 DOKUMEN SDD<br>
   &emsp;b. Contoh Software Design Document (SDD) Moch. Bambang Sulistio<br>
**3.** **Penjelasan Dekomposisi**
	&emsp;**3.1.** **Dekomposisi modul**<br>
			   &emsp;&emsp;Kebutuhan fungsional (Functional Requirements) ini adalah kebutuhan utama yang diharapkan dari sistem ini, yang terkait langsung dengan sistem ini. Kebutuhan fungsional dari sistem ini adalah sebagai berikut:<br>
					&emsp;&emsp;&emsp;1. Pencatatan Hak Akses<br>
					&emsp;&emsp;&emsp;2. Pencatatan Nama aplikasi , Nama Kategori dan Nama Client<br>
					&emsp;&emsp;&emsp;3. Pencatatan Target Waktu , Jumlah Orang dan Biaya Aplikasi<br>
			   &emsp;&emsp;Spesifikasi yang diharapkan pada Pencatatan Hak Akses:<br>
					&emsp;&emsp;&emsp;* Membedakan antara user dan admin dalam hak ases<br>
					&emsp;&emsp;&emsp;* Sistem dapat memproses secara otomatis jika kita terdaftar dalam admin memiliki hak ases penuh dan sebaliknya jika terdaftar dalam user tidak memiliki hak ases penuh<br>
			   &emsp;&emsp;Spesifikasi yang diharapkan pada Pencatatan Nama aplikasi, Nama Kategori dan Nama Client:<br>
					&emsp;&emsp;&emsp;* Mencatat nama aplikasi apa yang akna di buat dalam sebuah project<br>
					&emsp;&emsp;&emsp;* Mencatat nama-nama kategori apa yang akan di buat di sebuah project<br>
					&emsp;&emsp;&emsp;* Mencatat nama client yang mau di buat kan sebuah project<br>
			   &emsp;&emsp;Spesifikasi yang diharapkan pada Pencatatan Target Waktu , Jumlah Orang dan Biaya Aplikasi:<br>
					&emsp;&emsp;&emsp;* Sistem dapat memproses secara otomatis target waktu aplikasi yang akan dibuat dalam sebuah project<br>
					&emsp;&emsp;&emsp;* Sistem dapat memproses secara otomatis jumlah orang dalam sebuah project<br>
					&emsp;&emsp;&emsp;* Sistem dapat memproses secara otomatis biaya dalam sebuah aplikasi yang akan di buat<br>
	&emsp;**3.2.** **Dekomposisi prosis konkuren**<br>
			&emsp;&emsp;Konkurensi adalah proses-proses (lebih dari satu proses) yang terjadi pada saat bersamaan. Konkurensi merupakan landasan umum perancangan sistem operasi.<br>
			&emsp;&emsp;Proses-proses disebut konkuren jika proses-proses berada pada saat yang sama.<br>
			&emsp;&emsp;Pada proses-proses konkuren yang berinteraksi mempunyai beberapa masalah yang harus diselesaikan:<br>
				&emsp;&emsp;&emsp;1. Mutual Exclusion<br>
				&emsp;&emsp;&emsp;2. Sinkronisasi<br>
				&emsp;&emsp;&emsp;3. Deadlock<br>
				&emsp;&emsp;&emsp;4. Startvation<br>
			&emsp;&emsp;Pada sistem dengan banyak proses (kongkuren), terdapat 2 katagori interaksi, yaitu:<br>
				&emsp;&emsp;&emsp;1. Proses-proses Saling Tidak Peduli (Independen).<br>
					&emsp;&emsp;&emsp;&emsp;Proses-proses ini tidak dimaksudkan untuk bekerja untukmencapai tujuan tertentu. Pada multiprogramming dengan proses-proses independen, dapat berupa batch atau sesi interaktif, atau campuran keduanya.<br>
				&emsp;&emsp;&emsp;2. Proses-proses Saling Mempedulikan Secara Tidak Langsung.<br>
					&emsp;&emsp;&emsp;&emsp;Proses-proses tidak perlu saling mempedulikan identitas proses-proses lain, tapi sama-sama mengakses objek tertentu, seperti buffer masukan/keluaran. Proses-proses itu perlu bekerja sama (cooperation) dalam memakai bersama objek tertentu.<br>
				&emsp;&emsp;&emsp;3. Proses-proses konkuren mengharuskan beberapa hal yang harus ditangani, antara lain:<br>
					&emsp;&emsp;&emsp;&emsp;a. Sistem operasi harus mengetahui proses-proses yang aktif<br>
					&emsp;&emsp;&emsp;&emsp;b. Sistem operasi harus mengalokasikan dan mendealokasikan beragam sumber daya untuk tiap proses aktif. Sumber daya yang harus dikelola, antara lain:<br>
						&emsp;&emsp;&emsp;&emsp;&emsp;1. Waktu pemroses<br>
						&emsp;&emsp;&emsp;&emsp;&emsp;2. Memori<br>
						&emsp;&emsp;&emsp;&emsp;&emsp;3. Berkas-berkas<br>
						&emsp;&emsp;&emsp;&emsp;&emsp;4. Perangkat I/<br>
					&emsp;&emsp;&emsp;&emsp;c. Sistem operasi harus memproteksi data dan sumber daya fisik masingmasing proses dari gangguan proses-proses lain.<br>
					&emsp;&emsp;&emsp;&emsp;d. Hasil-hasil proses harus independen terhadap kecepatan relatif proses-proses lain dimana eksekusi dilakukan.<br>
&emsp;**3.3.** **Dekomposisi data**<br>

