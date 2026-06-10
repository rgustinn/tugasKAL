# Singular Value Decomposition (SVD)

## Definisi Matematis

Dekomposisi nilai singular (Singular Value Decomposition/SVD) dari matriks riil $A$ berukuran $m \times n$ adalah faktorisasi:

$$
A = U \Sigma V^T
$$

dengan:

* **$U$** adalah matriks ortogonal berukuran $m \times m$.
* **$\Sigma$** adalah matriks diagonal berukuran $m \times n$ yang memuat nilai-nilai singular.
* **$V$** adalah matriks ortogonal berukuran $n \times n$.

Nilai singular diperoleh dari:

$$
\sigma_i=\sqrt{\lambda_i}
$$

dengan $\lambda_i$ adalah nilai eigen dari matriks $A^TA$.

---

## Algoritma SVD

### Langkah 1: Menghitung Matriks $AA^T$

Hitung:

$$
AA^T
$$

Kemudian cari nilai eigen dan vektor eigennya.

### Langkah 2: Membentuk Matriks $U$

Jika diperoleh vektor eigen:

$$
u_1,u_2,\ldots,u_m
$$

Normalisasi:

$$
\hat{u}_i=\frac{u_i}{|u_i|}
$$

Kemudian susun sebagai kolom matriks:

$$
U=
\begin{bmatrix}
\hat{u}_1 & \hat{u}_2 & \cdots & \hat{u}_m
\end{bmatrix}
$$

### Langkah 3: Menghitung Matriks $A^TA$

Hitung:

$$
A^TA
$$

Cari nilai eigen:

$$
\lambda_1,\lambda_2,\ldots,\lambda_n
$$

Nilai singular:

$$
\sigma_i=\sqrt{\lambda_i}
$$

### Langkah 4: Membentuk Matriks $V$

Cari vektor eigen:

$$
v_1,v_2,\ldots,v_n
$$

Normalisasi:

$$
\hat{v}_i=\frac{v_i}{|v_i|}
$$

Susun:

$$
V=
\begin{bmatrix}
\hat{v}_1 & \hat{v}_2 & \cdots & \hat{v}_n
\end{bmatrix}
$$

### Langkah 5: Membentuk Matriks $\Sigma$

Susun nilai singular pada diagonal utama:

$$
\Sigma=
\begin{bmatrix}
\sigma_1 & 0 & \cdots & 0\
0 & \sigma_2 & \cdots & 0\
\vdots & \vdots & \ddots & \vdots\
0 & 0 & \cdots & \sigma_r
\end{bmatrix}
$$

dengan:

$$
\sigma_1 \ge \sigma_2 \ge \cdots \ge \sigma_r > 0
$$

### Langkah 6: Hasil Dekomposisi

$$
A = U\Sigma V^T
$$

---

# Contoh Perhitungan SVD

Diberikan matriks:

$$
A=
\begin{bmatrix}
3 & 1 & 1\
-1 & 3 & 1
\end{bmatrix}
$$

## 1. Menghitung $AA^T$

$$
AA^T=
\begin{bmatrix}
3 & 1 & 1\
-1 & 3 & 1
\end{bmatrix}
\begin{bmatrix}
3 & -1\
1 & 3\
1 & 1
\end{bmatrix}
=============

\begin{bmatrix}
11 & 1\
1 & 11
\end{bmatrix}
$$

---

## 2. Menentukan Nilai Eigen $AA^T$

Persamaan karakteristik:

$$
\det(AA^T-\lambda I)=0
$$

$$
\det
\begin{bmatrix}
11-\lambda & 1\
1 & 11-\lambda
\end{bmatrix}
=0
$$

$$
(11-\lambda)^2-1=0
$$

$$
\lambda^2-22\lambda+120=0
$$

$$
(\lambda-12)(\lambda-10)=0
$$

Sehingga diperoleh:

$$
\lambda_1=12
$$

$$
\lambda_2=10
$$

Karena terdapat dua nilai eigen tidak nol:

$$
\text{rank}(A)=2
$$

---

## 3. Menentukan Matriks $U$

### Untuk $\lambda_1=12$

$$
u_1=
\begin{bmatrix}
1\
1
\end{bmatrix}
$$

Normalisasi:

