# Tugas-4

daftar_nilai = []

ulangi = True

while ulangi:
    nama = input("Masukan Nama: ")
    nim = input("Masukan Nim: ")
    nilai = int(input("Masukan Nilai Tugas: "))
    uts = int(input("Masukan Nilai UTS: "))
    uas = int(input("Masukan Nilai UAS: "))
    akhir = (nilai * 30 / 100) + (uts * 35 / 100) + (uas * 35 / 100)

    daftar_nilai.append([nama, int(nim), int(nilai),  int(uts), int(uas), int(akhir)])
    if (input("Tambah Data Lagi (y/t): ") == 't'):
        ulangi = False

print("\nDaftar Nilai Mahasiswa:")
print("=========================================================================================")
print("| NO |     Nama     |      Nim    | Nilai Tugas | Nilai UTS | Nilai UAS | Akhir |")
print("=========================================================================================")
i=0
for item in daftar_nilai:
    i+=1
    print("| {no:2d} | {nama:12s} | {nim:11d} | {nilai:5.2f} | {uts:5.2f} | {uas:5.2f} | {akhir:5.2f} |"
          .format(nama=item[0], nim=item[1], nilai=item[2], uts=item[3], uas=item[4], akhir=item[5], no=i))
