# Praktikum 8
# Nama : Muhammad Dikaisa ibnu amin
# Nim : 312210289
# Kelas : TI.22.A.3

# Input

1. Pertama buat deklarasi class 
```python
class Mahasiswa:
    nama = ""
    nim = ""
    uts = ""
    uas = ""
    tugas = ""
    akhir = ""
```
    
2. Buat list kosong data mahasiswa
```python
DataMhs = []
```

3. Buat Fungsi Tambah data
```python
def add():
    system("cls")
    Mhs = Mahasiswa()
    print("TAMBAH DATA")

    Mhs.nama = input("Nama        : ")
    Mhs.nim  = input("NIM         : ")
    Mhs.tugas = int(input("Nilai Tugas : "))
    Mhs.uts = int(input("Nilai UTS   : "))
    Mhs.uas = int(input("Nilai UAS   : "))
    Mhs.akhir = (Mhs.tugas * 30/100) + (Mhs.uts * 35/100) + (Mhs.uas * 35/100)

    DataMhs.append(Mhs)
```

4. Buat Fungsi Tampilkan data yang sudah di input
```pyhton
def show():
    system("cls")
    print("      DAFTAR NILAI MAHASISWA")
    if len(DataMhs) <= 0:
        print("=================================")
        print("         TIDAK ADA DATA")
        print("\n")
        print("=================================")
    else:
        for Mhs in DataMhs:
            print("=================================")
            print("Nama        : {} ".format(Mhs.nama))
            print("NIM         : {} ".format(Mhs.nim))
            print("Nilai Tugas : {} ".format(Mhs.tugas))
            print("Nilai UTS   : {} ".format(Mhs.uts))
            print("Nilai UAS   : {} ".format(Mhs.uas))
            print("Nilai Akhir : {:.1f} ".format(Mhs.akhir))
            print("=================================")
```

5. Buat Fungsi untuk menghapus data
```python
def delete():
    system("cls")
    print("HAPUS DATA")
    nama = Mahasiswa()
    nama = input("Nama : ")
    for data in DataMhs:
        if nama == data.nama:
            DataMhs.remove(data)

            print("Berhasil Dihapus")
    
        else:
            print("DATA TIDAK DITEMUKAN")
```            

6. Buat fungsi untuk mengubah data 
```python
def update():
    system("cls")
    print("UBAH DATA")
    nama = Mahasiswa()
    nama = input("Nama : ")
    print("\n")

    for data in DataMhs:
        if nama == data.nama:
            data.tugas = int(input("Nilai Tugas : "))
            data.uts = int(input("Nilai UTS   : "))
            data.uas = int(input("Nilai UAS   : "))
            data.akhir = (data.tugas * 30/100) + (data.uts * 35/100) + (data.uas * 35/100)

            print("DATA BERHASIL DIUBAH")

        else:
            print("DATA TIDAK DITEMUKAN")
```            

7. Program untuk looping, menggunakan while
```python
while True:
    print("\n")
    print("==========================")
    print("    Program Input Nilai   ")
    print("==========================")

    print("[1] LIHAT DATA")
    print("[2] TAMBAH DATA")
    print("[3] UBAH DATA ")
    print("[4] HAPUS DATA")
    print("[5] KELUAR ")

    ask = input("PILIH MENU >")

    if ask == '1':
        show()

    elif ask == '2':
        add()
    
    elif ask == '3':
        update()
    
    elif ask == '4':
        delete()
    
    elif ask == '5':
        print("\n")
        print("thank you for using the code :) ")

        exit()

    else:
        print("KELEBIHAN !!!!!!!!!!!!!!!!")
```        

# Output

<img width="223" alt="pert12 1" src="https://user-images.githubusercontent.com/115516378/207048407-dda35f91-2606-4d45-a432-cb00facd961a.png">