$$
\hat{u}_1=
\frac{1}{\sqrt2}
\begin{bmatrix}
1\
1
\end{bmatrix}
$$

### Untuk $\lambda_2=10$

$$
u_2=
\begin{bmatrix}
1\
-1
\end{bmatrix}
$$

Normalisasi:

$$
\hat{u}_2=
\frac{1}{\sqrt2}
\begin{bmatrix}
1\
-1
\end{bmatrix}
$$

Maka:

$$
U=
\begin{bmatrix}
\dfrac1{\sqrt2} & \dfrac1{\sqrt2}\
\dfrac1{\sqrt2} & -\dfrac1{\sqrt2}
\end{bmatrix}
$$

---

## 4. Menghitung $A^TA$

$$
A^TA=
\begin{bmatrix}
10 & 0 & 2\
0 & 10 & 4\
2 & 4 & 2
\end{bmatrix}
$$

Nilai eigennya:

$$
\lambda_1=12,\qquad
\lambda_2=10,\qquad
\lambda_3=0
$$

---

## 5. Menghitung Nilai Singular

$$
\sigma_1=\sqrt{12}=2\sqrt3
$$

$$
\sigma_2=\sqrt{10}
$$

---

## 6. Menentukan Matriks $V$

### Untuk $\lambda_1=12$

$$
v_1=
\begin{bmatrix}
1\
2\
1
\end{bmatrix}
$$

$$
\hat v_1=
\frac1{\sqrt6}
\begin{bmatrix}
1\
2\
1
\end{bmatrix}
$$

### Untuk $\lambda_2=10$

$$
v_2=
\begin{bmatrix}
2\
-1\
0
\end{bmatrix}
$$

$$
\hat v_2=
\frac1{\sqrt5}
\begin{bmatrix}
2\
-1\
0
\end{bmatrix}
$$

### Untuk $\lambda_3=0$

$$
v_3=
\begin{bmatrix}
1\
2\
-5
\end{bmatrix}
$$

$$
\hat v_3=
\frac1{\sqrt{30}}
\begin{bmatrix}
1\
2\
-5
\end{bmatrix}
$$

Sehingga:

$$
V=
\begin{bmatrix}
\dfrac1{\sqrt6} & \dfrac2{\sqrt5} & \dfrac1{\sqrt{30}}\
\dfrac2{\sqrt6} & -\dfrac1{\sqrt5} & \dfrac2{\sqrt{30}}\
\dfrac1{\sqrt6} & 0 & -\dfrac5{\sqrt{30}}
\end{bmatrix}
$$

dan

$$
V^T=
\begin{bmatrix}
\dfrac1{\sqrt6} & \dfrac2{\sqrt6} & \dfrac1{\sqrt6}\
\dfrac2{\sqrt5} & -\dfrac1{\sqrt5} & 0\
\dfrac1{\sqrt{30}} & \dfrac2{\sqrt{30}} & -\dfrac5{\sqrt{30}}
\end{bmatrix}
$$

---

## 7. Matriks $\Sigma$

Karena ukuran matriks $A$ adalah $2 \times 3$, maka:

$$
\Sigma=
\begin{bmatrix}
2\sqrt3 & 0 & 0\
0 & \sqrt{10} & 0
\end{bmatrix}
$$

---

## 8. Hasil Akhir SVD

$$
A=U\Sigma V^T
$$

$$
\begin{bmatrix}
3 & 1 & 1\
-1 & 3 & 1
\end{bmatrix}
=============

\begin{bmatrix}
\dfrac1{\sqrt2} & \dfrac1{\sqrt2}\
\dfrac1{\sqrt2} & -\dfrac1{\sqrt2}
\end{bmatrix}
\begin{bmatrix}
2\sqrt3 & 0 & 0\
0 & \sqrt{10} & 0
\end{bmatrix}
\begin{bmatrix}
\dfrac1{\sqrt6} & \dfrac2{\sqrt6} & \dfrac1{\sqrt6}\
\dfrac2{\sqrt5} & -\dfrac1{\sqrt5} & 0\
\dfrac1{\sqrt{30}} & \dfrac2{\sqrt{30}} & -\dfrac5{\sqrt{30}}
\end{bmatrix}
$$