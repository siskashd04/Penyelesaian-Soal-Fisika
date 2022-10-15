# Penyelesaian-Soal-Fisika
A. Prosedur Percobaan
1.  Buka web google colab pada browser
2.  Masukkan perintah soal pada google colab untuk soal gerak parabola dan focus jarak lensa.    
3.  Untuk soal jarak focus lensa, masukkan persamaan, indeks bias medium, R1, dan R2.
4.  Masukkan perinta “print (f)”  di akhir codingan agar bisa memunculkan hasilnya.
5.  Untuk soal gerak parabola juga sama, yaitu masukkan persamaan dan indicator lainnya pada soal.
6.  Masukkan rumus untuk mencari jarak horizontal dan jarak vertical.
7.  Masukkan codingan untuk membuat grafik gerak parabola dengan menggunakan file matplotlib.
8.  Simulasikan semua codingan dengan mengklik opsi “Run”.
9.  Buka aplikasi python 3.
10. Copy paste kan semua codingan yang telah dibuat pada google colab.
11. Simulasikan lagi seperti halnya di google colab dengan mengklik opsi “Run”. 
12. Hasil yang muncul akan sama anatar di google colab dan python. 

B. Pembahasan
      Pada praktikum ini akan dibuat sebuah pemodelan soal fisika tentang jarak fokus lensa dan gerak parabola menggunakan google colab dan python 3. Google colab adalah sebuah executable dokumen yang dapat digunakan untuk menyimpan, menulis, serta membagikan program. Sedangkan python adalah bahasa pemrograman yang digunakan untuk membuat aplikasi, perintah komputer, dan melakukan analisis data. Jadi, kedua software tersebut sama - sama digunakan untuk melakukan programming.
       Untuk soal jarak fokus lensa, codingan yang dimasukkan pertama yaitu persamaan fokus jarak lensa, kemudian masukkan juga indikator nilai yang lainnya yang ada si soal, seperti indeks bias medium dan jejari kelengkungnan permukaan 1 dan 2. Setelah itu, masukkan perintah untuk menampilkan hasilnya yaitu print(f). maka ketika disimulasikan, akan muncul hasilnya yaitu 18.94736842105263 cm. Sedangkan untuk soal gerak parabola, yang diketahui yaitu rumus gerkak parabola dan yang ditanyakan yaitu jarak horizontal dan vertikal. Maka di codingannya yang ditampilkan adalah sudutnya yaitu 45 derajat, percepatan gravitasi, dan juga kecepatan awal. Setelah itu, masukkan rumus yang ada pada soal untuk sumbu x dan y. Setelah itu, kita akan memunculkan grafik gerak parabola dengan menampilkan perintah matplotlib. Setelah dilakukan simulasi, diidapat nilai jarak horizontal yaitu 5.1020408163265305 m, jarak vertikal adalah 2.5510204081632657 m, dan waktu untuk mencapai jarak horizontal adalah 1.4430750636460152 s. Penyelesaian ini bisa dilakukan pada google colab dan python 3 yang akan menghasilkan nilai yang sama.
       

Codingan jarak fokus lensa dan gerak parabola :

#Soal Fokus Lensa
'''Rumus Fokus Lensa
   1/f = (n-1)[1/R1 + 1/R2]
'''
n = 1.5 #indeks bias medium
R1 = 20 #Jejari kelengkungan R1 (cm)
R2 = 18 #Jejari kelengkungan R2 (cm)

F = (n-1)*((1/R1)+(1/R2))
F = 1/F
print(F)

#Soal Gerak Parabola
import numpy as np 
import matplotlib.pyplot as plt 

alpha = np.radians(45)
g = 9.8
v0 = 10

v0x = v0*np.cos(alpha)
v0y = v0*np.sin(alpha)

X = ((v0**2)*np.sin(2*alpha))/(2*g)
print("Jarak Horizontal Maksimum = ",X," m")
Y = ((v0**2)*(np.sin(alpha)**2))/(2*g)
print("Jarak Vertikal Maksimum = ",Y," m")
T = (2*v0*np.sin(alpha))/g
print("Waktu Mencapai jarak Horizontal Maksimum = ",T," s")
print("\n")

t = np.arange(0.0, T, 0.01)
y = v0y*t - 0.5*g*t**2
x = v0x*t

fig, ax = plt.subplots()
ax.plot(x, y)
ax.set(xlabel='x (m)', ylabel= 'y (m)', title = 'Grafik Gerak Parabola')
ax.grid()
plt.show()


