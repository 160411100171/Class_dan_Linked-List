# Class_dan_Linked-List
Modul 3 - Struktur Data

Class - suatu nama dari sebuah tipe data baru yang dapat berisi integer,list,tupple,dic,dll

--------------------------------------------------------------------------------------------------------------------------------
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

--------------------------------------------------------------------------------------------------------------------------------
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

--------------------------------------------------------------------------------------------------------------------------------
Constructor - method yang otomatis dijalankan ketika suatu obyek dibuat dan inisialisasi baru untuk data agar tidak boros variable.

        def __ini__():

--------------------------------------------------------------------------------------------------------------------------------
Method - merupakan fungsi-fungsi yang terdapat di dalam suatu class.

        def namaMethod():
                namaObyek.anamMethod()

--------------------------------------------------------------------------------------------------------------------------------
Override Method - penambahan fungsi-fungsi pada syntax-syntax yang sudah ada. Seperti yang dijelaskan sebelumnya, untuk menampilkan property yang terdapat pada suatu obyek, 
tidak dapat dilakukan dengan menggunakan perintah print().

        def __init__():
        override
        adalah suatu penamaan fungsi agar tidak memakan banyak kalimat 

        def __str__():
        override method:
        adalah sebuah penamaan method
        def __add__():

--------------------------------------------------------------------------------------------------------------------------------
        class BilanganKompleks:
            def __init__(self,a,b):
                self.real=a
                self.im=b
            def display(self):
                print (self.real,'+',self.im,'i')
            def __str__(self):
                return str(self.real) + " + " + str(self.im) + " i "
            def addKompleks(self,obj):
                a=self.real+obj.real
                b=self.im+obj.im
                return BilanganKompleks(a,b)
        data1=BilanganKompleks(4,6)
        data2=BilanganKompleks(2,5)
        jumlah=data1.addKompleks(data2)
        data1.display()
        data2.display()
        print(jumlah)

--------------------------------------------------------------------------------------------------------------------------------
Linked List - data berupa list yang biasanya ada di python namun linked list tidak ada di python.
manfaat linked list:
1.	Bisa menambah data sewaktu waktu
2.	Bisa del data di mana mana
3.	Bisa insert data di mana mana
4.	Dinamis bisa di ubah

--------------------------------------------------------------------------------------------------------------------------------
Node List - metode untuk mencari alamat sebuah data yang tersimpan di memory point penting node:
1.	data
2.	pointer

--------------------------------------------------------------------------------------------------------------------------------
Travel List - karena dengan method travel kita dapat jalan jalan mengetahui data yang di masukkan.

Berikut adalah class node list dan travel: 

        class LinkedList:
            def __init__(self):
                self.head = None
            def isEmpty(self):
                return self.head==None
            def add(self, item):
                temp = Node(item)
                temp.setNext(self.head)
                self.head = temp
            def size(self):
                curent = self.head
                count = 0
                while curent != None:
                    count = count + 1

                    curent = curent.getNext()           
                return count
        mylist=LinkedList()
        mylist.add(45)
        mylist.add(34)
        mylist.add(70)
        print(mylist.size())

        output: 3

--------------------------------------------------------------------------------------------------------------------------------
Tugas Praktikum
1.	Buatlah class Matrix dengan beberapa method seperti berikut : 
a.	Constructor : untuk inisialisasi matriks, dengan parameter berupa jumlah baris dan kolom suatu matrix, dan elemen matriks merupakan inputan dari user (di dalam constructor)
b.	Override method __str__ : untuk menampilkan matriks. Gunakan formatting string jika diperlukan 
c.	Override method __add__ : untuk menjumlahkan dua buah matriks. 
Pada method ini, haruslah dilakukan pengecekan, jika ukuran dua buah matriks yang akan dijumlahkan tidak sama, maka akan mengeluarkan warning bahwa ukuran tidak sama 
d.	Override method __mul__ : untuk mengalikan dua buah matriks 
Pada method ini, haruslah dilakukan pengecakan, jika jumlah kolom pada matriks pertama tidak sama dengan jumlah baris pada matriks kedua, maka akan mengeluarkan warning bahwa ukuran matriks tidak sesuai. 

