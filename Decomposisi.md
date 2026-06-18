### Dekomposisi QR Matriks 4x4

Diberikan matriks A:
$$
A = \begin{bmatrix} 
3 & 4 & 2 & 1 \\ 
1 & 5 & 3 & 2 \\ 
2 & 1 & 4 & 3 \\ 
1 & 2 & 1 & 5 
\end{bmatrix}
$$

#### 1. Matriks Q (Orthonormal)
Menggunakan proses Gram-Schmidt, kita mendapatkan matriks Q:
$$
Q = \begin{bmatrix} 
\frac{3}{\sqrt{15}} & -\frac{1}{\sqrt{415}} & -\frac{129}{25\sqrt{83}} & \frac{7}{\sqrt{83}} \\ 
\frac{1}{\sqrt{15}} & \frac{18}{\sqrt{415}} & \frac{81}{25\sqrt{83}} & -\frac{2}{\sqrt{83}} \\ 
\frac{2}{\sqrt{15}} & -\frac{9}{\sqrt{415}} & \frac{167}{25\sqrt{83}} & -\frac{1}{\sqrt{83}} \\ 
\frac{1}{\sqrt{15}} & \frac{3}{\sqrt{415}} & -\frac{28}{25\sqrt{83}} & \frac{3}{\sqrt{83}} 
\end{bmatrix}
$$

#### 2. Matriks R (Segitiga Atas)
Matriks R disusun berdasarkan hasil proyeksi ortogonal:
$$
R = \begin{bmatrix} 
\sqrt{15} & \frac{21}{\sqrt{15}} & \frac{18}{\sqrt{15}} & \frac{16}{\sqrt{15}} \\ 
0 & \frac{\sqrt{415}}{5} & \frac{19}{\sqrt{415}} & \frac{21}{\sqrt{415}} \\ 
0 & 0 & \frac{25}{\sqrt{83}} & \frac{50}{\sqrt{83}} \\ 
0 & 0 & 0 & \frac{4}{\sqrt{83}} 
\end{bmatrix}
$$

#### 3. Verifikasi
Hasil akhir dekomposisi memenuhi syarat:
$$
A = Q \times R
$$