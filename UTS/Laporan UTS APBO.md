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
| no_kamar        | Int (PK)  | Nomor kamar (auto increment)                    |
| foto_kos        | String    | File foto kos/kamar                             |
| tipe_kamar      | Enum      | Tipe kamar: A / B / C                           |
| harga_perbulan  | Decimal   | Harga sewa per bulan                            |
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
| id_sewa          | Int (PK)  | ID unik sewa (auto increment) |
| id_penyewa       | Int (FK)  | ID penyewa yang menyewa       |
| no_kamar         | Int (FK)  | Nomor kamar yang disewa       |
| tanggal_mulai    | DateTime  | Tanggal mulai sewa            |
| tanggal_selesai  | DateTime  | Tanggal selesai sewa          |
| status_sewa      | Enum      | Status sewa: Sewa / Selesai   |



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
#### A. Daftar Akun - Penyewa
![image](https://github.com/user-attachments/assets/b36df7eb-ed07-4a73-81d8-5a46cef04364)




#### B. Login - Penyewa/Admin
![image](https://github.com/user-attachments/assets/ac18c328-471e-4ba2-abe4-ff0bc61ae367)




#### C. Mengelola Daftar Kos - Admin
![image](https://github.com/user-attachments/assets/ec864e32-fae2-4c9a-baa5-2d7c6396c3eb)
![image](https://github.com/user-attachments/assets/ed56e6b9-8d3e-463f-8992-b4aeb13d89e4)
![image](https://github.com/user-attachments/assets/51cf925a-6636-4044-89f8-215abe9e703c)




#### D. Melihat Data Penyewa - Admin
![image](https://github.com/user-attachments/assets/6eee8e71-4e10-4f33-826b-487ab0373dce)



#### E. Melihat Histori Pembayaran - Admin
![image](https://github.com/user-attachments/assets/3e0a40e4-3082-4cab-b8eb-83abaf11745e)



#### F. Melihat Data Status Sewa - Admin
![image](https://github.com/user-attachments/assets/0232bc4c-bff7-43cf-83e1-5c70b538bf1f)


#### G. Mengelola Keluhan Penyewa - Admin
![image](https://github.com/user-attachments/assets/b5c46297-d39f-4e9b-a26d-e9640d46026c)


#### H. Tampilan Form Pembayaran - Penyewa
![image](https://github.com/user-attachments/assets/ef566f76-5e62-4ba5-a6ff-20f80aafd448)
![image](https://github.com/user-attachments/assets/390ac96a-ef98-431b-ad8f-0414a9334661)


#### I. Tampilan Mengajukan Keluhan - Penyewa
![image](https://github.com/user-attachments/assets/c709d748-20d9-4d41-9c21-65d1aae9c2cd)

### 7. Sequence Diagram
#### A. Register/Login 
![Sequence regis   login_page-0001](https://github.com/user-attachments/assets/d942ca6a-31f1-4db4-b8c4-edcc8a6f8f42)

#### B. Pendaftaran Sewa
![pendaftaran sequence (1)_page-0001](https://github.com/user-attachments/assets/5387e9fb-87a8-40b7-8713-480105b64324)

#### C. Perpanjangan Sewa
![sequence perpanjangan sewa_page-0001](https://github.com/user-attachments/assets/77d5a3e0-5f0b-4b2f-bb6b-81d68f15efd9)

#### D. Pengajuan Feedback
![sequence feedback_page-0001](https://github.com/user-attachments/assets/4c847fac-d766-4bbd-9655-1766566ca354)
