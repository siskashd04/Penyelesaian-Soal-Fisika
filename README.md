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



