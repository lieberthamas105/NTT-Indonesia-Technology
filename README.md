# 🚗 Console Parking System (.NET 5)

Sistem parkir berbasis console yang dibangun menggunakan .NET 5. Sistem ini menggunakan konsep *slot parkir* di mana setiap slot dapat menampung **1 mobil kecil dan 1 motor**, dan setiap orang hanya mendapatkan **1 lot**.

---

## 🔧 Cara Menjalankan

### 1. Clone atau download proyek ini.

### 2. Masuk ke folder proyek:
```bash
cd ParkingSystem
```

Jalankan program:
```bash
Copy
Edit
dotnet run
```
Atau, jalankan dari file perintah:

```bash
Copy
Edit
dotnet run < input.txt
```
💡 Gunakan terminal Git Bash, karena PowerShell tidak mendukung < input.txt.

**Perintah yang Didukung**

Perintah	Deskripsi:

- create_parking_lot {jumlah}	: Membuat tempat parkir dengan jumlah lot tertentu
- park {no_plat} {warna} {tipe}	: Memasukkan kendaraan ke slot tersedia
- leave {nomor_slot}	: Mengosongkan slot parkir
- status	: Menampilkan status parkir saat ini

`type_of_vehicles {Mobil	Motor}`

registration_numbers_for_vehicles_with_ood_plate	   : Menampilkan plat nomor kendaraan ganjil
registration_numbers_for_vehicles_with_event_plate	   : Menampilkan plat nomor kendaraan genap
registration_numbers_for_vehicles_with_colour {warna}  : Plat nomor berdasarkan warna
slot_numbers_for_vehicles_with_colour {warna}	       : Slot berdasarkan warna kendaraan
slot_number_for_registration_number {no_plat}	       : Menampilkan slot dari plat tertentu
exit	                                               : Keluar dari aplikasi

*** Contoh Input Pada Soal ***

Jika ingin membuat tempat parkir dengan 6 slot secara manual, gunakan perintah:
> create_parking_lot 6
>output: Created a parking lot with 6 slots

> park B-1234-XYZ Putih Mobil
>output: Allocated slot number: 1

> park B-9999-XYZ Putih Motor
>output: Allocated slot number: 2

> park D-0001-HIJ Hitam Mobil
>output: Allocated slot number: 3

> park B-7777-DEF Red Mobil
>output: Allocated slot number: 4

> park B-2701-XXX Biru Mobil
>output: Allocated slot number: 5

> park B-3141-ZZZ Hitam Motor
>output: Allocated slot number: 6

> leave 4
>output: Slot number 4 is free

> status
>output: 
```bash
Slot No.    Type       Registration No    Colour
1         Mobil      B-1234-XYZ          Putih
2         Motor      B-9999-XYZ          Putih
3         Mobil      D-0001-HIJ          Hitam
5         Mobil      B-2701-XXX          Biru
6         Motor      B-3141-ZZZ          Hitam
```
> park B-333-SSS Putih Mobil
>output: Allocated slot number: 4

> park A-1212-GGG Putih Mobil
>output: Sorry, parking lot is full

> type_of_vehicles Motor
>output: 2

> type_of_vehicles Mobil
>output: 4

> registration_numbers_for_vehicles_with_ood_plate
>output: B-9999-XYZ, D-0001-HIJ, B-2701-XXX, B-3141-ZZZ

> registration_numbers_for_vehicles_with_event_plate
>output: B-1234-XYZ

> registration_numbers_for_vehicles_with_colour Putih
>output: B-1234-XYZ, B-9999-XYZ, B-333-SSS

> slot_numbers_for_vehicles_with_colour Putih
>output: 1, 2, 4

> slot_number_for_registration_number B-3141-ZZZ
>output: 6

> slot_number_for_registration_number Z-1111-AAA
>output: Not found

> exit

## 🙏 Penutup

Proyek ini dibuat sebagai bagian dari tes penyaluran kerja.  
Tujuannya untuk menunjukkan kemampuan dalam membuat aplikasi console dengan logika bisnis sederhana menggunakan .NET 5.  

Terima kasih telah meluangkan waktu untuk menilai proyek ini.  
Saya terbuka untuk diskusi lebih lanjut dan siap menerima masukan demi perbaikan dan pengembangan ke depan.

Salam hormat,  
