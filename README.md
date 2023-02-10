# PERTEMUAN 11
<p> Nama    :   MAFTUKHIN JAFAR NADWI <p>
<p> NIM     :   312210704
<p> Kelas   :   TI.22.C9

## Latihan 1
![2](https://user-images.githubusercontent.com/124107247/218024069-0557173a-0266-4a93-b95d-4590a7cdb62d.png)

<p> berikut kode programnya <p>

```python
import math
def a(x):
  return x**2
a = lambda x : x**2
print(a(2))
def b(x, y):
  return math.sqrt(x**2 + y**2)
b = lambda x, y : x ** 2 + y ** 2
print(b(2, 2))
def c(*args):
  return sum(args)/len(args)
c = lambda *args : sum(args)/len(args)
print(c(1,2,3,4,5))
def d(s):
  return "".join(set(s))
d = lambda s: "".join(set(s))
print(d("buku"))
```
<p> Hasil run seperti berikut <p>

![latihan2](https://user-images.githubusercontent.com/124107247/218022984-4853748f-6e49-4626-87ae-4d8d77cb8a94.png)


## Tugas Praktikum

![3 (1)](https://user-images.githubusercontent.com/124107247/218024098-032638c5-ce5a-4b56-af9a-8d224e9fa498.png)

<p> berikut kode programnya <p>

```python
x = {}
def tambah():
    print("Tambah Data")
    nama = input("Masukkan Nama Mahasiswa   : ")
    nim = input("Masukkan NIM              : ")
    tugas = int(input("Masukkan Nilai Tugas      : "))
    uts = int(input("Masukkan Nilai UTS        : "))
    uas = int(input("Masukkan Nilai UAS        : "))
    akhir = tugas * 30/100 + uts * 35/100 + uas * 35/100
    x[nama] = nim , tugas, uts , uas , akhir
def tampilkan():
    if x.items():
        print("---------------------------------------------------------------------------------")
        print("\n                               DAFTAR NILAI MAHASISWA                    ")
        print("---------------------------------------------------------------------------------")
        print("| No |      Nama      |     NIM     |  Tugas  |   UTS   |   UAS   |    Akhir    |")
        print("---------------------------------------------------------------------------------")
        i = 0                                                                         
        for b in x.items():                                                             
             i += 1
             print("| {no:2d} | {0:14s} | {1:11s} | {2:7d} | {3:7d} | {4:7d} | {5:7f}   |"
                . format ( b [ 0 ][: 14 ], b [ 1 ][ 0 ], b [ 1 ][ 1 ], b [ 1 ][ 2 ], b [ 1 ][ 3 ], b [ 1 ][ 4 ] , no = i ))
        print("---------------------------------------------------------------------------------")
    else :
        print("---------------------------------------------------------------------------------")
        print("\n                               DAFTAR NILAI MAHASISWA                    ")
        print("---------------------------------------------------------------------------------")
        print("| No |      Nama      |     NIM     |  Tugas  |   UTS   |   UAS   |    Akhir    |")
        print("---------------------------------------------------------------------------------")
        print("|                                TIDAK ADA DATA                                 |")
        print("---------------------------------------------------------------------------------")
def hapus():
    print ( "Hapus Data" )
    nama = input("Masukkan Nama Mahasiswa   : ")
    if  nama in  x . keys ():
        del  x [ nama ]
    else :
        print ( "Nama {0} Tidak Ditemukan" . format ( nama ))
def ubah():
    print ( "Ubah Data" )
    nama = input("Masukkan Nama Mahasiswa   : ")
    if nama in  x . keys ():
        nim = input("Masukkan NIM              : ")
        tugas = int(input("Masukkan Nilai Tugas      : "))
        uts = int(input("Masukkan Nilai UTS        : "))
        uas = int(input("Masukkan Nilai UAS        : "))
        akhir = tugas * 30/100 + uts * 35/100 + uas * 35/100
        x[nama] = nim , tugas, uts , uas , akhir
    else :
        print ( "Nama{0} Tidak Ditemukan" . format(nama ))
while True:
    print("")
    print("===========================")
    print("|   Program Input Nilai   |")
    print("===========================")
    c = input("L)ihat, T)ambah, U)bah, H)apus, K)eluar: ")
    if c.lower() == "l":
        tampilkan()
    elif c.lower() == "t":
        tambah()
    elif c.lower() == "u":
        ubah()
    elif c.lower() == "h":
        hapus()
    elif c.lower() == "k":
        print()
        print("---------------------------------------------------------------------------------")
        print("                                 PROGRAM TELAH SELESAI                    ")
        print("---------------------------------------------------------------------------------")
        break
    else:
        print()
        print("Kode yang anda masukkan salah!")
```

<p> kemudian run, dan akan muncul pilihan seperti berikut <p>

![Untitled10](https://user-images.githubusercontent.com/124107247/218023071-c9b8d44e-f7d9-4d46-b709-e595fcb413db.png)

<p> kemudian ketik huruf sebagai pilihan yang diinginkan <p>
<p> L = untuk melihat/menampilkan data <p>
<p> T = untuk menambahkan data <p>
<p> U = untuk mengubah data <p>
<p> H = untuk menghapus data <p>
<p> K = untuk keluar dari program ini <p>

### T)ambah
<p> ketik t, kemudian isi data. misal mengisi 2 data<p>

![Untitled20](https://user-images.githubusercontent.com/124107247/218023161-d761dd51-4a5a-46e1-89c8-9b10671afb32.png)

### L)ihat
<p> ketik l, kemudian menampilkan data yang tadi ditambahkan <p>

![Untitled30](https://user-images.githubusercontent.com/124107247/218023194-c24b1ff7-4743-4bb0-af31-991fb277c916.png)


### U)bah
<p> ketik u, kemudian ubah data yang diinginkan 

![Untitled40](https://user-images.githubusercontent.com/124107247/218023260-b312ee4d-2bf2-46e5-a9de-7253093a19df.png)

### H)apus
<p> ketik h, kemudian ketik nama data yang akan dihapus <p>

![Untitled50](https://user-images.githubusercontent.com/124107247/218023307-19dba525-d885-45a9-928a-ec2e20a88a30.png)

### K)eluar

![Untitled60](https://user-images.githubusercontent.com/124107247/218023364-9fea1332-5c87-4b7e-be42-c6f0c202d35b.png)
<p> makasi <p>
