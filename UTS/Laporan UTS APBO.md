# UTS APBO A KELOMPOK  
Repositori ini berisi hasil Ujian Tengah Semester (UTS) mata kuliah Analisis Pemrograman Berbasis Objek (APBO) - Kelas A 

## Dosen Pengampu
Adi Wahyu Pribadi, S.Si., M.Kom

## Anggota Kelompok 

| No | Nama Anggota             | NPM         |
|----|-----------------------   |-------------|
| 1  | Firdaus Fatan Nugraha    | 4523210049  |
| 2  | Fahran Maulana Febryan   | 4523210044  |
| 3  | Jovan Alfito Praditia    | 4523210055  |
| 4  | Abiyyu Muflih Az-Arianto | 4523210124  |
| 5  | M. Akbar Ramadhan O.S    | 4523210132  |


## _Kos Putra Agan_
Kos Putra Agan terletak di Srengseng Sawah, Jakarta Selatan. Tempat strategis untuk mahasiswa yang berkuliah disekitar Jakarta Selatan atau Depok.

### 1. Aktor/Role
A. Penyewa
Berperan sebagai konsumen yang akan jadi penyewa kamar kosan.

B. Admin
Berperan sebagai pemegang sistem dalam sistem informasi kos-kosan.

### 2. Use Case Diagram
![UC Diagram vr 2](https://github.com/user-attachments/assets/7cd2478a-e810-4e07-9877-859c742b45ef)

### 3. Tabel Database
#### A. Tabel Master
##### 1. Penyewa

| Nama Atribut      | Tipe Data | Keterangan                                              |
|-------------------|-----------|---------------------------------------------------------|
| id_penyewa        | Int (PK)  | ID unik penyewa (auto increment)                        |
| nama_penyewa      | String    | Nama lengkap penyewa                                    |
| email_penyewa     | String    | Email penyewa                                           |
| no_telp_penyewa   | String    | Nomor telepon penyewa                                   |
| password_penyewa  | String    | Password penyewa                                        |
| status_akun       | Enum      | Status akun: Menunggu Verifikasi / Terverifikasi / Umum |


##### 2. Admin

| Nama Atribut   | Tipe Data  | Keterangan                     |
|----------------|------------|--------------------------------|
| id_admin       | Int (PK)   | ID unik admin (auto increment) |
| nama_admin     | String     | Nama lengkap admin             |
| email_admin    | String     | Email admin                    |
| no_telp_admin  | String     | Nomor telepon admin            |
| password_admin | String     | Password admin                 |




##### 3. Kamar

| Nama Atribut    | Tipe Data | Keterangan                                      |
| --------------- | --------- | ----------------------------------------------- |
| no_kamar       | Int (PK)  | Nomor kamar (auto increment)                     |
| foto_kos       | String    | File foto kos/kamar                              |
| tipe_kamar     | Enum      | Tipe kamar: A / B / C                            |
| harga_perbulan | Decimal   | Harga sewa per bulan                             |
| status          | Enum      | Status kamar: Kosong / Isi                      |
| deskripsi       | Text      | Deskripsi tambahan kamar                        |
| fasilitas       | String    | Daftar fasilitas kamar (dipisahkan dengan koma) |


#### B. Tabel Transaksi
##### 1. Pembayaran

| Nama Atribut       | Tipe Data | Keterangan                               |
| -------------------| --------- | ---------------------------------------  |
| id_pembayaran      | Int (PK)  | ID unik pembayaran (auto increment)      |
| id_sewa            | Int (FK)  | ID sewa yang dibayarkan                  |
| tanggal_pembayaran | DateTime  | Tanggal pembayaran dilakukan             |
| jumlah_bayar       | Decimal   | Jumlah uang yang dibayarkan              |
| metode_pembayaran  | Enum      | Metode: E-Wallet / Transfer Bank / Cash  | 
| bukti_pembayaran   | String    | Nama file bukti pembayaran               |
| status_pembayaran  | Enum      | Status: Lunas / Cicil                    |
| tenggat_pembayaran | DateTime  | Tenggat waktu pembayaran (jika ada)      |



##### 2. Sewa

| Nama Atribut     | Tipe Data | Keterangan                    |
| ---------------- | --------- | ----------------------------- |
| id_sewa         | Int (PK)  | ID unik sewa (auto increment)  |
| id_penyewa      | Int (FK)  | ID penyewa yang menyewa        |
| no_kamar        | Int (FK)  | Nomor kamar yang disewa        |
| tanggal_mulai   | DateTime  | Tanggal mulai sewa             |
| tanggal_selesai | DateTime  | Tanggal selesai sewa           |
| status_sewa     | Enum      | Status sewa: Sewa / Selesai    |



##### 3. Feedback

| Nama Atribut      | Tipe Data | Keterangan                                                                |
| ----------------- | --------- | ------------------------------------------------------------------------- |
| id_feedback       | Int (PK)  | ID unik feedback (auto increment)                                         |
| no_kamar          | Int (FK)  | Nomor kamar yang diberi feedback                                          |
| tanggal_feedback  | DateTime  | Tanggal saat feedback diberikan                                           |
| isi_feedback      | String    | Isi atau pesan feedback                                                   |
| status_feedback   | Enum      | Status: Belum Dibaca / Sudah Dibaca / Sedang Diproses / Selesai Ditangani |



### 4. Relasi / ERD
![image](https://github.com/user-attachments/assets/808ed6ca-4d62-49a1-a726-7cbfa7a1b6a9)




### 5. Class Diagram
![class diagram](https://github.com/user-attachments/assets/23a8e123-3ae1-480f-8bcc-46740c5f6ffb)



### 6. Wireframe/Mockup
#### A. Daftar Akun - Pembeli


#### B. Mengelola Data Makanan - Penjual


#### C. Makanan  - Penjual, Pembeli


#### D. Pesan Makanan - Pembeli


#### E. Pembayaran - Pembeli


#### F. Konfirmasi - Penjual


#### G. Notifikasi - Pembeli