Tugas Menampilkan Data, Operasi Perhitungan Sederhana, dan Matriks pada Google Colab
A. Prosedur Percobaan
1. Buka web google colab pada browser.
2. Masukkan percobaan pertama untuk menampilkan data misal penjumlahan, perkalian, dan lainnya.        
3. Coba juga untuk menampilakn karakter huruf. 
4. Yang kedua yaitu menghitung eperasi perhitungan sederhana menggunakan rumus fisika. 
5. Yang ketiga adalah menampilkan matriks.
6. Selanjutnya yaitu menampilkan grafik sinusoidal dengan menggunakan perintah matplotlib.
        
B. Pembahasan        
       Pada praktikum ini akan dibuat program - program untuk menampilkan data, operasi perhitungan sederhana, matriks, dan membuat grafik. Simulasi ini dibuat menggunakan google collab. Untuk percobaan pertama yaitu menampilkan data, misal penjumlah, perkalian, dan lainnya. Misal jika m = 10, maka jika kita ingin menjumlahkan, programnya adalah print("hasil m+m = ", m+m). Kemudian kita juga bisa menampilkan karakter, misal kar1 = 'kalau orang lain bisa', kar2 = 'kenapa harus aku', maka bisa kita lakukan perintah print(kar1+' '+kar2), maka hasilnya kalau orang lain bisa kenapa harus aku.
       Untuk percobaan kedua yaitu operasi perhitungan sederhana, misal diketahui a = 10, b = -4,5, c = 5, dan d = 5/2. Kita bisa menghitung perkalian dari nilai - nilai tersebut. Misal print(perkalian c x d = ", c*d), maka hasil yang muncul adalah 12,5. Selain itu, kita juga bisa menghitung persoalan fisika dengan menggunakan google colab ini dengan memasukkan rumus fisika, seperti untuk mencari kecepatan menggunakan rumus s dibagi t. Selanjutnya, untuk membuat bentuk matriks juga bisa, dengan mengetik angka - angkanya saja misal [[0,1,1,0] , [2,3,2,1]]. Untuk percobaan yang terakhir yaitu membuat grafik sinusoidal dengan menggunakan program matplotlib.
       
C. Codingan
#cara menampilkan hasil

m = 10
print(m)
print("hasilm+m= ", m+m)
print("hasil m x m = ", m*m)

#cara menampilkan karakter
kar_1 = 'kalau orang lain bisa'
kar_2 = 'kenapa harus aku'
print(kar_1+' '+kar_2)
print(kar_1[0:10])
karakter = 'kalau orang lain bisa kenapa harus aku'
print(karakter.split())

from math import pi
from math import sqrt
#operasi perhitungan sederhana
a = 10
b = -4.5
c = 5.0
d= 5/2

print(a+b)
print("bentuk bilangan integer = ", int(b))
print("bentuk bilangan float = ", float(a))
print("perkalian c x d = ", c*d)
print('-----------------------')
print("contoh soal = tentukan kecepatan v (W (usaha) = 20; s(jarak)=-10; t(waktu)=2)")
W = 20
s = -10
t = 2

#v = s/t
kecepatan = s/t
print(kecepatan, 'm/s')

print('------------------')
print("soal 1 = tentukan energi dalam J dari m = 9,31x10^-31; c = 3x10^8")
m = 9.31*10**-31
c = 3*10**8
#energi : E = m x c^2
E = m* c**2
print(E)

print('------------------')
print("soal 2 = tentukan periode dalam s (l = 0.5 m ; g = 9.8 m/s^2)")
l = 0.5
g = 9.8
periode = 2*pi*sqrt(l/g)
print (periode)

from numpy import *
#menampilkan matriks
M = [[0 ,1 ,1, 0] , [2,3,2,1]]
print(M)

a = zeros ((3,3),int)
print (a)
print(" ")

a[0] = [1,4,2]
a[1,1] = 9
a[2,0:2] = [9,4]
print (a)

from numpy import array
print(' ')
A = array ([[2,3,4],[2,3,6]])
print (A)

import matplotlib.pyplot as plt
from numpy import arange,sin,cos

x = arange(0.0, 6.0, 0.1)
plt.plot(x,sin(x),'o-',x,cos(x),'s-')
plt.title('grafik sinusoidal')
plt.xlabel('x')
plt.ylabel('y')
plt.legend(('sinus','cosinus'),loc = 0)
plt.grid(True)
plt.show()


