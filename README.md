# Sistem Absensi Mahasiswa dengan PIN

> Program sederhana berbasis **CLI (Command Line Interface)** untuk proses absensi mahasiswa menggunakan PIN.

---

## Tentang Program

Program ini dibuat untuk mensimulasikan sistem absensi mahasiswa dengan **keamanan PIN sederhana**. Mahasiswa diberi maksimal **3 kali percobaan** untuk memasukkan PIN yang benar.

Logika program menggunakan **perulangan dan percabangan** agar alurnya mudah dipahami oleh pemula.

### Alur Logika Program

1. Program meminta **nama mahasiswa**.
2. Mahasiswa diminta memasukkan **PIN**.
3. Jika PIN benar (sesuai dengan PIN yang ditentukan), maka:

   * Absensi dinyatakan **berhasil**.
   * Nama mahasiswa ditampilkan.
4. Jika PIN salah:

   * Program menampilkan pesan **PIN salah**.
   * Menampilkan **sisa percobaan**.
5. Jika hingga 3 kali percobaan PIN tetap salah:

   * Absensi **ditolak**.

---

## Kamus Variabel

* `nama` : string → menyimpan nama mahasiswa
* `inputPin` : integer → PIN yang dimasukkan pengguna
* `pinBenar` : boolean → status kecocokan PIN
* `pin` : integer → PIN yang benar (default: **1234**)

---

## Pseudocode / Algoritma

```
Kamus
nama : string
inputPin : integer
pinBenar : boolean
pin : integer = 1234

Algoritma
output("Masukkan nama mahasiswa: ")
input(nama)

for i = 1 to 3 do
    output("Masukkan PIN: ")
    input(inputPin)

    pinBenar = inputPin == pin
    
    if pinBenar then
       output("Absensi berhasil")
       output("Nama:", nama)
       stop
    else
       output("PIN salah")
       output("Sisa percobaan", 3-i)
    endif
endfor

output("Absensi ditolak, terlalu banyak percobaan")
Endprogram
```

---

## Contoh Output Program

```text
Masukkan nama mahasiswa: Fauji
Masukkan PIN: 1111
PIN salah
Sisa percobaan 2

Masukkan PIN: 1234
Absensi berhasil
Nama: Fauji
```

---

## Tujuan Pembelajaran

* Memahami penggunaan **input & output**
* Menerapkan **percabangan (if-else)**
* Menggunakan **perulangan (loop)**
* Membuat logika autentikasi sederhana

---
