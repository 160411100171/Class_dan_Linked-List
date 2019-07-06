# Class_dan_Linked-List
Modul 3 - Struktur Data

Class - suatu nama dari sebuah tipe data baru yang dapat berisi integer,list,tupple,dic,dll

----------------------------------------------------------------------------------------------------------------------------------
String dan List - variabel yang berbentuk lists ataupun string, memiliki dua buah elemen yang terkandung di dalam variabel tersebut, yaitu nilai atau state/property, serta method atau fungsi, yang digunakan untuk mengolah nilai pada variabel tersebut.

namaObyek.NamaMethod()

        # String
        dataStr='Struktur Data' 
        print(dataStr)
        dataStr=dataStr.upper()
        print(dataStr)

# Lists
dataLs=[4,10,21]
print(dataLs)
data.append(45)
print(dataLs)


Istilah dalam PBO – 
Beberapa istilah dasar yang terdapat pada pemrograman berbasis object ini antara lain :
•	class, tipe data yang tidak hanya berisi data tetapi juga method
•	object, suatu variabel dengan tipe data class
•	state, property, bagian data dari suatu class yang berisi nilai, dapat berupa string, integer, float
•	method, fungsi yang melekat pada class
•	constructor, fungsi yang dijalankan oleh python ketika pertama kali suatu objek dibuat.  Method constructor ini dibuat dengan cara mendefinisikan fungsi _ init _ (dua underscore)
•	self, merupakan suatu argumen atau parameter spesial agar nilai balik dari method dikembalikan ke objek itu sendiri.  Argumen ini tidak perlu dipanggil (walaupun sudah didefinisikan)pada saat pemanggilan method
•	instance, suatu objek yang telah dibuat
•	override, mendefinisikan kembali fungsi-fungsi umum yang sudah ada, agar sesuai dengan kebutuhan programmer.

Constructor - method yang otomatis dijalankan ketika suatu obyek dibuat dan inisialisasi baru untuk data agar tidak boros variable.

def __ini__():
