# Labspy06
## Latihan 1
- Ubahlah kode dibawah ini menjadi fungsi menggunakan *lambda*

```bash
import math
def a(x):
    return x**2
def b(x, y)
    return math.sqrt(x**2 + y**2)  
def c(*args):
    return sum(args)/len(args)
def d(s):
    return "".join(set(s))
```

### Penjelasan
- Untuk memperluas daftar fungsi matematika gunakan `import math`

- Fungsi lambda yang menggunakan variabel a-d
```baSH
def a(x):
    return x**2
    a = lambda x : x ** 2
print(a(2))
def b(x, y):
    return math.sqrt(x**2 + y**2)
    b = lambda x, y : x ** 2  + y ** 2
print(b(2, 2))
def c(*args):
    return sum(args)/len(args)
    c = lambda *args : sum(args)/len(args)
print(c(5, -1, 8, 19))
def d(s):
    return "".join(set(s))
    d = lambda s: "".join(set(s))
print(d("Jenab"))
```

### Output
![Screenshot (77)](https://user-images.githubusercontent.com/92736847/145682096-0a72b00d-b549-4426-bf69-8a07aee35495.png)
![Screenshot (78)](https://user-images.githubusercontent.com/92736847/145682101-6f69c99d-8947-4168-ae0a-38f301ce19ee.png)

## Praktikum
  Buat program sederhana dengan mengaplikasikan penggunaan fungsi yang akan menampilkan daftar nilai mahasiswa, dengan ketentuan:
 - Fungsi *tambah()* untuk menambah data
 - Fungsi *tampilkan()* untuk menampilkan data
 - Fungsi *hapus(nama)* untuk menghapus data berdasarkan nama
 - Fungsi *ubah(nama)* untuk mengubah data berdasarkan nama
 - Buatlah flowchart dan penjelasan programnya pada README.md

### Penjelasan
  Buatlah dictionary yang akan diinput dengan data
```bash
data = {}
```

  Membuat perulangan dan keterangan untuk pilihan menu
```bash
while True:
    c = input("\n(L)ihat, (T)ambah, (U)bah), (H)apus, (C)ari, (K)eluar: ")
```

- Menambahkan data yang akan diinput kemudian masuk ke dalam dictionary
```bash
if c.lower() == 't':
        print("Tambah Data")
        nama = input("Nama\t\t: ")
        nim = int(input("NIM\t\t: "))
        uts = int(input("Nilai UTS\t: "))
        uas = int(input("Nilai UAS\t: "))
        tugas = int(input("Nilai Tugas\t: "))
        akhir = tugas*30/100 + uts*35/100 + uas*35/100
        data[nama] = nim, uts, uas, tugas, akhir
```

Output Menambahkan Data


- Jika ingin menampilkan data dapat menggunakan
```py
elif c.lower() == 'l':
        if data.items():
            print("="*78)
            print("|                               Daftar Mahasiswa                             |")
            print("="*78)
            print("|No. | Nama            |       NIM       |  UTS  |  UAS  |  Tugas  |  Akhir  |")
            print("="*78)
            i = 0
            for z in data.items():
                i += 1
                print("| {no:2d} | {0:15s} | {1:15d} | {2:5d} | {3:5d} | {4:7d} | {5:7.2f} |"
                      .format(z[0][:13], z[1][0], z[1][1], z[1][2], z[1][3], z[1][4], no=i))
            print("=" * 78)
        else:
            print("="*78)
            print("|                               Daftar Mahasiswa                             |")
            print("="*78)
            print("|No. | Nama            |       NIM       |  UTS  |  UAS  |  Tugas  |  Akhir  |")
            print("="*78)
            print("|                                TIDAK ADA DATA                              |")
            print("="*78)
```

Mengubah data dapat menggunakan 
```py
elif c.lower() == 'u':
        print("Ubah Data")
        nama = input("Masukkan Nama   : ")
        if nama in data.keys():
            nim = int(input("NIM\t\t: "))
            uts = int(input("Nilai UTS\t: "))
            uas = int(input("Nilai UAS\t: "))
            tugas = int(input("Nilai Tugas\t: "))
            akhir = tugas*30/100 + uts*35/100 + uas*35/100
            data[nama] = nim, uts, uas, tugas, akhir
        else:
            print("Nama {0} tidak ditemukan".format(nama))
```

- Menghapus data dapat menggunakan
```py
elif c.lower() == 'h':
        print("Hapus Data")
        nama = input("Masukkan Nama  : ")
        if nama in data.keys():
            del data[nama]
        else:
            print("Nama {0} Tidak Ditemukan".format(nama))
```

- Mencari data dapat menggunakan
```py
 elif c.lower() == 'c':
        print("Cari Data[case-sensitive]")
        nama = input("Masukkan Nama : ")
        if nama in data.keys():
            print("="*73)
            print("|                             Daftar Mahasiswa                          |")
            print("="*73)
            print("| Nama            |       NIM       |  UTS  |  UAS  |  Tugas  |  Akhir  |")
            print("="*73)
            print("| {0:15s} | {1:15d} | {2:5d} | {3:5d} | {4:7d} | {5:7.2f} |"
                  .format(nama, nim, uts, uas, tugas, akhir))
            print("="*73)
        else:
            print("Nama {0} Tidak Ditemukan".format(nama))
```

- Jika sudah selesai input pilih menu 'K' untuk memberhentikan program
```py
elif c. lower() == 'k':
        break
```
### output
![Screenshot (70)](https://user-images.githubusercontent.com/92736847/145682176-4d721989-09f9-48a7-a075-aa837e27aae9.png)
![Screenshot (71)](https://user-images.githubusercontent.com/92736847/145682177-7fac3590-1140-4f17-89fa-2eaa2d48ccdd.png)
![Screenshot (76)](https://user-images.githubusercontent.com/92736847/145682173-30f67549-93a7-4aac-81b1-54eb53ff03ae.png)

### flowchart

![png](https://user-images.githubusercontent.com/92736847/145682224-31098e61-3ef2-4f3f-872a-6326e133a49d.png)








