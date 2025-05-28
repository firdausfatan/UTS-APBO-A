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

| Nama Atribut  | Tipe Data    | Keterangan                          |
|---------------|--------------|-------------------------------------|

#### B. Tabel Transaksi
##### 1. Pembayaran

| Nama Atribut      | Tipe Data    | Keterangan                                         |
|-------------------|--------------|----------------------------------------------------|


##### 2. Sewa

| Nama Atribut | Tipe Data    | Keterangan                                   |
|--------------|--------------|----------------------------------------------|


##### 3. Feedback

| Nama Atribut | Tipe Data    | Keterangan                                   |
|--------------|--------------|----------------------------------------------|


### 4. Relasi / ERD
![erdkosan](https://github.com/user-attachments/assets/c6f0d414-f274-4567-8a0f-4637bc3a9639)



### 5. Class Diagram
![image](https://github.com/user-attachments/assets/5e70b5fb-7c04-4a02-abee-7f5485da76c8)


### 6. Wireframe/Mockup
#### A. Daftar Akun - Pembeli


#### B. Mengelola Data Makanan - Penjual


#### C. Makanan  - Penjual, Pembeli


#### D. Pesan Makanan - Pembeli


#### E. Pembayaran - Pembeli


#### F. Konfirmasi - Penjual


#### G. Notifikasi - Pembeli
