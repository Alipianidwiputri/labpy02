# labpy02

# latihan 1 : membuat program menentukan nilai akhir

![Latihan 1 bahasa pemograman](https://github.com/user-attachments/assets/dbefdf90-4a73-4dff-babe-70e50a59b795)
Input Data:

Kode ini meminta pengguna untuk memasukkan nilai tugas, UTS (Ujian Tengah Semester), dan UAS (Ujian Akhir Semester).

Penentuan Keterangan Lulus atau Tidak:

Jika nilai akhir lebih dari 60, maka keterangan akan menjadi "LULUS", jika tidak akan menjadi "TIDAK LULUS".

Penentuan Nilai Huruf:

Nilai huruf diberikan berdasarkan rentang nilai akhir: A jika lebih dari 80 B jika lebih dari 70 C jika lebih dari 50 D jika lebih dari 40 E jika di bawah atau sama dengan 40

# Latihan 2 : Membuat programan menampilkan status gaji karyawan

![Latihan 2 bahasa pemograman](https://github.com/user-attachments/assets/e7ab151a-6dce-4a0f-bbb5-a637781fc346)

Input Data:

Kode ini meminta pengguna untuk memasukkan gaji, status keluarga, dan kepemilikan rumah. Variabel gaji menyimpan nilai gaji sebagai integer. Variabel berkeluarga akan bernilai True jika pengguna memasukkan "Y" (sudah berkeluarga) dan False jika "T". Variabel punya_rumah akan bernilai True jika pengguna memasukkan "Y" (punya rumah) dan False jika "T".

Pengecekan Gaji:

Jika gaji lebih dari 3.000.000, maka program akan mencetak "Gaji sudah di atas UMR". Jika tidak, program akan langsung mencetak "Gaji belum UMR" pada bagian else.

Pengecekan Status Keluarga:

Jika berkeluarga bernilai True, program akan menampilkan "Wajib ikutan asuransi dan menabung untuk pensiun". Jika berkeluarga bernilai False, program akan menampilkan "Tidak perlu ikutan asuransi". Pengecekan

Kepemilikan Rumah:

Jika punya_rumah bernilai True, program akan menampilkan "Wajib bayar pajak rumah". Jika punya_rumah bernilai False, program akan menampilkan "Tidak wajib bayar pajak rumah".

Gaji di Bawah UMR:

Jika gaji tidak lebih dari 3.000.000, program akan langsung menampilkan "Gaji belum UMR" tanpa melakukan pengecekan tambahan.

Hasil Program:

Pada contoh output di sisi kanan gambar, jika gaji 5.000.000, status berkeluarga "T", dan punya rumah "Y": Program menampilkan bahwa gaji di atas UMR. Menampilkan bahwa pengguna Tidak perlu ikutan asuransi Tidak wajib bayar pajak rumah

# Latihan 3 : Memggunkan kondisi OR Program membandingkan 3 input bilangan, apabila penjumlahan 2 bilangan hasilnya sama dengan bilangan lainnya, maka cetak pernyataan "BENAR"

![Latihan 3 bahasa pemograman](https://github.com/user-attachments/assets/56c372e8-6aa9-4d0f-aabf-d7a431e1f386)

Input Data:

Kode ini meminta pengguna untuk memasukkan tiga bilangan: a, b, dan c. Input dari pengguna dikonversi ke tipe int agar dapat digunakan dalam operasi aritmatika

# Latihan 3 Kasus 1 Pemesanan Tiket Bioskop

![Flowchartr](https://github.com/user-attachments/assets/7a19516e-b0a6-42dc-a53d-b946a2c63ea0)

![Screenshot 2024-11-01 174235](https://github.com/user-attachments/assets/74c223fd-b798-4f19-b907-08329c78be39)

Saya akan menjelaskan alur flowchart tersebut yang menggambarkan sistem pembayaran dengan dua tipe tiket:

Mulai dari atas, terdapat pilihan jenis tiket:

Reguler dengan harga dasar Rp 50.000

VIP dengan harga dasar Rp 100.000

Kemudian ada pengecekan status member:

Jika "Ya" (anggota):

Dari Regular: Mendapat diskon 20% sehingga total bayar = Rp 40.000

Dari VIP: Mendapat diskon 20% sehingga total bayar = Rp 80.000

Jika "Tidak" (bukan member):

Dari Regular: Tidak ada diskon, total bayar = Rp 50.000

Dari VIP: Tidak ada diskon, total bayar = Rp 100.000

Semua alur berakhir di "Selesai" setelah perhitungan total pembayaran

Sistem ini menerapkan:

Dua kategori tiket (Reguler dan VIP)

Sistem keanggotaan yang memberikan keuntungan diskon 20%

Harga akhir yang berbeda tergantung kombinasi tipe tiket dan status member

Penjelasan code tersebut bagian per bagian:
1.	Definisi Fungsi dan Header:
def hitung_harga_tiket():
    print("=== Program Pemesanan Tiket Bioskop ===")
    print("1. Reguler (Rp50.000)")
    print("2. VIP (Rp100.000)")
•	Definisikan fungsi bernamahitung_harga_tiket
•	Menampilkan judul program dan menu pilihan tiket
2.	Input Tipe Tiket:
while True:
        try:
            tipe_tiket = int(input("\nPilih tipe tiket (1/2): "))
            if tipe_tiket in [1, 2]:
                break
            print("Error: Pilihan tidak valid. Silakan pilih 1 atau 2.")
        except ValueError:
            print("Error: Masukkan angka 1 atau 2.")
•	Menggunakan loop while Trueuntuk terus meminta input sampai valid
•	try-exceptmenangani kesalahan jika pengguna memasukkan bukan angka
•	if tipe_tiket in [1, 2]memeriksa apakah inputnya 1 atau 2
•	breakkeluar dari loop jika input valid
3.	Status Input Anggota:
while True:
        member = input("Apakah anda memiliki kartu member? (y/n): ").lower()
        if member in ['y', 'n']:
            break
        print("Error: Masukkan 'y' untuk ya atau 'n' untuk tidak.")
•	Loop yang sama untuk status anggota
•	.lower()mengubah input menjadi huruf kecil
•	Memeriksa apakah inputnya adalah 'y' atau 'n'
4.	Penghitungan Harga dengan Operator Ternary:
    harga_dasar = 50000 if tipe_tiket == 1 else 100000
    diskon = 0.2 if member == 'y' else 0
•	Format terner operator:nilai_jika_benar if kondisi else nilai_jika_salah
•	Jika tipe_tiket == 1, harga 50000, jika tidak 100000
•	Jika member == 'y', diskon 0,2 (20%), jika tidak 0
5.	Menghitung Harga Akhir:
harga_akhir = harga_dasar * (1 - diskon)
•	Menghitung harga setelah diskon
•	Contoh: jika harga 100000 dan diskon 0,2, maka: 100000 * (1 - 0,2) = 80000
6.	Menampilkan Hasil:
    print("\n=== Detail Pemesanan ===")
    print(f"Tipe Tiket: {'Reguler' if tipe_tiket == 1 else 'VIP'}")
    print(f"Status Member: {'Ya' if member == 'y' else 'Tidak'}")
    print(f"Harga Dasar: Rp{harga_dasar:,.0f}")
    print(f"Diskon: {diskon * 100:.0f}%")
    print(f"Total Bayar: Rp{harga_akhir:,.0f}")
•	Menggunakan f-string untuk memformat output
•	:,.0funtuk format angka dengan pemisah ribuan tanpa desimal
•	Menggunakan operator ternary lagi untuk menampilkan tipe tiket dan status member
7.	Menjalankan Program:
if __name__ == "__main__":
    hitung_harga_tiket()
•	Pemutaran fungsi hanya dijalankan jika file dieksekusi langsung (tidak diimpor sebagai modul)


Program di atas memiliki beberapa fitur:
1.	Menggunakan operator ternary untuk: 
•	Menentukan harga dasar:harga_dasar = 50000 if tipe_tiket == 1 else 100000
•	Hitung diskon:diskon = 0.2 if member == 'y' else 0
2.	Validasi masukan: 
•	mengubah tipe tiket yang dimasukkan valid (1 atau 2)
•	mengubah status member yang dimasukkan valid (y atau n)
3.	Format keluaran yang rapi: 
•	Menggunakan format mata uang dengan perpecahan ribuan
•	Menampilkan detail pemesanan secara terstruktur
4.	Penanganan kesalahan: 
•	Gunakan try-kecuali untuk menangani input yang tidak valid
Memberikan pesan error yang informative













 Jawaban (Contoh Program) :
=== Program Pemesanan Tiket Bioskop ===  
1. Reguler (Rp50.000)
2. VIP (Rp100.000)

Pilih tipe tiket (1/2): 1
Apakah anda memiliki kartu member? (y/n): y

=== Detail Pemesanan ===
Tipe Tiket: Reguler
Status Member: Ya
Harga Dasar: Rp50,000
Diskon: 20%
Total Bayar: Rp40,000















Penjelasan contoh program :
1.	Tampilan Awal Menu
=== Program Pemesanan Tiket Bioskop ===  
1. Reguler (Rp50.000)
2. VIP (Rp100.000)
•	Program menampilkan 2 pilihan tipe tiket
•	Reguler dengan harga Rp50.000
•	VIP dengan harga Rp100.000
2.	Input Pemilihan Tiket
Pilih tipe tiket (1/2): 1
•	Pengguna diminta memilih angka 1 atau 2
•	Dalam contoh ini pengguna memilih 1 (Reguler)
3.	Status Input Anggota
Apakah anda memiliki kartu member? (y/n): y
•	Pengguna diminta memasukkan y atau n untuk status anggota
•	y = Ya, memiliki kartu member
•	n = Tidak memiliki anggota kartu
•	Dalam contoh ini pengguna memilih y (Ya)
4.	Detail Pemesanan
=== Detail Pemesanan ===
Tipe Tiket: Reguler
Status Member: Ya
Harga Dasar: Rp50,000
Diskon: 20%
Total Bayar: Rp40,000
•	Harga dasar Reguler = Rp50.000
•	Karena memiliki kartu member, dapat diskon 20%
•	Diskon perhitungan: 20% × Rp50.000 = Rp10.000
•	Total bayar: Rp50.000 - Rp20.000 = Rp40.000
Jika kasusnya berbeda:
1.	Jika pilih VIP (2) dan member (y): 
o	Harga dasar = Rp100.000
o	Diskon 20% = Rp20.000
o	Total pembayaran = Rp80.000
2.	Jika pilih VIP (2) tapi non-anggota (n): 
o	Harga dasar = Rp100.000
o	Tidak ada diskon
o	Total pembayaran = Rp100.000
3.	Jika pilih Reguler (1) dan non-member (n): 
o	Harga dasar = Rp50.000
o	Tidak ada diskon
o	Total pembayaran = Rp50.000


# Latihan 3 Khusus 2 Program Kalkulator Sederhana
![WhatsApp Image 2024-11-01 at 16 20 10_4cc33fec](https://github.com/user-attachments/assets/1db00987-4f7e-4895-8db1-43df3813a20a)

![Screenshot 2024-11-01 174459](https://github.com/user-attachments/assets/b1eb7745-1b6a-4277-a5f0-82c4481a0b74)

penjelasan python :
Saya akan menjelaskan kode tersebut secara detail:
1.	Definisi Fungsi:
ular piton
Menyalin
def kalkulator():
    """
    Program kalkulator sederhana yang dapat melakukan operasi dasar aritmatika
    (penjumlahan, pengurangan, perkalian, dan pembagian)
    """
•	Ini mendefinisikan fungsi bernamakalkulator()
•	Teks dalam """ """ adalah docstring yang menjelaskan fungsi tersebut
2.	Tampilan Menu:
ular piton
Menyalin
print("=== Program Kalkulator Sederhana ===")
print("Operasi yang tersedia:")
print("1. Penjumlahan (+)")
print("2. Pengurangan (-)")
print("3. Perkalian (*)")
print("4. Pembagian (/)")
•	Menampilkan judul program dan daftar operasi yang tersedia
•	Memberikan informasi kepada pengguna tentang operator yang bisa digunakan
3.	Blok Coba-Kecuali:
ular piton
Menyalin
try:
    angka1 = float(input("\nMasukkan angka pertama: "))
    angka2 = float(input("Masukkan angka kedua: "))
    operator = input("Masukkan operator (+, -, *, /): ")
•	trydigunakan untuk menangani kemungkinan error
•	float(input())mengubah input string dari pengguna menjadi angka desimal
•	Jika pengguna memasukkan input yang bukan angka, akan ditangkap olehexcept ValueError
4.	Struktur Bersyarat:
ular piton
Menyalin
if operator == '+':
    hasil = angka1 + angka2
    print(f"\nHasil: {angka1} + {angka2} = {hasil}")
elif operator == '-':
    hasil = angka1 - angka2
    print(f"\nHasil: {angka1} - {angka2} = {hasil}")
•	Menggunakan if-elifuntuk memeriksa operator yang dimasukkan
•	Setiap blok melakukan operasi aritmatika yang sesuai
•	Hasil menggunakan f-string yang ditampilkan untuk memformat output
5.	Penanganan Kasus Khusus:
ular piton
Menyalin
elif operator == '/':
    if angka2 == 0:
        print("\nError: Pembagian dengan nol tidak diperbolehkan!")
    else:
        hasil = angka1 / angka2
        print(f"\nHasil: {angka1} / {angka2} = {hasil}")
•	Untuk Pembagian, ada pengecekan tambahan untuk mencegah pembagian dengan nol
•	Jika angka kedua adalah 0, tampilkan pesan error
•	Jika bukan 0, lakukan pembagian
6.	Penanganan Kesalahan:
ular piton
Menyalin
except ValueError:
    print("\nError: Masukkan angka yang valid!")
•	Menangkap error jika input bukan angka yang valid
•	Menampilkan pesan error yang informatif
7.	Menjalankan Program:
ular piton
Menyalin
if __name__ == "__main__":
    kalkulator()
•	Kondisi ini memeriksa apakah file dijalankan langsung (tidak diimpor sebagai modul)
•	Jika ya, maka fungsi kalkulator()akan dijalankan
Program ini menggunakan konsep-konsep penting dalam Python:
•	Fungsi
•	Masukan/Keluaran
•	Penanganan kesalahan (coba-kecuali)
•	Struktur kontrol (if-elif-else)
•	Konversi tipe (float())
•	Pemformatan string (f-string)

Program di atas memiliki beberapa fitur:
1.	Menu yang menampilkan operasi yang tersedia
2.	Masukan ke dua angka dan operator
3.	Penanganan operasi aritmatika menggunakan if-elif-else
4.	Penanganan kesalahan untuk: 
o	Pembagian dengan nol
o	Input yang bukan angka (ValueError)
o	Operator yang tidak valid
Cara menggunakan program:
1.	Jalankan program
2.	Masukkan angka pertama
3.	Masukkan angka kedua
4.	Masukkan operator yang diinginkan (+, -, *, /)
5.	Program akan menampilkan hasil perhitungan


contoh program :
=== Program Kalkulator Sederhana ===
Operasi yang tersedia:
1. Penjumlahan (+)
2. Pengurangan (-)
3. Perkalian (*)
4. Pembagian (/)
Masukkan angka pertama: 5
Masukkan angka kedua: 10
Masukkan operator (+, -, *, /): *
Hasil: 5.0 * 10.0 = 50.0

=== Program Selesai ===
PS C:\Users\user\OneDrive\Documents>

Penjelasan contoh program di atas :
Saya akan menjelaskan detail dari contoh program eksekusi tersebut:
1.	Tampilan Awal Program:
Menyalin
=== Program Kalkulator Sederhana ===
Operasi yang tersedia:
1. Penjumlahan (+)
2. Pengurangan (-)
3. Perkalian (*)
4. Pembagian (/)
•	Ini adalah tampilan menu awal program
•	Menunjukkan kepada pengguna operasi matematika yang tersedia
•	Setiap operasi diberi nomor dan simbol operatornya
2.	Input Pertama:
Menyalin
Masukkan angka pertama: 5
•	Program meminta pengguna memasukkan angka pertama
•	Pengguna memasukkan angka 5
•	Program mengkonversi input "5" menjadi float (5.0)
3.	Input Kedua:
Menyalin
Masukkan angka kedua: 10
•	Program meminta pengguna memasukkan angka kedua
•	Pengguna memasukkan angka 10
•	Program mengkonversi input "10" menjadi float (10.0)
4.	Operator Masukan:
Menyalin
Masukkan operator (+, -, *, /): *
•	Program meminta pengguna memilih operator
•	Pengguna memilih operator perkalian (*)
5.	Hasil Perhitungan:
Menyalin
Hasil: 5.0 * 10.0 = 50.0
•	Program menampilkan hasil perhitungan dalam format: 
o	Angka pertama (5.0)
o	Operator (*)
o	Angka kedua (10.0)
o	Tandai sama dengan (=)
o	Hasil perhitungan (50.0)
•	Perhitungan yang dilakukan: 5×10 = 50
•	Hasilnya ditampilkan dalam format float (50.0)
6.	Akhir Program:
Menyalin
=== Program Selesai ===
•	Menandakan program telah selesai menjalankannya
•	Program berakhir dengan sukses tanpa kesalahan
Dalam contoh ini:
•	Program berhasil menerima dua angka (5 dan 10)
•	Operator yang dipilih adalah perkalian (*)
•	Program melakukan perkalian: 5 × 10
•	Menghasilkan output 50.0
•	Semua input valid sehingga tidak ada pesan error
•	Program berjalan dengan lancar dari awal hingga akhir
Program ini mendemonstrasikan cara kerja kalkulator sederhana yang:
1.	Menerima masukan dari pengguna
2.	Memproses input tersebut
3.	Melakukan perhitungan matematika
4.	Menampilkan hasil dengan format yang rapi
5.	Mengakhiri eksekusi dengan teratur




Secara praktis, pelanggan dapat menghemat:

Rp 10.000 untuk tiket Regular jika memiliki keanggotaan

Rp 20.000 untuk tiket VIP jika memiliki keanggotaan
