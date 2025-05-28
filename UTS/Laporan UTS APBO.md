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

### 3. Entitas Utama
#### A. Penyewa

| Nama Atribut  | Tipe Data    | Keterangan                 |
|---------------|--------------|----------------------------|
| id_pembeli    | String (PK)  | ID unik milik pembeli      |
| nama_pembeli  | String       | Nama lengkap pembeli       |
| alamat        | String       | Alamat lengkap pembeli     |
| notelp        | String       | Nomor telepon pembeli      |

#### B. Admin

| Nama Atribut   | Tipe Data    | Keterangan                  |
|----------------|--------------|-----------------------------|
| id_makanan     | String (PK)  | ID unik makanan             |
| nama_makanan   | String       | Nama makanan                |
| stok           | Int          | Stok tersedia               |
| harga          | Double       | Harga makanan               |
| foto           | String       | File foto makanan           |
| deskripsi      | String       | Deskripsi makanan           |

#### C. Kamar

| Nama Atribut  | Tipe Data    | Keterangan                          |
|---------------|--------------|-------------------------------------|
| id_pesanan    | String (PK)  | ID unik pesanan                     |
| id_pembeli    | String (FK)  | Relasi ke tabel Pembeli            |
| id_makanan    | String (FK)  | Relasi ke tabel Makanan            |
| jumlah        | Int          | Jumlah makanan yang dipesan        |
| subtotal      | Double       | Harga dikali jumlah                |
| waktu_pesan   | Datetime     | Waktu pemesanan                    |

#### D. Pembayaran

| Nama Atribut      | Tipe Data    | Keterangan                                         |
|-------------------|--------------|----------------------------------------------------|
| id_pembayaran     | String (PK)  | ID unik pembayaran                                 |
| id_pesanan        | String (FK)  | Relasi ke tabel Pesanan                            |
| subtotal          | Double       | Total harga yang dibayarkan                        |
| metode            | String       | Metode pembayaran (ENUM: COD, Transfer)        |
| waktu_pembayaran  | Datetime     | Waktu pembayaran dilakukan                         |

#### E. Sewa

| Nama Atribut | Tipe Data    | Keterangan                                   |
|--------------|--------------|----------------------------------------------|
| id_notif     | String (PK)  | ID unik notifikasi                           |
| id_pesanan   | String (FK)  | Relasi ke tabel Pesanan                      |
| konfirmasi   | Boolean      | Status konfirmasi pembayaran                 |
| status       | String       | Status pesanan (pending, selesai)        |
| notif        | String       | Pesan notifikasi                             |

#### F. Feedback

| Nama Atribut | Tipe Data    | Keterangan                                   |
|--------------|--------------|----------------------------------------------|
| id_notif     | String (PK)  | ID unik notifikasi                           |
| id_pesanan   | String (FK)  | Relasi ke tabel Pesanan                      |
| konfirmasi   | Boolean      | Status konfirmasi pembayaran                 |
| status       | String       | Status pesanan (pending, selesai)        |
| notif        | String       | Pesan notifikasi                             |

### 4. Relasi
![Screenshot 2025-05-29 000921](https://github.com/user-attachments/assets/b8f0da03-7a46-4226-a396-ca8e0d8799c4)

### 5. Class Diagram
![class diagram](https://github.com/user-attachments/assets/423a3be5-7a8e-40cc-904a-08cbdd1cd391)

### 6. Wireframe/Mockup
#### A. Daftar Akun - Pembeli


#### B. Mengelola Data Makanan - Penjual


#### C. Makanan  - Penjual, Pembeli


#### D. Pesan Makanan - Pembeli


#### E. Pembayaran - Pembeli


#### F. Konfirmasi - Penjual


#### G. Notifikasi - Pembeli