Berikut adalah contoh penggunaan class Matrix

        class matriks:
            #mat = ()

            def __init__(self,baris,kolom):
                self.b = []
                self.baris = baris
                self.kolom = kolom
                for line in range (self.baris):
                    k = []
                    for cols in range(self.kolom):
                        k.append(0)
                    self.b.append(k)
                inp = int(input("Masukkan jumlah element: "))
                for i in range(inp):
                    bar = str(input("Baris ke ? "))
                    kol = str(input("Kolom ke ? "))
                    element = str(input("baris [{}][{}] : ".format(bar.kol)))
                    self.b[bar][kol] = element

            def __str__(self):
                data = ""
                for i in range(len(self.b)):
                    data += "| "
                    for t in range(len(self.b[0])):
                        data += str(self.b[i][t])
                    data += " |\n"
                return data

            def __add__(self, tambah):
                angka = "1234567890"
                mat1 =[]
                kol1 = []
                hasil = []
                data = ""
                for t in range(len(tambah.b)):
                    if str(tambah.b[t]) in angka:
                        kol1.append(tambah.b[t])
                    else:
                        kol1 = []
                        mat1.append(kol1)
                if len(self.b) == len(tambah.b):
                    if len(tambah.b[0]) == len(self.b[0]):
                        for u in range(len(self.b)):
                            data += "| "
                            kolo =[]
                            for j in range(le(self.b[0])):
                                has = tambah.b[u][j] + self.b[u][j]
                                data += str(has)
                                kolo.append(has)
                            mat1.append(kolo)
                            data += " |\n"
                        return "Hasil Penjumlahan\n" + data
                    else:
                        return "Penjumlahan tidak bisa dilakukan karena jumlah kolom tidak sama"
                else:
                    return "Penjumlahan tidak bisa dilakukan karena jumlah baris tidak sama"

            def __mul__(self, kali):
                angka = "1234567890"
                data = ""
                mat1 = []
                kol1 = []
                for t in range(len(kali.b)):
                    if str(kali.b[t]) in angka:
                        kol1.append(kali.b[t])
                    else:
                        kol1 = []
                        mat1.append(kol1)
                if len(self.b[0]) == len(kali.b):
                    mat_bar = []
                    for i in range(len(self.b)):
                        data += "| "
                        hasil = 0
                        mat_kol = []
                        for y in range(len(kali.b[0])):
                            for t in range(len(self.b[0])):
                                a= self.b[i][t]
                                b= kali.b[t][y]
                                perkalian = a*b
                                hasil = hasil + perkalian
                            data += str(hasil)
                            mat_kol.append(hasil)
                        mat_bar.append(hasil)
                        data += " |\n"
                    return "hasil dari perkalian = \n" + data
                else:
                    return "perkalian tidak bisa dilakukan karena jumlah kolom matriks1 tidak sama"

        obj1 = matriks(2,2)
        print(obj1)
        obj2 = matriks(2,2)
        print(obj2)
        jumlah = obj1.__add__(obj2)
        print(jumlah)

        kali = obj1.__mul__(obj2)
        print(kali)


2.	Buatlah class LinkedList, dengan beberapa method tambahan pada class LinkedList seperti berikut (untuk constructor LinkedList, dan class Node dapat dilihat pada materi perkuliahan): 
a.	addRear : untuk menambahkan node di belakang linkedlist .
b.	override method __str__ : untuk menampilkan data linked list.
c.	override method __add__ : untuk menambahkan data dari dua buah linked list, dengan ketentuan, jumlah node pada linked list hasil penjumlahan sama dengan jumlah node terbanyak dari linked list yang akan dijumlahkan. 

Berikut contoh penggunaan class LinkedList

        class Node:
            def __init__(self,data):
                self.data = data
                self.next = None

        class LinkedList:
            def __init__(self):
                self.head = None
            def push(self,new_data):
                new_node= Node(new_data)
                new_node.next = self.head
                self.head = new_node
            def sum2Lists(self,list1,list2):
                prev=None
                temp=None
                carry = 0
                while (list1 is not None or list2 is not None):
                    if list1 is None:
                        fdata=0
                    else:
                        fdata=list1.data
                    if list2 is None:
                        sdata=0
                    else:
                        sdata=list2.data
                    Sum = carry + fdata + sdata
                    temp = Node(Sum)
                    if self.head is None:
                        self.head = temp
                    else:
                        prev.next = temp
                    prev = temp
                    if list1 is not None:
                        list1 = list1.next
                    if list2 is not None:
                        list2= list2.next
                if carry > 0:
                    temp.next = Node(carry)
            def printList(self):
                temp=self.head
                x=[]
                while(temp):
                    x.append(temp.data)
                    temp=temp.next
                print(x)

        list1=LinkedList()
        list2=LinkedList()

        n=int(input('Banyak data untuk list 1 : '))
        for i in range (n):
            x = int(input('Data : '))
            list1.push(x)
            i=i+1
        m=int(input('Banyak data untuk list 2 : '))
        for j in range (m):
            y=int(input('Data : '))
            list2.push(y)
            j=j+1

        truck= LinkedList()
        truck.sum2Lists(list1.head, list2.head)
        print("First List is ")
        list1.printList()
        print("Second List is ")
        list2.printList()
        print("Result List is ")
        truck.printList()
